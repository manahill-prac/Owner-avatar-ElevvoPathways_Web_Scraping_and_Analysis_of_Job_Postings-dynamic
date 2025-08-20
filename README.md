# LinkedIn Dynamic Job Scraper & Analyzer

A Python Selenium-based dynamic scraper to extract job listings from LinkedIn, analyze trends, visualize data, and export results.

---

## Features

- Scrape LinkedIn jobs dynamically (title, company, location, posted date, job URL)
- Extract in-demand skills from job titles
- Human-like delays and scrolling to mimic real browsing
- Data analysis:
  - Top hiring companies
  - Top job locations
  - Most demanded skills
  - Jobs scraped per page
- Visualizations using Matplotlib & Seaborn
- Export:
  - CSV of scraped jobs
  - TXT summary report

---

## Requirements

Python 3.9+ recommended.

Install dependencies using `requirements.txt`:

```bash
pip install -r requirements.txt
````

**For Google Colab:**

```bash
!apt-get update -qq
!apt-get install -y google-chrome-stable -qq
!pip install selenium pandas matplotlib seaborn chromedriver-autoinstaller -q
```

## Usage

```python
from linkedin_scraper import LinkedInJobScraper

# Initialize scraper
scraper = LinkedInJobScraper(headless=True)

# Scrape jobs (example: Data Entry in Pakistan)
jobs = scraper.scrape_linkedin_jobs(
    search_term="data entry",
    location="Pakistan",
    max_pages=2
)

# Analyze data
df = scraper.analyze_scraped_data()

# Visualize results
scraper.create_visualizations(df)

# Save results to CSV and TXT report
scraper.save_results('linkedin_data_entry')
```

---


[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/YOUR_FILE_ID_HERE)



