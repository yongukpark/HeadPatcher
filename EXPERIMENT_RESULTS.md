# HBB CLI Experiment Results

이 문서는 `hbb-cli` 실험 결과를 모아두는 전용 페이지입니다.
README 본문은 실행 흐름과 결과 미리보기 중심으로 유지하고, 상세 테이블은 여기에서 갱신합니다.

## Dashboard

- https://headbb.vercel.app/

## Notes

- 실행 산출물은 `outputs/*.csv`, `outputs/*.jsonl`을 기준으로 정리합니다.
- 지표 정의와 실행 방법은 [`README.md`](./README.md)를 참고합니다.
- 아래 표는 카테고리별 대표 결과를 그대로 옮겨 둔 스냅샷입니다.

## Dataset Coverage

현재 저장소에 포함된 데이터셋 기준으로 정리하면 다음과 같습니다.

|category|dataset|status|
|---|---|---|
|capitals|africa|결과 포함|
|capitals|asia|결과 포함|
|capitals|easy|결과 포함|
|capitals|europe|결과 포함|
|capitals|north_america|결과 포함|
|capitals|oceania|결과 포함|
|capitals|south_america|결과 포함|
|chemical|chemical_symbols|결과 포함|
|country|general|결과 포함|
|currencies|money|결과 표 미정리|
|languages|blah|결과 표 미정리|
|logical|order2|결과 포함|
|logical|order3|결과 포함|
|mathematics|add|결과 포함|
|mathematics|arithmetic+geometric_progression|결과 포함|
|mathematics|arithmetic_progression|결과 포함|
|mathematics|constant|결과 포함|
|mathematics|geometric_progression|결과 포함|
|mathematics|mul|결과 포함|
|mathematics|sub|결과 포함|
|opposite|opposite|결과 포함|
|place|architecture|결과 포함|
|place|birthplace|결과 포함|
|profession|celebrity|결과 포함|
|time|historical_year|결과 포함|

## 1. capitals

### africa

- 프롬프트 예시: `What is the capital of Egypt? Answer:`

  |head|prompt_count|base_token_prob_delta_mean|base_token_prob_decrease_ratio|donor_token_rank_up_ratio|donor_token_rank_pre_replace_mean|donor_token_rank_post_replace_mean|
  |---|---|---|---|---|---|---|
  |L15.H7|16|-0.2303|0.9375|1|393|15|
  |L17.H6|16|-0.0484|1|1|393|105|
  |L15.H3|16|-0.0355|0.875|0.9375|393|290|
  |L22.H2|16|-0.0204|0.8125|0.875|393|333|
  |L17.H0|16|-0.0131|0.8125|0.875|393|306|
  |L23.H9|16|-0.013|0.875|0.875|393|367|
  |L19.H7|16|-0.0104|0.8125|0.8125|393|375|

### asia

- 프롬프트 예시: `What is the capital of Japan? Answer:`

  |head|prompt_count|base_token_prob_delta_mean|base_token_prob_decrease_ratio|donor_token_rank_up_ratio|donor_token_rank_pre_replace_mean|donor_token_rank_post_replace_mean|
  |---|---|---|---|---|---|---|
  |L15.H7|25|-0.1726|0.96|0.96|550|19|
  |L15.H3|25|-0.038|0.8|0.96|550|379|
  |L17.H6|25|-0.0334|0.8|0.92|550|145|
  |L18.H9|25|-0.0287|0.8|0.88|550|321|
  |L22.H2|25|-0.0183|0.88|0.8|550|512|
  |L23.H13|25|-0.0101|0.84|0.8|550|523|

### easy

- 프롬프트 예시: `What is the capital of Italy? Answer:`

  |head|prompt_count|base_token_prob_delta_mean|base_token_prob_decrease_ratio|donor_token_rank_up_ratio|donor_token_rank_pre_replace_mean|donor_token_rank_post_replace_mean|
  |---|---|---|---|---|---|---|
  |L15.H7|28|-0.201|0.9643|1|725|7|
  |L17.H6|28|-0.0687|0.9643|1|725|76|
  |L17.H0|28|-0.0186|0.8571|1|725|376|
  |L23.H9|28|-0.0137|0.9286|0.8571|725|671|

### europe

- 프롬프트 예시: `What is the capital of France? Answer:`

  |head|prompt_count|base_token_prob_delta_mean|base_token_prob_decrease_ratio|donor_token_rank_up_ratio|donor_token_rank_pre_replace_mean|donor_token_rank_post_replace_mean|
  |---|---|---|---|---|---|---|
  |L15.H7|20|-0.2513|1|0.95|227|3|
  |L17.H6|20|-0.0387|0.95|0.95|227|52|
  |L22.H2|20|-0.0173|0.8|0.95|227|203|

