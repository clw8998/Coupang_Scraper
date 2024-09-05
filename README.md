# Coupang Scraper

This project is a web scraping tool designed to extract product information from an e-commerce site based on specific search terms. The tool automates the process of data collection and organization for further analysis.

**[中文版本](./README_ZH.md)**

## Table of Contents

- [Environment Setup](#environment-setup)
- [Usage](#usage)
  - [Scraping Script](#scraping-script)
  - [Search Term Preparation](#search-term-preparation)
  - [Parameter Settings](#parameter-settings)
- [Scraped Data Submission](#scraped-data-submission)
  - [Product Information to Extract](#product-information-to-extract)
  - [Data Storage Format](#data-storage-format)
  - [File Naming Convention](#file-naming-convention)
  - [Submit All Data](#submit-all-data)
- [Important Notes](#important-notes)
  - [Scraper Notes](#scraper-notes)

## Environment Setup

Run the following command to install the required modules:

```bash
pip install -r requirements.txt
```

## Usage

### Scraping Script

The complete scraping script is located in the `scraper.ipynb` file. Execute it sequentially from the beginning.

### Search Term Preparation

You can use the provided search terms in `./queries/M11207321_queries.txt` or prepare your own.

If you want to use custom search terms, ensure they are saved in a `.txt file`, with **one search term per line**:

```
筆電
衣服
餅乾
洗衣精
衛生紙
...
```

### Parameter Settings

Open `scraper.ipynb` and locate the **Parameter Setting** section. Here, you can define or modify the following parameters:

1. **student_id**: Your student ID.
2. **query_path**: The path to the search terms.
3. **results_path**: The path where scraping results will be saved.
4. **search_url**: The e-commerce site URL to scrape (must be the Taiwan Coupang page).
5. **short_time_sleep**: Short wait time.
6. **medium_time_sleep**: Medium wait time.
7. **long_time_sleep**: Long wait time.

## Scraped Data Submission

### Product Information to Extract

During the scraping process, ensure you collect the following product information:

1. **Product Name**
2. **Product Price**
3. **Product URL**

### Data Storage Format

Save the collected data as a `.csv` file, including the following columns:

1. **product_name**: Product name
2. **product_price**: Product price
3. **product_url**: Product URL

Ensure the `.csv` file is encoded in **UTF-8-SIG**.

### File Naming Convention

After scraping product data for each search term, save the results using the following file naming convention: `StudentID_QueryName.csv`, e.g., `M11207321_口罩.csv` (if your student ID contains letters, use uppercase letters).

### Submit All Data

If you need to submit the scraped data, place all result files for the search terms into a folder named after your **student ID**, then compress the folder into a `.zip` file named after your student ID, e.g., `M11207321.zip` (if your student ID contains letters, use uppercase letters).

## Important Notes

### Scraper Notes
- While scraping, you may open other windows, but **do not close or minimize the Chrome window running the scraper** (important).
- Ensure that the **screen remains on** during the scraping process (important).