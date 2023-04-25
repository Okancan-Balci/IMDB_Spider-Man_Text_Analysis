# IMDB Spider-Man Movies User Reviews EDA/LDA

## Data Acquisition

The data was collected with a custom Selenium Webdriver web scraper for IMDb reviews which could be found [here.](https://github.com/Okancan-Balci/Selenium_Web_Scrapers/tree/master/IMDB_Review_Scraper)

## Data Cleaning

The initial cleaning was done in [Python Jupyter Notebook environment](https://github.com/Okancan-Balci/Selenium_Web_Scrapers/blob/master/IMDB_Review_Scraper/IMDB_Review_Scraper.ipynb) and then the cleaned data was stored in a *.csv* file. Further cleaning and analysis were done with R and the steps could be followed on Table of Contents below.

The rendered notebook is on Kaggle and it can be accessed from [here.](https://www.kaggle.com/code/okancan/imdb-spider-man-movies-user-reviews-eda-lda)

## Data Analysis

I analyzed Spider-Man movie reviews from IMDb. As well as text analysis I also analyzed review related variables such as Review Rating, Review Helpfulness and Review Date.

In text analysis I used basic Natural Language Processing techniques such as:

* Counts and Frequency of the Words in a review
* TF-IDF Analysis
* Sentiment Analysis
* Topic Modelling with Latent Dirichlet Allocation (LDA)

## Table of Contents

<li><a href="https://www.kaggle.com/code/okancan/imdb-spider-man-movies-user-reviews-eda-lda#introduction" target="_self" rel=" noreferrer nofollow">Introduction</a></li>
<li><a href="https://www.kaggle.com/code/okancan/imdb-spider-man-movies-user-reviews-eda-lda#non-textual-analysis" target="_self" rel=" noreferrer nofollow">Non-Textual Analysis</a>
<ul>
<li><a href="https://www.kaggle.com/code/okancan/imdb-spider-man-movies-user-reviews-eda-lda#univariate-analysis" target="_self" rel=" noreferrer nofollow">Univariate Analysis</a></li>
<li><a href="https://www.kaggle.com/code/okancan/imdb-spider-man-movies-user-reviews-eda-lda#bivariate-analysis" target="_self" rel=" noreferrer nofollow">Bivariate Analysis</a></li>
</ul></li>
<li><a href="https://www.kaggle.com/code/okancan/imdb-spider-man-movies-user-reviews-eda-lda#text-analysis" target="_self" rel=" noreferrer nofollow">Text Analysis</a>
<ul>
<li><a href="https://www.kaggle.com/code/okancan/imdb-spider-man-movies-user-reviews-eda-lda#unigrams" target="_self" rel=" noreferrer nofollow">Unigrams</a>
<ul>
<li><a href="https://www.kaggle.com/code/okancan/imdb-spider-man-movies-user-reviews-eda-lda#titles" target="_self" rel=" noreferrer nofollow">Titles</a></li>
<li><a href="https://www.kaggle.com/code/okancan/imdb-spider-man-movies-user-reviews-eda-lda#reviews" target="_self" rel=" noreferrer nofollow">Reviews</a></li>
</ul></li>
<li><a href="https://www.kaggle.com/code/okancan/imdb-spider-man-movies-user-reviews-eda-lda#bigrams" target="_self" rel=" noreferrer nofollow">Bigrams</a>
<ul>
<li><a href="https://www.kaggle.com/code/okancan/imdb-spider-man-movies-user-reviews-eda-lda#titles-1" target="_self" rel=" noreferrer nofollow">Titles</a></li>
<li><a href="https://www.kaggle.com/code/okancan/imdb-spider-man-movies-user-reviews-eda-lda#reviews-1" target="_self" rel=" noreferrer nofollow">Reviews</a></li>
<li><a href="https://www.kaggle.com/code/okancan/imdb-spider-man-movies-user-reviews-eda-lda#bigram-graph" target="_self" rel=" noreferrer nofollow">Bigram Graph</a></li>
</ul></li>
<li><a href="https://www.kaggle.com/code/okancan/imdb-spider-man-movies-user-reviews-eda-lda#trigrams" target="_self" rel=" noreferrer nofollow">Trigrams</a>
<ul>
<li><a href="https://www.kaggle.com/code/okancan/imdb-spider-man-movies-user-reviews-eda-lda#review" target="_self" rel=" noreferrer nofollow">Review</a></li>
<li><a href="https://www.kaggle.com/code/okancan/imdb-spider-man-movies-user-reviews-eda-lda#trigram-graph" target="_self" rel=" noreferrer nofollow">Trigram Graph</a></li>
</ul></li>
<li><a href="https://www.kaggle.com/code/okancan/imdb-spider-man-movies-user-reviews-eda-lda#tf-idf-analysis" target="_self" rel=" noreferrer nofollow">TF-IDF Analysis</a></li>
<li><a href="https://www.kaggle.com/code/okancan/imdb-spider-man-movies-user-reviews-eda-lda#bigram-tf-idf" target="_self" rel=" noreferrer nofollow">Bigram TF-IDF</a></li>
<li><a href="https://www.kaggle.com/code/okancan/imdb-spider-man-movies-user-reviews-eda-lda#sentiment-analysis" target="_self" rel=" noreferrer nofollow">Sentiment Analysis</a>
<ul>
<li><a href="https://www.kaggle.com/code/okancan/imdb-spider-man-movies-user-reviews-eda-lda#total-sentiment-for-each-movie" target="_self" rel=" noreferrer nofollow">Total Sentiment for Each Movie</a></li>
<li><a href="https://www.kaggle.com/code/okancan/imdb-spider-man-movies-user-reviews-eda-lda#sentiment-score-for-each-rating" target="_self" rel=" noreferrer nofollow">Sentiment Score for Each Rating</a></li>
<li><a href="https://www.kaggle.com/code/okancan/imdb-spider-man-movies-user-reviews-eda-lda#sentiment-contribution-by-each-word" target="_self" rel=" noreferrer nofollow">Sentiment Contribution by Each Word</a></li>
<li><a href="https://www.kaggle.com/code/okancan/imdb-spider-man-movies-user-reviews-eda-lda#sentiment-score-versus-review-helpfulness" target="_self" rel=" noreferrer nofollow">Sentiment Score versus Review Helpfulness</a></li>
<li><a href="https://www.kaggle.com/code/okancan/imdb-spider-man-movies-user-reviews-eda-lda#the-best-and-the-worst-reviews" target="_self" rel=" noreferrer nofollow">The Best and the Worst Reviews</a></li>
<li><a href="https://www.kaggle.com/code/okancan/imdb-spider-man-movies-user-reviews-eda-lda#negated-words" target="_self" rel=" noreferrer nofollow">Negated Words</a></li>
</ul></li>
</ul></li>
<li><a href="https://www.kaggle.com/code/okancan/imdb-spider-man-movies-user-reviews-eda-lda#topic-modelling" target="_self" rel=" noreferrer nofollow">Topic Modelling</a>
<ul>
<li><a href="https://www.kaggle.com/code/okancan/imdb-spider-man-movies-user-reviews-eda-lda#movie-series" target="_self" rel=" noreferrer nofollow">Movie Series</a></li>
<li><a href="https://www.kaggle.com/code/okancan/imdb-spider-man-movies-user-reviews-eda-lda#individual-movies" target="_self" rel=" noreferrer nofollow">Individual Movies</a></li>
<li><a href="https://www.kaggle.com/code/okancan/imdb-spider-man-movies-user-reviews-eda-lda#modelling-with-bigrams" target="_self" rel=" noreferrer nofollow">Modelling with Bigrams</a></li>
</ul></li>
<li><a href="https://www.kaggle.com/code/okancan/imdb-spider-man-movies-user-reviews-eda-lda#conclusion" target="_self" rel=" noreferrer nofollow">Conclusion</a></li>