### north_america

- 프롬프트 예시: `What is the capital of the United States? Answer:`

  |head|prompt_count|base_token_prob_delta_mean|base_token_prob_decrease_ratio|donor_token_rank_up_ratio|donor_token_rank_pre_replace_mean|donor_token_rank_post_replace_mean|
  |---|---|---|---|---|---|---|
  |L15.H7|16|-0.1305|0.9375|1|207|18|
  |L17.H6|16|-0.0419|0.9375|0.9375|207|79|
  |L15.H3|16|-0.0366|0.875|0.8125|207|131|
  |L22.H2|16|-0.016|0.875|0.8125|207|192|
  |L23.H13|16|-0.0132|0.875|0.875|207|193|

### oceania

- 프롬프트 예시: `What is the capital of Solomon Islands? Answer:`

  |head|prompt_count|base_token_prob_delta_mean|base_token_prob_decrease_ratio|donor_token_rank_up_ratio|donor_token_rank_pre_replace_mean|donor_token_rank_post_replace_mean|
  |---|---|---|---|---|---|---|
  |L15.H7|7|-0.102|1|0.8571|44|9|
  |L17.H6|7|-0.0441|1|0.8571|44|21|
  |L13.H1|7|-0.017|0.8571|0.8571|44|31|

### south_america

- 프롬프트 예시: `What is the capital of Argentina? Answer:`

  |head|prompt_count|base_token_prob_delta_mean|base_token_prob_decrease_ratio|donor_token_rank_up_ratio|donor_token_rank_pre_replace_mean|donor_token_rank_post_replace_mean|
  |---|---|---|---|---|---|---|
  |L15.H7|11|-0.1811|1|1|94|13|
  |L16.H2|11|-0.0612|0.9091|1|94|67|
  |L22.H2|11|-0.0334|1|1|94|77|
  |L13.H1|11|-0.022|0.8182|1|94|54|
  |L17.H6|11|-0.0204|0.9091|1|94|58|
  |L23.H13|11|-0.0146|0.9091|0.9091|94|87|

## 2. logical

### order2

- 프롬프트 예시: `1, 2,`

  |head|prompt_count|base_token_prob_delta_mean|base_token_prob_decrease_ratio|donor_token_rank_up_ratio|donor_token_rank_pre_replace_mean|donor_token_rank_post_replace_mean|
  |---|---|---|---|---|---|---|
  |L12.H0|38|-0.2342|0.8421|0.7368|408|121|

### order3

- 프롬프트 예시: `1, 2, 3,`

  |head|prompt_count|base_token_prob_delta_mean|base_token_prob_decrease_ratio|donor_token_rank_up_ratio|donor_token_rank_pre_replace_mean|donor_token_rank_post_replace_mean|
  |---|---|---|---|---|---|---|
  |L12.H0|32|-0.527|1|0.9688|1111|229|

## 3. mathematics

### add

- 프롬프트 예시: `Cal : 12+35=`

  |head|prompt_count|base_token_prob_delta_mean|base_token_prob_decrease_ratio|donor_token_rank_up_ratio|donor_token_rank_pre_replace_mean|donor_token_rank_post_replace_mean|
  |---|---|---|---|---|---|---|
  |L12.H0|159|-0.2842|0.93|0.84|1893|466|
  |L22.H2|159|-0.0502|0.86|0.97|1893|764|

### arithmetic_geometric_progression

- 프롬프트 예시: `Find the pattern: 3, 7, 15, 31, 63, 127,`

  |head|prompt_count|base_token_prob_delta_mean|base_token_prob_decrease_ratio|donor_token_rank_up_ratio|donor_token_rank_pre_replace_mean|donor_token_rank_post_replace_mean|
  |---|---|---|---|---|---|---|
  |L7.H7|30|-0.1946|0.7667|0.7333|2177|168|

### arithmetic_progression

- 프롬프트 예시: `Find the pattern: 2, 5, 8, 11,`

  |head|prompt_count|base_token_prob_delta_mean|base_token_prob_decrease_ratio|donor_token_rank_up_ratio|donor_token_rank_pre_replace_mean|donor_token_rank_post_replace_mean|
  |---|---|---|---|---|---|---|
  |L12.H0|30|-0.1685|0.8|0.8667|32|14|
  |L13.H6|30|-0.1058|1|0.9333|32|20|

### constant

- 프롬프트 예시: `Output only the number. pi =`

  |head|prompt_count|base_token_prob_delta_mean|base_token_prob_decrease_ratio|donor_token_rank_up_ratio|donor_token_rank_pre_replace_mean|donor_token_rank_post_replace_mean|
  |---|---|---|---|---|---|---|
  |L11.H11|50|-0.0119|0.62|0.38|140|106|
  |L14.H5|50|-0.0107|0.64|0.38|140|83|

