# A sarcasm checker for news headlines
Ethan King  063-00-3743

# Table of Contents
[Description](#Description)  
[Users](#Users)  
[System Design](#System-Design)  
[Conclusions](#Conclusions)  
[References](#References)  

## Description

English is a notoriously difficult language to learn with unique pronunciations and figures of speech that can confuse people. For a machine to be able to interpret language programmatically, the programmer would have to account for many edge cases. Often, meaning is hidden in words that defies rule-based logic. Thankfully, there are algorithms that can assist in training a computer how to interpret human language.  

This sarcasm checker web app allows users to quickly categorize news headlines using machine learning. 
Our model was trained on a labeled dataset from Kaggle, but can be adapted to work with any labeled text data.

https://www.kaggle.com/rmisra/news-headlines-dataset-for-sarcasm-detection.

Onion headlines make up the sarcastic headlines while Huffington Post headlines are not sarcastic. 
We train a Naive Bayes classifier on this dataset and deploy it using Flask.

## Users
Users of this system include investment managers and quantitative analysts who need to make sense of news headlines and easily interpret them. 


## System Design

The system's backend is built using Flask, the classifier uses the sci-kit learn Python package, and our front end makes use of html and css for styling.
Users are prompted with an instructional headline and a text input field where the user may enter in headline they wish to classify. 

Our application uses a single module that runs the home function when the homepage is requested, returning home.html.
The POST method sends the text entered into the box to the predict function, where the model is trained and the submitted text is entered into the model.

## Conclusions
The performance of the model could be improved by saving a serialized version of the pretrained model instead of retraining the model every time we want to check a headline.

## References

https://en.wikipedia.org/wiki/Naive_Bayes_spam_filtering  
https://medium.com/@onejohi/building-a-simple-rest-api-with-python-and-flask-b404371dc699  
https://www.udemy.com/the-complete-python-web-course-learn-by-building-8-apps/  





