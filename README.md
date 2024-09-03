# Coupang Scraper

This project is a web scraping tool designed to extract product information from an e-commerce website based on specific queries. The tool automates the process of data collection and organization, facilitating further analysis.

## Table of Contents

- [Environment Setup](#environment-setup)
- [Usage Instructions](#usage-instructions)
  - [Scraping Script](#scraping-script)
  - [Query Preparation](#query-preparation)
  - [Parameter Settings](#parameter-settings)
- [Important Notes](#important-notes)
  - [Scraping Precautions](#scraping-precautions)
  - [Required Product Information](#required-product-information)
  - [Result Storage Format](#result-storage-format)
  - [File Naming Conventions](#file-naming-conventions)
  - [Submitting Scraping Results](#submitting-scraping-results)

## Environment Setup

Run the following command to install the necessary modules:

```bash
pip install -r requirements.txt
```

## Usage Instructions

### Scraping Script

The complete scraping script is located in the `scraper.ipynb` file. Execute the cells sequentially from the beginning.

### Query Preparation

You can use the provided queries in `./queries/M11207321_queries.txt` or prepare your own.

If you wish to use custom queries, please ensure that the queries are saved in a `.txt` file, with **one query per line**:

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
2. **query_path**: The path to the queries file.
3. **results_path**: The path to save the scraping results.
4. **search_url**: The e-commerce website URL to be scraped (must be the Taiwan Coupang page).
5. **short_time_sleep**: Short wait time.
6. **medium_time_sleep**: Medium wait time.
7. **long_time_sleep**: Long wait time.

## Important Notes

### Scraping Precautions
- During scraping, you may open other windows, but **do not close or minimize the Chrome window that is performing the scraping.**
- Make sure the screen **remains on** while the **scraper is running**

### Required Product Information

During the scraping process, ensure that the following product information is collected:

1. **Product Name**
2. **Price**
3. **Product Link**

### Result Storage Format

Save the collected data in a `.csv` file with the following columns:

1. **product_name**: Product Name
2. **product_price**: Price
3. **product_url**: Product Link

Ensure that the `.csv` file is encoded in **UTF-8-SIG**.

### File Naming Conventions

After scraping the product data for each query, save the results using the following file naming convention: `StudentID_QueryName.csv`, e.g., `M11207321_Mask.csv` (if your student ID contains letters, use uppercase letters).

### Submitting Scraping Results

If you need to submit the scraping results, place all the result files for each query in a folder named after your `Student ID`, then compress that folder into a `StudentID.zip`, e.g., `M11207321.zip` (if your student ID contains letters, use uppercase letters).