### geometric_progression

- 프롬프트 예시: `Find the pattern: 2, 4, 8, 16,`

  |head|prompt_count|base_token_prob_delta_mean|base_token_prob_decrease_ratio|donor_token_rank_up_ratio|donor_token_rank_pre_replace_mean|donor_token_rank_post_replace_mean|
  |---|---|---|---|---|---|---|
  |L13.H6|30|-0.0679|0.7333|0.7333|111|71|
  |L19.H5|30|-0.0112|0.7|0.7333|111|95|

### mul

- 프롬프트 예시: `Cal : 12*24=`

  |head|prompt_count|base_token_prob_delta_mean|base_token_prob_decrease_ratio|donor_token_rank_up_ratio|donor_token_rank_pre_replace_mean|donor_token_rank_post_replace_mean|
  |---|---|---|---|---|---|---|
  |L12.H15|200|-0.1181|0.89|0.81|2858|2339|
  |L22.H2|200|-0.0472|0.87|0.85|2858|1969|

### sub

- 프롬프트 예시: `Cal : 39 minus 38=`

  |head|prompt_count|base_token_prob_delta_mean|base_token_prob_decrease_ratio|donor_token_rank_up_ratio|donor_token_rank_pre_replace_mean|donor_token_rank_post_replace_mean|
  |---|---|---|---|---|---|---|
  |L22.H2|100|-0.0156|0.75|0.9|377|217|

## 4. Grammar

### opposite

- 프롬프트 예시: `The opposite of 'hot' is '`

  |head|prompt_count|base_token_prob_delta_mean|base_token_prob_decrease_ratio|donor_token_rank_up_ratio|donor_token_rank_pre_replace_mean|donor_token_rank_post_replace_mean|
  |---|---|---|---|---|---|---|
  |L13.H2|100|-0.2199|0.97|0.97|327|80|
  |L14.H12|100|-0.0567|0.83|0.95|327|197|
  |L22.H0|100|-0.0253|0.8|0.93|327|236|
  |L23.H2|100|-0.0179|0.8|0.86|327|283|
  |L23.H9|100|-0.0162|0.82|0.92|327|282|

### past

- 프롬프트 예시: `TThe past tense of 'go' is '`

  |head|prompt_count|base_token_prob_delta_mean|base_token_prob_decrease_ratio|donor_token_rank_up_ratio|donor_token_rank_pre_replace_mean|donor_token_rank_post_replace_mean|
  |---|---|---|---|---|---|---|
  |L23.H2|23|-0.0643|1.0|1.0|492|343|
  |L22.H9|23|-0.0366|0.87|1.0|492|395|
  |L12.H15|23|-0.0312|0.87|1.0|492|351|

### find_subject

- 프롬프트 예시: `The subject in the sentence 'Dog sleeps' is '`

  |head|prompt_count|base_token_prob_delta_mean|base_token_prob_decrease_ratio|donor_token_rank_up_ratio|donor_token_rank_pre_replace_mean|donor_token_rank_post_replace_mean|
  |---|---|---|---|---|---|---|
  |L17.H7|50|-0.0432|0.84|0.84|757|381|
  |L22.H2|50|-0.0212|0.96|0.98|757|634|
  |L13.H6|50|-0.0195|0.94|0.96|757|607|
  |L12.H15|50|-0.0173|0.84|0.96|757|557|
  |L23.H6|50|-0.0156|0.92|0.92|757|671|

### find_verb

- 프롬프트 예시: `The verb in the sentence 'The dog runs' is '`

  |head|prompt_count|base_token_prob_delta_mean|base_token_prob_decrease_ratio|donor_token_rank_up_ratio|donor_token_rank_pre_replace_mean|donor_token_rank_post_replace_mean|
  |---|---|---|---|---|---|---|
  |L22.H2|50|-0.0577|0.94|0.96|372|282|
  |L12.H15|50|-0.0531|0.9|0.96|372|260|
  |L22.H0|50|-0.0467|0.96|0.96|372|304|
  |L15.H11|50|-0.0431|0.82|0.8|372|295|
  |L13.H6|50|-0.0369|0.9|0.94|372|285|

### active_passive

- 프롬프트 예시: `The chef prepared the meal. The meal was`

  |head|prompt_count|base_token_prob_delta_mean|base_token_prob_decrease_ratio|donor_token_rank_up_ratio|donor_token_rank_pre_replace_mean|donor_token_rank_post_replace_mean|
  |---|---|---|---|---|---|---|
  |L12.H8|37|-0.0414|0.8108|0.9189|1273|764|
  |L18.H4|37|-0.0301|0.9189|1.0|1273|675|
  |L15.H6|37|-0.0224|0.8649|0.9459|1273|890|

