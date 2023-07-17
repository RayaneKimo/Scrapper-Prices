# Web Scraping, Data Processing, and Sentiment Analysis for Laptop Products from Multiple Retailers

This repository contains Python code for web scraping laptop products from three popular online retailers, 'rueducommerce', 'Amazon', and 'Cdiscount'. The code uses Selenium and BeautifulSoup libraries to extract laptop information from the websites. The scraped data is then processed and features are extracted to prepare the data for further analysis. Additionally, a sentiment analysis part has been added to understand customer sentiment towards each retailer.

## Requirements
- Python
- Selenium 
- BeautifulSoup 
- Chrome WebDriver 
- Transformers Library (pip install transformers)

## Web Scraping
The web scraping code in this repository retrieves laptop product information from three different websites. The `get_products_from_page` function is responsible for scraping data from a given URL and category for each retailer. The function retrieves product names, links, promotional and original prices, and descriptions. The data is then stored in a list of dictionaries named 'products'.

## Fetching All Products from Multiple Retailers
The `get_all_products` function reads the URLs and corresponding categories from a file named 'urls.txt'. It then iterates through each URL for all three retailers, fetching the respective products using the web scraping function. The function allows for a specific waiting time and a number of retries in case of timeouts.

## Data Processing
The data is processed after scraping to convert prices to floats, extract key features like screen size, processor, storage, RAM, GPU brand, and operating system. The code also adds a new column 'Tactile' to indicate whether a laptop is tactile or not.

## Sentiment Analysis
The sentiment analysis part involves analyzing customer reviews for each retailer. The code reads customer reviews from separate text files for 'Amazon', 'Cdiscount', and 'RueDuCommerce'. It then uses the Transformers library to perform sentiment analysis on each review. The sentiment labels ('POSITIVE' or 'NEGATIVE') and scores are assigned to each review and stored in a DataFrame named 'avis_df'. The sentiment analysis helps to understand customer satisfaction towards each retailer.

## Data Cleaning
Finally, the data is cleaned, and any remaining special characters in the 'Ecran' (Screen size) column are removed. The screen sizes are converted to float values, and RAM values are standardized.

## Usage
1. Ensure you have Python installed on your system.
2. Download the Chrome WebDriver and place it at "C:/Users/asus/Desktop/chromedriver.exe".
3. Install the required Python libraries (Selenium, BeautifulSoup, pandas, numpy, and transformers).
4. Prepare the 'urls.txt' file with categories and corresponding URLs for the products you want to scrape from all three retailers.
5. Run the script, and it will fetch and process the laptop products from the given URLs and perform sentiment analysis on customer reviews.

Please note that this code is tailored to the specific websites 'rueducommerce.fr', 'Amazon', and 'Cdiscount' and may need modifications if used for scraping other websites. Also, be considerate and adhere to the websites' terms of service while web scraping.
