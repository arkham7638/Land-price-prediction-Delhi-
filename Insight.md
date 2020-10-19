# *Land-price-prediction-Delhi*

The data set is provided by the (https://www.kaggle.com/ruchi798/housing-prices-in-metropolitan-areas-of-india) 

Now our project deals with the problems. 
->Prediction of the Land Price.
->Deployment for the user.
->Which machine learning algorithm to be used to get the get the good score.

# Prediction 

In this project we are basically using the Python (3.6) to be exact the library including 
->Numpy
->Seaborn
->Matplotlib
->Sklearn

STEP1: First step is the most impportant step as we are reading the data - set and checking if there is any null value.

Numpy = NumPy is a library for the Python programming language, adding support for large, multi-dimensional arrays and matrices, along with a large collection of high-level mathematical functions to operate on these arrays.

Seaborn = Seaborn is a Python data visualization library based on matplotlib. It provides a high-level interface for drawing attractive and informative statistical graphics.

Mtaplotlib = Matplotlib is a plotting library for the Python programming language and its numerical mathematics extension NumPy. It provides an object-oriented API for embedding plots into applications using general-purpose GUI toolkits like Tkinter, wxPython, Qt, or GTK+.

Scikit-learn is a free software machine learning library for the Python programming language. It features various classification, regression and clustering algorithms including support vector machines.


# Exploring The Feature Engineering 

STEP2: Second step consist of the feature engineering part which will do the (new feature called price per square feet).

df3['price_per_sqft'] = df3['Price']*100000/df3['Area']

(b) - Examine locations which is a categorical variable. We need to apply dimensionality reduction technique here to reduce number of locations

df3.Location = df3.Location.apply(lambda x: x.strip())
Location_stats = df3['Location'].value_counts(ascending=False)

# Dimensionality Reduction

STEP3: Third step consist of the Any location having less than 10 data points should be tagged as "other" location. This way number of categories can be reduced by huge amount. Later on when we do one hot encoding, it will help us with having fewer dummy columns

# Build The Model

STEP4: Building the model for the deployment and use Logistic regression for getting the prediction score ((np.sqrt(mean_squared_error(y_test,prediction)))) and why we use Logistic Regression because the logistic model is used to model the probability of a certain class or event existing such as pass/fail, win/lose, alive/dead or healthy/sick.
 
So this becomes the perfect case for losgistic regression