### plural

- 프롬프트 예시: `The plural of child is`

  |head|prompt_count|base_token_prob_delta_mean|base_token_prob_decrease_ratio|donor_token_rank_up_ratio|donor_token_rank_pre_replace_mean|donor_token_rank_post_replace_mean|
  |---|---|---|---|---|---|---|
  |L23.H9|23|-0.0539|1.0000|1.0000|5220.48|4312.78|
  |L22.H2|23|-0.0450|1.0000|1.0000|5220.48|3850.52|
  |L20.H6|23|-0.0324|0.8261|0.8696|5220.48|4689.78|
  |L19.H2|23|-0.0287|1.0000|1.0000|5220.48|3644.30|
  |L14.H7|23|-0.0126|0.8261|0.8261|5220.48|3936.09|
  |L23.H2|23|-0.0113|0.9130|0.8696|5220.48|4933.70|

## 5. place

### architecture

- 프롬프트 예시: `The Eiffel Tower is in`

유의미한 헤드를 찾지 못함

### birthplace

- 프롬프트 예시: `Albert Einstein was born in`

  |head|prompt_count|base_token_prob_delta_mean|base_token_prob_decrease_ratio|donor_token_rank_up_ratio|donor_token_rank_pre_replace_mean|donor_token_rank_post_replace_mean|
  |---|---|---|---|---|---|---|
  |L15.H7|50|-0.0372|0.76|0.62|276|142|
  |L17.H0|50|-0.0206|0.74|0.66|276|138|

## 6. time

### historical_year

- 프롬프트 예시: `Answer using only a 4-digit number. World War I began in`

  |head|prompt_count|base_token_prob_delta_mean|base_token_prob_decrease_ratio|donor_token_rank_up_ratio|donor_token_rank_pre_replace_mean|donor_token_rank_post_replace_mean|
  |---|---|---|---|---|---|---|
  |L14.H2|79|-0.1016|0.7722|0.8734|597|91|

## 7. country

### general

- 프롬프트 예시: `What country is Paris in? Answer:`

  |head|prompt_count|base_token_prob_delta_mean|base_token_prob_decrease_ratio|donor_token_rank_up_ratio|donor_token_rank_pre_replace_mean|donor_token_rank_post_replace_mean|
  |---|---|---|---|---|---|---|
  |L15.H7|28|-0.1611|1|1|47|8|
  |L17.H6|28|-0.0587|1|0.9643|47|23|
  |L19.H5|28|-0.0452|1|0.9286|47|31|
  |L22.H2|28|-0.0344|1|0.9286|47|38|
  |L17.H0|28|-0.0319|0.9643|0.9286|47|32|
  |L21.H10|28|-0.0212|0.8929|0.8571|47|38|
  |L19.H2|28|-0.012|0.8214|0.8214|47|40|

### ISO code

- 프롬프트 예시: `The ISO country code for United States is`

  |head|prompt_count|base_token_prob_delta_mean|base_token_prob_decrease_ratio|donor_token_rank_up_ratio|donor_token_rank_pre_replace_mean|donor_token_rank_post_replace_mean|
  |---|---|---|---|---|---|---|
  |L22.H2|165|-0.043|0.818|0.993|325|197|

### university

- 프롬프트 예시: `What is the country of Tohoku University? Answer: The country is '`

  |head|prompt_count|base_token_prob_delta_mean|base_token_prob_decrease_ratio|donor_token_rank_up_ratio|donor_token_rank_pre_replace_mean|donor_token_rank_post_replace_mean|
  |---|---|---|---|---|---|---|
  |L15.H7|50|-0.1442|0.94|1.0|80|11|
  |L17.H6|50|-0.0963|0.86|0.96|80|35|
  |L22.H2|50|-0.0252|0.82|0.94|80|61|
  |L17.H0|50|-0.0201|0.86|0.96|80|57|
  |L21.H10|50|-0.0169|0.84|0.92|80|66|
  |L23.H13|50|-0.0139|0.84|0.82|80|71|
  |L23.H9|50|-0.0119|0.8|0.84|80|74|
  
## 8. profession

### celebrity

- 프롬프트 예시: `Taylor Swift's profession is`

유의미한 헤드를 찾지 못함

## 9. languages

### blah_corr

- 프롬프트 예시: `The official language of South Korea is`

  |head|prompt_count|base_token_prob_delta_mean|base_token_prob_decrease_ratio|donor_token_rank_up_ratio|donor_token_rank_pre_replace_mean|donor_token_rank_post_replace_mean|
  |---|---|---|---|---|---|---|
  |L17.H6|105|-0.0752|0.8095|0.9810|620|58|


