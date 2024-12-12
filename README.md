# Google News Scraper

[![Promo](https://github.com/luminati-io/Google-News-Scraper/blob/main/images/Proxies%20and%20scrapers%20GitHub%20bonus%20banner.png)](https://brightdata.com/products/serp-api/google-search/news?promo=github15) 

This repository provides two methods to collect news data from Google News.
- **Free Method:** Perfect for small projects and learning
- **Google News API:** Ideal for large-scale, reliable, real-time data extraction

## Table of Contents

- [Method 1: Free Google News Scraper](#method-1-free-google-news-scraper)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Usage](#usage)
  - [Output](#output)
- [Common Scraping Challenges](#common-scraping-challenges)
- [Method 2: Bright Data Google News API](#method-2-bright-data-google-news-api)
  - [Key Benefits](#key-benefits)
  - [Getting Started with the Google News API](#getting-started-with-the-google-news-api)
  - [Key Input Parameters](#key-input-parameters)
  - [Sample Result](#sample-result)
  - [Ready-to-Use Python Code](#ready-to-use-python-code)
  - [Understanding the API Implementation](#understanding-the-api-implementation)
  - [Customizing Your Data Collection](#customizing-your-data-collection)

## Method 1: Free Google News Scraper
<img width="700" alt="image" src="https://github.com/user-attachments/assets/a7d34ffe-17c6-4c59-acbf-aaf84ed1b13e">

This free tool lets you collect news articles based on any topic you're interested in. You'll get everything from headlines to publication dates, all neatly organized.

### Prerequisites
- Python 3.9+
- Two key packages:
  - [aiohttp](https://pypi.org/project/aiohttp/) (for making requests)
  - [beautifulsoup4](https://pypi.org/project/beautifulsoup4/) (for parsing HTML)

### Installation
1. Clone the repository:

    ```bash
    git clone https://github.com/luminati-io/Google-News-Scraper.git
    ```
3. Navigate to the project directory:

    ```bash
    cd Google-News-Scraper
    ```
4. Install required dependencies:

    ```bash
    pip install -r requirements.txt
    ```
### Usage
1. Navigate to the `free_scraper` directory and open `main.py`
2. Define your search terms in the file:

    ```bash
    search_terms = [
        "artificial intelligence",
        "climate change",
        "space exploration",
        # Add more search terms as needed
    ]
    ```
3. Run the scraper:

    ```bash
    python main.py
    ```
### Output
The scraper generates JSON files:
- Individual JSON files for each search term
- A `combined_results.json` file containing data from all search terms

Each article in the JSON output contains:
```json
{
    "title": "OpenAI launches full o1 model with image uploads and analysis, debuts ChatGPT Pro - VentureBeat",
    "link": "https://news.google.com/rss/articles/CBMipgFBVV95cUxQTTVmS1I4aW1QanZXTnBfa2tBR3d0Y2JzNjJJNldBZTd1TVVfRmpxaUM3bGJld3RycXhPbU8wM1loT0JGd2JDRzFmU1pLU3FSbkRRZ0FPY29INmdhU1RsWXFqXzdLTjNCbU5ES3pIQXZLbTVmMWVhc0FqVlljeWNPOHZMeFlXV2F5Q21ac0lSZVhIOHlnS05sdkR5ZjhJTU9HazJ6MWJR?oc=5",
    "publication_date": "Thu, 05 Dec 2024 18:00:00 GMT",
    "source": "VentureBeat",
    "source_url": "https://venturebeat.com",
    "guid": "CBMipgFBVV95cUxQTTVmS1I4aW1QanZXTnBfa2tBR3d0Y2JzNjJJNldBZTd1TVVfRmpxaUM3bGJld3RycXhPbU8wM1loT0JGd2JDRzFmU1pLU3FSbkRRZ0FPY29INmdhU1RsWXFqXzdLTjNCbU5ES3pIQXZLbTVmMWVhc0FqVlljeWNPOHZMeFlXV2F5Q21ac0lSZVhIOHlnS05sdkR5ZjhJTU9HazJ6MWJR",
}
```

👉 You can find a complete example output in our [free_scraper/data/](https://github.com/luminati-io/Google-News-Scraper/tree/main/free_scraper/data) directory.

## Common Scraping Challenges
Scraping data from Google News can be quite challenging. Here are some common issues you may encounter:
1. **CAPTCHA and Anti-Bot Mechanisms:** Google often employs CAPTCHAs or rate-limiting mechanisms to prevent bots from accessing its content.
2. **Scalability:** Scraping large volumes of data or performing high-frequency scraping can overwhelm free scrapers.
3. **Global and Localized News Access:** Customizing scrapers for different regions and languages often requires significant effort and manual adjustments.

## Method 2: Bright Data Google News API
Want something more robust? Let's talk about [Bright Data's Google News API](https://brightdata.com/products/serp-api/google-search/news). Here's why it's worth considering:

### Key Benefits
- **Zero Infrastructure Headaches:** Forget about proxies and CAPTCHAs
- **Built to Scale:** Handles heavy traffic with exceptional performance
- **Global Reach:** Get news from any country, any language
- **Privacy First:** GDPR & CCPA compliant
- **Pay for Success:** Only charged for successful requests
- **Try Before You Buy:** 20 free API calls to test things out

## Getting Started with the Google News API
> For a detailed guide on setting up the Google News API, check our [Step-by-Step Setup Guide](https://github.com/luminati-io/Google-News-Scraper/blob/main/google_news_api_setup.md).
### Key Input Parameters
| **Parameter**| **Required?** | **Description**                                            | **Example**               |
|---------------|--------------|------------------------------------------------------------|---------------------------|
| `url`         | Yes          | Base Google News URL                                   | `news.google.com`|
| `keyword`     | Yes          | Your search topic                        | `"ChatGPT"`             |
| `country`     | No           | Where to get news from                                | `"US"`                    |
| `language`    | No           | What language you want                                | `"en"`                    |

### Sample Result
Here’s what the API returns:
```json
{
    "url": "https://www.tomsguide.com/news/live/12-days-of-openai-live-blog-chatgpt-sora",
    "title": "12 Days of OpenAI Day 2 LIVE: o1 full is here and every new ChatGPT AI announcement as it happens",
    "publisher": "Tom's Guide",
    "date": "2024-12-06T20:54:01.000Z",
    "category": null,
    "keyword": "chatgpt",
    "country": "US",
    "image": "https://news.google.com/api/attachments/CC8iK0NnNW9SbTFVTWtkNGFGSjJSVGhGVFJDb0FSaXNBaWdCTWdhQmtJcWpOQWM=-w200-h112-p-df-rw",
    "timestamp": "2024-12-08T10:06:05.122Z",
    "input": {
        "url": "https://news.google.com/",
        "keyword": "chatgpt",
        "country": "US",
        "language": "en",
    },
}
```
👉 You can find a complete example output in our [news_scraper_output.json](https://github.com/luminati-io/Google-News-Scraper/blob/main/google-news-api-scraper/data/news_scraper_output.json) file.

### Ready-to-Use Python Code
Here's a script to get you started:
```python
import requests
import json
import time


class BrightDataNews:
    def __init__(self, api_token):
        self.api_token = api_token
        self.headers = {
            "Authorization": f"Bearer {api_token}",
            "Content-Type": "application/json",
        }
        self.dataset_id = "gd_lnsxoxzi1omrwnka5r"

    def collect_news(self, search_queries):
        """
        Collect Google News articles using BrightData API
        """
        # 1. Trigger data collection
        print("Starting news collection...")
        trigger_response = self._trigger_collection(search_queries)
        snapshot_id = trigger_response.get("snapshot_id")
        print(f"Snapshot ID: {snapshot_id}")

        # 2. Wait for data to be ready
        print("Waiting for data...")
        while True:
            status = self._check_status(snapshot_id)
            print(f"Status: {status}")

            if status == "ready":
                # Check if data is actually available
                data = self._get_data(snapshot_id)
                if data and len(data) > 0:
                    break
            time.sleep(10)  # Wait 10 seconds before next check
        # 3. Get and save the data
        print("Saving data...")
        filename = f"news_scraper_output.json"
        with open(filename, "w", encoding="utf-8") as f:
            json.dump(data, f, indent=2, ensure_ascii=False)
        print(f"✓ Data saved to {filename}")
        print(f"✓ Collected {len(data)} news articles")
        return data

    def _trigger_collection(self, search_queries):
        """Trigger news data collection"""
        response = requests.post(
            "https://api.brightdata.com/datasets/v3/trigger",
            headers=self.headers,
            params={"dataset_id": self.dataset_id, "include_errors": "true"},
            json=search_queries,
        )
        return response.json()

    def _check_status(self, snapshot_id):
        """Check collection status"""
        response = requests.get(
            f"https://api.brightdata.com/datasets/v3/progress/{snapshot_id}",
            headers=self.headers,
        )
        return response.json().get("status")

    def _get_data(self, snapshot_id):
        """Get collected data"""
        response = requests.get(
            f"https://api.brightdata.com/datasets/v3/snapshot/{snapshot_id}",
            headers=self.headers,
            params={"format": "json"},
        )
        return response.json()
```
Here's how to use it:
```python
# Initialize the client
news_client = BrightDataNews("<YOUR_API_TOKEN>")

# Define what you want to collect
queries = [
    {
        "url": "https://news.google.com/",
        "keyword": "artificial intelligence startups",
        "country": "US",
        "language": "en",
    },
    {
        "url": "https://news.google.com/",
        "keyword": "tech industry layoffs",
        "country": "US",
        "language": "en",
    },
]

# Start collection
try:
    news_data = news_client.collect_news(queries)
    print(f"Successfully collected {len(news_data)} articles")
except Exception as e:
    print(f"Collection failed: {str(e)}")
```
### Understanding the API Implementation
1. **Setting Up Your API Token**
    - First things first: you'll need an API token
    - If you haven't got one yet, check out our [setup guide](https://github.com/luminati-io/Google-News-Scraper/blob/main/google_news_api_setup.md)
2. **Starting the Collection**
    - Pass your search parameters to the API
    - You'll get back a `snapshot_id`
3. **Monitoring Progress**
    - The process takes a few minutes
    - Our code checks the status automatically:
      - "running" = Still collecting your data
      - "ready" = Time to collect your results!
4. **Getting Your Data**
    - Once the status shows "ready", we fetch and save your results
    - Data comes in clean JSON format
    - Each article includes all the fields we discussed earlier

## Customizing Your Data Collection
You can use the following parameters to fine-tune your results:
| **Parameter**       | **Type**   | **Description**                                            | **Example**                  |
|---------------------|------------|------------------------------------------------------------|------------------------------|
| `limit`             | `integer`  | Max results per input                                   | `limit=10`                   |
| `include_errors`    | `boolean`  | Get error reports for troubleshooting                     | `include_errors=true`        |
| `notify`            | `url`      | Webhook notification URL to be notified upon completion  | `notify=https://notify-me.com/` |
| `format`            | `enum`     | Output format (e.g., JSON, NDJSON, JSONL, CSV)         | `format=json`                |

💡 **Pro Tip:** You can also select whether to deliver the data to an [external storage](https://docs.brightdata.com/scraping-automation/web-data-apis/web-scraper-api/overview#via-deliver-to-external-storage) or to deliver it to a [webhook](https://docs.brightdata.com/scraping-automation/web-data-apis/web-scraper-api/overview#via-webhook).

----

Need more details? Check the [official API docs](https://docs.brightdata.com/scraping-automation/web-data-apis/web-scraper-api/overview).
