# Deutsche Welle Web Scraping for Article Data

This Python script performs web scraping on the Deutsche Welle website to extract and organize essential attributes of articles within a specified date range. The extracted information is then converted into a Pandas DataFrame for further analysis.

## Project Overview

The objective is to gather articles from Deutsche Welle within a specific time frame and structure the data, including attributes such as title, summary, publication date, subheadings, related topics, text content, category, and region.

## Code Explanation

1. **Initialization:**
   - `main_url` and `short_url` are defined to represent the main search URL and the shortened URL for article links, respectively.

2. **Scraping Function:**
   - The `scrape_dw` function takes two input dates and performs the web scraping.
   - It uses the BeautifulSoup library to parse HTML content and extract relevant information.
   - The main URL is modified to include the search navigation and date parameters.
   - Articles are extracted from the modified URLs, and a Pandas DataFrame is created with columns for title, summary, and link.

3. **Accessing Article Details:**
   - The `access_articles` function iterates through article links and retrieves additional details such as subheadings, related topics, text content, category, and region.
   - The obtained information is appended to lists and then added as new columns in the DataFrame.

4. **Data Processing:**
   - The script processes the DataFrame to organize the data and ensure consistency in format.
   - Date formatting is applied, and unnecessary columns are dropped to create a clean and structured dataset.

## Running the Script

To perform web scraping for articles within a specific date range, call the `scrape_dw` function with the desired start and end dates. The resulting DataFrame (`Data` in this example) will contain all relevant information about the extracted articles.

```python
Data = scrape_dw('08.10.2023', '09.10.2023')
```

Note: Ensure that the required libraries (`requests`, `BeautifulSoup`, `pandas`) are installed before running the script.

## Project Usage

This project provides a foundation for extracting and analyzing articles from Deutsche Welle's website. It can be extended for various applications, such as sentiment analysis, topic modeling, or trend analysis, based on the structured data obtained through web scraping.