## 10. feelings

### positive

- 프롬프트 예시: `I finally achieved a goal I worked toward for years. The word for this feeling is '`

  |head|prompt_count|base_token_prob_delta_mean|base_token_prob_decrease_ratio|donor_token_rank_up_ratio|donor_token_rank_pre_replace_mean|donor_token_rank_post_replace_mean|
  |---|---|---|---|---|---|---|
  |L16.H4|50|-0.0141|0.76|0.84|192|122|
  |L18.H2|50|-0.0110|0.78|0.86|192|121|
  |L13.H13|50|-0.0103|0.78|0.88|192|125|

### negative
- 프롬프트 예시: `I made a serious mistake that hurt someone. The word for this feeling is '`

  |head|prompt_count|base_token_prob_delta_mean|base_token_prob_decrease_ratio|donor_token_rank_up_ratio|donor_token_rank_pre_replace_mean|donor_token_rank_post_replace_mean|
  |---|---|---|---|---|---|---|
  |L13.H13|50|-0.0225|0.86|0.82|73|31|

## 11. relations

### object-function relations
- 프롬프트 예시: `A knife is used to '`

  |head|prompt_count|base_token_prob_delta_mean|base_token_prob_decrease_ratio|donor_token_rank_up_ratio|donor_token_rank_pre_replace_mean|donor_token_rank_post_replace_mean|
  |---|---|---|---|---|---|---|
  |L14.H5|180|-0.0223|0.87|0.96|354|204|
  |L12.H8|180|-0.0170|0.85|0.91|354|291|
  |L11.H1|180|-0.0104|0.82|0.84|354|309|

### IATA_airport
- 프롬프트 예시: `The IATA code for Los Angeles International Airport is`

  |head|prompt_count|base_token_prob_delta_mean|base_token_prob_decrease_ratio|donor_token_rank_up_ratio|donor_token_rank_pre_replace_mean|donor_token_rank_post_replace_mean|
  |---|---|---|---|---|---|---|
  |L18.H0|110|-0.0645|0.85|0.85|49|32|
  |L13.H6|110|-0.0652|0.88|0.88|49|18|
  |L22.H2|110|-0.0450|0.9|0.85|49|30|
  |L11.H6|110|-0.0242|0.89|0.85|49|36|

## 12. famous_patching

### indirect_object_identification
- 프롬프트 예시: `When John and Mary went to the store, Mary gave a book to`
  
  |head|prompt_count|base_token_prob_delta_mean|base_token_prob_decrease_ratio|donor_token_rank_up_ratio|donor_token_rank_pre_replace_mean|donor_token_rank_post_replace_mean|
  |---|---|---|---|---|---|---|
  |L22.H2|103|-0.1422|0.9903|0.9903|490|258|
  |L17.H0|103|-0.1322|0.9806|0.9903|490|296|
  |L15.H15|103|-0.0892|0.9029|0.9709|490|339|
  |L19.H5|103|-0.049|0.8835|0.9417|490|385|
  |L23.H13|103|-0.038|0.9903|0.9903|490|429|

### induction_head
- 프롬프트 예시: `dax wug mib dax wug`
  
  |head|prompt_count|base_token_prob_delta_mean|base_token_prob_decrease_ratio|donor_token_rank_up_ratio|donor_token_rank_pre_replace_mean|donor_token_rank_post_replace_mean|
  |---|---|---|---|---|---|---|
  |L10.H0|27|-0.1466|0.963|1.0|371|137|
  |L15.H11|27|-0.0409|0.8148|0.8148|371|279|
  |L22.H2|27|-0.0406|0.9259|0.8889|371|261|
  |L10.H9|27|-0.035|0.963|0.8519|371|307|
  |L12.H15|27|-0.0273|0.963|0.8889|371|345|
  |L16.H3|27|-0.021|0.9259|0.9259|371|355|

## 13. computer

### http_error_code
- 프롬프트 예시: `The HTTP status code for 'Not Found' is '`
  
  |head|prompt_count|base_token_prob_delta_mean|base_token_prob_decrease_ratio|donor_token_rank_up_ratio|donor_token_rank_pre_replace_mean|donor_token_rank_post_replace_mean|
  |---|---|---|---|---|---|---|
  |L14.H5|13|-0.079|1.0|0.85|15|9|

### file_extension
- 프롬프트 예시: `The file extension for Python source files is .`
  
  |head|prompt_count|base_token_prob_delta_mean|base_token_prob_decrease_ratio|donor_token_rank_up_ratio|donor_token_rank_pre_replace_mean|donor_token_rank_post_replace_mean|
  |---|---|---|---|---|---|---|
  |L22.H2|100|-0.016|0.82|0.86|408|318|

