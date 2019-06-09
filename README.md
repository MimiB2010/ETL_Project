ETL Project

For this project, our team extracted data from Lending Club, US Census, and Zillow. The Lending Club data was a SQLite file from [Kaggle.com](https://www.kaggle.com/wendykan/lending-club-loan-data#database.sqlite). The US Census and Zillow data were csv files obtained from [Kaggle.com](https://www.kaggle.com/goldenoakresearch/us-household-income-stats-geo-locations). and [Zillow.com](https://www.zillow.com/research/data/) respectively.

We cleaned the data from each source using Jupyter Notebook, Pandas,and pgAdmin 4. Finally, we loaded the clean data in to Relational database with four tables. These tables are home_values, income_by_zip, loan_info(numeric aggregates), and loan_information(varchars).
