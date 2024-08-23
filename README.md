<h2>
ABC AUTOMOBILE End to End Data Engineering Project
<h2>
<h4>
Business Description
<h4>
<p></p>ABC Automobile is a manufacturing company that sells all kinds of automobiles and lately they have been noticing that some areas are performing better than others. As of now, the company does not have any data tools that offer some transparency to the managers making this process quite tedious. After some deep evaluation and feasibility process, the managers at ABC Automobile decided to reach out to Prerana’s company to help them build a Data Driven solution which will help them understand sales trend and come up with better future strategies for sales growth.<p></p>
<img src="https://github.com/PreranaC96/Prerana_Data_engineering/blob/main/Problem%20statement.png"/>
<h4>
Business Solution
<h4>
<p></p>The company has decided to deliver a Sales Dashboard using Azure Cloud Technology. Prerana’s company has suggested Azure Synapse for data ingestion (from excel) and transformation and creating the dashboards on Power BI for better insights and self-service capabilities. ABC Automobile would like that the complete process can be automated using Azure Data Services, like extracting the data from SQL DB, ingesting it to ADLS Gen2 using Synapse Pipeline and then transform the data using synapse spark notebooks, creating views on top of the transformed dataset to feed it to Power BI and later auto refresh of Power BI Dashboard is published on a workspace in the Power BI Service so that the managers can share and edit as they wish. The company together with Prerana’s company have gathered a list of parameters and Key performance indicators (KPIs) that they would like to be existent in the Power BI Dashboard.<p></p>
<h4>
Step- 1
<h4>
The whole process is divided into 5 parts - 
<h4>
INGEST
<h4>
<h4>
STORE
<h4>
<h4>
PROCESS
<h4>
<h4>
MODEL
<h4>
<h4>
SERVE
<h4>
<img src="https://github.com/PreranaC96/Prerana_Data_engineering/blob/main/End%20to%20end.png"/>
<h4>
Step- 2: INGEST AND STORE
<h4>
<p></p>In the process of developing End to end pipeline we used Azure SQL DB as the Data Source and created Linked Service to Ingest the Data into Azure Synapse. Using a Copy Activity stored the data into Azue Data lake Storage Gen-2 in Raw- Parquet Format. Here we choose Parquet format because it is Culumnar Storage format.<p></p>
<img src="https://github.com/PreranaC96/Prerana_Data_engineering/blob/main/copy%20activity.png"/>
<h4>
Step- 3: PROCESS AND STORE
<h4>
<p></p>In this stage I used Apache Spark to form a Curated Notebook and created a clean data Model fro the Flat table data. I used a Star Schema for the modelling and UUID to form the primary keys. After that I stored the curated data in the Delta Lake to keep it's ACID properties intact.<p></p>
<img src="https://github.com/PreranaC96/Prerana_Data_engineering/blob/main/Star%20Schema%20notebook.png"/>
<h4>
Step- 4: MODEL AND SERVE
<h4>
<p></p>In the last stage I am using OPENROWSET to create Views in Synapse Serverless SQL and use the Curated data in PowerBi to deliver the Client A Power Bi dashboard.<p></p>
<img src="https://github.com/PreranaC96/Prerana_Data_engineering/blob/main/View%20Creation%20notebook.png"/>
<img src="https://github.com/PreranaC96/Prerana_Data_engineering/blob/main/View%20creation.png"/>
<h4>
Step- 5: Master PipeLine And Trigger
<h4>
<p></p>At the end I have installed a trigger with the Master Pipeline which will Automatically Refresh the data Everyday at a perticular time.<p></p>
<img src="https://github.com/PreranaC96/Prerana_Data_engineering/blob/main/Master%20pipeline.png"/>
<img src="https://github.com/PreranaC96/Prerana_Data_engineering/blob/main/Trigger.png"/>
<h4>
Step- 5: POWERBI DASHBOARD
<h4>
<p></p>As per the Client requirement I delivered a PowerBi Dashboard and Client was very happy with the End Product and all the Delivary conditions were meet.<p></p>
<h5>Page 1</h5>
<img src="https://github.com/PreranaC96/Prerana_Data_engineering/blob/main/PowerBI_DE_1.png"/>
<h5>Page 2</h5>
<img src="https://github.com/PreranaC96/Prerana_Data_engineering/blob/main/PowerBI_DE_2.png"/>
<h5>Page 3</h5>
<img src="https://github.com/PreranaC96/Prerana_Data_engineering/blob/main/PowerBI_DE_3.png"/>
