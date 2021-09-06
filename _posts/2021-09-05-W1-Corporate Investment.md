---
title:  "ACF-W1-01-Corporate Investment"

categories:
  - UvA_Advanced Corporate Investment
tags:
  - ACF-W1-01-Identifying Investmet Opportunity
---


# Identifying Investmet Opportunity

## How do firms make investment decisions?
  - Common rule of thumb: NPV>0 인것 고려
  - NPV : discounted value of all progect cash flow
  - r   : Opportunity cost of capital (회사가 다른 투자를 했을 때 얻을 수 있는 가장 큰 가치)   
    - return은 **risk**를 고려해서 조정이 되어야 한다.
  - NPV > 0:
    - 프로젝트가 그 다음 차선의 투자 기회보다 더 큰 보상을 제공 
    - Value created from investment exceeds the firm's initital cost of purchasing caiptal
    - Stock market participandts should anticipate this. 그래서 투자가 시작 되기 전에도 입찰에 참여
    - **Tobin's Q** 
      - Market vlaue of firm/ Replacement cost of capital
      - 회사의 가치(시가 총액)를 capital의 가치(순자산 가치)로 나눈 것
      - 주식시장에서 평가된 기업의 가치를 기업의 총실물자본의 구입가격으로 나눈 값
        - replacement cost: price firm would have to pay on market for capital
        - **Market-book ratio**가 이것 과 비슷하고 가끔씩 대체해서 사용 되기도 한다.
      - **해석하는 방법**
        - Q>1 
          - Has **positive NPV opportunity**
          - Firm generate more value using capital than other investors or firms would
          - 다른 회사들 보다 같은 capital을 사용했을 때 더 많은 자본 창출
          - 기업은 적은 비용을 들여 주식 시장에서 높은 가치를 창출 할 수 있다는 뜻. 
          - 그렇기에 Q가 높다는 것은 주식시장에 있어서 과대평가가 된다고 해석할 수도 있다.
            - internal value of capital higher than what market willing to pay
            - Ex. Shipping firm with Q of 1.5 can buy new truck for 100 and use it to generate NPV of 50
              - capital * (Tobin Q - 1) 만큼 NPV 생김
          - 기업은 기업의 가치를 높이기 위해 투자를 더 할 것이다.
        - Q<1
          - Wasting some capital, better off selling assets
          - 자본 활용을 너무 못한 다는 뜻
          - 기업은 감소하는 자본을 대체하지 않을 것이다.
        - Q=1
          - 기업은 최적자본량을 달성한 것이다.
        - 여기서 **분자(numerator) = firm's market cap + debt**
        - **분자(numerator) = 시장 총액의 가격+ 부채**
          - 여기서 **debt**도 **반드시 시장의 가치를 사용**해야 하는데 종종 book value로 사용 된다.
        - **분모(denumerator)** = **book** value of total assets or PP&E
        - **분모(denumerator)** = **총 자산의 가격**
          - book value: 회사가 *그 자산을 사기위해 시장에서 지불한 가치*
        - **Q= (시가총액+debt)/total asset** ( 총자산은 장부가격으로 한다. 추정가격 x)
      - Q는 투자심리나 성장 가능성을 나타내는 지표와 적절히 사용하면 활용 가능 성이 높다.

## 문제
![](2021-09-05-17-46-11.png)</p>

**정답 1**
    - 여기서 궁금한 것은 NPV의 상승이 market cap을 증가시키는 것인가 이다.
    - 물론 npv의 상승의 주가의 상승에 기여를 해서 market cap을 상승시킬 수 있지만 이는 간접적인 영향으로 인해서 증가한 것이다. 그렇기 때문에 1번이 왜 맞는지에 대해서 확신이 없다.  


![](2021-09-05-17-53-17.png)</p>
  - numerator(분자)는 market cap + debt를 합친 것인데 내 생각에는 brand value는 분자에 포함이 된다. 브랜드는 무형의 중요한 자산이다. 코카콜라의 판매에 있어서 브랜드는 상당한 비중을 차지한다. 이는 팹시와 코카콜라가 맛이 큰 차이가 없지만 코카콜라가 브랜드 인식으로 인해서 더 잘 팔리는 것을 통해서 알 수 있다. 그렇기 때문에 brand 가치는 분자에 포함이 된다.
  
  - denumerator(분모)는 내 생각에는 회계적 장부에서 나타나는 가치를 의미하는 것 같다. 브랜드가 무형의 자산이기 때문에 회계적 장부에 나올수 없기에(?) 분모에는 변화가 없다.
  
  - 정리하면 분자는 올라가고 분모는 그대로 이다.  

# Intro to Q Theory
## Brief overview of Q theory

- K: capital
  - Captial depreciates at annual rate δ
- δ: discount rate 
- I: investment amount (Spend I on new assets)
- Firm's value
      -  v_0=αk_1∕(1+r)
      -  k_1 = I_0 + (1-δ)K_0
- (I_0/k_0)^2 = Capital adjustment cost 
    - Ex: Operating more machines requires increasing amount of attention from mangement.
      - capital의 양이 많아지면 많아질 수록 or 회사 사이즈가 커질 수록 관리비가 기하 급수적(?)으로 늘어난다.

