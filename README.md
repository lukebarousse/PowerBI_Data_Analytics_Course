# 📊 Power BI for Data Analytics - Full Course

Data Nerds! This repo contains all the files needed to follow along my free course: [Power BI for Data Analytics]()
[![Power BI for Data Analytics](/Resources/images/0_PowerBI_Thubmnail.png)]()

> ⚠️ **Download from Google Drive, not GitHub!** Some files are missing here due to GitHub's 100MB limit. Get complete course files from [**Google Drive**](https://lukeb.co/powerbi-files)

## Team Members 👥
**🙋🏼‍♂️ Course Leader:** [Luke Barousse](https://www.linkedin.com/in/luke-b)  
**🎬 Course Producer:** [Kelly Adams](https://www.linkedin.com/in/kellyjianadams)  
**📺 Video Editor:** [Brannon Linder](https://www.linkedin.com/in/brannonlinder)

## Table of Contents

### 📚 Course Modules
- **[1. Grand Tour](1_Grand_Tour/)** - Introduction to Power BI App and Dashboard Building
  - [1.1 PBI App Intro](1_Grand_Tour/1.1_PBI_App_Intro.pbix)
  - [1.2 Dashboard Build](1_Grand_Tour/1.2_Dashboard_Build.pbix)

- **[2. Visualizations](2_Visualizations/)** - Core Chart Types and Visual Elements
  - [2.1 Visualizations](2_Visualizations/2_Visualizations.pbix)

- **[3. Power Query](3_Power_Query/)** - Data Transformation and ETL
  - [3.1 Power Query Intro](3_Power_Query/3.1_Power_Query_Intro.pbix)
  - [3.1 Power Query Intro (BigQuery Demo)](3_Power_Query/3.1_Power_Query__Intro(BigQuery%20Demo).pbix)
  - [3.2 Power Query Editor](3_Power_Query/3.2_Power_Query_Editor.pbix)
  - [3.3 Project2 Import](3_Power_Query/3.3_Project2_Import.pbix)
  - [3.4 Advanced Transformations](3_Power_Query/3.4_Adv_Transformations.pbix)
  - [3.5 Append](3_Power_Query/3.5_Append.pbix)
  - [3.5 Merge](3_Power_Query/3.5_Merge.pbix)
  - [3.6 M Language](3_Power_Query/3.6_M_Language.pbix)

- **[4. DAX](4_DAX/)** - Data Analysis Expressions
  - [4.1 DAX Intro](4_DAX/4.1_DAX_Intro.pbix)
  - [4.2 Explicit Measures](4_DAX/4.2_Explicit_Measures.pbix)
  - [4.3 Parameters](4_DAX/4.3_Parameters.pbix)

### 🎯 Projects
- **[Project 1: Data Jobs Dashboard](_Project_1/)** - Comprehensive two-page dashboard
  - Features: Market overview, drill-through analysis, interactive filtering
  - [📊 Dashboard File](_Project_1/Data_Jobs_Dashboard.pbix)
  - [🌐 View Interactive Dashboard](https://lukeb.co/powerbi-project1)

- **[Project 2: Data Jobs Dashboard 2.0](_Project_2/)** - Single-page focused dashboard
  - Features: Streamlined insights, advanced DAX, star schema modeling
  - [📊 Dashboard File](_Project_2/Data_Jobs_Dashboard_2.0.pbix)
  - [🌐 View Interactive Dashboard](https://lukeb.co/powerbi-project2)

### 📊 Data Sources
- **[Data Folder](Data/)** - Real-world 2024 data science job postings
  - [📄 job_postings_flat.csv](Data/job_postings_flat.csv) - Single table format
  - [📊 job_postings_monthly.xlsx](Data/job_postings_monthly.xlsx) - Monthly breakdown
  - [📁 monthly_files/](Data/monthly_files/) - Individual monthly Excel files
  - [📁 star_schema_files/](Data/star_schema_files/) - Normalized star schema format

### 🧩 Practice Problems
- **[Problems Folder](Problems/)** - Hands-on exercises with solutions
  - Organized by module (1_Grand_Tour, 2_Visualizations, 3_Power_Query, 4_DAX)
  - Includes problem files and solution files
  - Practice datasets included

### 📁 Additional Resources
- **[Resources Folder](Resources/)** - Supporting materials
  - Project screenshots and GIFs
  - Example dashboards
  - Course images and assets

## How to Run Power BI Files

### 📋 Prerequisites
- **Power BI Desktop** (Free) - Download from [Microsoft Power BI](https://powerbi.microsoft.com/desktop/)
- **Power BI Service Account** (Free tier available) - For publishing and sharing dashboards
- **Microsoft Excel** (Optional) - For viewing data files

### 🚀 Getting Started

#### 1. Download Power BI Desktop
- Visit [Microsoft Power BI Desktop download page](https://powerbi.microsoft.com/desktop/)
- Download and install the latest version (free)
- Sign in with your Microsoft account when prompted

#### 2. Open Course Files
1. Navigate to the desired module folder (e.g., `1_Grand_Tour/`, `2_Visualizations/`, etc.)
2. Double-click any `.pbix` file to open it in Power BI Desktop
3. If prompted, click "Enable Content" to allow data connections

#### 3. Working with Data Files
- **CSV Files**: Can be opened directly in Power BI Desktop using "Get Data" → "Text/CSV"
- **Excel Files**: Use "Get Data" → "Excel Workbook" to import
- **Monthly Files**: Import individual files or use folder import for batch processing

### 📁 File Types Explained

#### Data Files
- **[job_postings_flat.csv](Data/job_postings_flat.csv)**: Single table with all job data
- **[job_postings_monthly.xlsx](Data/job_postings_monthly.xlsx)**: Multi-sheet Excel file organized by month
- **[monthly_files/](Data/monthly_files/)**: Individual Excel files for each month
- **[star_schema_files/](Data/star_schema_files/)**: Normalized database structure (4 separate tables)

### 🔧 Troubleshooting

#### Common Issues
- **"Enable Content" Dialog**: Always click "Enable Content" when opening `.pbix` files
- **Data Source Errors**: If data connections fail, check the file paths in Power Query
- **Missing Visuals**: Ensure all required data fields are loaded and relationships are established

#### Data Connection Issues
- If you encounter data source errors:
  1. Go to **Home** → **Transform Data** → **Data Source Settings**
  2. Update the file paths to match your local directory structure
  3. Click "Change Source" and navigate to the correct data files

#### Performance Tips
- **Large Datasets**: Use filters in Power Query to reduce data size
- **Refresh Issues**: Close and reopen Power BI Desktop if refresh fails
- **Memory**: Close other applications if Power BI runs slowly

### 💡 Pro Tips
- **Save Frequently**: Power BI Desktop files can be large - save often
- **Use Bookmarks**: Create bookmarks to save different views of your data
- **Test Interactions**: Always test slicers, filters, and drill-through features
- **Performance**: Use measures instead of calculated columns when possible
- **Documentation**: Use the "About" section in your reports to document data sources and methodology

## Found a Typo? Want to Contribute?
- If you find an error in this repo, please feel free to make a pull request by:
    - Forking the repo
    - Making any changes
    - Submitting a pull request