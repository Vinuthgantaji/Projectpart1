<h1 align="center">Vinuth Project 1</h1>

___

# Project Description
In this assignment we will be discussing regrading the Housing and comes the part where we earn or establish a business for our living sustenance so we wanted to check on the details related to business licenses and get some inputs from it. I got my datasets from website [City of Vancouver Open Data Portal](https://opendata.vancouver.ca/explore/dataset/business-licences-2013-to-2024/information/?disjunctive.status)
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
* Data cleaning involved converting the columns into desired schema format and ensuring consistency between the two datasets.
* We also need to ensure the Missing or incomplete records by reviewing the datasets for accuracy of analysis.
* For this we are going to use the **"AWS DataBrew"** service.
* AWS-DataBrew helps in formatting, handling missing values, schema changes and other data cleaning and structuring tasks.<br>
* The above image display the details of “Schema Information” for “**Issued Dataset**” using ‘AWS-DataBrew’.<br>
### Step 10: Data Pipeline Implementation 
* We can begin putting the ETL pipelines created in "Step 7" into practice after our datasets have been cleansed and organized.
* The "**AWS Glue**" service will be used for the ETL implementation.
* With the help of this service, we may transform operational data sources' structured data into the appropriate analytical data source for our purposes.
* We may provide the schema we want for our datasets, create an ETL job to carry out the entire design, and create an ETL pipeline diagram utilizing the components that "AWS Glue" offers.
* If necessary, we may even guarantee that the result of the ETL operation is stored in our "AWS-S3."<br>
* The above image display the details of “ETL information” for my dataset using ‘AWS-Glue’.
### Step 11: Data Analysis 
* The analytical datasets for the operational datasets we utilized are now available.
* The structural datasets produced by the ETL pipeline are now available for use in the analysis.
* On the basis of the ETL outputs, we can even build a query service using the "**AWS-Athena**" service.
* We may build tables with this service, and then use straightforward SQL queries to get the necessary data from the tables.<br>
* The above image display the details of “Table” for my dataset using ‘AWS-Athena’.
* Once the results are generated based on our query we can use the resultant data by downloading it as a **".csv"** file.
### Step 12: Data Visualization 
* In this step I used "Microsoft Excel" to create reports of the **".csv"** file downloaded from AWS-Athena in "Step 11".
* My resultant reports were generated as below:<br>
