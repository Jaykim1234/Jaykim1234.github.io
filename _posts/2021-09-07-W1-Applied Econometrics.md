---
title:  "AE-W1-OLS_Experiements"

categories:
  - Applied Econometrics
tags:
  - AE_OLS_Experiements
---


# OLS & Experience

# Part A

- Causal inference
  - 종속 변수를 바꾸면 독립 변수가 **어떻게 변할 까**?
  - ![](2021-09-07-10-10-02.png)!
    - 내가 학교를 15년 다니는 것에서 16년 다니면 income이 얼마 오른다.
    - 여기서 관건은 이 연관 관계가 진짜인지 단순히 같이 나타나는 현상인지 알아내야 한다.


- Prediction
  - 종속 변수 Y를 **예측** 하는 것
  - ![](2021-09-07-10-12-34.png)
    - 형광펜 부분을 예측

# Part B

- OLS: Drawing a line through data(CH4, p146-159)
  - ![](2021-09-07-10-22-56.png)
  - ![](2021-09-07-10-34-58.png)
  - ![](2021-09-07-10-35-19.png)
  - ![](2021-09-07-10-40-32.png)

  -Core assumptions
    - ![](2021-09-07-10-41-46.png)
    - ![](2021-09-07-10-43-15.png)
    - Consistency
      - ![](2021-09-07-14-17-19.png)
      - ![](2021-09-07-14-23-15.png)
  - Endogeneity
    - Endogeneity leads to OLS inconsistency
      - ![](2021-09-07-14-24-59.png)
      - ![](2021-09-07-14-26-41.png) 
    - Sources of endogeneity
      - ??
      - ![](2021-09-07-14-36-48.png)
      - ![](2021-09-07-14-37-18.png)

  - Does knowledge increae loan take-up? or Does loan takeup increase knowledge?
    - ![](2021-09-07-15-05-43.png)
    - ![](2021-09-07-15-05-08.png)
    - **Statistical association does not imply causation!**

# Part C: Potential outcome
- Causal effects
  - ex)
    - Effect of Education on earnings
    - Effect of Performance pay on firm profits
    - Effect of FDI on economics growth
    - Effect of finanical regulation on finanical stability
  - Typically the average imapct of a one unit 'exogenous' change in '**treatment**' X_i on outcome variable of interst Y_i

  - Knowldege of causal effects important for economic policy & business decisions

- Potential outcome
  - ![](2021-09-08-08-42-26.png)
  - ![](2021-09-08-08-46-17.png)
- Potntial outcomes example: loan take-up and knowledge
  - ![](2021-09-08-08-49-34.png)
- The counterfactual problem 
  - What would happen in the other world
  - ![](2021-09-08-08-50-14.png)
  - ![](2021-09-08-08-50-43.png)
    - Here is no causal effect
  - ![](2021-09-08-08-52-58.png)
  - ![](2021-09-08-08-53-51.png)
- The counterfactual problem: Solve by OLS?
  - ![](2021-09-08-09-04-43.png)
- The counterfactual problem and endogeneity
  - ![](2021-09-08-09-06-02.png)
- Identifiaction: Solutions to the counterfactual problem
  - ![](2021-09-08-09-06-56.png)
  - ![](2021-09-08-09-07-11.png)
  - Identification 2가지 방법

    - ![](2021-09-08-09-09-59.png)

# Part D 
## Experiments - Design
## How to set up experiments

- Experiments in the social sciences
  - ![](2021-09-08-09-29-09.png)
- Identification using **experimental** data 
  - ![](![](2021-09-08-09-35-30.png).png)
  - Unconditional Random assignment
    - ![](2021-09-08-09-36-16.png)
    - ![](2021-09-08-09-37-37.png)
  - Conditional Random assignment
    - ![](2021-09-08-09-45-31.png)
  - Testing random assignment
    - ![](2021-09-08-09-50-51.png)
    - Tablue mean comparison
      - Experimental design
        - 개별적으로 t-test를 한 것
        - ![](2021-09-08-09-52-08.png)
        - ![](2021-09-08-09-51-49.png)
      - Convincing others of random assignment
        - ![](2021-09-08-09-52-46.png)
        - Covriance balance test
          - 그냥 전체 변수가 0인지를 F-test로 확인 하는 것
          - ![](2021-09-08-09-59-33.png)

# Part E
## Experiments - Analysis

## Analysis by simple regression

- ![](2021-09-08-10-20-50.png)

## Good Control

- ![](2021-09-08-10-21-15.png)
- ![](2021-09-08-10-26-34.png)
- Case #1
  - Conditional Assignment: Only CMI holds

- Conditional Mean Independence
  - ![](2021-09-08-16-19-55.png)
  - ![](2021-09-08-16-20-47.png)
  - ![](2021-09-08-16-23-57.png)
  - ![](2021-09-08-16-28-35.png)
- 
## Good Control Case #2
  - ![](2021-09-08-16-33-48.png)
  - ![](2021-09-08-17-20-37.png)
  
## Good Control Case #3
  -![](2021-09-08-17-25-12.png)
  -![](2021-09-08-17-26-24.png)
    - B_3 Male 을 빼먹었을 때 
## Bad Control
  - ![](2021-09-08-17-30-32.png)
  - ![](2021-09-08-17-37-24.png)
    - 교육 효과에 직업을 변수로 넣으면 교육이 endougenous 된다.

 # Part F

 ## Validity
 - ![](2021-09-08-18-02-43.png)
 - Where validity fails
   - Internal validity fails
     - ![](2021-09-08-18-06-43.png)
       - 집단이 선택하는게 또 치우침
     - Attrition: dropping out
       - ![](2021-09-08-18-50-23.png)
         - Sample 들이 빠져 나가는 것
     - Experimental effects
       - ![](2021-09-08-18-53-41.png)
       - 실험 받고 있다는 사실 때문에 대상자들이 바꾸는 것
     - Spillovers
       - ![](2021-09-08-18-55-29.png)
       - 감염률이 줄어 드는 것
         - 전염성을 두 집단 모두 줄여서 생기는 것
     - Wrong standard errors (s.e)
       - ![](2021-09-08-19-03-09.png)
       - 이분산성은 모델이
     - Fraud
       - prof Stapel from Tilburg Uni
   - External validity
     - ![](2021-09-09-13-13-28.png)!
       - General equilibrium effects???
       - Black Box???
# f
## Summary

- ![](2021-09-09-13-34-48.png)


![](2021-09-09-13-37-27.png)