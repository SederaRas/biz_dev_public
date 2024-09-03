# INDEED for Growth Engine
## Project Overview
This project is part of a **Client's Business Development** initiative, specifically targeting the **Saudi Arabian market**. The primary goal was to develop a **growth engine** to identify companies hiring data talents, locate key contacts, and predict engagement opportunities with the Client.

#### Key Milestones:

- Identifying companies hiring data talents.
- Extracting relevant company data and key contacts from **Crunchbase**.
- Reaching out to key contacts on **LinkedIn**.
- Profiling companies.
- Predicting collaboration opportunities.
  
This project mainly focuses on the first two steps of the milestones for the Saudi Arabian market.

## Full Workflow
The "Full Workflow Indeed" folder contains all the scripts necessary to:

1. **Scrape Job Listings**: Scrape job listings from Indeed to obtain job keys for all relevant jobs.

2. **Scrape Job Details**: Use the job keys to scrape detailed job information. The results are saved in the "job_details_Indeed" folder, tagged and dated by job role.

3. **Concatenate and Process Files**: Concatenate and process the scraped files to filter out irrelevant jobs, extract mentioned skills and tools, and prepare the data for dashboard visualization. This step produces four output files:

    - **output.csv**: Consolidated job data.
    - **soft_skills_df.csv**: List of mentioned soft skills for each job.
    - **industry_skills_df.csv**: List of mentioned industry skills for each job.
    - **tools_df.csv**: List of mentioned tools for each job.
4. **Company Name Matching**: Extract unique company names from **output.csv** and match them with company names from **companies.csv** (which includes companies listed on Crunchbase with their URLs). The NLP-based library **Rapidfuzz** is used for matching. The output is a list of matched companies with corresponding URLs.

5. **Scrape Company Information**: Scrape detailed company information from Crunchbase based on the matched companies. This step produces four output files:
    - **errors.csv**: Entries where no company information was available.
    - **companies_data.csv**: Detailed information about the matched companies.
    - **people_data.csv**: Contact details of individuals associated with the matched companies.
    - **contact.csv**: A processed version of people_data.csv, ready for visualization.
6. **Build Dashboard**: Finally, use Tableau to build a dashboard that visualizes the insights derived from all the gathered data.

## Skills and Tools Used
- **Web Scraping**and **APIs**: ScraperAPI, Scrapfly
- **Data Processing**: Python (Pandas, NumPy)
- **NLP**: Rapidfuzz
- **Data Storage**: CSV files
- **Visualization**: Tableau
- **Other Tools**: VSCode
