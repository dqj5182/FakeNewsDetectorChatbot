# FakeNewsDetectorChatbot
Fake News Detecting Chatbot using RNN and LSTM with Keras and Discord (HackPSU 2020 Project)

### Collaborator
Jun Ki Ahn, Daniel Jung, Yujin Lim, Joshua Chung , Inae Choi

## Installation/Setup Guide

### 1. Discord Bot API
In order to use this program, Discord's Bot API is required. Please follow below step to get Discord Bot API:
  1. Login to Discord and Go to https://discord.com/developers/applications
  2. Create New Application by clicking the button right top corner of the screen
  3. Go to your discord and create a server
  4. Create Bot and copy the Bot's token code
  5. Got to the OAuth2 tab and authenticate your API to add your bot to your Discord server
  
### 2. Setting up environment and required preparation
  1. Make sure to install all the packages required for the code using requirement.txt
  2. If you are a Mac user, go to Application/Python 3.x/ and install certificates.command to allow the code to run without authentication error
  3. Due to data file size, data is zipped into data folder, please unzip before use
  4. Go to discordbot.py and at the bottom of the code client.run(), put your Bot's token code that you copied from previous step
  5. Go to MMModels.py and check the file directory, the both .py files have to be in same directory

### 3. After running the code
  1. Use /FakeNews <content> to get result
  2. Content can be whole article for better result, but also can be just the title
  3. Enjoy! :)
  
-----------------------------------------------------------------------------------------------------------

# HackPSU 2020 Project Report

 ## Inspiration

Imagine, what if the news you read were apparently FAKE? Our smart Discord Chatbot “Fake News Detector” identifies the credibility of news articles and eliminates any possibility of you falling for it.
## What it does

When a user types the title of an article or a publication, the chatbot states the likelihood of the news to be fake . The probability is then displayed as a percentage. Inputting title has been chosen instead of content because content can vary widely among each publication and we thought the software will be most widely used by many users when it is as easy as to just type title of news and chatbot can just give a probability of whether it is fake news


## How we built it

### Inspiration
Living through chaotic 2020, our team members agreed that it is crucial to follow up with the most recent issues.
As students who are still in the process of establishing our societal preference, we are eager to keep what we hear and see as impartial until everything has been verified. While we know the press is the best source to catch up on what happens around the world, its aspect of the need to hook and get attention from the general public somehow makes it hard to take it in as an Apocrypha and often makes us face the fake news.
Therefore, we decided to build software that would fact check any publications. While considering many kinds of software with AI, the chatbot customer services inspired us the most as we all have experienced its user-friendliness. Hence, we concluded to build a simple, fast, precise, and interactive chatbot that would let us know the rate of the factuality of each article just by typing the headline on the chat.

### What it does
When a user types the title of an article or a publication, the chatbot states the likelihood of the news to be fake. The probability is then displayed as a percentage. Inputting title has been chosen instead of content because content can vary widely among each publication and we thought the software will be most widely used by many users when it is as easy as to just type title of news and chatbot can just give a probability of whether it is fake news

### How we built it:
 The Fake News Detector chatbot we built is deployed in Discord messaging software and run by python codes. The codes are based upon python libraries such as Pandas, Numpy, Scikit Learn, and Keras. 

Pandas and Numpy took a role in data handling and data analysis, Scikit Learn in a role in basic machine learning, and Keras on Recurrent Neural Network (RNN) and Long Short-term Memory (LSTM). Dataset was given from Kaggle with a contribution from Clement Bisaillon titled “Fake and real news dataset”.  The dataset consists of two CSV files: Fake.csv and True.csv. Each contains columns named “title”, “text”, “subject”, and “date”. 

To make our chatbot user-friendly, we decided on the main classifier as the article headline. Therefore, we have trained our data model with the news title and whether its content is fake or not. We transformed every text data (the title of each news) into vectorized form and used them for training and testing. As we are dealing with text data, to be specific sentences, we implemented RNN and LSTM which are widely used deep learning methods in Natural Language Processing. Our data model gives Loss value and Accuracy value from each instance on how likely each sentence is to be fake news.

## Challenges we ran into

Although we did face countless awful challenges before coding, just as “well begun is half done”, the difficulties faced while simulating were doable.

### 1. Integration
We faced many issues such as security measures while connecting the python with the discord chatbot. For example, the terminal would output credential issues, which is an issue that happens in MacOS to prevent hackers and other malicious software from gaining access to the file. Secondly, integrating a deep learning model with Discord bot API was also a challenge due to error during hosting servers and also first-time use of Discord API
 
### 2. Understanding of Deep Learning Model
Applying RNN and LSTM was difficult as it was our first time using it. To understand, we spent nearly half of our given time examining through reports and papers, causing us to have a slow starting point. The websites used for understanding are:

[link](https://builtin.com/data-science/recurrent-neural-networks-and-lstm)
[link](https://towardsdatascience.com/learn-how-recurrent-neural-networks-work-84e975feaaf7)
[link](https://arxiv.org/pdf/1706.07206.pdf)

### Group work
3.	As a group of five, we wanted all our group mates to fully contribute and do their best at their position. We wanted to come up with acceptable front-end and back-end ideas to find a balance between each of our skills. We did succeed in doing that with our best teamwork. (Although some of us didn’t know each other until 48 hours ago!)

## Accomplishments that we're proud of

We are proud to announce two significant steps. First, we are very proud of our team to be able to deploy python codes on Recurrent Neural Network and Long Short-term Memory. Many of our team members do have background knowledge on Machine Learning, however, we have never dived more deeply into the field such as RNN and LSTM. Being able to deploy concepts that we have never learned before was the first significant accomplishment that we are proud of. Second, we are very proud of our team to be able to connect our backend python ML code with Discord API. No one in our team could connect python code with a messaging application or any front-end software. This was also an accomplishment that none of us were able to do before this hackathon but became an expert in it after finishing this project.

## What we learned

Keras, Natural Language Processing, Connecting backend with frontend, transforming text input as a vector, model evaluation

## What's next for Fake New Detector Chatbot using Neural Networking

Can be implemented in various social media platform, Reddit where people discuss political or societal agenda

##References

1. "A GUIDE TO RNN: UNDERSTANDING RECURRENT NEURAL NETWORKS AND LSTM." builtin, 16 June 2019,
    builtin.com/data-science/recurrent-neural-networks-and-lstm. Accessed 7 Nov. 2020.

2. "How Recurrent Neural Networks work." Towards Data Science, 2 Dec. 2017, towardsdatascience.com/
    learn-how-recurrent-neural-networks-work-84e975feaaf7. Accessed 7 Nov. 2020.

3. Arras, Leila, et al. "Explaining Recurrent Neural Network Predictions in Sentiment Analysis." Pdf
    file, 7 Nov. 2020.



## Data:

[link](https://www.kaggle.com/clmentbisaillon/fake-and-real-news-dataset)
