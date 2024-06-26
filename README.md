# zillow_scraper
Collect complete rental and sales data for any location from Zillow.


## Description
Python package designed for scraping real estate data from Zillow. The scraper collects comprehensive details for rental and sale properties in specified locations. Extracted information includes unit number, price, square footage, number of baths, number of beds, and availability dates. The data is cleaned and formatted for further analysis and can be saved to CSV files.

## Features
- Scrape property details for specific locations from Zillow.
- Extract both sale and rental information.
- Data cleaning and structuring utilities.
- Output data to CSV for easy downstream analysis.

## Requirements
- bs4
- pandas
- requests
- json
- selenium

## Installation
```
git clone https://github.com/hansenrhan/zillow_scraper.git
cd zillow_scraper
python setup.py install
```


## Basic Usage

```Python
import zillow_scraper

# Define the target locations and types of properties to scrape
# locations should typically follow a city-state format
locations = ["manhattan-ny", "san-francisco-ca"]
property_types = ["rent", "sale"]

# Collect and save the data
zillow_scraper.collect_real_estate_data(locations, property_types)

```

For more detailed examples on usage and outputs you can expect, see ```examples/```

## Runtime & Issues
Please be advised that this scraper is designed to avoid overwhelming their servers and preventing you from being blocked. Therefore, the default setting makes a web request every two minutes. This means the scraper can run for an extended period depending on the number of locations and property types you specify. Make sure to allocate sufficient time for the scraping operation to complete. 

Collecting complete rental data can take considerably longer than sales data, and may take between several hours to days for a sufficiently large city (ie. Manhattan).

Although running it slowly should prevent this from happening - if you are having issues with collecting data, you may have to change your IP address since it may be blocked.
