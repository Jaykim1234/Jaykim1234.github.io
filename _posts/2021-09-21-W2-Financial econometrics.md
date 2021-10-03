---
title:  "AE-W2-Solution to endogeneity"

categories:
  - Applied Econometrics
tags:
  - AE_OLS_Experiements
---
- 이번 챕터에서는 독립 변수들이 다른 변수들과 연관이 생겨서 우리가 정확한 독립 변수들의 효과를 파악하지 못하는 경우을 어떻게 과연 해결하는 지에 대해서 다루겠다.

- 이번에 배울 것들 
  - Instrumental Variables
      -  Assumes that variable Z is exogenous (in stead of X)
      -  Estimation and testing
      -  Internal validity
  - Heterogeneity
      - ▸ Students, people, firms, counties, observational units i in general have different effects β1i
      - ▸ Consequence for
      - ▸ OLS : ATE
      - ▸ Instrumental Variables: LATE
- 이걸 배우는 이유: 변수가 생략됨으로서 생기는 bias 
   - Omitted Variable Bias in the returns to education
      - ![](2021-09-21-09-12-38.png)
        - 여기 그래프는 학교를 다닌 기간과 임금 두 변수를 regression을 돌렸다.
      - ![](2021-09-21-09-14-38.png)
        - 하지만 우리가 학창시절을 생각해보면 학생들 수준이 모두 다름을 알 수 있다. 과연 단순하게 학교를 다닌 기간과 임금만을 따지는 것이 맞을까?
        - 이에 대한 의문으로 인해서 우리는 학생들 High ability와 Low ability 두 집단으로 나누어서 그래프를 다시 살펴보았다.
        - 위를 보면 우리는 각 집단 별 분포가 다름을 알 수 있다.
      - ![](2021-09-21-09-16-22.png)
        - 각 집단마다 선형 그래프가 그려진다. 이를 통해서 알 수 있는 것은 보이는 상관성이 인과관계를 나타내는 것은 아니라는 것이다. 첫 번째 그림에서 보이다 싶히 schooling과 wage는 언뜻 보면 서로 연관 된 것 처럼 보인다. 하지만 그 다음 high ability low ability 로 나누었을 때 shooling과 wage 두 변수 간의 상관관계를 정의하는 것은 오류가 있음을 알 수 있다.
        - 그렇기 때문데 통계적 연관성은 인과관계와 다르다.
      - ![](2021-09-21-09-18-06.png)
        - 그렇다면 우리는 그 숨겨진 변수를 어떻게 하면 찾을 수 있을까? 그 학생들간의 수준을 어떻게 하면 측정할 수 있을 까?
        - 이에 대해서 좀더 자세히 알아보겠다.
# Part B instrumental Variables -  Method

- ![](2021-09-21-09-19-20.png)
- ![](2021-09-21-09-27-18.png)
- ![](2021-09-21-09-28-44.png)
- ![](2021-09-21-09-33-25.png)
  - 정리하면 학생들의 Ability는 생년 월일로 정한다. 그래서 생년월일이 Instrument variable Z 가 된다. Independent variable X는 Schooling 기간 즉 학생들이 학교다니는 시기 Dependent variable Y는 Wage다.
  - 그러면 여기서 또 두 가지 단계가 생긴다.
    - 첫 번째는 X와 Z Dependent variable과 instrument variable 간의 상관관계이다. 이는 First stage가 된다.
    - 두 번째는 Y와 Z이다. 이는 Reduced form이라고 한다.
## Core assumptions & distribution
-   ![](2021-09-21-09-40-52.png)
    - FS: Schooling을 year of birth와 Control 변수인 W로 리그레션을 돌린 후 schooling에 대한 추정치를 구한다.
    - Second Stage: Wage를 FS에서 구한 X의 추정치를 독립변수로 하고 Control 변수인 W를 넣어서 리그레션을 돌린다. 
-   ![](2021-09-21-09-46-06.png)
    -   Relevance  : Z랑 X는 서로 연관성이 있어야 한다. COV(X,Z) != 0
    -   Exogeneity : Z는 다른거랑은 연관성이 없어야 한다. W랑 연관성이 있으면 안된다. 이게 마지막이여야 한다.
-   ![](2021-09-21-09-48-19.png)
-   ![](2021-09-21-09-49-46.png)
-   ![](2021-09-21-09-53-06.png)

## Estimation and testing

- ![](2021-09-21-09-53-37.png)
- ![](2021-09-21-09-54-35.png)

# Part C

- ![](2021-09-21-09-58-23.png)
- ![](2021-09-21-10-01-52.png)
- ![](2021-09-21-10-02-37.png)
- ![](2021-09-21-10-03-28.png)
- ![](2021-09-21-10-08-22.png)
- ![](2021-09-21-10-10-48.png)
- ![](2021-09-21-10-14-11.png)