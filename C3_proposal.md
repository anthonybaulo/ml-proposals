# What are you trying to do?
I am trying to extract descriptive features, such as musical genre, from songs based on their audio signal. This endeavor falls under the science of Music Information Retrieval (MIR), which has applications in recommender systems, track separation/instrument recognition, automatic music transcription, automatic categorization, and even music generation. 

# How has this problem been solved before?
The [Free Music Archive](https://arxiv.org/pdf/1612.01840.pdf) has provided an open benchmark dataset, making reproducible research possible, and therefore opening the doors to collaborative and independent research. In the paper, lower-bound scores of 52-63% accuracy on genre classification were cited for the medium dataset. These methods employed Linear Regression, KNN, SVM, and MLP, none of which were trained on the audio signal directly, but on features extracted from the audio signal, such as RMS energy and zero-crossing rate. 

Due to the ease of access to the data, there is no shortage of research and references on the internet. The competition [“WWW 2018 Challenge: Learning to Recognize Musical Genre”](https://www.crowdai.org/challenges/www-2018-challenge-learning-to-recognize-musical-genre) was held on the FMA dataset, with the top score being 1.31 Log Loss, and 0.63 F1 Score. Many different approaches were employed, including CNNs and XGBoost. At least two papers were published as a result of the contest: [1](https://doi.org/10.1145/3184558.3191823) , [2](https://doi.org/10.1145/3184558.3191822) 
Many educational articles, such as [this one](https://towardsdatascience.com/using-cnns-and-rnns-for-music-genre-recognition-2435fb2ed6af) also explore multiple techniques on this dataset, such as combining CNNs and RNNs.

# What is new about your approach, why do you think it will be successful?
As mentioned, there is no shortage of research in this area, and I don’t expect to make any groundbreaking discoveries over the course of a week. Therefore, my motivation for this project is to familiarize myself with CNNs, particularly their application to audio, and more broadly, sequential data. I will survey the most accessible research and explore a combination of techniques that will enhance my current understanding of audio data, as well as model architectures. 

# Who cares? If you're successful, what will the impact be?
Success in this endeavor will result in my ability to intelligently participate in the discussions of MIR and CNNs. The skills gained in this project can serve as an entrypoint into multiple fields of research, all of which can benefit from more people joining the discussion.  

# How will you present your work?
A slide deck will serve to introduce the project over a 5 minute presentation. A well-documented readme will accompany the code on github. Time permitting, an interactive web-app could allow a user to upload an mp3 and receive a classification score.

# What are your data sources? What is the size of your dataset, and what is your storage format?
As mentioned, the FMA dataset has facilitated this kind of work. There are multiple subsets available, ranging from 8,000 30-second tracks (7 GB) to 106,574 full-length tracks (879 GB). The songs are in mp3 format, and the metadata is in csv format (342 MB). 
I will start with the small dataset for initial building and tuning, and scale to the medium set if the results are promising. 

# What are potential problems with your capstone?
* Unfamiliarity with CNN architecture, including quirks and limitations, and how to mitigate them.
	* Research into what has worked in the past, and what modifications are within my scope of understanding.
* Unbalanced classes in the larger datasets.
	* Under- and over-sampling
	* Use better evaluation metrics, such as F1
* Converting the audio into a format suitable for CNNs.
	* Research existing python libraries for converting audio. 
	* It seems like the Mel Spectrogram will be the best format
* Working in AWS.
	* Practice makes perfect
	* Ask lots of questions

# What is the next thing you need to work on?
* Set up a GPU environment in AWS and get the data into a useable location. 
* Read the articles and papers that have used this dataset
* Sketch out modifications of the architectures I’d like to try

