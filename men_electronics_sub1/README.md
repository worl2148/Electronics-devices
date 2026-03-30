# Men's Electronics Scraper - Group 1 (Audio, Video & Car)

This module scrapes men's electronics products from Boutiqaat.com, specifically focusing on audio, video, and car accessories.

## Covered Subcategories

- Accessories
- Earphones
- Headphones
- Microphones
- Speakers
- TV & Projector
- Bike Accessories
- Car Accessories
- Car Charger
- Car Mount
- Jump Starter
- AirPods & AirTag Case
- Phone Accessories

## Features

- **Async Processing**: Uses asyncio with semaphore (max 3 concurrent) for efficient scraping
- **Playwright Integration**: Handles JavaScript-rendered content and infinite scroll
- **S3 Integration**: Uploads product images and Excel files to AWS S3
- **Excel Generation**: Creates formatted Excel workbooks with product data
- **Date Partitioning**: Stores data in S3 with year/month/day structure

## S3 Storage Path

```
boutiqaat-data/year=YYYY/month=MM/day=DD/men/electronics/
```

## Usage

```bash
python -m men_electronics_sub1.main
```

## Dependencies

- Python 3.11+
- playwright
- beautifulsoup4
- boto3
- openpyxl

## Part of GitHub Actions Workflow

This module runs as part of the automated daily workflow at 1:30 AM UTC.
