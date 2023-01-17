# Text-Mining

In today's world, one of the biggest source of information is text data, which is unstructured in nature.
Finding customer sentiments from product reviews, extracting opinions from social media data are a few exmaple of text mining.

### 1 SENTIMENT CLASSIFICATION
* text:-Actual review comment on the tweet.
* sentiment:- Positive sentiments are labelled as 1 and negative sentiments are labelled as 0.

### 2 TEXT PRE-PROCESSING 
Unstructure data, features are not explicitly available in text data. Thus we need to use a process to extract feature from the text data.

#### 2.1 BAG-OF-WORDS(BoW) MODEL
The first step in creating a Bow model is to create a dictionary of all words used in the corpus. Not worry about grammer.
Then we will convert each document to a vector that represents words available in the document.
There are three ways to identify the importance of words in Bow model
* 1 Count Vector Model
* 2 Term Frequency Vector Model
* 3 Term Frequency-Inverse Document Frequency (TF-IDF) Model

##### 2.1.1 Count Vector Model:- We will use CountVectorizer to create count vectors. In CountVectorizer, the documents will be represented by the number of times each word appears in the document.

##### 2.1.2 Term Frequency Vector Model:- It is simply the frequency in which a word appears in a document in comparion to the total number words in the document.
                            TF(t) = (Number of times term t appears in a document) / (Total number of terms in the document)
                            
##### 2.1.3 Term Frequency-Inverse Document Frequency (TF-IDF) Model:- TF-IDF measures how important a word is to a document in the corpus. the importance if a words
increases proportinally to the number of times a word appears in the document but is reducedby the frequency of the word present in the corpus.
                            TF(t) = (Number of times term t appears in a document) / (Total number of terms in the document).
                            IDF(t) = log_e(Total number of documents / Number of documents with term t in it).

#### 2.2 Displaying Documnets Vectors
To visulize the count vectors, we will convert this matrix into a DataFrame and ser the column names to the actual feature names.

#### 2.3 Removing Low-frequency words
One of the challenges of dealing with text is the number of words available in corpus is too large. Some words would be common words and present across most of
the documents, while some words would be rare.

#### 2.4 Removing Stop Words
Stop words are such words which are very common in occurance such as "a","an","the","at" etc.
We ignore such word during the pre-processing part since thet do not give any information and would just take additional space.
Library for stop words is:- from nltk.corpus import stopwords

#### 2.5 Stemming and Lemmatization
Stemming:- Means mapping a group of words to the same stem by removing prefixes or suffixes without giving any value to th "grammatical meaning" of the stem formed after the processs.
Libray:- from nltk.stem import porterstemmer,lancasterstemmer, snowballstemmer.

Lemmatization:- also does the same things as stemming and to bring a word to its base form, but unlike stemming it do keep in account the actual meaning of the base word i.e the base words belongs to any specify language. The 'base words' is know as 'Lemma'.
Library:- from nltk.stem import WordNet Lemmatizer.


