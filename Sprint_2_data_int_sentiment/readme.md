### Sprint Goals 
- This sprint is about analysing Branch performance for the Bank. The problem is that the data is held in silos and its impossible to build a full picture of how each branch is doing without first combing data from the CRM (customer relationship management) system with with the Bank accounts, loans, client info thats in the [operational database](https://github.com/siandav/lbg_incubation_delegates/blob/main/Sprint_2_data_int_sentiment/QB%20Database%20Technical%20Documentation.pdf). 
- This is where you will start - using SQL to [enhance an existing database and compile some useful branch focused analytics](https://github.com/siandav/lbg_incubation_delegates/blob/main/Sprint_2_data_int_sentiment/Sprint%202%20-%20CRM%20data%20integration%20and%20Branch%20Analysis.pdf) by adding in 3 CRM tables : [reviews](https://github.com/siandav/lbg_incubation_delegates/blob/main/Sprint_2_data_int_sentiment/CRM_2015_17_reviews.csv), [events](https://github.com/siandav/lbg_incubation_delegates/blob/main/Sprint_2_data_int_sentiment/CRM_Events.csv) and [call centre logs](https://github.com/siandav/lbg_incubation_delegates/blob/main/Sprint_2_data_int_sentiment/CRM_Call_Center_Logs.csv)
- You will continue using this database throughout the sprint, so once the CRM tables are embedded you should find a way to back up your database, so that you can restore it whenever you need it. You will use your database to dig into customer reviews in particular, [enhancing your branch analysis](https://github.com/siandav/lbg_incubation_delegates/blob/main/Sprint_2_data_int_sentiment/Sprint%202%20-%20NLP%20and%20Sentiment%20Analysis.pdf) applying NLP techniques, to provide usable insights around common topics of complaints, sentiment analysis per product, at a branch level and resting on naive bayes statistical theory. 
- In the previous sprint you had high level requirements to work towards. This time your audience is senior executives rather than the Marketing team so you should keep in mind what the priorities of that type of stakeholder are and tune the work you produce accordingly.
- At the end of this Sprint (Friday at 2pm) Dylan and Yobi will host a Sprint Round Table event with you, to give you a chance to reflect and share what you have discovered during the sprint. 

### Data Source for this sprint 

You will find the Quay_Banking database you need for this sprint on your LOD machine, on the SQL Server (2022 Express) instance. 
You can access the database through SQL Server Management Studio (SSMS) by launching SSMS19.1 from the desktop and connect to the server using the default credentials

### Useful links for SQL Server and database management in SSMS
- https://www.w3schools.com/sql/ 
- https://learn.microsoft.com/en-us/sql/ssms/sql-server-management-studio-ssms?view=sql-server-ver16
- https://www.geeksforgeeks.org/sql-constraints/
- https://learn.microsoft.com/en-us/sql/relational-databases/tables/create-foreign-key-relationships?view=sql-server-ver16

### Useful links for Sentiment Analysis: 
- https://www.analyticsvidhya.com/blog/2022/07/sentiment-analysis-using-python/
- https://www.datacamp.com/tutorial/text-analytics-beginners-nltk

### Useful Statistical articles 
- https://betterexplained.com/articles/an-intuitive-and-short-explanation-of-bayes-theorem/
- https://jakevdp.github.io/PythonDataScienceHandbook/05.05-naive-bayes.html
