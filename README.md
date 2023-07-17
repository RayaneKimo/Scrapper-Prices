# Web Scraping and Data Processing for Laptop Products

This repository contains Python code for web scraping laptop products from a popular online retailer. The code uses Selenium and BeautifulSoup libraries to extract laptop information from the website. The scraped data is then processed and features are extracted to prepare a cleaned dataset for further analysis (like comparison between online stores which is the purpose of this project or you can make it for your own needs).

## Requirements
- Python 
- Selenium
- BeautifulSoup 
- Chrome WebDriver (Downloaded and placed at "C:/Users/asus/Desktop/chromedriver.exe")

## Web Scraping
The web scraping code in this repository retrieves laptop product informations. The `get_products_from_page` function is responsible for scraping data from a given URL and category. The function retrieves product names, links, promotional and original prices, and descriptions. The data is then stored in a list of dictionaries named 'products'.

## Fetching All Products
The `get_all_products` function reads the URLs and corresponding categories from a file named 'urls.txt'. It then iterates through each URL, fetching the respective products using the web scraping function. The function allows for a specific waiting time and a number of retries in case of timeouts.

## Data Processing
The data is processed after scraping to convert prices to floats, extract key features like screen size, processor, storage, RAM, GPU brand, and operating system. The code also adds a new column 'Tactile' to indicate whether a laptop is tactile or not.

## Rule-Based Data Featuring
In the rule-based data featuring section, the code categorizes the data based on specific keywords present in the 'Carte Graphique' (GPU) and 'Processeur' (Processor) columns. It sets the 'GPU brand' and 'Processeur' columns based on the identified keywords.

## Data Cleaning
Finally, the data is cleaned, and any remaining special characters in the 'Ecran' (Screen size) column are removed. The screen sizes are converted to float values, and RAM values are standardized.

## Usage
1. Ensure you have Python installed on your system.
2. Download the Chrome WebDriver and keep in mind the folder were you puted it (in my case :"C:/Users/asus/Desktop/chromedriver.exe")
3. Install the required Python libraries (Selenium, BeautifulSoup, pandas, and numpy).
4. Prepare the 'urls.txt' file with categories and corresponding URLs for the products you want to scrape.
5. Run the script, and it will fetch and process the laptop products from the given URLs.

Please note that this code is tailored to the specific website mentionned in the code and may need modifications if used for scraping other websites. Also, be considerate and adhere to the website's terms of service while web scraping.
