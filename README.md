# hbb_cli

`hbb_cli`는 attention head replace 실험을 실행하고, 프롬프트별/head별 지표를 저장하는 CLI 프로젝트입니다.

## 지표
### 프롬프트 별
* base_token_prob_delta : base token 확률 변화량
* base_token_prob_direction : base token 확률 변화 방향 (감소/증가)
* base_token_changed : replace 후 base token이 예측 토큰에서 바뀌었는지
* base_token_rank_pre_replace/post_replace/change : base token이 몇 등에서 몇 등으로 바뀌었는지
* donor_token : donor 프롬프트의 원래 토큰
* donor_token_prob_pre_replace/post_replace/delta : donor 토큰의 확률이 얼마나 증가/감소했는지
* donor_token_rank_pre_replace/post_replace/change : donor 토큰이 base 분포에서 몇 등에서 몇 등으로 이동했는지
* baseline_base_token(prob) : 원래 출력값과 그 확률
* replaced_base_token(prob) : 바뀐 출력값과 그 확률 

### head 별
* prompt_count : 실험에 사용한 프롬프트 개수
* base_token_prob_delta_mean : base token 확률 변화량 평균
* base_token_prob_delta_variance : base token 확률 변화량 분산
* base_token_prob_decrease_ratio : 전체 프롬프트 중 base token 확률이 떨어진 비율
* base_token_changed_ratio : 전체 프롬프트 중 base token이 바뀐 비율
* base_token_rank_post_replace_mean : base token의 replace 후 평균 등수
* donor_token_prob_delta_mean : donor 토큰 확률 변화량 평균
* donor_token_prob_delta_variance : donor 토큰 확률 변화량 분산
* donor_token_prob_increase_ratio : donor 토큰 확률이 증가한 비율
* donor_token_rank_up_ratio : donor 토큰 rank가 실제로 상승한 비율
* donor_token_rank_pre_replace_mean : donor 토큰의 replace 전 평균 rank
* donor_token_rank_post_replace_mean : donor 토큰의 replace 후 평균 rank

## 요구 사항

- Python 3.10+
- CUDA 사용 시 NVIDIA GPU + CUDA 환경
- requirement.txt 참고

## 설치

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirement.txt
```

## 실행

### 1) 모든 head 스캔

```bash
python3 scripts/head_mining.py \
  --scan-all-heads \
  --dataset-root datasets \
  --output-dir outputs
```

### 1-1) 특정 프롬프트 파일만 사용 (`--prompts-file`)

- `--prompts-file`를 주면 `--dataset-root`는 무시됩니다.
- `.jsonl` 파일 경로를 쉼표(`,`)로 연결해서 여러 파일을 동시에 넣을 수 있습니다.

```bash
python3 scripts/head_mining.py \
  --scan-all-heads \
  --prompts-file "datasets/by_category/country/general.jsonl,datasets/by_category/chemical/chemical_symbols.jsonl" \
  --output-dir outputs
```

### 2) 특정 head 세트 평가

```bash
python3 scripts/head_mining.py \
  --multi-heads L1.H2,L3.H5 \
  --dataset-root datasets \
  --output-dir outputs
```

## 결과물

- 기본 출력 경로: `outputs/`
- 주요 산출물:
  - `prompt_output_map.csv`, `prompt_output_map.jsonl` (프롬프트와 baseline 출력 토큰 매핑)
  - `summary_by_head.csv`, `summary_by_head.jsonl`
  - `prompt_by_head.csv`, `prompt_by_head.jsonl`
  - (특정 head 세트 실행 시) `prompt_metrics_*.csv/json`, `summary_*.csv/json`

### `summary_by_head`가 안 생길 수 있는 경우

- 버킷(카테고리/소스 파일) 안 프롬프트가 2개 미만이면 해당 버킷은 스킵됩니다.
- `scan-all-heads`에서 summary 필터를 통과한 head가 하나도 없으면 새 `summary_by_head`가 생성되지 않을 수 있습니다.
  - 필터: `base_token_prob_decrease_ratio >= threshold(0.8 -> 0.1 fallback)` 그리고 `base_token_prob_delta_mean < -0.01`
- 재실행 시 이미 같은 `(head_label, prompt_count)` 키가 있으면 중복 추가하지 않습니다.

## 결과 미리보기

- 대시보드: https://headbb.vercel.app/
- 상세 실험 결과: [EXPERIMENT_RESULTS.md](./EXPERIMENT_RESULTS.md)
- 배치 실행 결과는 `outputs/*.csv`, `outputs/*.jsonl` 기준으로 누적 관리합니다.

### 빠르게 볼 포인트

- `capitals`와 `country` 계열에서는 `L15.H7`이 여러 버킷에서 반복적으로 강한 변화량을 보였습니다.
- `logical/order3`와 `mathematics/add`에서는 `L12.H0`가 비교적 크게 반응했습니다.
- `chemical_symbols`, `opposite`, `birthplace`처럼 카테고리별로 두드러지는 head가 따로 관찰됩니다.