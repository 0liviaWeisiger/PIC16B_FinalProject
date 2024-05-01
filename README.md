# PIC16B_FinalProject
Repo for PIC 16B group project @ UCLA during the spring 2024 quarter.

# Problem Proposal

This project will explore the current United States real-estate market, investigate what factors influence the price of property, and create multiple machine learning models that predict these housing costs throughout the country. This topic is very relevant to our present day lives, as we are students that pay to live in housing off-campus and will eventually be looking to move to various cities post-college. Being able to infer and understand the trends of real estate is extremely valuable economic knowledge that will provide important insights about our country.

We are also curious about what underlying societal factors such as average income, political alignment, or quality of schools for example affect the prices of houses. These concepts tie in to general education humanities courses we have taken at UCLA that explore the relationship between societal factors and external structures like the economy. Additionally, we aim to focus a major part of the complexity of our project on the machine learning aspect of our data. We are data science majors and minors, and are excited to gain valuable practice with testing different machine learning models and evaluating their accuracy because this closely ties into our academic and career aspirations.

# Required Resources

#### Data: https://www.kaggle.com/datasets/ahmedshahriarsakib/usa-real-estate-dataset

Our main dataset (linked above) contains over 2.2 million entries of housing listings on the market in the United States, that have been collected starting in April 2022 and updated weekly through present day. These listing entries contain the locations of the houses, house area/size, information regarding dates it was previously sold, number of bedrooms, and other attributes that are physically related to the houses. To expand upon this data and investigate underlying societal factors of real estate, we will join this main dataset with others.

#### Initial thoughts on data to join the main real estate dataset with include:

- https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/42MVDX (Source of election data with dates from 1976-2020. We will need to filter by `year == ‘2020’` to isolate rows pertaining to the most recent presidential election. The dataset has a detailed breakdown of all candidates that received votes by state and their affiliated political parties. State will be the key we join on with the real estate data)
- https://www.kaggle.com/code/kerneler/starter-sociological-metrics-of-all-50-cc3e3664-f/input (Sociological data of US from 2021 with percentages related to education, peace, religious affiliation, and poverty by state.)
- https://fredaccount.stlouisfed.org/ (Using this site, we were able to extract minimum wage data by state from the years 2020 - 2024; potentially we can look across years of the minimum wages by state to create new features that detect the change in minimum wage across our years of interest.)


# Prior Works Associated 

https://www.kaggle.com/code/binfeng2021/regression-problem-house-price-prediction

Most of the previous works that have to do with this data set are in regards to data visualization. There are a few public notebooks that investigate the correlation between column variables such as number of acres, bedrooms, etc with home prices, and graph the results using various visualization techniques. We will aim to dive beyond this current work by merging our dataset with new data, in order to add more abstract variables to analyze the home prices trends with. This will create new material to visualize in creative ways, and draw more insightful conclusions from. 

There are limited prior works on this data set regarding machine learning. A couple employ linear regression and look at a mean squared error, but they conclude that the data does not fit a linear pattern very conclusively. There are also better results with a random forest regressor and gradient boosting regressor which provide R^2 values of 0.9 and 0.76. 
Our goal is to expand on this previous work by employing more complex machine learning techniques, and possibly deep learning techniques in order to refine our predictive model and obtain a high accuracy value.

# Required Tools and Skills

Knowledge of the sklearn library will be required for this project to conduct regressions and ML algorithms to make predictions regarding real estate costs based on the original variables in the real estate data (which are more literal about the house e.g., location, acres, number of rooms and bathrooms). 

Beyond these basic attributes of the home, we wish to expand upon the real estate data and join/merge it by zip code or state, using manipulation tricks in the pandas library. Some of the features we wish to add include political party, school quality, age of population, quality of life, income demographics, population density of zip code, etc.This will allow our project to expand beyond the physical features of the home, and attempt to make connections to housing prices in relation to socioeconomic factors in the areas. 
Once we widen the data using joins, we will test if adding these features improves the accuracy of the model. Additionally, PCA and/or other dimension reduction methods will be utilized to remove uninformative features from the model. 

In addition to model building, since the housing data is geographical, we will expand upon our current visualization skills (using plotly and plotly.express) to build interesting maps to visualize locations of real estate, and color by features that produce compelling insights. We plan to attempt to employ geoplot, which is a high-level geospatial plotting library, which will allow us to create even more interesting visualizations. 

For more basic graphics and visualizations (comparing prevalence of categories or densities of the numerical predictors, etc.) we will leverage libraries such as seaborn and matplotlib. 

# Learning Outcomes

To complete this project, we will formulate some machine learning models, using software such as TensorFlow that we have not yet learned. In addition, with the large scope of data accumulation needed for our project, we will be dealing with more data than we have used before, and more complicated data sorting, manipulation, and cleaning. By the end of this project we want to have learned how to process large amounts of data, synthesize different datasets, manipulate them to provide us with significant information, and use this data to train a complicated machine learning algorithm. In addition, we are interested in doing some complex data visualization to further investigate our data and the links between housing prices and various sociological, economic, and political factors influencing those prices. To do this we will investigate the uses of plotly, further than what we have learned with plotly.express.

# Group Members & Roles & Timeline

### Fionnuala : 
- Clean and join the various data sets (join /merge data) (By end of week 6)
- Process data for machine learning: Identify and separate the testing and training data (By week 7)
- Write the report
    - Intro (By week 10)
    - Descriptions for each part - specifically explaining each data feature
    - Conclusion (By week 10)

### Grace :
- Do data visualization
- Maps
- Correlation matrix for numeric data
- Bar plots// visualizing categories
- Scatter plots, … (By end of week 8)

### Olivia Weisiger 
- Train a model + Use the model to predict + obtain measures of how well the model is fitting unseen data
- Use PCA/dimension reduction methods
- Test random forest regressor and gradient boosting regressor (By end of week 9)

### All of us:
- Write respective parts (By week 10)
- Help Olivia with training the model and doing the more complex calculation driven code (By end of week 9)
