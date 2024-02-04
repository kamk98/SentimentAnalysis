# Sentiment Analysis


This is a Women’s Clothing E-Commerce dataset revolving around the reviews written by customers. Because this is real commercial data, it has been anonymized, and references to the company in the review text and body have been replaced with “retailer”. This dataset includes 23486 rows and 10 feature variables. Each row corresponds to a customer review, and includes the variables:

Clothing ID: Integer Categorical variable that refers to the specific piece being reviewed.

**Age**: Positive Integer variable of the reviewers age.    

**Title**: String variable for the title of the review.

**Review Text**: String variable for the review body.

**Rating**: Positive Ordinal Integer variable for the product score granted by the customer from 1 Worst, to 5 Best.

**Recommended IND**: Binary variable stating where the customer recommends the product where 1 is recommended, 0 is not recommended.

**Positive Feedback Count**: Positive Integer documenting the number of other customers who found this review positive.

**Division Name**: Categorical name of the product high level division.

**Department Name**: Categorical name of the product department name.

**Class Name**: Categorical name of the product class name.


## Aim
This project deals with the fundamentals of natural language processing. We will be performing sentiment analysis i.e., building prediction models aimed at predicting the rating of the products, based on the textual reviews submitted by users.

## Background
This is a project that was assigned to me when I was a machine learning intern at a Bangalore (India) based e-learning institute called Verzeo. This was a comprehensive internship which taught concepts of machine learning and data science that cemented my foundations in the field of data analytics.

## Prediction Models
The prediction models built for this project include: Naive Bayes, K-Nearest Neighbors, SVM and Logistic Regression.

## Data Analysis Workflow
I first downloaded and imported the 'stopwords' package from nltk.corpus. This is followed by removal of rows having null values. It is important to remove null to avoid discrepancy in the performance of the prediction models. The 'Rating' column, which had values 1...5, will now be modified to contain binary values: 'Good' and 'Bad', with 'Bad' referring to 1..3, and 'Good' referring to 4 and 5 (this was done using a lambda function). I then performed removal of punctuations and stopwords from the 'Review Text' column's data. Using the 'pipeline' function, I performed countvectorization, followed by tf-idf vectorization, and then finally the application of the aforementioned models. Used only accuracy from the classification matrix to determine which model's is most suited for the task at hand.

## Future work
I wish to perform Exploratory Data Analysis of the given dataset. I believe there are some valuable insights that one can derive from this dataset, such as: observing any trends in the purchases of the clothing categories across different age groups, visualize the ratings on different categories of clothing given by customers of different age groups, etc. Since I was working on this project the day it was due, due to personal reasons, I did not have time to explore more models I could have used. I now wish to include a Random Forest model for this task and see how it performs. Instead of depending only on accuracy to determine the performance of a model, I wish to take into consideration other metrics, such as precision, f-1 score etc., because it was in my Data Mining course (Dr. Shastri) at University of Houston - Downtown, that I was made to understand (via an assignment) that only accuracy is not enough when coming to a conclusion about a better performing model. Might also perform cross-validation as well. In my pipeline functions, I had included countvectorization as well as tf-idf vectorization. I understood in the data mining class that tf-idf vectorization includes the functions of countvectorization. Hence, it is possible that involving both the functions in the pipeline instead of just tf-idf vectorizatrion (likely more suitable) might be computationally expensive. By comparing the elapsed times (by making use of the 'time' module in python), I can get an idea of the computational cost associated with each approach (countvectorization+tf-idf and tf-idf only).
