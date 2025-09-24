# Indeed Job Scraper (Playwright)

This project scrapes **Software Developer** job postings from [Indeed.com](https://www.indeed.com) for the **USA**, collecting up to 500 recent postings.  
The scraper extracts:

- Job Title  
- Full Description  
- Posting Link URL  
- Salary Range  
- Location  
- Job Level (Entry-Level, Experienced, Internship – inferred from text)  

All results are saved into a CSV file.

---

## 🚀 Setup

1. **Clone this repo** or copy the script to your project folder.

2. **Create a virtual environment** (recommended):
   ```bash
   python3 -m venv venv
   source venv/bin/activate   # Mac/Linux
   venv\Scripts\activate      # Windows


3. **Install dependencies**
    pip3 install -r requirements.txt

4. **Install Playwright browsers**
    playwright install


**▶️ Run the Scraper**
    python3 scrape_software_dev.py

The script will:

Open Indeed search results (q=software+developer, sort=date)
Visit each job card and fetch details
Save them to software_developer_jobs_USA_full.csv
Repeat this for other Job Titles

**⚠️ Notes**

Playwright runs a real browser, so scraping may be slower but more reliable than Selenium.
Random delays are added between requests to reduce the chance of being blocked.
If a CAPTCHA appears, complete it manually in the opened browser window.


**🛠️ Customization**

Change the search keyword by updating:
    JOB_TITLE = "software developer"

Change the number of postings:
    MAX_POSTINGS = 300


**✅ Requirements**

Python 3.9+
Internet connection
Indeed.com accessible in your region