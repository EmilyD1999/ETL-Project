# ETL-Project
                                                               Project overview

Through this ETL project out group primarily wanted to investigate the potential trends and variations of the crime rate throughout the UK, Canada and Australia. We wanted to be able to shape the data in such a way as to enrich people’s knowledge regarding crimes in both their home country and other countries throughout the world. Furthermore, if explored further the data we have extracted could reveal strategies to reduce crime in other cities by delving into the laws and regualtions of the country who has the least amount of crime. 

The data is located on the following websites: 
-	http://www.data.gov.au
-	http://www.ons/gov.uk
-	http://www150.statcan.gc.ca

What are the data set formats?
-	Web scraping (HTML)
-	API (JSON)
-	CSV

How will you get this data? (e.g. API, scraped data, download data)
-	Web scraping
-	API request
-	Downloading the .csv file
 
Our assumptions about the data: 
-	We assume the data is representative of the general population and is complete.
-	The data sets cover the crimes committed over a certain timeline in three different places in the world
-	The CSV data may be missing some details as it doesn’t go into great detail about the type of crime’s that have been committed.

Transforing and cleaing our data involved: 
-	Filtering 
-	Converting the English data to 100,000 to match corresponding data sets (Normalise)
-	Creating one data point for each month (no duplicate dates)
-	Removing text/number decoration
-	Grouping Australian data by month or, get total count for each month
-	Getting the amount of single offences and then finsing the count of these offences

Issues we encountered: 
-	Outliers
-	Null values
-	Large data sets 
-	Integration of variying data in different forms (this will be done through joins)
 
We applied these transformations through the following: 
-	Requests module to transform API (Request API to obtain web data).
-	HTML to transform scrapped data (bs4 to pass and transform data).
-	Pandas to transform CSV

Why did we apply these transformations?
- We applied these transformations to ensure our data would integrate smoothly with the different data sources.

What type of database did we use and why? 
-	We used a SQL Database due to the way it provided us with ease of access to the data we needed to analyse 

What are your expected tables / documents and relationships between tables / documents in your database?
-	Table for each country, combined table with rows(dates), columns(countries).

What are the potential limitations of our above proposed steps?
-	Data stored in different ways (Detailed vs Not detailed)
-	Difficult to determine what data needs to be pulled
-	Demographic difference between cities may influence the findings
-	2015–2019-time range

How can we control these potential issues?
-	Normalise data (percentage as opposed to total number)
-	Find most uniform statistics to use (i.e. number of crimes)
-	Break data down into basic forms without excessive formatting to better understand
