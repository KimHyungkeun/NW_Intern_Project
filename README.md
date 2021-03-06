# NAVER WEBTOON 하계 인턴 프로젝트

**프로젝트명 : DailyStatJob 개선**

**개요** : 
1) 웹툰으로부터 수집된 데이터는 최종적으로 분석을 위한 테이블인 **Stat**테이블로 생성됩니다.
2) 이 때, 테이블은 Impala SQL 로직을 따르기 때문에 **Impala 형태**로 생성됩니다. 
3) 현재의 Stat테이블 생성 로직을 Impala로직에만 한정 짓지 않고 다른 방면으로도 개편될 수 있는 확장성 확보가 필요합니다.
4) 따라서, 기존의 DailyStatJob을 **새로운 로직을 통해 개편**해 볼 수 있도록 하며, **SparkJob**으로 개편해 볼 수 있도록 합니다.
![TotalOverview](https://github.com/KimHyungkeun/NW_Intern_Project/blob/main/Pictures/TotalOverview.jpg)

**과제 목표 1** :  Stat테이블의 생성과정을 **SparkJob으로 재구성**해보는 것입니다.
![MakeTableOverview](https://github.com/KimHyungkeun/NW_Intern_Project/blob/main/Pictures/MakeTableOverview.jpg)

**과제 목표 2** :  기존 Job의 결과테이블과 내용을 비교하여 **정확성을 검증**합니다. 
![CheckTableOverview](https://github.com/KimHyungkeun/NW_Intern_Project/blob/main/Pictures/CheckTableOverview.jpg)

**설명**

1) 웹툰으로 부터 수집된 데이터들을 가공해서 만든 테이블들은 모두 **Stat**이라는 prefix가 붙으며 분석에 이용됩니다.

2) 일별로 단위를 나눈 후, 매일 테이블을 만들어내는 작업은 **DailyStatJob**이라는 **Java app**을 통해 진행중에 있습니다. 

3) 즉, Java App으로 구성된 테이블 생성 로직을 SparkJob으로 재구성하는것이 이번 과제의 목표입니다.

4) Spark로직 구성 시, **Scala**를 이용해 로직을 구성하고, SQL부문은 **SparkSQL**로 대체 됩니다.

**결과**

1) DailyStatJob에 의해 생성되는 테이블을 **SparkJob**으로 생성되도록 **진행 완료**

2) SparkJob으로 생성된 테이블과 DailyStatJob으로 생성된 테이블을 비교하여 **정확성 검증 확인 완료**

