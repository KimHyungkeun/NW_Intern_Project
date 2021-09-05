# NAVER WEBTOON 하계 인턴 프로젝트

- DailyStatJob 개선

1) NAVER WEBTOON 하계인턴을 통해 진행한 프로젝트입니다.

2) 인턴 과정 진행 중, 분석에 필요한 테이블들은 모두 "Stat"이라는 prefix가 붙습니다.

3) 이번 목표의 과제는 Stat테이블의 생성과정을 SparkJob으로 재구성해보는 과제입니다.

(기존의 Job은 Java로 구성되어있고, Impala로직을 전달하여 테이블을 생성하는 과정입니다.) 

4) 생성을 모두 완료하고 나면 기존의 Job의 결과테이블과 비교하여 정확성을 검증합니다. 