### port_number
- 프롬프트 예시: `The default port for HTTP is`
  
  |head|prompt_count|base_token_prob_delta_mean|base_token_prob_decrease_ratio|donor_token_rank_up_ratio|donor_token_rank_pre_replace_mean|donor_token_rank_post_replace_mean|
  |---|---|---|---|---|---|---|
  |L14.H5|41|-0.133|0.92|0.90|70|29|
  |L15.H6|41|-0.106|0.92|0.88|70|33|
  |L15.H7|41|-0.075|0.87|0.80|70|47|

## 14. colors

### color_fs_corr
- 프롬프트 예시: `The color of banana is yellow.\nThe color of snow is '`
  
  |head|prompt_count|base_token_prob_delta_mean|base_token_prob_decrease_ratio|donor_token_rank_up_ratio|donor_token_rank_pre_replace_mean|donor_token_rank_post_replace_mean|
  |---|---|---|---|---|---|---|
  |L11.H1|75|-0.0193|0.88|0.5733|7|5|
  |L14.H7|75|-0.0165|0.84|0.56|7|5|

## 15. music

### instruments_fs
- 프롬프트 예시: `Violin is a string instrument. Trumpet is a`
  
  |head|prompt_count|base_token_prob_delta_mean|base_token_prob_decrease_ratio|donor_token_rank_up_ratio|donor_token_rank_pre_replace_mean|donor_token_rank_post_replace_mean|
  |---|---|---|---|---|---|---|
  |L18.H8|37|-0.0464|0.9730|0.8108|17|9|
  |L14.H5|37|-0.0421|0.8378|0.8919|17|6|

## 16. medical

### disease-organ
- 프롬프트 예시: `Identify the affected organ. Disease: Hepatitis / Organ: '`
  
  |head|prompt_count|base_token_prob_delta_mean|base_token_prob_decrease_ratio|donor_token_rank_up_ratio|donor_token_rank_pre_replace_mean|donor_token_rank_post_replace_mean|
  |---|---|---|---|---|---|---|
  |L15.H13|25|-0.0442|0.88|0.8|69|13|
  |L22.H2|25|-0.0126|0.84|0.8|69|58|

### sympytom-disease
- 프롬프트 예시: `In a medical context, the term for 'high blood pressure' is '`
  
  |head|prompt_count|base_token_prob_delta_mean|base_token_prob_decrease_ratio|donor_token_rank_up_ratio|donor_token_rank_pre_replace_mean|donor_token_rank_post_replace_mean|
  |---|---|---|---|---|---|---|
  |L14.H5|26|-0.1298|0.9231|1.0|892|228|
  |L15.H13|26|-0.1195|0.8462|0.9231|892|343|
  |L11.H1|26|-0.0412|0.8077|0.8846|892|673|
  |L14.H7|26|-0.0364|0.8077|0.9231|892|576|
  |L18.H4|26|-0.0298|0.8462|0.8077|892|732|

### specialty
- 프롬프트 예시: `The medical field that treats the heart is called`
  
  |head|prompt_count|base_token_prob_delta_mean|base_token_prob_decrease_ratio|donor_token_rank_up_ratio|donor_token_rank_pre_replace_mean|donor_token_rank_post_replace_mean|
  |---|---|---|---|---|---|---|
  |L15.H13|32|-0.1717|0.9063|0.9688|340|18|

## 17. translation

### eng-chinese
- 프롬프트 예시: `Answer with a Chinese Hanzi. English: 'Star' / Chinese: '`
  
  |head|prompt_count|base_token_prob_delta_mean|base_token_prob_decrease_ratio|donor_token_rank_up_ratio|donor_token_rank_pre_replace_mean|donor_token_rank_post_replace_mean|
  |---|---|---|---|---|---|---|
  |L14.H5|45|-0.0447|0.8222|0.8444|149|89|
  |L12.H8|45|-0.0199|0.8|0.8|149|131|
  |L19.H2|45|-0.0109|0.8667|0.8222|149|129|

### eng-french
- 프롬프트 예시: `Answer with a French word. English: 'Sun' / French: '`
  
  |head|prompt_count|base_token_prob_delta_mean|base_token_prob_decrease_ratio|donor_token_rank_up_ratio|donor_token_rank_pre_replace_mean|donor_token_rank_post_replace_mean|
  |---|---|---|---|---|---|---|
  |L11.H1|41|-0.0454|0.8049|0.8537|234|183|
  |L23.H13|41|-0.018|0.8049|0.878|234|202|

