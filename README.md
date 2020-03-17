
# Agri Machine Chatbot

This chatbot helps user(farmers ) to resolve their queries.This project uses similarity matching for the purpose of fetching the most suitable answer for the query.This includes similarity matching ,machine learning  and auto web scraping to download data autometically at regular intervals.

# Auto web scraping

Used selenium python library for generating autoclicks and downloading the data. This helps us to redirect to the particular website and then with the help of few attributes fetch the required data.this helps in generating multipole clicks in order to get data.


chrome driver must be pre [installed] in the current  computer.Its executable path must be included as shown below.

(https://chromedriver.chromium.org/downloads)

driver = webdriver.Chrome(executable_path='/Users/HP/Desktop/folders/others/chromedriver/chromedriver.exe')

xpath helps us to direct to ther required part of the webpage.Now how to find xpath?Its simple .Go to the required webpage go to a particular section of webpage you need to generate action then right click on that part and select inspect option to view the code of the webpage.Then in the opened new tab go to the required section and then rightclick on the section and select copy.You will get few option from which you nedd to select copy full xpath.we can generate action with the help of clasess,xpaths,id's and few more.

wordcloud is generated to know the  frequency of the words in the data set.the data and the query will undergo all steps of cleaning including tokenizing,stemming ,Lemmatisation,removal of stopwords and so on.

    When raw data is fed to the algorithm there are plenty of unwanted things that cause faults , so they need to be taken care of .We use tokenization as the first process which tokenizes both data and the input query and proceeds to further pre-processing

Stop word are nothing but  helping verbs in the sentence and they do not play much important role in similarity matching and for computer to understand the speech.


count vectorizer

The Count Vectorizer provides a simple way to both tokenize a collection of text documents and build a vocabulary of known words, but also to encode new documents using that vocabulary. The above syntax is of count vectorizer along with all of its parameters.


tf-idf transformer

It generates IDF weights for the tokens generated.Less the IDF value more the number of times the word appear and they have less uniqueness in the data. The lower the IDF value of a word, the less unique it is to any particular document.

With Tfidftransformer you will systematically compute word counts using CountVectorizer and then compute the Inverse Document Frequency (IDF) values and only then compute the Tf-idf scores.

With Tfidfvectorizer on the contrary, you will do all three steps at once. Under the hood, it computes the word counts, IDF values, and Tf-idf scores all using the same dataset.


Similarity matching


    Cosine similarity is a measure of similarity between two non zero vectors of inner product space that measure the cosine of the angle between them .Similarity matching is nothing but the matching of two data i,e comparison of two things and finding out the result as the most similar data to the required data in our case the input query.



# Human Machine Interaction System

Building a Simple Chatbot from Scratch in Python (using NLTK)

![Alt text](https://cdn-images-1.medium.com/max/800/1*pPcVfZ7i-gLMabUol3zezA.gif)

History of chatbots dates back to 1966 when a computer program called ELIZA was invented by Weizenbaum. It imitated the language of a psychotherapist from only 200 lines of code. You can still converse with it here: [Eliza](http://psych.fullerton.edu/mbirnbaum/psych101/Eliza.htm?utm_source=ubisend.com&utm_medium=blog-link&utm_campaign=ubisend). 

On similar lines let's create a very basic chatbot utlising the Python's NLTK library.It's a very simple bot with hardly any cognitive skills,but still a good way to get into NLP and get to know about chatbots.


# Outline
* [Motivation](#motivation)
* [Blogpost](#blogpost)
* [Pre-requisites](#pre-requisites)
* [How to run](#how-to-run)


## Motivation
The idea of this project was not to create some SOTA chatbot with exceptional cognitive skills but just to utilise and test my Python skills.This was one of my very first projects, created  when I just stepped into the world of NLP and I thought of creating a simple chatbot just to make use of my newly acquired knowledge.

## BlogPost
For detailed overview, here is the accompanying blog titled:**[Building a Simple Chatbot in Python (using NLTK)](https://medium.com/analytics-vidhya/building-a-simple-chatbot-in-python-using-nltk-7c8c8215ac6e)**


## Pre-requisites
**NLTK(Natural Language Toolkit)**

[Natural Language Processing with Python](http://www.nltk.org/book/) provides a practical introduction to programming for language processing.

For platform-specific instructions, read [here](https://www.nltk.org/install.html)

### Installation of NLTK
```
pip install nltk
```
### Installing required packages
After NLTK has been downloaded, install required packages
```
import nltk
from nltk.stem import WordNetLemmatizer
nltk.download('popular', quiet=True) # for downloading popular packages
nltk.download('punkt') 
nltk.download('wordnet') 
```

## How to run
* Jupyter Notebook [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/parulnith/Building-a-Simple-Chatbot-in-Python-using-NLTK/master)

You can run the [chatbot.ipynb](https://github.com/parulnith/Building-a-Simple-Chatbot-in-Python-using-NLTK/blob/master/Chatbot.ipynb) which also includes step by step instructions.
* Through Terminal
```
python chatbot.py
```
