# Summarizing Text with Amazon Reviews

Updated to work with TensorFlow Version: 1.3.0

The objective of this project is to build a model that can create relevant summaries for reviews written about fine foods sold on Amazon. This dataset contains above 500,000 reviews, and is hosted on [Kaggle](https://www.kaggle.com/snap/amazon-fine-food-reviews).

Here are two examples to show what the data looks like
```
Review # 1
Good Quality Dog Food
I have bought several of the Vitality canned dog food products and have found them all to be of good quality. The product looks more like a stew than a processed meat and it smells better. My Labrador is finicky and she appreciates this product better than  most.

Review # 2
Not as Advertised
Product arrived labeled as Jumbo Salted Peanuts...the peanuts were actually small sized unsalted. Not sure if this was an error or if the vendor intended to represent the product as "Jumbo".
```
To build our model we will use a two-layered bidirectional RNN with LSTMs on the input data and two layers, each with an LSTM using bahdanau attention on the target data.

The sections of this project are:
- 1.Inspecting the Data
- 2.Preparing the Data
- 3.Building the Model
- 4.Training the Model
- 5.Making Our Own Summaries

## Download data
Amazon Reviews Data: [Reviews.csv](https://www.kaggle.com/snap/amazon-fine-food-reviews/downloads/Reviews.csv) and copy it to **./Reviews.csv**

word embeddings [numberbatch-en-17.06.txt.gz](https://conceptnet.s3.amazonaws.com/downloads/2017/numberbatch/numberbatch-en-17.06.txt.gz)
after download, extract to **./model/numberbatch-en-17.06.txt**

## Dependencies
Python 3.5 packages: tensorflow v1.3, pandas, numpy, nltk

### How to Run
Run the python notebook by cd into the directory in command line then run
```
jupyter notebook
```
choose this in the browser

**summarize_reviews.ipynb**


Inspired by the post [Text Summarization with Amazon Reviews](https://medium.com/towards-data-science/text-summarization-with-amazon-reviews-41801c2210b), with a few improvements.

I wrote an [article](https://www.dlology.com/blog/tutorial-summarizing-text-with-amazon-reviews/)  about this project that explains parts of it in detail.