# NewsAPI
```
BASE_URL = "https://saurav.tech/NewsAPI/"
API_URL_FORMAT = "<BASE_URL>/top-headlines/category/<category>/<country>.json"
```

eg: [https://saurav.tech/NewsAPI/top-headlines/category/health/in.json](https://saurav.tech/NewsAPI/top-headlines/category/health/in.json)

```json
{
  "status": "ok",
  "totalResults": 70,
  "articles": [
    {
      "source": {
        "id": null,
        "name": "Thestatesman.com"
      },
      "author": "SNS Web",
      "title": "‘Olympics in 2021 unrealistic unless COVID-19 vaccine found’ - The Statesman",
      "description": "Olympics is not the only sporting tournament to be pushed back because of the dreaded coronavirus pandemic and high-profile tournaments including the cash-rich Indian Premier League (IPL) have been affected.",
      "url": "https://www.thestatesman.com/sports/olympics-in-2021-unrealistic-unless-covid-19-vaccine-found1502879079-1502879079.html",
      "urlToImage": "https://www.thestatesman.com/wp-content/uploads/2020/03/Tokyo2020.jpg",
      "publishedAt": "2020-04-19T14:41:24Z",
      "content": "Holding the Tokyo Olympics any time before a vaccine is found will be “very unrealistic,” according to a leading global health expert. Professor Devi Sridhar said that the development of the vaccine will be key to when the Olympics can be held.\r\nSridhar, howe… [+1886 chars]"
    }
    ...
    ...
    ...
    {
      "source": {
        "id": null,
        "name": "Hindustantimes.com"
      },
      "author": "HT Correspondent",
      "title": "Covid-19: Staying at home and want to use AC? Here’s what you need to know - Hindustan Times",
      "description": "A recent study in China suggested that air conditioning aided the transmission of coronavirus infection between people in a restaurant.",
      "url": "https://www.hindustantimes.com/india-news/covid-19-staying-at-home-and-want-to-use-ac-here-s-what-you-need-to-know/story-ZToEjpKIT5DuT99xw4wz5M.html",
      "urlToImage": "https://www.hindustantimes.com/rf/image_size_960x540/HT/p2/2020/04/19/Pictures/virus-outbreak-india_5ceba5dc-81f4-11ea-aedf-4d2519fcedc3.jpg",
      "publishedAt": "2020-04-19T04:36:11Z",
      "content": "As coronavirus disease Covid-19 spreads rapidly, there is a barrage of information floating along with it on what should be used and what shouldn’t to check the spread of the disease.\r\nAmong such information is the use of air conditioners (ACs) - many on the … [+2178 chars]"
    }
  ]
}
```


## Supported Countries
| Country  | 2-letter ISO 3166-1 code |
| ------------- | ------------- |
| :india:	India  | in  |
|  :us:	USA | us  |
|  :australia:	Australia | au  |
|  :us:	Russia | ru  |
|  :fr:	France | fr  |
|  :gb:	United Kingdom | gb  |

## Introduction

[News API](https://newsapi.org/) is an amazing source of information as it provides a single API that exposes breaking news headlines and older articles from over 3,000 news sources and blogs!

You can [sign up here](https://newsapi.org/account) for a free developer plan which allows you to make 500 requests per day. One can easily exceed the limit

## Solution

This project queries the newsapi at a regular interval (currently at 10 mins) and logs the reponse to a JSON file.
This json file is then committed and pushed to github. Now one can get the latest news from this json instead of newsapi.

## Pros

- No API KEY needed
- No limit in number of requests

## Cons

- Cannot query for news (Can be fixed by cloning this repo and customizing according to your needs)
- Slightly delayed result (Can be reduced by reducing the query time interval to newsapi)