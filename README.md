## Sentiment analysis - Amazon Health and Personal Care Reviews
![](https://gitlab.com/sayantan.world98/sentiment-analysis-amazon-health-and-personal-care/-/raw/master/images/img1.jpg)

Sentiment analysis is the use of natural language processing, text analysis, computational linguistics, and biometrics to systematically identify, extract, quantify, and study affective states and subjective information.

We are using the **Amazon Health and Personal Care Reviews** dataset to perfom Sentiment Analysis. The dataset contains **346,355 reviews**.

Link to the original dataset source: http://jmcauley.ucsd.edu/data/amazon/

Find the project and dataset here: https://gitlab.com/sayantan.world98/sentiment-analysis-amazon-health-and-personal-care

Code Part 1: https://jovian.ai/sayantan-world98/001-amazon-hpc-sentiement-analysis-binary

Code Part 2: https://jovian.ai/sayantan-world98/002-amazon-hpc-sentiement-analysis-binary

Lets see what is there in our dataset.

Sample data
```
{
  "reviewerID": "A2SUAM1J3GNN3B",
  "asin": "0000013714",
  "reviewerName": "J. McDonald",
  "helpful": [2, 3],
  "reviewText": "I bought this for my husband who plays the piano.  He is having a wonderful time playing these old hymns.  The music  is at times hard to read because we think the book was published for singing from more than playing from.  Great purchase though!",
  "overall": 5.0,
  "summary": "Heavenly Highway Hymns",
  "unixReviewTime": 1252800000,
  "reviewTime": "09 13, 2009"
}
```
Where,

- reviewerID - ID of the reviewer, e.g. A2SUAM1J3GNN3B
- asin - ID of the product, e.g. 0000013714
- reviewerName - name of the reviewer
- helpful - helpfulness rating of the review, e.g. 2/3
- reviewText - text of the review
- overall - rating of the product
- summary - summary of the review
- unixReviewTime - time of the review (unix time)
- reviewTime - time of the review (raw)

### Model tested

- Logistic Regression
- Linear Support Vector Classification
- Random Forest Classifier
- Naive Bayes
- Multinomial Naive Bayes (TF-IDF only)

### Part 1 - TF-IDF 

TF-IDF stands for “Term Frequency — Inverse Document Frequency”. This is a technique to quantify a word in documents, we generally compute a weight to each word which signifies the importance of the word in the document and corpus. This method is a widely used technique in Information Retrieval and Text Mining.


### Part 2 - Word2Vec

![](https://gitlab.com/sayantan.world98/sentiment-analysis-amazon-health-and-personal-care/-/raw/master/images/word2vec.png)

Word2vec is a technique for natural language processing. The word2vec algorithm uses a neural network model to learn word associations from a large corpus of text. Once trained, such a model can detect synonymous words or suggest additional words for a partial sentence.

### Future Work

- Training using RNN (Deep Learning).
- Trying to handle sarcastic reviews.
- Trying to resolve overfitting, which we found in some models.
- Trying sentiment analysis on multiple class (for example Positive, Neutral, Negative).
