# Healthcare-Analytics-Snowflake-dbt

This project demonstrates a healthcare analytics workflow using **Snowflake**, **dbt**, and synthetic patient data. It is fully version-controlled in GitHub and is designed to showcase data engineering, transformation, and analytics skills.

---
Table of Contents:

- [Project Overview](#project-overview)  
- [Setup Guide](#setup-guide)
  - [Precheck (Installs)](#precheck-installs)  
  - [1. Clone the Repository](#1-clone-the-repository)  
  - [2. Organize the Project Folder](#2-organize-the-project-folder)
  - [3. Initialize dbt Project](#3-initialize-dbt-project)
  - [4. Connect dbt to Snowflake](#4-connect-dbt-to-snowflake)

---

## Project Overview

This project uses synthetic patient data to simulate real-world healthcare analytics. Key features:

- **Raw CSVs**: patients, encounters, diagnoses, medications, labs  
- **Snowflake**: cloud data warehouse for storing raw and transformed data  
- **dbt**: for transforming raw data into staging and mart tables  
- **GitHub**: version control for all project files  

---

## Setup Guide

### Precheck (Installs)

Please ensure that you have Python installed! 

You can check this in Terminal:

``` bash
# Check Python version
python3 --version
```
Otherwise you can install it with Homebrew.

``` bash
brew install python
```

This project will use dbt, which I recommend to be installed in a virtual environment.

``` bash
# Create a virtual environment called "healthcare"
python3 -m venv ~/envs/healthcare

# Activate the virtual environment
source ~/envs/healthcare/bin/activate
```

You can deactivate later when you are not working on the project.

``` bash
deactivate
```
Upgrade pip

``` bash
pip install --upgrade pip
```
Install dbt for Snowflake

``` bash
pip install dbt-core dbt-snowflake

# Verify the installation
dbt --version
```
Now you should have everything you need installed for this project! 

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
```
### 3. Initialize dbt Project
``` bash
# Navigate to dbt folder in the repo
cd ~/Documents/Healthcare-Analytics-Snowflake-dbt/dbt

# Initialize project
dbt init healthcare_dbt
```
### 4. Connect dbt to Snowflake

At this step the Terminal will require you to log into Snowflake using your own credentials.

Test the connection

```bash
# Navigate to project folder
cd ~/Documents/Healthcare-Analytics-Snowflake-dbt/dbt/healthcare_dbt

dbt debug
```

If everything is set up properly, you'll see 'All checks passed!'
