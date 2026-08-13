# stocksight-works
**Investment Research Assistant and Stock Predictor using Elasticsearch and Sentiment Analysis**

Analyze emotions on Twitter and news headlines to predict stock prices.

## About
stocksight-works is an open source investment research assistant that uses Elasticsearch to store Twitter and news headlines data for stocks. It analyzes the emotions of what the author writes and does sentiment analysis on the text to determine how the author "feels" about a stock.

## Features
- **Analyze Tweets**: Listen to Twitter streams and extract relevant tweets for sentiment analysis.
- **Sentiment Analysis**: Use natural language processing (NLP) to determine the sentiment of tweets and news headlines.
- **Store Data in Elasticsearch**: Store extracted tweets and their sentiment values in Elasticsearch for further analysis.
- **Predict Stock Prices**: Use sentiment analysis to predict stock prices based on Twitter and news headlines data.
- **News Headline Analysis**: Extract and analyze news headlines for sentiment and store in Elasticsearch.

## Installation
```shell
$ git clone https://github.com/AvicenaIG/stocksight.git
$ cd stocksight
$ python -m venv venv
$ source venv/bin/activate
$ pip install -r requirements.txt
```

## Quick Start
```python
from sentiment import get_sentiment_from_url, clean_text_sentiment
url = 'https://www.example.com/news-headline'
sentiment = get_sentiment_from_url(url)
clean_text_sentiment = clean_text_sentiment(sentiment)
```

## Usage
```python
from stockprice import GetStock
stock = GetStock('AAPL')
print(stock.price)
```

## Configuration
| Option | Type | Default | Description |
| --- | --- | --- | --- |
| ELASTICSEARCH_HOST | str | 'localhost' | Elasticsearch host |
| ELASTICSEARCH_PORT | int | 9200 | Elasticsearch port |
| TWITTER_API_KEY | str | '' | Twitter API key |
| TWITTER_API_SECRET | str | '' | Twitter API secret |
| NEWS_HEADLINE_URL | str | '' | News headline URL |

## Contributing
Contributions to stocksight-works are welcome. Please see the [CONTRIBUTING.md](CONTRIBUTING.md) file for details.

## License
stocksight-works is released under the MIT License. See the [LICENSE](LICENSE) file for details.