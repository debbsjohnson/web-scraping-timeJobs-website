# Job Scraper

This is a Python script that scrapes job listings from the TimesJobs website, filters out job postings that require certain skills you are not familiar with, and saves the relevant job listings to individual text files for later reference. It runs in a loop and periodically checks for new job postings.

## Prerequisites

Before using this script, make sure you have Python installed on your system. You will also need to install the following Python libraries if you haven't already:

- BeautifulSoup (bs4)
- requests

You can install these libraries using pip:

```bash
pip install beautifulsoup4 requests
```

## Getting Started

1. Clone or download this repository to your local machine.

2. Open a terminal and navigate to the directory containing the script.

3. Run the script using the following command:

```bash
python job_scraper.py
```

## Usage

1. When you run the script, it will prompt you to enter skills you are not familiar with. Enter the skills you want to filter out from job listings.

2. The script will then start scraping job listings from the TimesJobs website, filtering out jobs that require the specified unfamiliar skill(s).

3. The relevant job listings are saved to individual text files in a "posts" directory, each with a filename containing a numerical index.

4. The script runs in a continuous loop, periodically checking for new job postings.

5. To stop the script, press `Ctrl+C` in the terminal.

## Customization

You can customize the script by modifying the URL of the job search page and the time interval for checking new job listings. By default, the script searches for Python-related jobs, but you can change the URL in the `find_jobs` function to search for jobs in different categories or locations.

```python
html_text = requests.get("https://www.timesjobs.com/candidate/job-search.html?searchType=personalizedSearch&from=submit&txtKeywords=python&txtLocation=").text
```

You can adjust the time interval (in minutes) between job checks by changing the value of the `time_wait` variable:

```python
time_wait = 10  # Wait for 10 minutes
```


## Acknowledgments

- This script uses the BeautifulSoup library for web scraping.
- TimesJobs website is the source of job listings. Please review their terms and conditions for usage.