### eng-german
- 프롬프트 예시: `Answer with a German word. English: 'Moon' / German: '`
  
  |head|prompt_count|base_token_prob_delta_mean|base_token_prob_decrease_ratio|donor_token_rank_up_ratio|donor_token_rank_pre_replace_mean|donor_token_rank_post_replace_mean|
  |---|---|---|---|---|---|---|
  |L11.H1|40|-0.0594|0.825|0.75|219|184|
  |L22.H2|40|-0.0403|0.75|0.8|219|170|
  |L16.H6|40|-0.0246|0.825|0.7|219|175|

### eng-italian
- 프롬프트 예시: `Answer with an Italian word. English: 'Sun' / Italian: '`
  
  |head|prompt_count|base_token_prob_delta_mean|base_token_prob_decrease_ratio|donor_token_rank_up_ratio|donor_token_rank_pre_replace_mean|donor_token_rank_post_replace_mean|
  |---|---|---|---|---|---|---|
  |L22.H2|40|-0.0506|0.8|0.925|343|219|

### eng-spanish
- 프롬프트 예시: `Answer with a Spanish word. English: 'Moon' / Spanish: '`
  
  |head|prompt_count|base_token_prob_delta_mean|base_token_prob_decrease_ratio|donor_token_rank_up_ratio|donor_token_rank_pre_replace_mean|donor_token_rank_post_replace_mean|
  |---|---|---|---|---|---|---|
  |L22.H2|42|-0.053|0.9286|0.9524|110|81|

## 18. science

### chemical_symbols
- 프롬프트 예시: `The chemical symbol for Hydrogen is`
  
  |head|prompt_count|base_token_prob_delta_mean|base_token_prob_decrease_ratio|donor_token_rank_up_ratio|donor_token_rank_pre_replace_mean|donor_token_rank_post_replace_mean|
  |---|---|---|---|---|---|---|
  |L13.H6|100|-0.1218|0.81|1|136|9|
  |L22.H2|100|-0.0557|0.82|0.98|136|62|

### unit
- 프롬프트 예시: `The force is 50 newtons. Unit:`
  
  |head|prompt_count|base_token_prob_delta_mean|base_token_prob_decrease_ratio|donor_token_rank_up_ratio|donor_token_rank_pre_replace_mean|donor_token_rank_post_replace_mean|
  |---|---|---|---|---|---|---|
  |L14.H5|43|-0.0611|1.0|1.0|401|124|
  |L12.H8|43|-0.0291|0.814|0.8605|401|269|
  |L18.H4|43|-0.0243|0.8837|0.9767|401|196|
  |L11.H1|43|-0.0144|0.907|0.9302|401|309|
  |L22.H2|43|-0.0143|0.8605|0.9535|401|332|

## 19. law

### US_amendments
- 프롬프트 예시: `The 1st Amendment protects freedom of`
  
  |head|prompt_count|base_token_prob_delta_mean|base_token_prob_decrease_ratio|donor_token_rank_up_ratio|donor_token_rank_pre_replace_mean|donor_token_rank_post_replace_mean|
  |---|---|---|---|---|---|---|
  |L23.H9|19|-0.0381|0.8421|0.8421|1833|1467|

### versus
- 프롬프트 예시: `The famous case is Miranda v.`
  
  |head|prompt_count|base_token_prob_delta_mean|base_token_prob_decrease_ratio|donor_token_rank_up_ratio|donor_token_rank_pre_replace_mean|donor_token_rank_post_replace_mean|
  |---|---|---|---|---|---|---|
  |L22.H2|29|-0.0353|0.7586|0.8621|2481|2208|

## 20. job

### workplace 
- 프롬프트 예시: `A librarian works in a`
  
  |head|prompt_count|base_token_prob_delta_mean|base_token_prob_decrease_ratio|donor_token_rank_up_ratio|donor_token_rank_pre_replace_mean|donor_token_rank_post_replace_mean|
  |---|---|---|---|---|---|---|
  |L16.H1|70|-0.0146|0.7429|0.8|637|428|
  |L21.H10|70|-0.0120|0.80|0.7714|637|497|
  |L23.H9|70|-0.0101|0.80|0.7143|637|566|

## 21. food

### yum
- 프롬프트 예시: `The taste of lemon is sour.\nThe taste of chocolate is '`
  
  |head|prompt_count|base_token_prob_delta_mean|base_token_prob_decrease_ratio|donor_token_rank_up_ratio|donor_token_rank_pre_replace_mean|donor_token_rank_post_replace_mean|
  |---|---|---|---|---|---|---|
  |L14.H7|60|-0.0187|0.75|0.8333|18|10|
  |L11.H1|60|-0.0131|0.85|0.7|18|14|