## Firm's maximization problem

- Firm choose I_0 to maximize:
  -   ![](2021-09-06-13-24-36.png)
      -   Q>1 보다 커야만 투자를 한다.

- 문제
  - ![](2021-09-06-13-41-23.png)
    - 독립변수는 market cap+ debt이다.
    - 종속변수는 k_0에 영향을 미치는 요인이다.


## A few technical details
  - In Maximization problem
    - q = *(∂V_1)/(∂K_1)* <<< why?? : ∂V_1 refers to changes of market value
      - Interpretation can be 
        - ' How much market values changes with the one extra unit of capital'
      - This makes investment depends on the **marginal** profits from one extra unit of captital.
      - q is measured as average value of capital
        - Total market value/total capital cost
      - Hayashi Theorem
        - under same plausible condition
          - average q = marginal q
  - When there is **no adjustment costs**
    - ![](2021-09-06-14-42-22.png)
    - Maximization problem
      - ![](2021-09-06-14-43-23.png)
      - q = 1 **always**

#  Evidence on Q Theory

확인 할 것
1. 투자와 Q는 양의 상관 관계
2. Q가 유일한 변수 (다른 변수는 영향 ㄴㄴ)

## 연구 결과 밝혀진 문제들 Lack of empirical evidence

1. Q가 투자의 변화를 설명을 잘 못한다.(R^2가 값이 낮음)
2. **Adjustment costs** 가 **클 때**만 Regression estimates of Q가 영향이 있는 것으로 나타났다.
3. Q뿐만 아니라 **많은 다른 변수**들이 *투자와 연관성이 있는 것*으로 들어남
  
요약하면 Q는 coporate investment에 있어서 중요하지만 다른 factor들이 더 중요하다.

## Hypothesis 1: Mesurement error in Q

- *Measurement error could explain* **lack of empirical evidence**
- **측정 오류**가 Q 이론이 실제적으로 적용이 안되는 부분을 **설명**할 수 있음
    - OLS regression에서 measurement error가 있으면 coefficient 가 거의 0에 가까워 진다.(Q 변수가 설명력이 없어진다는 뜻, 그리고 R^2 도 줄어든다.)
    - Bias can also lead to significant coefficients on other variables(이거 이해 x)
- **Q는 measurment error가 있다.** 왜 measurement error가 있는지에 대한 이유로는
  - market value of equity가 투자기회(investment opportunity) 말고도 다양한 요인들에 의해서 영향을 받기 때문이다.
  - Q는 **debt**의 **시장가격**에 기초해야 하는데 book value가 종종 사용된다.
  - book value of assets 는 과거의 가격에 기초했는데 이는 현재의 replacement costs를 반영하지 못할 수 있다.
  
- *Measurement error를 고려한 새로운 실험 결과*
  - Erickson and Whited (2000) employ advanced statistical thechinique to remove measurement error from Q
    - 결과
      - R^2 more than doubles after accounting for measurement error
      - Coefficient estimates on Q ar esubstantially larger than simple OLS
      - Estimates of other variables( e.g cashflosw) small and insignificant
      - ![](2021-09-06-23-31-06.png)
  - Peters and Taylor (2017) find that Q work much better when intangible assets are included
    - ![](2021-09-07-00-06-54.png)  
- 문제
  ![](2021-09-07-00-05-37.png) 

## Hypothesis 2: Financial constraints


- Firms must invests C_0 up front, and receive cashflows in future
  - But where doese initial cash C_0 come from?
  - **이게 왜 문제인거?? cash랑 어떻게 연관이 되는거지? marcap?**

    - Young firms start with almost no cash, and are also not profitable
      - Main way to fund investment is raising external financing
      - mature firms typically hold cash and are profitable, but may face  very large upfront investment costs.
  - If a firm has difficulty raising external financing, it may pass up investment opps **even when Q is high**
- 정리하면 Starting firm한테는 Q가 높아도 financing 받는거 아니면 돈 벌기가 힘들기 때문에 Q이론이 적용되지 않을 수 있다는 말이다.
  - 그렇다면 왜 financing이 어려울까? 왜 financing이 costly할까?
    - Pecking order theory predicts that investment is cheaper to finance using internal funds(i.e.,cash) than external/ 외부에서 돈 받는 것 보다 내부 회사 돈 쓰는게 더 싸다
      - Internal financing이 더 싼 이유
        - **Asymmetric info**
          - Firm's managers know its condition better than external investors
          - 회사의 매니저는 외부투자자보다 더 많은 정보를 가지고 있음
            - 회사가 external financing 즉 주식을 팔아서 자금을 충당하려고 한다면 이는 외부 투자자들에 있어서 회사의 미래가 어둡다고 생각하게 할 수 있다.
            - 회사가 주식을 매각하지 않고 cash를 사용하면 외부 투자자들은 회사가 안정적이다라고 생각할 수 있다.
          - 그래서: Firms with volatile cashflows should build up internal funds, to ensure sufficient liquidity during bad years.
            - 회사는 안정적인 현금 흐름을 확보하는 것이 중요하다. 