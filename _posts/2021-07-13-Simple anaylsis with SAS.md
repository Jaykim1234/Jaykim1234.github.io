# Simple analysis with SAS



## **< Simple regression analysis >**

![img](file:///C:/Users/USER01/AppData/Local/Temp/msohtmlclip1/01/clip_image001.png)

![img](file:///C:/Users/USER01/AppData/Local/Temp/msohtmlclip1/01/clip_image003.jpg)

![img](file:///C:/Users/USER01/AppData/Local/Temp/msohtmlclip1/01/clip_image005.jpg)

 

**DF**

- Degrees of freedom. This term refers to the number of values that are free to vary

**F values**

- The **value** of Prob(**F**) is the probability that the null hypothesis for the full model is true (i.e., that all of the **regression** coefficients are zero).

- The F value is a value on the F distribution. Various statistical tests generate an F value. The value can be used to determine whether the test is statistically significant.
- The F value is used in analysis of variance (ANOVA). It is calculated by dividing two mean squares. This calculation determines the ratio of explained variance to unexplained variance.

- The F distribution is a theoretical distribution. There are many of these distributions, and each of them differs based on the degrees of freedom.
- The F value and the degrees of freedom of the sources of variance are used to determine the probability of the F value. The probability is the significance value for the test.

[Source : https://www.ibm.com/docs/en/cognos-analytics/11.1.0?topic=terms-f-value]()

**R-squared**

- R-squared is expressed as a percentage between 0 and 100, with 100 signaling [perfect correlation](https://www.investopedia.com/terms/c/correlation.asp) and zero no correlation at all. The figure does not indicate how well a particular group of securities is performing. It only measures how closely the ‘returns’ align with those of the measured benchmark. It is also backwards-looking—it is not a predictor of future results.

 

**Adjusted R-squared**

- Adjusted R-squared can provide a ‘more precise’ view of that correlation by also taking into account how many independent variables are added to a particular model. This is done because such additions of independent variables usually increase the reliability of that model—meaning, for investors, the correlation with the index.

[Source : https://www.investopedia.com/ask/answers/012615/whats-difference-between-rsquared-and-adjusted-rsquared.asp]()

**MSE**

- The MSE either assesses the quality of a **predictor** (i.e., a function mapping arbitrary inputs to a sample of values of some [random variable](https://en.wikipedia.org/wiki/Random_variable)), or of an [**estimator**](https://en.wikipedia.org/wiki/Estimator) (i.e., a [mathematical function](https://en.wikipedia.org/wiki/Mathematical_function) mapping a [sample](https://en.wikipedia.org/wiki/Sample_(statistics)) of data to an estimate of a [parameter](https://en.wikipedia.org/wiki/Statistical_parameter) of the [population](https://en.wikipedia.org/wiki/Statistical_population) from which the data is sampled). MSE measures the mean square difference between the estimated value and the actual value.

[`Source : https://en.wikipedia.org/wiki/Mean_squared_error#Definition_and_basic_properties`]()

 

 

![img](file:///C:/Users/USER01/AppData/Local/Temp/msohtmlclip1/01/clip_image007.jpg)

**Confidence limits**

- Confidence limits for the mean ([Snedecor and Cochran, 1989](https://www.itl.nist.gov/div898/handbook/eda/section4/eda43.htm#Snedecor)) are an interval estimate for the mean. Interval estimates are often desirable because the estimate of the mean varies from sample to sample. Instead of a single estimate for the mean, a confidence interval generates a lower and upper limit for the mean. The interval estimate gives an indication of how much uncertainty there is in our estimate of the true mean. The narrower the interval, the more precise is our estimate.

- Confidence limits are expressed in terms of a confidence coefficient. Although the choice of confidence coefficient is somewhat arbitrary, in practice 90 %, 95 %, and 99 % intervals are often used, with 95 % being the most commonly used.

- As a technical note, a 95 % confidence interval does not mean that there is a 95 % probability that the interval contains the true mean. The interval computed from a given sample either contains the true mean or it does not. Instead, the level of confidence is associated with the method of calculating the interval. The confidence coefficient is simply the proportion of samples of a given size that may be expected to contain the true mean. That is, for a 95 % confidence interval, if many samples are collected and the confidence interval computed, in the long run about 95 % of these intervals would contain the true mean.

[`Source: https://www.itl.nist.gov/div898/handbook/eda/section3/eda352.htm`]()

 

![img](file:///C:/Users/USER01/AppData/Local/Temp/msohtmlclip1/01/clip_image009.jpg)

 

## **< Multiple linear regression analysis >**

 

![img](file:///C:/Users/USER01/AppData/Local/Temp/msohtmlclip1/01/clip_image011.jpg)

![img](file:///C:/Users/USER01/AppData/Local/Temp/msohtmlclip1/01/clip_image013.jpg)

 

 

 

## **< Testing differences between two group means >**

 

**Testing****
 
**

\-    In statistics, "testing" refers to a series of processes in which observed statistics are determined whether or not statistically significant. At this time, we need to be particularly careful that we use the expression "statistically significant," not just the expression "significant."

[Source: https://babilusa.tistory.com/42]()

 

**proc** **ttest** data=a.thesis_total;

class DS1_SEX ;

VAR cbmi;

**RUN**;

 

![img](file:///C:/Users/USER01/AppData/Local/Temp/msohtmlclip1/01/clip_image015.jpg)

**Pooled vs Satterthwaite**

\-    The main difference is that the **Satterthwaite** approximation does not assume equal variances, whereas the **pooled** method does. In other words, you can always use the **Satterthwaite** method and be correct, but you can only use the **pooled** method in very specific (and rare) circumstances.

 

[Source: https://www.bgsu.edu/content/dam/BGSU/college-of-arts-and-sciences/center-for-family-and-demographic-research/documents/Help-Resources-and-Tools/Statistical%20Analysis/Annotated-Output-T-Test-SAS.pdf]()

 

## **< ANOVA >**

 

The distribution used for ANOVA is the F-distribution.

 Total Variation represents the overall variation of the response variable.

 

![SE22016031722341470.png](file:///C:/Users/USER01/AppData/Local/Temp/msohtmlclip1/01/clip_image016.png) 

\-    Calculating the allows you to obtain the total variation SST (Total Sum of Squares.)

 

\-    Between Group Variation is the variation described by an independent variable.

 

![SE22016031722360270.png](file:///C:/Users/USER01/AppData/Local/Temp/msohtmlclip1/01/clip_image017.png) 

\-    Calculating the allows you to obtain Model Sum of Squares (SSMs) of variation between groups.

 

\-    Within Group Variation is a variation that is not described by the model.

 

![SE22016031722372070.png](file:///C:/Users/USER01/AppData/Local/Temp/msohtmlclip1/01/clip_image018.png) 

\-    Calculating the allows you to obtain within-group error sum of squares (SSE).

 

 

 **SST=SSM+SSE**

 

 

The F statistic used for ANOVA can be calculated as follows: 

 

![SE22016031722403770.png](file:///C:/Users/USER01/AppData/Local/Temp/msohtmlclip1/01/clip_image019.png)

![SE22016031722421770.png](file:///C:/Users/USER01/AppData/Local/Temp/msohtmlclip1/01/clip_image020.png)

 

You can also obtain a coefficient of determination in ANOVA. The coefficient of determination can be obtained as the proportion of variation described by the model, that is, the proportion of variability described by the independent variable.

 

 

**proc** **ANOVA** data=a.thesis_total;

class DS1_MARRY_A;

MODEL BR_AGE = DS1_MARRY_A;

MEANS effects

RUN;

 

![img](file:///C:/Users/USER01/AppData/Local/Temp/msohtmlclip1/01/clip_image022.jpg)

 