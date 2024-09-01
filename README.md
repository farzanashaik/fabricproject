# fabricproject
                                Microsoft Fabric End to End Ecommerce Project

	
	This Ecommerce Project contains data files which replicates a transactional sales and returns of the ecommerce website. I have implemented a Fabric Lakehouse to which data is loaded incrementally on a daily basis. The data is loaded to Current folder and the Medallion Architecture implemented as Bronze ,Silver and Gold layers. The raw data with added current timestamps loaded in to Bronze tables by using Notebooks. And have practiced to load in to tables by using Dataflows but here in my there are less sources for data ingestion so I prefer to use Notebooks.

	
	The data is loaded in to Bronze tables and implemented Incremental logic based on the products which are returning. Created surrogate keys for the dimension tables to apply SCD type 2 tables. The fact table is created with all the required measures. The data of previous date is archived to Archive folder. Only fresh data ingested loaded to Current folder daily. I have used a Data Pipeline to execute the flow on the daily basis.

	The Semantic Model is implemented by creating Relationships between dimension and fact tables. After creating Semantic Model I have created a Automatic Report which shows the most Retuned products and the region from where these returns are processed. And after that I generated a detailed PowerBI report based on Automatic Report and published to the Dashboard. 
