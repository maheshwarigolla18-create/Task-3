# News Headline Scraper

A simple Python project that scrapes the top headlines from a news website and saves them to a text file.

## Objective

Scrape top headlines from a news website.

## Tools Used

- Python 3
- `requests` – to download the web page
- `BeautifulSoup` (bs4) – to parse the HTML and extract headlines

## Deliverables

- `headline_scraper.py` – the Python script
- `headlines.txt` – the output file containing the scraped headlines

## Installation

```bash
pip install requests beautifulsoup4
```

## Usage

```bash
python headline_scraper.py
```

The script prints the headlines in the terminal and saves them to `headlines.txt`.

## How It Works

1. Sends an HTTP request to the news website using `requests`.
2. Parses the HTML with `BeautifulSoup`.
3. Finds all `<h2>` and `<h3>` tags, which usually contain headlines.
4. Removes very short text and duplicates, then keeps the top 10.
5. Saves the headlines as a numbered list in `headlines.txt`.

## Sample Output

```
Top Headlines:

1. Global leaders meet to discuss climate agreement
2. Markets rise as inflation figures ease
3. New tech hub announced in southern India

Saved to headlines.txt
```

*(Actual headlines will vary, since news changes daily.)*

## Customization

- Change `URL` in the script to scrape a different news website.
- If no headlines are found, inspect the site in your browser and update the tags in `soup.find_all([...])` to match.
- Change `headlines[:10]` to get more or fewer headlines.

## Notes

- Websites change their layout often, so the tags may need updating over time.
- Check a website's terms of service and `robots.txt` before scraping it.

## Author

G Maheswari
