# Classifying Recipes into Cuisines
As a former restauranteur and foodie, I strived to provide authentic culinary experiences through my food and restaurant and seek authentic experiences in food myself. In this project I utilized classification models and natural langauge processing to classify the recipes of different dishes into cuisines.

## Business Problem/Motivation
Knowing the cuisine of dish is important for restaurants, food delivery and meal kit companies, and consumers. Restaurants need to protect their brand image and attract customers based on their food's authenticity and experience. Food delivery companies and meal kit companies use cuisines as a part of their recommendation system. Consumers especially foodies want to experience authentic culinary experiences and to understand their cultural palates. I used various classification models to predict cuisine and identify important ingredients that is characteristic of different cuisines.

## Methodology
**1. Gathering Data**
I gathered data from Kaggle consisting of 21 Cuisines, 3000+ Ingredients, 30000 unique recipes from Yummly

**2. Data Cleaning**
Using Regular Expressions and NLTK, I removed numbers, punctuation, and undercased all recipes. Afterward I vectorized the words using TFIDFvectorizer, which weighted individual ingredients and created a sparse matrix of ingredient weights.

**3. Exploratory Data Analysis**
I created plots and vizualizations for each cuisine to discover the relationships between key ingredients and each cuisine. I discovered class imbalances, for example, there are not many Thai dishes compared to Italian dishes, so I added weights to underrepresented cuisines.

**4. Model Training and Validation**
I split the data into a train set and test set and created a basic KNN model as the Base Model, which achieved an accuracy score of 64%. I improved upon this base model by adjusting parameters and class weights and utilized other more complex models such as logistic regression, OVA naye bayes, decision trees, random forests, and xgBoost. 

**5. Testing**
Arrived at the best performing model, Logistic Regression with Custom Class Weights.

## Exploratory Data Analysis

English Cuisine

Japanese Cuisine

Insights from Misclassifcations

## Modeling

The next step is to find the model that best generalizes the relationships between the features and the target, price. After splitting the data into train and test parts, I decided to use a number of linear regression models starting from a base line Linear Regression towards more advanced models such as polynomial regressions with lasso and ridge regularization. Below is a table of the performance of each model. 


| Algorithm           | R^2                                    | Notes                         |
| ----------------- | --------------------------------------- | ---------------------------- |
| Base Linear Regression               | 0.67                    | Removed New Listings and added Engineered Features |
| Second Degree PolyReg                |  0.05                 | Overfit the test data significantly|
| Linear Regression with Lasso | 0.71                        | Performed Reasonably well       |
| Linear Regression  with Ridge  | 0.70| Performed well                   |
| Polyreg Model with Lasso  | 0.68| Performed well, however after CV, LinReg with Lasso performed better                   |
| Polyreg Model with Ridge  | 0.70| Performed well, however after CV, LinReg with Lasso performed better                   |


![Best Model](finalmodel.png)

## Take Aways

There are a number of key take aways from the project I want hosts and guests to benefit from. 

If you are a host, focus on accomodating as many guests as you can comfortably fit in your space increasing the number of beds in your space. Focus on getting good reviews, cleanliness, accuracy of description, and communication are the most important components in getting a good review. Lastly, if you can give your guests a private bathroom, that will also increase the amount you can charge for your space.

If you are a guest, look for private or shared listings and be willing to venture out uptown near Harlem for better deals on spaces. If you are also willing to share a bathroom, that would also lower the price of your stay.

At the end of the day, a night's stay in the city of Manhattan during the holidays is really expensive but using these strategies can help you maximize the rent you could charge or minimize your cost of staying.

