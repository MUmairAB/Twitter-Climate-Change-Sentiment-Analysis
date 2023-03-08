# Twitter Climate Change Sentiment Analysis
This project investigates the sentiments of people about the existential threat of **Climate Change**. The tweets of people on the same are analyzed to get an overview of people's views about climate change. Thus the problem can be divided into two main sub-problems:

1. **Getting tweets about climate change**
2. **Analyzing the sentiments of the tweets**

The former problem is solved using **Twitter Scrapping**. While the latter is dealt with using **Machine Learning**. Let's dig deeper.

|        Task      |            Description              |         Tools/Packages Used               |
| :---             |                :----:                   |          :---                             |
| Data Collection           | Getting climate change tweets from Twitter| Snscrape Library                                |
| Data Pre-Processing        | 1. Data cleaning 2. Removal of all links and special characters from the tweets 3. Tokenization and removal of stopwords 4. Lemmatization of the words of tweets  | 1. Natural Language Toolkit (NLTK) 2. RegEx or re      |
| Visual Text Analysis| Visual display of text data for simple text analysis| Wordcloud and Matplotlib                  |
| Text Analysis       | Analysis of sentiments in tweets  | vaderSentiment package |
| Data Visualization | Graphs of resultant sentiments | Matplotlib, Seaborn |

# Getting tweets about climate change
The tweets were obtained through Twitter scrapping. For that, [Snscrape](https://pypi.org/project/snscrape/)'s **TwitterSearchScraper** function was used. The detailed code is available in the **Twitter_scrapping** notebook.

Totally, 3000 tweets per day were extracy=ted for the 370 days. This amounts to 1,110,000 or **1.1 Million** tweets. The tweets data is present in the **Dataset** directory.

# Analyzing the sentiments of the tweets
This part consisted of a couple of steps.

## Removing NULL/Missing values
Since the data scrapped data had some NULL values, the first step was to take care of it. The following graph shows the NULL values count against each column.
<img src="https://github.com/MUmairAB/Twitter-Climate-Change-Sentiment-Analysis/blob/main/Visualizations/null%20values%20heatmap.png" style="height: 284px; width:443px;"/>

## Dropping duplicate tweets
Then, duplicate tweets were dropped. The following pie chart shows the ratio of original vs. duplicate tweets.
<img src="https://github.com/MUmairAB/Twitter-Climate-Change-Sentiment-Analysis/blob/main/Visualizations/Original%20vs%20duplicate%20tweets%20pie%20chart.png" style="height: 240px; width:734px;"/>

## Text data manipulation
After the initial data cleaning, some manipulation of text data was carried out. This processing involves:
1. Removal of all links and special characters from the tweets
2. Tokenization and removal of stopwords
3. Lemmatization of the words of tweets
To do this, **Natural Language Toolkit (NLTK)** was used. It is a very popular suite of libraries and programs used for statistical natural language processing for the English language.

## Visual text analysis / WordCloud
It is nice to plot a Wordcloud to get a glimpse of the frequently used words in tweets. The resultant graph is shown below.
<img src="https://github.com/MUmairAB/Twitter-Climate-Change-Sentiment-Analysis/blob/main/Visualizations/word%20cloud.png" style="height: 576px; width:1080px;"/>

## Sentiment analysis
For analyzing the sentiments of tweets, the [vaderSentiment](https://pypi.org/project/vaderSentiment/) package was used.

The tweets were classified as:

1. Positive
2. Overly Positive
3. Negative
4. Overly Negative
5. Neutral

For a better understanding of the sentiments, some interesting visualizations were created:

**1. Time series plot of sentiments**
This plot shows how sentiments propagate over time.
<img src="https://github.com/MUmairAB/Twitter-Climate-Change-Sentiment-Analysis/blob/main/Visualizations/Time%20Series%20Plot.png" style="height: 290px; width:850px;"/>

**2. Bar plot of sentiments**
<img src="https://github.com/MUmairAB/Twitter-Climate-Change-Sentiment-Analysis/blob/main/Visualizations/bar%20plot.png" style="height: 432px; width:720px;"/>

**3. Pie chart of sentiments**

<img src="https://github.com/MUmairAB/Twitter-Climate-Change-Sentiment-Analysis/blob/main/Visualizations/sentiment%20pie%20chart.png" style="height: 283px; width:440px;"/>

## Word sentiments

Words were also segregated into:
1. Positive Words
2. Neutral Words
3. Negative Words

The following pie chart shows their distribution:

<img src="https://github.com/MUmairAB/Twitter-Climate-Change-Sentiment-Analysis/blob/main/Visualizations/sentiment%20words%20pie%20chart.png" style="height: 281px; width:438px;"/>

# Summing it up
The analysis can be summed up using the following graph:

<img src="https://github.com/MUmairAB/Twitter-Climate-Change-Sentiment-Analysis/blob/main/Visualizations/sentiment3%20pie%20chart.png" style="height: 284px; width: 430px;"/>

This graph shows that **pro-climate tweets and anti-climate tweets are equal in numbers**. This means that we need to have an aggressive climate awareness campaign and let people know that **Climate Change is Real and is an Existential Threat**.

