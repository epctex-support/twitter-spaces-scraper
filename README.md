# Actor - Twitter Spaces Scraper

Since Twitter doesn't provide a good and free API, this actor should help you to retrieve data from it.

## Features

-   Scrape space detail - Scrape any metadata, admins of the space, contributors, speakers and listeners related information from any Twitter Space.

- Scrape statistics - Gather all the statistical information of a space.

## Why using this actor?

This actor is extremely fast and optimized. It'll scrape Twitter space information around 21 times faster than the other equivalent scrapers. Therefore you will consume less resources and it will be cheaper to use it.

## Bugs, fixes, updates and changelog

This scraper is under active development. If you have any feature requests you can create an issue from [here](https://github.com/epctex/twitter-spaces-scraper/issues).

## Input Parameters

The input of this scraper should be JSON containing the list of pages on Twitter Spaces Scraper that should be visited. Possible fields are:

- `startUrls`: (Optional) (Array) List of Twitter Spaces URLs. You should only provide space URLs.

- `proxy`: (Required) (Proxy Object) Proxy configuration.

This solution requires the use of **Proxy servers**, either your own proxy servers or you can use [Apify Proxy](https://www.apify.com/docs/proxy).

##### Tip

When you want to have a scrape over a specific Twitter Spaces URL, just copy and paste the link as one of the **startUrl**.

### Compute Unit Consumption

The actor optimized to run blazing fast and scrape many data as much as possible. Therefore, it forefronts all space detail requests. If actor doesn't block very often it'll scrape 100 Twitter Spaces in 14 seconds with ~0.02-0.04 compute units.

### Twitter Spaces Scraper Input example

```json
{
  "proxy": {
    "useApifyProxy": true
  },
  "startUrls": [
    "https://twitter.com/i/spaces/1lDGLnQnNlkxm/peek"
  ]
}

```

## During the Run

During the run, the actor will output messages letting you know what is going on. Each message always contains a short label specifying which page from the provided list is currently specified.
When items are loaded from the page, you should see a message about this event with a loaded item count and total item count for each page.

If you provide incorrect input to the actor, it will immediately stop with failure state and output an explanation of what is wrong.

## Twitter Spaces Scraper Export

During the run, the actor stores results into a dataset. Each item is a separate item in the dataset.

You can manage the results in any languague (Python, PHP, Node JS/NPM). See the FAQ or <a href="https://www.apify.com/docs/api" target="blank">our API reference</a> to learn more about getting results from this Twitter Spaces actor.

## Scraped Space Properties

```json
https://api.apify.com/v2/datasets/fhKHd5q6ov0gAH7vd/items?clean=true&format=json
```
