## Table of Contents
[Spotify Song Popularity](#spotify)<br>
[Psych Study - Emerging Adulthood](#eammi)<br>
[Third Proposal](#third)<br>

---
<a name="spotify"></a>
# Spotify Song Popularity

## Description
Can the popularity of a song on Spotify be predicted by its audio features? 

At present, the features I intend to include are:
* danceability
* energy
* key
* loudness
* mode
* speechiness
* acousticness
* instrumentalness
* liveness
* valence
* tempo
* timbre
* duration_ms
* time_signature

## Approach
I plan to compare different ML techniques, beginning with a simple Linear Regression, then escalating in feature complexity and model complexity, dictated by the results of the previous iteration. 

The popularity target ranges from 0-100, so I would also like to break the scores into ‘n’ equal classes and test out classification algorithms.

If possible, I would also like to get the predicted feature vector for various popularity ratings.

Features -> Popularity Score <br>
Popularity Score -> Features


## How will people interact with the work?

If I can develop an effective model, an interactive web app would be interesting. The user can manipulate sliders, buttons, or drop-down lists to dictate the features of their “song” that would be fed into the model to predict a popularity rating.

A slide deck or markdown file can outline the process and insights found during the making of the model.

## Data Sources

The Million Song Dataset (+300G) is a freely-available collection of audio features and metadata for a million contemporary popular music tracks. Once I determine an adequate sample of tracks, I can query the Spotify API with each track name to obtain the popularity score.


<a name="eammi"></a>
# Psych Study - Emerging Adulthood 

## Description


## Approach


## How will people interact with the work?


## Data Sources


<a name="third"></a>
# Third Proposal 

## Description


## Approach


## How will people interact with the work?


## Data Sources
