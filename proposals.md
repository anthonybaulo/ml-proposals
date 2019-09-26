<a name="top"></a>
# Table of Contents
[Spotify Song Popularity](#spotify)<br>
[Psych Study - Emerging Adulthood](#eammi)<br>
[Predicting Stock Movement](#stock)<br>

---
<a name="spotify"></a>
# Spotify Song Popularity

## Description
### Predictive
* Can the popularity of a song on Spotify be predicted by its audio features? 

	* At present, the features are: danceability, energy, key, loudness, mode, speechiness, acousticness, instrumentalness, liveness, valence, tempo, timbre, duration, time-signature

### Inferential 
* Is the relationship between the features and response linear?
* Can we quantify the relationship between the features and response? 
* Do some features contribute negatively?
* Which features contribute most?



## Approach

I plan to compare different ML techniques, beginning with a simple Linear Regression, then escalating in feature complexity and model complexity, dictated by the results of the previous iteration. 

If a linear relationship exists, I will explore the coefficients and p-values of each feature (and polynomials), and use additional techniques to determine the best combination of predictors. 

The popularity target ranges from 0-100, so I would also like to break the scores into ‘n’ equal classes and test out classification algorithms for prediction. 

If possible, I would also like to predict feature vectors for given popularity ratings.



## How will people interact with the work?

If I can develop an effective predictive model, an interactive web app would be interesting. The user can manipulate sliders, buttons, or drop-down lists to dictate the features of their “song” that would be fed into the model to predict a popularity rating.

A slide deck or markdown file can outline the process and insights found during the making of the model.

## Data Sources

The Million Song Dataset (+300G) is a freely-available collection of audio features and metadata for a million contemporary popular music tracks. Once I determine an adequate sample of tracks, I can query the Spotify API with each track name to obtain the popularity score. The data will be merged and stored in a Postgres DB.

Given the size of the dataset, this work should be done on an AWS instance, potentially leveraging Spark.


[Table of Contents^](#top)<br>

---
<a name="eammi"></a>
# Psych Study - Emerging Adulthood 

## Description

### Predictive
* Can we accurately predict a young adult's relation to certain aspects of life (media, well-being, politics, etc) based on their responses to a +200 question survey?


### Inferential\*
* What hidden patterns can we find through cluster analysis?
* What are the relationships between different sections of the survey / aspects of life?

\*These questions will become more granular as the data is explored.

## Approach
After familiarizing myself with the study/questionnaire (see "Data Sources"), I can determine the best way to encode the results for modeling. 

I'd like to employ some unsupervised learning techniques to gain some insight into the data, which may inform some decisions into the predictive modeling. 

Since there are multiple sections of the survey (Markers of Adulthood, Subjective Well-Being, Politics, etc), and each section could be represented by a vector, I would like to find out which vector can best be predicted by the others if it were held out as the response variable. 

Alternatively, I could find a single variable target to predict, such as the participant's answer to a specific question (political affiliation, happiness, etc).


## How will people interact with the work?
The narrative format with markdown and/or slides is well suited to describe the insights and outcomes. 

If all of the above questions can be answered, and an effective model is reached early enough in the week, a more ambitious result would be an interactive web app where the user can submit their own answers to the parts of the study that ended up being used for modeling, and receive a score/classification/prediction based on their answers.

## Data Sources
The [Open Science Framework](https://osf.io/) provides a publicly available dataset containing ~3200 respondents who participated in an in-depth survey of +200 questions surrounding adulthood.

As stated in the consent form:
"The purpose of the study is to investigate how young adults ages 18­-25 view their experience in the world. We are examining many questions, but collectively these questions will explore your approach to life, what defines adulthood, and your general impressions and beliefs about politics, media, and other daily experiences."

This data will have to be cleaned and encoded for use with ML algorithms. 

[Table of Contents^](#top)<br>

---
<a name="stock"></a>
# Predicting Stock Movement 

## Description
### Predictive
* Can a stock's price be accurately classified as increasing or decreasing?
* What confidence levels can be achieved?
* Is the classifier's performance statistically significant over random chance?

### Inferential 
* Can we quantify the relationship between the features and response? 
* Which features are most effective for classification?

## Approach

I will begin with a simple Logistic Regression model, and escalate in feature and model complexity as dictated by the results of each iteration. 

Some Linear Regression may be used to infer the relationships between the features and response, and thus assist in feature engineering. 

## How will people interact with the work?
The narrative format with markdown and/or slides is well suited to describe the insights and outcomes. 

If all of the above questions can be answered, and an effective model reached early enough in the week, a more ambitious result would be an interactive web app where the user can input a stock ticker and receive a classification score. Behind the scenes, the app would have to call the Alpha Vantage API to obtain the required features, run them through the pipeline, and receieve a prediction. 

## Data Sources

The Alpha Vantage API will provide up to 20 years of daily stock history, including price and many technical indicators. I will create a pipeline that collects stock data from the API, merges the indicators with the price info, and stores it in a Postgres DB.

[Table of Contents^](#top)<br>
