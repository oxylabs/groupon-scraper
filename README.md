# Groupon Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs’ [Groupon Scraper](https://oxylabs.io/products/scraper-api/ecommerce/groupon?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Groupon website effortlessly. This brief guide explains how an Groupon Scraper works and provides code examples to understand better how you can use it hassle-free.

### How it works

You can get Groupon results by providing your own URLs to our service. We can return the HTML for any Groupon page you like.

#### Python code example

The example below illustrates how you can get HTML of Groupon page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal',
    'url': 'https://www.groupon.com/local/chicago?topcategory=travel'
}

# Get response.
response = requests.request(
    'POST',
    'https://realtime.oxylabs.io/v1/queries',
    auth=('user', 'pass1'),
    json=payload,
)

# Instead of response with job status and results url, this will return the
# JSON response with the result.
pprint(response.json())
```
Find code examples for other programming languages [**here**](https://github.com/oxylabs/groupon-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "\n<!DOCTYPE html>\n<!-- pull: gig_application_layout@7.0.141 e9ec5f2 -->\n<html lang=\"en\">\n<head data-a ... </html>",
      "created_at": "2023-12-18 10:27:33",
      "updated_at": "2023-12-18 10:27:38",
      "page": 1,
      "url": "https://www.groupon.com/local/chicago?topcategory=travel",
      "job_id": "7142460371272548353",
      "status_code": 200
    }
  ]
}
```
With our Groupon Scraper, you can effortlessly extract public data from any Groupon webpage. Collect specific consumer service information, such as ratings, service comments, or detailed descriptions, to gain a better market understanding and stay one step ahead of your competitors. If you need assistance, kindly reach out to our dedicated support team through live chat or drop an email at hello@oxylabs.io.