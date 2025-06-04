# 📊 Data Folder Background

This folder contains 2024 data on data job postings scraped from Google.

## Background

I've been collecting data on data job postings since 2022. I've been using a bot to scrape the data from Google, which come from a variety of sources. 

You can find the full dataset at my app [datanerd.tech](https://datanerd.tech).

> [Serpapi](https://serpapi.com/) has kindly supported my work by providing me access to their API. Tell them I sent you and get 20% off paid plans.

## Data Files

The datasets used in this course are a subset of the full dataset for 2024 and come in a variety of forms:

- `job_postings_flat.csv` - A CSV file that contains the data for the job postings in one single table.
- `job_postings_monthly.xlsx` - An Excel file that contains data broken up by months in each sheet.
- `/monthly_files` - A folder that contains the monthly Excel files for the job postings.
- `/star_schema_files` - A folder that contains the star schema files for the job postings.

> **NOTE:** Regardless of the format, all the data is the same. The only difference is the way it is organized.

## 📘 Data Dictionary

| Column Name             | Description                                                                 | Type         | Source           |
|-------------------------|-----------------------------------------------------------------------------|--------------|------------------|
| `job_title_short`       | Cleaned/standardized job title using BERT model (10-class classification)   | Calculated   | From `job_title` |
| `job_title`             | Full original job title as scraped                                          | Raw          | Scraped          |
| `job_location`          | Location string shown in job posting                                        | Raw          | Scraped          |
| `job_via`               | Platform the job was posted on (e.g., LinkedIn, Jobijoba)                   | Raw          | Scraped          |
| `job_schedule_type`     | Type of schedule (Full-time, Part-time, Contractor, etc.)                   | Raw          | Scraped          |
| `job_work_from_home`    | Whether the job is remote (`true`/`false`)                                  | Boolean      | Parsed           |
| `search_location`       | Location used by the bot to generate search queries                         | Generated    | Bot logic        |
| `job_posted_date`       | Date and time when job was posted                                           | Raw          | Scraped          |
| `job_no_degree_mention` | Whether the posting explicitly mentions no degree is required               | Boolean      | Parsed           |
| `job_health_insurance`  | Whether the job mentions health insurance                                   | Boolean      | Parsed           |
| `job_country`           | Country extracted from job location                                         | Calculated   | Parsed           |
| `salary_rate`           | Indicates if salary is annual or hourly                                     | Raw          | Scraped          |
| `salary_year_avg`       | Average yearly salary (calculated from salary ranges when available)        | Calculated   | Derived          |
| `salary_hour_avg`       | Average hourly salary (same logic as yearly)                                | Calculated   | Derived          |
| `company_name`          | Company name listed in job posting                                          | Raw          | Scraped          |
| `job_skills`            | List of relevant skills extracted from job posting using PySpark            | Parsed List  | NLP Extracted    |
| `job_type_skills`       | Dictionary mapping skill types (e.g., 'cloud', 'libraries') to skill sets   | Parsed Dict  | NLP Extracted    |

## Star Schema

For the `\star_schema_files` folder, I've created a star schema for the data that is organized in the following way:

> **NOTE:** We'll go over how to use this dataset in the course for those new to star schemas.

![Star Schema](../Resources/images/Data_star_schema.png)

### Tables
1. `job_postings_fact` - shows job postings (1 job posting per row)
2. `company_dim` - displays information on the company
3. `skills_dim` - list of skills and their type 
4. `skills_job_dim` - matches the skills to each job posting

### Relationships

1. `job_postings_fact` - `company_id` -> `company_dim`
2. `job_postings_fact` - `skill_id` -> `skills_dim`
3. `job_postings_fact` - `skill_id` -> `skills_job_dim`