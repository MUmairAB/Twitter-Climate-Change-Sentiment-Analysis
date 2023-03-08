# Twitter Climate Change Sentiment Analysis
This projects investigates the sentiments of people about the existential threat of **Climate Change**. The tweets of people on the same are analyzed to get an overview of people's view about climate change. Thus the problem can be divided into two main sub-problems:

1. **Getting tweets about climate change**
2. **Analyzing the sentiments of the tweets**

The former problem is solved using **Twitter Scrapping**. While the latter is dealt with using **Machine Learning**. Let's dig deeper.

|        Task      |           Task Description              |         Tools/Packages Used               |
| :---             |                :----:                   |          :---                             |
| Data Collection           | Getting climate change tweets from twitter| Snscrape Library                                |
| Data Pre-Processing        | 1. Data cleaning 2. Removal of all links and special characters from the tweets 3. Tokenization and removal of stopwords 4. Lemmatization of the words of tweets  | 1. Natural Language Toolkit (NLTK) 2. RegEx or re      |
| Visual Text Analysis| Visual display of text data for simple text analysis| Wordcloud and Matplotlib                  |
| Text Analysis       | Analysis of sentiments in tweets  | vaderSentiment package |
| Data Visualization | Graphs of resultant sentiments | Matplotlib, Seaborn |

# Getting tweets about climate change
The tweets were obtained through Twitter scrappig. For that, [Snscrape](https://pypi.org/project/snscrape/)'s **TwitterSearchScraper** function was used. The detailed code is available in **Twitter_scrapping** notebook.

Totally, 3000 tweets per day were extracy=ted for the 370 days. This amounts to 1,110,000 or **1.1 Million** tweets. The tweets data is present in **Dataset** directory.

# Analyzing the sentiments of the tweets
This part consisted of couple of steps. Firstly, duplicate tweets were dropped. 
[Original vs. Duplicate Ration](https://github.com/MUmairAB/Twitter-Climate-Change-Sentiment-Analysis/blob/main/Visualizations/pie%20chart.png)

Before
For analyzing the sentiments of tweets, [vaderSentiment](https://pypi.org/project/vaderSentiment/) package was used.

The tweets are classified as:

1. Positive
2. Overly Positive
3. Negative
4. Overly Negative
5. Neutral

Apart from this, visual text analysis was also done using Wordcloud.


