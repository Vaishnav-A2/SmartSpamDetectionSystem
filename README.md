# Overview
Two full-stack web applications were developed during the internship, combining Python-based machine learning with interactive web interfaces to deliver real-time predictions.

## 1 .Smart Spam Detection System

Objective:
The goal of this project was to build a web application that detects whether a message is spam or legitimate using machine learning.

Technologies Used:

The application was built using Python 3.11 as the core language, Flask as the web framework, and Scikit-learn for machine learning. Text data was processed using TF-IDF Vectorization, and the frontend was developed using HTML5 and CSS3.
Implementation:

A machine learning model was trained on a labeled SMS dataset using TF-IDF vectorization to convert text into numerical features. The trained model and vectorizer were saved as model.pkl and vectorizer.pkl for reuse. A Flask web server handles user input, vectorizes the submitted text, and passes it through the model to generate a prediction. The frontend provides a clean HTML form for users to enter and submit messages.

How It Works:
The user enters a message and submits the form. The Flask backend vectorizes the text and runs it through the trained model. The result is then displayed on the screen as either SPAM or HAM.

Key Learnings:
This project helped in understanding how to train and deploy machine learning models as web applications, work with text preprocessing techniques like TF-IDF, and build a complete full-stack application using Flask.

## 2. Sentiment Analysis Web Application

Objective:
The goal of this project was to develop a web application that classifies any text input as positive, negative, or neutral in real time.

Technologies Used:
The application was built using Python 3.11 and Flask for the backend. Sentiment detection was implemented using a rule-based keyword analysis approach. The frontend was developed using HTML5 and CSS3.

Implementation:
A rule-based sentiment analyzer was built using predefined sets of positive and negative keywords. The input text is tokenized and cleaned of punctuation, and each word is matched against both keyword sets. Flask handles the form submission and renders the result dynamically using Jinja2 templating.

How It Works:
The user enters a sentence and submits the form. The Flask backend counts the positive and negative keywords in the text and determines the overall sentiment. The result is displayed as Positive 😊, Negative 😞, or Neutral 😐.

Key Learnings:
This project provided hands-on experience with rule-based natural language processing, building dynamic web pages using Flask and Jinja2, and understanding the foundational concepts behind sentiment analysis.
