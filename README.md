# Ralphs Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs' [Ralphs Scraper](https://oxylabs.io/products/scraper-api/ecommerce/ralphs?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Ralphs website effortlessly. This brief guide showcases how Ralphs Scraper works, along with code examples to help you better understand how to use it hassle-free.

### How it works

You can get Ralphs results by providing your own URLs to our service. We can return the HTML for any page you like.

#### Python code example

The example below illustrates how you can get HTML of Ralphs page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal_ecommerce',
    'url': 'https://www.ralphs.com/pl/tvs-home-theater/29001?pzn=relevance'
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
Find code examples for other programming languages [**here**](https://github.com/oxylabs/ralphs-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<!doctype html>\n<html lang=\"en-us\">\n<head>\n  <meta charset=\"utf-8\" />\n  <meta name=\"viewport\" conten ... </html>",
      "created_at": "2024-02-20 12:52:04",
      "updated_at": "2024-02-20 12:52:06",
      "page": 1,
      "url": "https://www.ralphs.com/pl/tvs-home-theater/29001?pzn=relevance",
      "job_id": "7165689564273595393",
      "status_code": 200
    }
  ]
}
```
With our Ralphs Scraper, you can easily draw out publicly available data from any Ralphs web page. Gather necessary grocery item information, like prices, customer reviews, or product descriptions, to conduct thorough market analysis and outpace your rivals. If you encounter any issues or have any queries, feel free to reach out to our supportive team via live chat or you can also email us at hello@oxylabs.io.