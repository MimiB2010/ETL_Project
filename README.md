ETL Project

For this project, our team extracted data from Lending Club, US Census, and Zillow. The Lending Club data was a SQLite file from [Kaggle.com](https://www.kaggle.com/wendykan/lending-club-loan-data#database.sqlite). The US Census and Zillow data were csv files obtained from [Kaggle.com](https://www.kaggle.com/goldenoakresearch/us-household-income-stats-geo-locations). and [Zillow.com](https://www.zillow.com/research/data/) respectively.

<<<<<<< HEAD
We cleaned the data from each source using Jupyter Notebook and Pandas, before putting the data into a relational SQL database, called ZipCodes, via pgAdmin4. These tables are home_values, income_by_zip, loan_data, and loan_information.

Details about the cleaning and filtering process:
    
    -Zillow Real Estate Value Data: Source data set had the median real estate sale price by Zip Code for every month in the last 20 years along with a few other columns mostly indicating.  All entries before 2011 were dropped.   An Abr_Zip column was created - this simply extracted the first three numbers of the Zip_Code column.  The yearly averages were then computed for each year after and including 2011. The rest of the monthly median sale prices were then dropped.   The resulting table, home_values, that was loaded into the ZipCodes database had the following columns:  Abr_Zip, Zip_Code, City, State, CountyName, Rank, Metro, 2011_Current_Average, 2012_Current_Average, 2013_Current_Average, 2014_Current_Average, 2015_Current_Average, 2016_Current_Average, 2017_Current_Average, 2018_Current_Average, 2019_Current_Average.

    -Kaggle Income Data: From the source data set, a dataframe was created that grouped the Median Incomes based on the Zip_Code.  A third column, Abr_Zip, was created that extracted the first three digits from the Zip Code column.  The income_by_zip table, with three columns - Abr_Zip, Zip_Code, Median_Income - was loaded into the ZipCodes database.

    -Lending Club Data:  The Source data had only the first 3 numbers of the zip code.   A table, loan_data, grouped the numeric variables based on the abbreviated zip code.  (The abbreviated zip code of this table, zip_codes, serves as the primary key and is a foreign key in the other tables for this database).  The table has 9 columns: zip_code (pK), loan_amount, funded_amnt, funded_amnt_inv, term, int_rate, installment, annual_inc, dti.
    
    Another table kept the non numeric columns along with the abbreviated zip code.  This table, loan_information, has 11 columns: zip_code, funded_amnt_inv, sub_grade, home_ownership, emp_title, emp_length, issue_d, loan_status, pymnt_plan, purpose, addr_state.

    More information about the database can be found in Entity Relationship Diagram.png and Database Documentation.pdf
=======
We cleaned the data from each source using Jupyter Notebook, Pandas,and pgAdmin 4. Finally, we loaded the clean data in to Relational database with four tables. These tables are home_values, income_by_zip, loan_info(numeric aggregates), and loan_information(varchars).
>>>>>>> 31a8b8e1a9b665ec1d616432a6d5eb05c444d4e5