### nutrient
- 프롬프트 예시: `The main nutrient in beef is`
  
  |head|prompt_count|base_token_prob_delta_mean|base_token_prob_decrease_ratio|donor_token_rank_up_ratio|donor_token_rank_pre_replace_mean|donor_token_rank_post_replace_mean|
  |---|---|---|---|---|---|---|
  |L16.H2|50|-0.0194|0.8|0.86|168|127|
  |L11.H1|50|-0.0218|0.88|0.82|168|149|

### ingredient
- 프롬프트 예시: `The primary ingredient in guacamole is`
  
  |head|prompt_count|base_token_prob_delta_mean|base_token_prob_decrease_ratio|donor_token_rank_up_ratio|donor_token_rank_pre_replace_mean|donor_token_rank_post_replace_mean|
  |---|---|---|---|---|---|---|
  |L15.H7|35|-0.0664|0.94|1.00|453.77|106.54|
  |L11.H1|35|-0.0186|0.80|0.86|453.77|380.49|
  |L23.H13|35|-0.0165|0.86|0.94|453.77|395.17|

## 22. animals

### taxonomy
- 프롬프트 예시: `A dolphin is a type of mammal. An eagle is a type of`
  
  |head|prompt_count|base_token_prob_delta_mean|base_token_prob_decrease_ratio|donor_token_rank_up_ratio|donor_token_rank_pre_replace_mean|donor_token_rank_post_replace_mean|
  |---|---|---|---|---|---|---|
  |L16.H2|57|-0.1101|0.7895|0.9825|77.60|17.86|
  |L16.H15|57|-0.0500|0.7368|0.9474|77.60|28.23|
  |L21.H10|57|-0.0194|0.7895|0.8947|77.60|52.96|

### habitat
- 프롬프트 예시: `Habitat of camel is desert.\nHabitat of dolphin is`
  
  |head|prompt_count|base_token_prob_delta_mean|base_token_prob_decrease_ratio|donor_token_rank_up_ratio|donor_token_rank_pre_replace_mean|donor_token_rank_post_replace_mean|
  |---|---|---|---|---|---|---|
  |L14.H5|40|-0.0470|0.825|0.95|86.53|29.15|
  |L16.H15|40|-0.0454|0.825|0.95|86.53|19.05|
  |L21.H10|40|-0.0145|0.825|0.90|86.53|55.45|


## 23. universe

### celestial_object
- 프롬프트 예시: `Earth is a planet.\nSun is a`
  
  |head|prompt_count|base_token_prob_delta_mean|base_token_prob_decrease_ratio|donor_token_rank_up_ratio|donor_token_rank_pre_replace_mean|donor_token_rank_post_replace_mean|
  |---|---|---|---|---|---|---|
  |L14.H5|27|-0.09046|0.9259|0.7407|29.59|10.44|

## 24. sports

### stadium_location
- 프롬프트 예시: `The home stadium of Manchester United is the`
  
  |head|prompt_count|base_token_prob_delta_mean|base_token_prob_decrease_ratio|donor_token_rank_up_ratio|donor_token_rank_pre_replace_mean|donor_token_rank_post_replace_mean|
  |---|---|---|---|---|---|---|
  |L15.H7|25|-0.2321|0.92|1.0|464.48|49.8|
  |L17.H6|25|-0.1213|0.8|0.92|464.48|99.64|

### worldclass
- 프롬프트 예시: `Tottenham Hotspur is associated with which sports? Answer:`
  
  |head|prompt_count|base_token_prob_delta_mean|base_token_prob_decrease_ratio|donor_token_rank_up_ratio|donor_token_rank_pre_replace_mean|donor_token_rank_post_replace_mean|
  |---|---|---|---|---|---|---|
  |L18.H8|44-0.0933|1.0|0.9545|46.09|13.43|
  
## 25. greek mythology

### gods
- 프롬프트 예시: `In Greek mythology, Zeus is the god of the`
  
  |head|prompt_count|base_token_prob_delta_mean|base_token_prob_decrease_ratio|donor_token_rank_up_ratio|donor_token_rank_pre_replace_mean|donor_token_rank_post_replace_mean|
  |---|---|---|---|---|---|---|
  |L15.H7|25|-0.2321|0.92|1.0|464.48|49.8|
  |L17.H6|25|-0.1213|0.8|0.92|464.48|99.64|

## 26. gender

### opposite_gender
- 프롬프트 예시: `The opposite gender of queen is the`
  
  |head|prompt_count|base_token_prob_delta_mean|base_token_prob_decrease_ratio|donor_token_rank_up_ratio|donor_token_rank_pre_replace_mean|donor_token_rank_post_replace_mean|
  |---|---|---|---|---|---|---|
  |L13.H2|17|-0.0442|0.8235|0.7059|222.00|115.88|
  |L16.H1|17|-0.0264|0.7647|0.7059|222.00|105.94|
