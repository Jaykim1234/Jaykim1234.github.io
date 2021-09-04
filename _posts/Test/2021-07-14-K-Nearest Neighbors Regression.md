

![image](https://user-images.githubusercontent.com/78076248/125558420-fa4a6bea-87d3-4fd6-80e3-daf12c5ac88c.png)



## 1. Principle of K-Nearest Neighbors Regression



Regression using the K-Nearst Neighbors algorithm is eventually the same in classification and principle.
 

When new movie data comes in, you will find the nearest k neighbors through the Distance Formula. In classification, the number of labels for neighbors was confirmed and decided by majority vote, but in regression, there is a difference in that the average of neighbors is calculated. That's why if the three neighbors closest to the new film had ratings of 5.0, 6.8 and 9.2, they would expect it to be rated 7.0.

 

## 2. Understanding Weighted Regression

First of all, the principle is easy. However, we can also apply the average method more intelligently.

Why don't we find a weighted average based on how close each neighbor is, rather than just finding the average of nearby neighbors? The closer the distance is, the more similar the data will be, and the more weight it is given.


 For example, to predict the rating of movie X, let's say we found the three nearest neighbors as below.
 o Movie: A / Rated: 5.0 / Distance to X: 3.2
 o Movie: B / Rating: 6.8 / Distance to X: 11.5
 o Movie: C / Rated: 9.0 / Distance to X: 1.1


 If you just take the average, X's expected rating is 6.93.
 However, movie X is the closest to movie C (because distance is the closest), so the rating of movie C is more important when calculating the average.
 In the end, the weighted average is 7.9. (The expression is as follows.)

![image](https://user-images.githubusercontent.com/78076248/125558431-cb92542f-7b91-4659-a0eb-72c288d350b4.png)

The numerator is the sum of the scores of movies (neighbors) divided by the distance from X, and the denominator is the sum of the distances from X.

 

## 3. Selecting Parameters


 Choosing the best k-value is data-dependent. In general, the larger the k-value, the less the effect of noise in the classification. Good k can be chosen with a variety of heuristic. A special case (i.e., when k = 1) in which an item is predicted to be an item of the nearest training sample is called a nearest neighbor algorithm.

 The accuracy of the k-NN algorithm is significantly reduced when noise or irrelevant features exist or feature size does not match importance. Many studies have tried to improve classification by selecting or resizing features. A particularly popular approach is the use of evolutionary algorithms to optimize feature size. 

 In a binary (2-item) classification problem, it is desirable to select an odd number, k, to avoid a vote of equality. One popular method of empirically selecting the optimal k in this environment is the bootstrap method.





**Reference** 

 

http://hleecaster.com/ml-knn-regression-example/
https://ko.wikipedia.org/wiki/K-%EC%B5%9C%EA%B7%BC%EC%A0%91_%EC%9D%B4%EC%9B%83_%EC%95%8C%EA%B3%A0%EB%A6%AC%EC%A6%98
