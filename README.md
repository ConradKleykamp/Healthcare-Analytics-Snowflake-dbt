# Healthcare-Analytics-Snowflake-dbt

This project demonstrates a healthcare analytics workflow using **Snowflake**, **dbt**, and synthetic patient data. It is fully version-controlled in GitHub and is designed to showcase data engineering, transformation, and analytics skills.

---
Table of Contents:

- [Project Overview](#project-overview)  
- [Setup Guide](#setup-guide)  
  - [1. Clone the Repository](#1-clone-the-repository)  
  - [2. Organize the Project Folder](#2-organize-the-project-folder)

---

## Project Overview

This project uses synthetic patient data to simulate real-world healthcare analytics. Key features:

- **Raw CSVs**: patients, encounters, diagnoses, medications, labs  
- **Snowflake**: cloud data warehouse for storing raw and transformed data  
- **dbt**: for transforming raw data into staging and mart tables  
- **GitHub**: version control for all project files  

---

## Setup Guide

### 1. Clone the Repository

Open Terminal:

``` bash
# Go to the folder where you want to store the repo
cd ~/Documents

# Clone the repo from GitHub
git clone https://github.com/<ConradKleykamp>/Healthcare-Analytics-Snowflake-dbt.git

# Navigate into the repo
cd Healthcare-Analytics-Snowflake-dbt
```
### 2. Organize the Project Folder

``` bash
# Create folders for CSVs, scripts, dbt, and analysis
mkdir data snowflake dbt analysis

# Move CSVs into data folder
mv ~/Downloads/*.csv data/
