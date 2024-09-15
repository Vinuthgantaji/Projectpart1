<h1 align="center">Vinuth Project 1</h1>

___

# Project Description
In this assignment we will be discussing regrading the Business License and comes the part where we earn or establish a business for our living sustenance so we wanted to check on the details related to business licenses and get some inputs from it. I got my datasets from website [City of Vancouver Open Data Portal](https://opendata.vancouver.ca/explore/dataset/business-licences-2013-to-2024/information/?disjunctive.status)
## Project Title: Understanding Business License Information
The primary goal here is to conduct a descriptive analysis of the yearly trends in business License based on the datasets taken from [City of Vancouver Open Data Portal](City of Vancouver Open Data Portal](https://opendata.vancouver.ca/explore/dataset/business-licences-2013-to-2024/information/?disjunctive.status)). The goal is to identify the percentage of business Licenses over time, which can help inform operational strategies for this license services, improve response times, and increase the licenses for their respective businesses.
## Project Objective:
* Business Licenses have become crucial part of our lives.
* I decided this will be my dataset to get information related to  business Licenses  in city of Vancouver.
* For the DAP design there are close to 13 steps. Am going to define and describe all these steps below.
There is one  datasets which i will be using here.
* The  dataset is **"Issued Business License"**, it contains information on issued business license, with columns such as:
  * [Cummulative-business-licences-2024.xlsx](https://github.com/user-attachments/files/17004732/Cummulative-business-licences-2024.xlsx)
## Methodology:
* The process of DAP designing and implementation is complex.
* This involves close to 13 different steps. I will be explaining on these steps in detail below:
### Step 1 - Data Analytical Question Formulation
* Data or Datasets are very important when we are going to analyse something. Similarly for me to implement DAP I need some datasets and metrics to calculate.
* As explained above I have the Business Licenses dataset, using this am going to design my DAP. The first step is to carefully select all the relevant metrics.
* Below displayed are a few sample metrics I selected: <br>
![step1 vinuth](https://github.com/user-attachments/assets/0ca43f38-6ef1-4c53-96fd-cc075cbf6ff4)
*  From this list I am going to select the descriptive metric “What is theissued rate of business licenses?” analysis.
*  By doing this we can understand the total number of licenses issued, the number of licenses still pending , and also the percentage of issued licenses to that of total licenses.
### Step 2 - Data Discovery
* This is the dataset I gathered pertaining to business license questions. The  type of license, validation of license, name, date of inquiry, status, and other details about the license that have been issued are all included in this dataset.
* * The  dataset is **"Issued Business License"**, it contains information on issued business license, with columns such as:
  * [Cummulative-business-licences-2024.xlsx](https://github.com/user-attachments/files/17004732/Cummulative-business-licences-2024.xlsx)
### Step 3 - Data Storage Design
* This stage, which forms the foundation of the data analytic platform, stores data safely in S3, Redshift, Dynamo DB, and other storage services, depending on the type of data.
* Due to its availability, scalability, and durability, Amazon S3 is the best storage solution for storing large amounts of data. These attributes make it a top option.
* Because S3 Simple storage services are affordable and offer adequate scalability and availability, I have used them to store our clean and reliable data for analysis.
### Step 4: Dataset Preparation
* The "Preparation" stage, which is the following step in the DAP process.  
* We'll use the "Microsoft Excel" service for this.
* This is because we are unable to confirm that the datasets we used have the structure we require.
* In order to make sure the data is presented in an appropriate manner, we must take a number of steps.
* After the datasets are ready, we can make sure we can utilise them to develop a more effective DAP.
### Step 5: Data Ingestion & Step 6: Data Storage
* In these steps, we establish the proper Bucket structure that was indicated in Step 3.
* After creating the buckets and folders, we can proceed to uploading the dataset files into the S3 buckets within the AWS environment.
* This will allow ease of access to data sets in AWS environment.<br>
![figure 09](https://github.com/user-attachments/assets/c49aab95-8267-4848-91a1-25ff69a574c7)
### Step 7: Data Pipeline Design 
* The datasets we need are now available in the AWS environment.
* The ETL pipeline design can now be started.
* We are able to define the precise data flow, starting from the raw datasets' input and ending with the reports or final outcomes.
* The ETL pipeline implementation's algorithm is the sole thing involved in this stage. This will provide a visual depiction of how data moves through the ETL pipeline to produce the required outputs.<br>
![appx002](https://github.com/user-attachments/assets/56c5ff34-f2e5-46d3-98e4-0d10439608fb)
* The above image display the details of “business license” ETL process.
* ### Steps 8 & 9: Data Cleaning & Data Structuring
* In order to ensure consistency between the two datasets, data cleaning involved converting the columns into the desired schema format.
* In order to verify that the analysis of the datasets is accurate, we also need to check for missing or incomplete records.
* We'll be using the **"AWS DataBrew"** service for this.
* Formatting, handling missing values, changing the schema, and other data cleaning and structuring tasks are made easier with the aid of AWS-DataBrew.<br>
![figure 23](https://github.com/user-attachments/assets/9030ef6c-7904-47aa-a4ff-ef407ea93a43)
* The "Schema Information" for the "**Issued Dataset**" is displayed in detail using "AWS-DataBrew" in the above image.(br>
### Step 10: Data Pipeline Implementation 
* After our datasets are cleaned and arranged, we can start implementing the ETL pipelines built in "Step 7".
* The ETL implementation will make use of the "**AWS Glue**" service.
* We can convert the structured data from operational data sources into the right analytical data source for our needs with the aid of this service.
* Using the components that "AWS Glue" offers, we can create an ETL job to complete the entire design, and we can supply the schema we want for our datasets. If required, we could even ensure that the ETL operation's output is kept in our "AWS-S3."
![figure 29](https://github.com/user-attachments/assets/6b80549c-910c-4d20-81a7-2815793b2863)
* The details of the "ETL information" for my dataset using "AWS-Glue" are displayed in the above image.
### Step 11: Data Analysis 
* We now have access to the analytical datasets for the operational datasets we used.
* The structural datasets generated by the ETL process can now be utilised in the examination.
* We can even use the "**AWS-Athena**" service to create a query service based on the ETL outputs.
* Using this service, we might create tables, and then use simple SQL queries to extract the relevant data from the tables.<br>
![figure 33](https://github.com/user-attachments/assets/f58d8ee6-872b-4ee6-8e60-6d0fcb3d2378)
* The "Table" details for my dataset using "AWS-Athena" are displayed in the above image.
* We can use the resultant data by downloading it as a **".csv"** file once the results are generated based on our query.
### Step 12: Data Visualization 
* I created reports using **".csv"** files that I had downloaded from AWS-Athena in "Step 11" using "Microsoft Excel" in this step.
* My final reports came out looking like this:<br>
![figure 37](https://github.com/user-attachments/assets/23bb0d92-0074-4889-9ae6-2a853fb36afb)
![figure 37-1](https://github.com/user-attachments/assets/9341b7b8-59ef-44f4-9d9e-b104fa1aa7f5)
### Step 13: Data Publishing
* This is the crucial step for populating the needed data for both internal and external use.
* We can use the ***Web servers*** and ***General Servers*** for publishing the results and making them available.
## Tools and Technologies:
* The list of Tools or technologies used are:
  * Microsoft Excel
  * AWS-S3
  * AWS-DataBrew
  * AWS-Glue
  * AWS-Athena
  * AWS-EC2
  * Microsoft Web Server IIS Role Installation
### Deliverables:
* A few crucial deliverables are:
  * **Data Analytic Platform:** Implemented on AWS, integrating data from the City of Vancouver's Business Licenses.
  * **Visualizations & Reports:** Generated reports and visualizations in Excel, illustrating trends, match rates, and other key findings.
  * **Data Storage & Pipeline:** Utilized AWS S3 for storage, AWS Glue for ETL processes, and AWS Athena for querying.
  * **Documentation:** Detailed steps and methodology used in the DAP design, including data preparation, cleaning, and monitoring.
  * **Recommendations:** Suggestions for improving public awareness, reporting processes, and resource allocation based on the analysis. <br>


