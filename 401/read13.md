# Linear regression

- linear regression is a popular technique and you might as well seen the mathematical equation of linear regression.

- Scikit-learn is a powerful Python module for machine learning. It contains function for regression, classification, clustering, model selection and dimensionality reduction.

#### Exploring Boston Housing Data Set:

- The first step is to import the required Python libraries into Ipython Notebook.

![](https://bigdata-madesimple.com/wp-content/uploads/2016/04/Explore-1.png)

- We will import Boston data set into Ipython notebook and store it in a variable called boston.
![](https://bigdata-madesimple.com/wp-content/uploads/2016/04/sklearn.png)

- The object boston is a dictionary, so you can explore the keys of this dictionary.
![](https://bigdata-madesimple.com/wp-content/uploads/2016/04/boston-keys.png)

- We are going to print the feature names of boston data set.
![](https://bigdata-madesimple.com/wp-content/uploads/2016/04/boston-features.png)

- In this data set we have 506 instances(rows) and 13 attributes or parameters(columns).
![](https://bigdata-madesimple.com/wp-content/uploads/2016/04/boston-description.png)

- To convert boston.data into a pandas data frame.
![](https://bigdata-madesimple.com/wp-content/uploads/2016/04/Pandas-DataFrame.png)

- We are going to replace those numbers with the feature names.
![](https://bigdata-madesimple.com/wp-content/uploads/2016/04/bos-columns.png)

- boston.target contains the housing prices.
![](https://bigdata-madesimple.com/wp-content/uploads/2016/04/Boston-target.png)


#### Scikit Learn:
- In this section we are going to fit a linear regression model and predict the Boston housing prices. We will use the least squares method as the way to estimate the coefficients.

- Y = boston housing price(also called “target” data in Python)
- and
- X = all the other features (or independent variables)





