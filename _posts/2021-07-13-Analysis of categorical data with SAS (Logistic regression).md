## 1. Categorical data

- Definition: data (Qualitative data) in which the survey or observation results are categorized into categories or attributes rather than numbers.

- Quantitative data can also be replaced with categorical data if separated by intervals (categoryization of quantitative data)

- Factors : Categorical Variables

- Levels : values taken by categorical variables

  

## 2. Contingency table

- Definition: data in tabular form used to analyze categorical data

- Columns or rows are levels of factors (categorical variables)

- Cells are the frequency of observations corresponding to each level of the factor

  ![image](https://user-images.githubusercontent.com/78076248/125400762-40de5900-e3ed-11eb-8e29-548174bac5a3.png)



## 3. Logistic regression

![image](https://user-images.githubusercontent.com/78076248/125400780-46d43a00-e3ed-11eb-8fe2-0c1eb4a6de17.png)

Logistic regression is a supervised learning algorithm that uses regression to predict the probability that data fall into a category from 0 to 1 and categorizes it as belonging to a category that is more likely.

It's easy when you think of examples like spam classifiers. If you receive an email and the probability that it is spam is 0.5 or more, you can classify it as spam, and if the probability is less than 0.5, you can classify it as normal ones. This determination of data to fall into one of two categories is called binary classification.

In logistic regression, the following steps are taken to predict the probability that the data fall into a particular category.

1. It initializes the coefficients and intercepts of all properties to zero.
2. The value of each property is multiplied by a coefficient to obtain **log-odds**.
3. **log-odds** are inserted into the **sigmoid function** to obtain probabilities in the range [0,1].



### Log-odds



**log [p/(1-p)]**

**Where:**

- p = the probability of an event happening
- 1 – p = the probability of an event not happening



### Sigmoid function

A sigmoid function is a mathematical function with an S-shaped curve or sigmoid curve. An example of a sigmoid function is the logistic function shown in the first figure, defined by the following formula.

![image](https://user-images.githubusercontent.com/78076248/125400807-4fc50b80-e3ed-11eb-8c65-19926f0de19e.png)

The sigmoid function has an entire real number of real numbers, and although it is common for the return value to increase or decrease in monotony, it can also decrease in monotony. The return value (y-axis) of a sigmoid function often ranges from 0 to 1. Alternatively, it can range from -1 to 1.

![image](https://user-images.githubusercontent.com/78076248/125400816-53589280-e3ed-11eb-91b0-8807f77bc37d.png)



### Classification Threshold

The resulting value of the logistic regression algorithm is 'classification probability', so if this probability is obtained above a certain level, the sample can be determined whether it belongs to the class or not.

And, of course, the default threshold for most algorithms is 0.5.

However, the threshold of the model can be changed as necessary. For example, when creating a logistic regression model that diagnoses cancer, it is necessary to increase the sensitivity of the model by lowering the threshold to 0.3 or 0.4 to more sensitively check just in case. That way, even if there are more misclassifications overall, there will be fewer cases of missing cancer patients.

Let's understand the picture below.

If it's a 0.5 threshold, that's what it looks like.

![image](https://user-images.githubusercontent.com/78076248/125400833-58b5dd00-e3ed-11eb-9ffd-908453606308.png)

This is what happens when you adjust it to a threshold of 0.4.

![image](https://user-images.githubusercontent.com/78076248/125400846-5b183700-e3ed-11eb-9e1a-bb77d7866f33.png)



### Types of Logistic Regression

On the basis of the categories, Logistic Regression can be classified into three types:

- **Binomial:** In binomial Logistic regression, there can be only two possible types of the dependent variables, such as 0 or 1, Pass or Fail, etc.
- **Multinomial:** In multinomial Logistic regression, there can be 3 or more possible unordered types of the dependent variable, such as "cat", "dogs", or "sheep"
- **Ordinal:** In ordinal Logistic regression, there can be 3 or more possible ordered types of dependent variables, such as "low", "Medium", or "High".



## 4. Logistic regression with SAS



**The basic form of CODE**

proc logistic data= [Name of data you use]; where [Dependent variable]  not in ( [Null value] )  

class [All independent variables]

model [Dependent variable] = [All independent variables] ;



**Example**

proc logistic data=b.thesis; where csmok not in (99);    

	class DS1_SEX1(PARAM=REF REF='1') DS1_MARRY_A_1(PARAM=REF REF='1') DS1_EDU1 (PARAM=REF REF='1')  DS1_INCOME1 (PARAM=REF REF='1') DS1_JOB_1 (PARAM=REF REF='1') 
	          csmok(PARAM=REF REF='0') cdrink(PARAM=REF REF='0') gexer_wk1 (PARAM=REF REF='1') gbmi1 (PARAM=REF REF='1') PWI_2 (PARAM=REF REF='1') energy (PARAM=REF REF='1')
			  DS1_SRH_1 (PARAM=REF REF='1')  DS1_FCA_1 (PARAM=REF REF='1') 	 			
	          group (PARAM=REF REF='1');
	
	model csmok (ref='0') = group1 cage DS1_SEX1 DS1_MARRY_A_1 DS1_EDU1 DS1_INCOME1 DS1_JOB_1 cdrink gexer_wk1 gbmi1 PWI_2 energy DS1_SRH_1 DS1_FCA_1; 

run;



**Explanation of option [ PARAM=REF REF=   ]**

As an extra bit of flexibility, the REF= option in the CLASS statement determines the reference level for the EFFECT and REFERENCE coding. As with the PARAM= option To program the reference level for each variable individually, use the REF = “ “ option in parentheses immediately following the variable in the CLASS statement, or use the keyword FIRST or LAST. Note that unless you use FIRST or LAST, the reference level should be placed in either single or double quotation marks, as follows: 





**Result from the example code ** 

![image](https://user-images.githubusercontent.com/78076248/125400916-73885180-e3ed-11eb-89e9-62344400febb.png)

 

![image](https://user-images.githubusercontent.com/78076248/125400925-76834200-e3ed-11eb-9ad6-190602f8ad2d.png)

![image](https://user-images.githubusercontent.com/78076248/125400935-797e3280-e3ed-11eb-8f2b-82736f843ef7.png)

![image](https://user-images.githubusercontent.com/78076248/125400948-7c792300-e3ed-11eb-8539-01a8f5b4dcfe.png)

![image](https://user-images.githubusercontent.com/78076248/125400967-826f0400-e3ed-11eb-83d0-d3f704db55de.png)



### Interpretation of the result



Before we can interpret this result, we need to know the meaning of Chi-square value



**Chi-square**



**1. Fomular**

![image](https://user-images.githubusercontent.com/78076248/125400979-8733b800-e3ed-11eb-9c77-5a7b1986bdb9.png)



**2. Chi-Square Test Method**

 	1. Independence Test: Are the two variables related or not?
 	2. Conformity Test: Is the actual sample the same or different from the distribution I think?
 	3. Test of Consistency: Are the two groups equally distributed? Is it a different distribution?





**3. Chi-Square test Type**

1. One-way chi-square test: target one category -> conformity test

2. Two-way chi-square test: targets two or more categories -> independence, homogeneity test



**Logistic regression with Chi-Square**

In logistic regression, we use a calculus based function called Maximum Likelihood (or ML). ML does the same sort of thing in logistic regression. It finds the function that will maximize our ability to predict the probability of y based on what we know about x. In other words, ML finds the best values for the formulas to predict dependent variables. 

The Maximum Likelihood function in logistic regression gives us a kind of chi-square value. The chi-square value is based on the ability to predict y values with and without x. The ML method does a similar thing. It calculates the fitting function without using the predictor x and then recalculates it using what we know about x. The result is a difference in goodness of fit. The fit should increase with the addition of the predictor variable, x. Thus, a chi-square value is computed by comparing these two models (one utilizing x and one not utilizing x). Thus if the p-value of chi-square is less than 0.05 or 0.001, this means the selected independent variable affects the dependent variable. 



***Note**

The 2 X 2 contingency analysis with chi-square is really just a special case of logistic regression. With chi-square contingency analysis, the independent variable is dichotomous and the dependent variable is dichotomous.





### Reference



https://data-gardner.tistory.com/29

http://hleecaster.com/ml-logistic-regression-concept/

https://ko.wikipedia.org/wiki/%EC%8B%9C%EA%B7%B8%EB%AA%A8%EC%9D%B4%EB%93%9C_%ED%95%A8%EC%88%98

https://www.javatpoint.com/logistic-regression-in-machine-learning

http://web.pdx.edu/~newsomj/pa551/lectur21.htm

https://www.statisticshowto.com/log-odds/



