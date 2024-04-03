### Sprint 3 overview 

During this sprint you are diving into transaction data. You are working at the behest of the Quay Bank Markets and Finance team who want to use data analysis techniques to get a better handle on two operational risks : Fraud and Liquidity.
In order to add value to the team you are bringing modelling, visualisation, observation, and critical thinking skills together to answer speculative questions. 
Everything you work on during this sprint has to be documented because colleagues in other teams will use it when the Bank returns to these priorities another time. For this reason you should make sure your notebooks/ workbooks are well organised and clearly annotated, your assembled written reports are clean and concise. 

- you will start the sprint by taking a closer look at the Quay bank transactions
- Wednesday of week 1 is planned as a mop-up day; a chance to work again on anything from an earlier sprint.  
- Before or after the mop up, you will jump into [time series analysis and forecasting](https://github.com/siandav/lbg_incubation_delegates/blob/main/Sprint_3_prevent_forecast/Sprint%203%20-%20Time%20Series%20Analysis%20%26%20Forecasting%20Transactions.pdf) with the bank transactions, extracting your data set using SQL and using the data and time series techniques to answer questions about the transaction trends
- before the end of the sprint it is hoped you can [deploy your data set and models to the google cloud platform](https://github.com/siandav/lbg_incubation_delegates/blob/main/Sprint_3_prevent_forecast/Sprint%203%20-%20Forecast%20and%20Fraud%20deploy%20to%20GCP.pdf)
- At the end of the sprint (Friday, 2pm) Dylan and Yobi will host a retro and sprint post mortem with you 

## Data Source for this sprint 

You will find the Quay_Banking database you need for this sprint on your LOD machine, on the SQL Server (2022 Express) instance. 
You can access the database through SQL Server Management Studio (SSMS) by launching SSMS19.1 from the desktop and connect to the server using the default credentials

### Useful links for preparing the data:
- Working with transaction data means theres too many rows and you have to aggregate up - in SQL the clause we use is [GROUP BY](https://www.w3schools.com/mysql/mysql_groupby.asp) and in Python its [groupby](https://medium.com/nerd-for-tech/grouping-and-sampling-time-series-data-2bafe98302ab)
- Managing and manipulating dates can be tricky - in SQL we use [date functions](https://www.w3schools.com/sql/sql_ref_sqlserver.asp), in Pandas its the [date time library and to_datetime functions](https://pandas.pydata.org/docs/user_guide/timeseries.html) 


### Useful links for time series forecasting: 
- [Heres a cheat sheet for time series](https://machinelearningmastery.com/time-series-forecasting-methods-in-python-cheat-sheet/)
-  A superb [kaggle guide to time series](https://www.kaggle.com/code/prashant111/complete-guide-on-time-series-analysis-in-python)
-  If using ARIMA, the [stats model library documentation](https://www.statsmodels.org/stable/generated/statsmodels.tsa.arima.model.ARIMA.html#statsmodels.tsa.arima.model.ARIMA) is useful to have on hand and heres a complementary [gentle intro to Arima](https://www.kdnuggets.com/2023/08/times-series-analysis-arima-models-python.html)
-  If using Prophet, the [documentation](https://prophet.readthedocs.io/en/latest/) is useful to have on hand and heres a [quickstart guide direct from Meta](https://facebook.github.io/prophet/docs/quick_start.html#python-api) 

### Useful links for GCP Big Query ML 
- If your source data is not pre aggregated, you should first upload the file(s) to a [storage bucket](https://cloud.google.com/storage/docs/uploading-objects), then connect to that [bucket from Big Query](https://cloud.google.com/bigquery?hl=en#transfer-data-into-bigquery) as the data source, creating an [aggregated table](https://cloud.google.com/bigquery/docs/tables)  in Big Query
- An [Arima Plus model](https://cloud.google.com/bigquery/docs/reference/standard-sql/bigqueryml-syntax-create-time-series) can be created directly in Big Query, with or without Auto Arima functionality (which does some of the parameter tuning for you)
- Evaluation, Forecasting of your model in Big Query ML will be done using pre defined functions and you should search the [documentation](https://cloud.google.com/bigquery/docs/reference/standard-sql/) for key words like 'arima', 'forecast'
- [Inference](https://cloud.google.com/bigquery/docs/inference-overview) can be made using Big Query ML

### Useful links for GCP Vertex AI (optional) 
- Importing an [existing Python model to GCP Vertex AI](https://cloud.google.com/vertex-ai/docs/model-registry/import-model) in a jupyter notebook file can be achieved using the GUI or Cloud Shell, adding it to the GCP model registry
- Once your custom model is up on Vertex AI, you need to deploy the [model](https://cloud.google.com/vertex-ai/docs/predictions/overview#model_deployment) and follow the appropriate pipeline for this type of model to [get your predictions](https://cloud.google.com/vertex-ai/docs/tabular-data/forecasting/get-predictions)
- Heres a [time series / Vertex AI lab](https://codelabs.developers.google.com/codelabs/time-series-forecasting-with-cloud-ai-platform#0) you may find useful
- AutoML on Vertex AI for time series is shown [here](cloud.google.com/vertex-ai/docs/tabular-data/forecasting/overview)
- Theres a short [video tutorial](youtube.com/watch?v=5-qjRpjdE5s) showing something similar on youtube
- Another [youtube video about forecasting models with VertexAI](https://www.youtube.com/watch?v=5-qjRpjdE5s&list=PLIivdWyY5sqJ1YuMdGjRwJ3fFYZ_vWQ62&index=7) 

### Internal note : Mop-up 
A theoretical space was allocated during this sprint for Mop-Up on 10/4, you can review, iterate and improve upon any deliverables you have produced in Sprints 1 & 2 during this time. This is a great opportunity for you to apply an agile mindset to your work and achieve soft skills S1, S2, S5.  

Steps of a mop-up : 
- review any deliverable you developed earlier 
- request feedback from a peer/ instructor or line manager OR give the work a critical review yourself 
- note down a minimum of 2 and maximum of 5 improvements you could feasibly make inside a day 
- prioritise the identified improvements, considering business impact (or applying a MOSCOW methodology) 
- save a version 2 of your deliverable, before working through the improvements you have identified
- give yourself a hard cut off deadline (eg 4pm), so this work doesnt take over the sprint
- update any related documentation or note the dependencies 

