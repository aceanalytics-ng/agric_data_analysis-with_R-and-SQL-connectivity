# Crop Data Analysis Implemented via a R-SQL Connectivity

The goal of this project is to connect to a SQL database through an R environment and conduct exploratory data analysis (EDA) to gain useful insights into the Canadian Principal Crops dataset and The Bank of Canada Average Exchange rates dataset. Using SQL within an R environment is favoured for this project in order to maximize the Programming Interface - Database Connectivity compatibility between R and SQL, the data handling capabilities of R, and SQL's legendary capabilities to work with data from multiple tables and sources. 

## Agenda:

1.  Understand two real world datasets
2.  Create tables in a Db2 database
3.  Load the datasets into the two separate tables in the Db2 database
4.  Run SQL queries against the Db2 database using the RODBC package in R to conduct exploratory data analysis

## The datasets

This project uses a subsetted snapshot of one dataset from Statistics Canada, and one from the Bank of Canada. The links to the prepared datasets are provided in the next section; however, to explore the landing pages for the source datasets, the links are provided below:

1.  <a href="https://www150.statcan.gc.ca/t1/tbl1/en/tv.action?utm_medium=Exinfluencer&utm_source=Exinfluencer&utm_content=000026UJ&utm_term=10006555&utm_id=NA-SkillsNetwork-Channel-SkillsNetworkCoursesIBMRP0203ENSkillsNetwork23863830-2022-01-01&pid=3210035901">Canadian Principal Crops (Data & Metadata)</a>
2.  <a href="https://www.bankofcanada.ca/rates/exchange/daily-exchange-rates?utm_medium=Exinfluencer&utm_source=Exinfluencer&utm_content=000026UJ&utm_term=10006555&utm_id=NA-SkillsNetwork-Channel-SkillsNetworkCoursesIBMRP0203ENSkillsNetwork23863830-2022-01-01">Bank of Canada daily average exchange rates</a>

### 1. Canadian Principal Crops Data

This dataset contains agricultural production measures for the principal crops grown in Canada, including a breakdown by province and teritory, for each year from 1908 to 2020.

A detailed description of this dataset can be obtained from the StatsCan Data Portal at:
[https://www150.statcan.gc.ca/t1/tbl1/en/tv.action?pid=3210035901](https://www150.statcan.gc.ca/t1/tbl1/en/tv.action?utm_medium=Exinfluencer&utm_source=Exinfluencer&utm_content=000026UJ&utm_term=10006555&utm_id=NA-SkillsNetwork-Channel-SkillsNetworkCoursesIBMRP0203ENSkillsNetwork23863830-2022-01-01&pid=3210035901)\
Detailed information is included in the metadata file and as header text in the data file, which can be downloaded.

### 2. Bank of Canada daily average exchange rates

This dataset contains the daily average exchange rates for multiple foreign currencies. Exchange rates are expressed as 1 unit of the foreign currency converted into Canadian dollars. It includes only the latest four years of data, and the rates are published once each business day by 16:30 ET.

I am interested in only a snapshot of this dataset (with only the USD-CAD exchange rates)

A brief description of this dataset and the original dataset can be obtained from the Bank of Canada Data Portal at:
[https://www.bankofcanada.ca/rates/exchange/daily-exchange-rates/](https://www.bankofcanada.ca/rates/exchange/daily-exchange-rates/?utm_medium=Exinfluencer&utm_source=Exinfluencer&utm_content=000026UJ&utm_term=10006555&utm_id=NA-SkillsNetwork-Channel-SkillsNetworkCoursesIBMRP0203ENSkillsNetwork23863830-2022-01-01)

## Subsetted Dataset URLs:

Thanks to IBM Skills Network (through their IBM Data Exchange initiative), the needed snapshot of the datasets have been made available, and the links are provided below:

1.  Annual Crop Data: <https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBM-RP0203EN-SkillsNetwork/labs/Practice%20Assignment/Annual_Crop_Data.csv>

2.  Daily FX Data: <https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBM-RP0203EN-SkillsNetwork/labs/Practice%20Assignment/Daily_FX.csv>
