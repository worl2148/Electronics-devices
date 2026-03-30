# Men's Electronics Scraper - Group 4 (Home & Smart Devices)

This module scrapes men's electronics products from Boutiqaat.com, specifically focusing on home appliances and smart devices.

## Covered Subcategories

- Portable Blenders
- Coffee Makers & Grinders
- Heaters & Fans
- Home Accessories
- Irons & Steamers
- Vacuums
- Clocks
- Home Security
- Security Cameras
- Smart Accessories
- Smart Lighting
- Smart Plugs & Outlets

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
python -m men_electronics_sub4.main
```

## Dependencies

- Python 3.11+
- playwright
- beautifulsoup4
- boto3
- openpyxl

## Part of GitHub Actions Workflow

This module runs as part of the automated daily workflow at 1:30 AM UTC.
