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
### Data Discovery


