## 1. Comparing the results of various machine learning algorithms

# Compare Algorithms
import pandas
import matplotlib.pyplot as plt
from sklearn import model_selection
from sklearn.linear_model import LogisticRegression
from sklearn.tree import DecisionTreeClassifier
from sklearn.neighbors import KNeighborsClassifier
from sklearn.discriminant_analysis import LinearDiscriminantAnalysis
from sklearn.naive_bayes import GaussianNB
from sklearn.svm import SVC
# load dataset
url = "https://raw.githubusercontent.com/jbrownlee/Datasets/master/pima-indians-diabetes.data.csv"
names = ['preg', 'plas', 'pres', 'skin', 'test', 'mass', 'pedi', 'age', 'class']
dataframe = pandas.read_csv(url, names=names)
array = dataframe.values
X = array[:,0:8]
Y = array[:,8]
# prepare configuration for cross validation test harness
seed = 7
# prepare models
models = []
models.append(('LR', LogisticRegression()))
models.append(('LDA', LinearDiscriminantAnalysis()))
models.append(('KNN', KNeighborsClassifier()))
models.append(('CART', DecisionTreeClassifier()))
models.append(('NB', GaussianNB()))
models.append(('SVM', SVC()))
# evaluate each model in turn
results = []
names = []
scoring = 'accuracy'
for name, model in models:
	kfold = model_selection.KFold(n_splits=10, random_state=seed)
	cv_results = model_selection.cross_val_score(model, X, Y, cv=kfold, scoring=scoring)
	results.append(cv_results)
	names.append(name)
	msg = "%s: %f (%f)" % (name, cv_results.mean(), cv_results.std())
	print(msg)
# boxplot algorithm comparison
fig = plt.figure()
fig.suptitle('Algorithm Comparison')
ax = fig.add_subplot(111)
plt.boxplot(results)
ax.set_xticklabels(names)
plt.show()

## 2. Data Science and Data analytics difference.

   While Data Science focuses on finding meaningful correlations between large datasets, Data Analytics is designed to uncover the specifics of extracted insights. In other words, Data Analytics is a branch of Data Science that focuses on more specific answers to the questions that Data Science brings forth.

## 3.Types of biases that occur in machine learning

### Automation Bias
:사람들이 자동화된 결정을 그냥 신뢰하는 것

### Confirmation Bias
:문제를 해결하기 위해 정보를 뽑아내는 것이 편향된 정보 추출로 이루어질 수 있음

### Group Attribution bias
: 한 사람들의 기준이 그룹 전체의 기준이 될 수 있다고 가정하는 것
ex) Conveinence sampling

### Selection Bias


### Reporting Bias



### Reference
https://analyticsindiamag.com/bias-machine-learning/
https://machinelearningmastery.com/compare-machine-learning-algorithms-python-scikit-learn/