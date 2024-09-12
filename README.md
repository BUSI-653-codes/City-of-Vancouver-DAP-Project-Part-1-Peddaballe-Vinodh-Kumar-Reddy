<h1 align="center">AWS Project Assignemnt</h1>
<p align="center">
Peddaballe Vinodh Kumar Reddy [2212316] <br>
University Canada West<br>
BUSI 653, Section 04<br>
Instructor: Mahmood Mortazavi Dehkordi<br>
Due Date: 17th September 2024<br>
</p>

___

# Project Description: Descriptive Analysis of Lost and Found Animal Records
In this assignment I will be describing the details of the City of Vancouver project mainly about the Data Analytic Platform (DAP) implementation (the datasets used and the various derivations and DAP design using the datasets I selected. For this assignment I used the website [City of Vancouver Open Data Portal](https://opendata.vancouver.ca/explore/dataset/animal-control-inventory-lost-and-found/export/?disjunctive.breed&disjunctive.color&sort=date&refine.date=2023) for getting some open source available datasets for various segments related to the Vancouver City operations.

## Project Title: Understanding Yearly Lost and Found Animal Patterns
The primary need of this project is to conduct a descriptive analysis of the yearly trends in lost and found animals based on the datasets taken from [City of Vancouver Open Data Portal](https://opendata.vancouver.ca/explore/dataset/animal-control-inventory-lost-and-found/export/?disjunctive.breed&disjunctive.color&sort=date&refine.date=2023). The goal is to identify the percentage of animals matched (found) and lost over time, which can help inform operational strategies for animal control services, improve response times, and increase the likelihood of reuniting lost animals with their owners.
## Project Objective:
* Pets have become a major part of our lives.
* I decided this will be my dataset to get information related to lost and found cases related to pets in city of Vancouver.
* For the DAP design there are close to 17 steps. Am going to define and describe all these steps below.
## Datasets
* There are two datasets wi=hich i will be using here.
* The first dataset is **"Found Inventory Dataset"**, it contains information on animals found, with columns such as:
  * SNO: Serial Number
  * Breed: Animal breed
  * Color: Color description
  * Date: Date when the animal was found
  * Name: Name of the animal
  * Sex: Animal's sex
  * State: Status (Yes indicating matched or found)
  * [2024_animal_control_Found_inventory.xlsx](https://github.com/user-attachments/files/16974871/2024_animal_control_Found_inventory.xlsx) contains the information of this match found dataset.
* The second datset is **"Lost and Found Inventory Dataset"**, it Contains details on lost animals, with similar columns, including:
  * SNO: Serial Number
  * Breed: Animal breed
  * Color: Color description
  * Date: Date of the record
  * Name: Name of the animal
  * Sex: Animal's sex
  * State: Lost or Found status
  * [2024_animal_control_inventory_lost_and_found.xlsx](https://github.com/user-attachments/files/16974850/2024_animal_control_inventory_lost_and_found.xlsx) contains the information of this lost and found inventory dataset.
* Using both these datasets I will be planning my DAP for City of Vancouver.
## Methodology:
* The process of DAP designing and implementation is complex.
* This involves close to 17 different steps. I will be explaining on these steps in detail below:
### Step 1 - Data Analytical Question Formulation
* Data or Datasets are very important when we are going to analyse something. Similarly for me to implement DAP I need some datasets and metrics to calculate.
* As explained above I have the Animal Control Inventory Lost & Found dataset, using this am going to design my DAP. The first step is to carefully select all the relevant metrics.
* Below displayed are a few sample metrics I selected:
![step001](https://github.com/user-attachments/assets/496f5579-6aed-48a2-a71e-5b83cb3c331e)
*  From this list I am going to select the descriptive metric “What is the match rate of Pet Inquiries?” analysis.
*  By doing this we can understand the total number of pet inquiries done, the number of match found inquiries, the number of inquiries still pending , and also the percentage of matched inquiries to that of total inquiries.
### Step 2 - Data Discovery
* This is the dataset I gathered pertaining to pet-related questions. The breed, color, name, gender, date of inquiry, status, and other details about pets that have been reported missing or found are all included in this dataset.
* I also divided this into two, just like I explained int he Datasets section prior.
  * [2024_animal_control_Found_inventory.xlsx](https://github.com/user-attachments/files/16974871/2024_animal_control_Found_inventory.xlsx) contains the information of this match found dataset.
  * [2024_animal_control_inventory_lost_and_found.xlsx](https://github.com/user-attachments/files/16974850/2024_animal_control_inventory_lost_and_found.xlsx) contains the information of this lost and found inventory dataset.
### Step 3 - Data Storage Design
* This phase is the backbone of the data analytic platform, where data is stored securely in the storage services provided by S3, redshift, Dynamo DB, etc, depending on the data structure. * Amazon S3 is the ideal storage service for storing large volumes of data by providing availability, durability, and scalability, and all these features make it a preferred choice.
* I have utilized S3 Simple storage services for storing our clean and robust data for analysis purposes, as S3 offers sufficient scalability and availability and is cost-effective.
* Below image displays my data storage design
![step003](https://github.com/user-attachments/assets/c5b75964-cc2f-48ca-920c-3c60ea400ce0)
### Step 4: Dataset Preparation
* The next step in the DAP process, that is the ‘Preparation’ stage.
* For this we are going to use ‘Microsoft Excel’ service.
* This is because we can not be sure the datasets we took is structured as per out need.
* To ensure this we need to do set of actions to ensure the data is in presentable format.
* Once the datasets are prepared then we can ensure that we can use them to further design and efficient DAP.
### Step 5: Data Ingestion & Step 6: Data Storage
* These are the steps where we creat appropriate Bucket structure mentioned in Step 3.
* Once the buckets & folders are created wecan them move to uploading the dataset files into AWS environment of S3 buckets.
* This will allow ease of access to data sets in AWS environment.
![image](https://github.com/user-attachments/assets/4602b53b-ee88-475d-a77f-3e830077962b)
*The above image display the details of “Storage” & "Ingestion" for “**Pet Inquiries**” of "***Lost and Found Inventory Dataset***"using ‘AWS-S3’
![image](https://github.com/user-attachments/assets/bc5aa6bf-8f6c-481a-a63e-4c501c3f224f)
*The above image display the details of “Storage” & "Ingestion" for “**Matched Inquiries**” of "***Found Inventory Dataset***"using ‘AWS-S3’
### Step 7: Data Pipeline Design 
* The datasets we need are now available in the AWS environment.
* The ETL pipeline design can now be started.
* We are able to define the precise data flow, starting from the raw datasets' input and ending with the reports or final outcomes.
* The ETL pipeline implementation's algorithm is the sole thing involved in this stage. This will provide a visual depiction of how data moves through the ETL pipeline to produce the required outputs.
![appx004](https://github.com/user-attachments/assets/0f36382f-7be8-4005-927a-697802f6ccfd)
* The above image display the details of “Pets Lost & Found” ETL process.
### Steps 8 & 9: Data Cleaning & Data Structuring
* Data cleaning involved converting the columns into desired schema format and ensuring consistency between the two datasets.
* We also need to ensure the Missing or incomplete records by reviewing the datasets for accuracy of analysis.
* For this we are goign to use the **"AWS DataBrew"** service.
* AWS-DataBrew helps in formatting, handlng missing values, schema changes and other data cleaning and structuring tasks.
 ![image](https://github.com/user-attachments/assets/95ecfd16-db46-4427-893d-bb64ed76507a)
* The above image display the details of “Schema Information” for “**Found Inventory Dataset**” using ‘AWS-DataBrew’.
![image](https://github.com/user-attachments/assets/09b68971-8a03-45b0-80a1-f5ce49e5812f)
Note: The above image display the details of “Schema Information” for “**Matched Inquiries Dataset**” using ‘AWS-DataBrew’.
### Step 10: Data Pipeline Implementation 
* We can begin putting the ETL pipelines created in "Step 7" into practice after our datasets have been cleansed and organized.
* The "**AWS Glue**" service will be used for the ETL implementation.
* With the help of this service, we may transform operational data sources' structured data into the appropriate analytical data source for our purposes.
* We may provide the schema we want for our datasets, create an ETL job to carry out the entire design, and create an ETL pipeline diagram utilizing the components that "AWS Glue" offers.
* If necessary, we may even guarantee that the result of the ETL operation is stored in our "AWS-S3."
![figure 31](https://github.com/user-attachments/assets/a7283be8-16ce-48dd-bf2d-645f797a5b6b)
* The above image display the details of “ETL information” for my dataset using ‘AWS-Glue’.





