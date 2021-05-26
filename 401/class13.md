#Linear Regressions


## Regression analysis
Regression analysis  is one of the most important fields in statistics and machine learning. There are many regression methods available. Linear regression is one of them.
Regression searches for relationships among variables.


## When Do You Need Regression?
- to answer whether and how some phenomenon influences the other or how several variables are related
- is also useful when you want to forecast a response using a new set of predictors.
- Regression is used in many different fields: economy, computer science, social sciences, and so on

## What is Linear Regressions in Python?
- Linear regression is one of the fundamental statistical and machine learning techniques. Whether you want to do statistics, machine learning, or scientific computing, there are good chances that you’ll need it.
- Linear regression is probably one of the most important and widely used regression techniques. It’s among the simplest regression methods. One of its main advantages is the ease of interpreting results.

## scikit-learn:

The package scikit-learn is a widely used Python library for machine learning, built on top of NumPy and some other packages. It provides the means for preprocessing data, reducing dimensionality, implementing regression, classification, clustering, and more. Like NumPy, scikit-learn is also open source.


## use Linear regression :

## Exploring Boston Housing Data Set
1. The first step is to import the required Python libraries into Ipython Notebook.

    ``` 
    %matplotlib inline 
    import numpy as np
    import pandas as pd
    import scipy.stats as stats
    import matplitlib.pyplot as plt
    import sklearn
    
    ```

2. print the feature names of the  data set.

    ```
    data_set.featrue_names

    ```

3. convert boston.data into a pandas data frame.

    ```
    bos= pd.DataFram(boston.data)
    bos.head()
    #after this line of code is excuted the column names will be in numbers so we have to change the column names with feature names

    bos.columns = boston.freature_names
    bos.head()

    # add boston.target to the fram in a column named PRICE

    bos['PRICE'] = boston.target 

    ```

## Scikit Learn
 lets fit  a linear regression model and predict the Boston housing prices. using least squares method (to elemenate coefficients)

    ```
    from sklearn.linear_model import linearRegression
    x=bos.drop('PRICE' ,axis =1)
    lm = LinearRegression()

    ```

### Fitting a Linear Model
 * print the intercept and number of coefficients.

    ``` 
    print 'Estimated intercept coefficient' , lm.intercept_
    print 'Number of coefficients',len(lm.coef_)

    ```

 * construct a data frame that contains features and estimated coefficients.

    ``` 
    pd.DataFram(zip(X.columns,lm.coef_),columns =['features',estumatedCoefficients])


    ```

 * plot a scatter plot between True housing prices and True RM.

        ``` 
            plt.scatter(bos.RM,box.PRICE)
            plt.xlabel("Average number of rooms per dwelling (RM)")
            plt.ylabel("Housing Price")
            plt.title("Relationship between RM and Price")
            plt.show()
        ```


   

The Result:

![img](https://bigdata-madesimple.com/wp-content/uploads/2016/04/Relationship-between-RM-and-Price.png)

