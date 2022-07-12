# SLA-BREACHING
I am going to talk about  about the Service Level Aggrement. .
Breach of SLAs can be hazardous to a company's sustainability because most businesses give up control of their technology and data to third party suppliers to increase agility and cost effectiveness. Poor service performance or delayed product delivery are both examples of SLA breaches.

# An SLA breach is what?
An SLA is a written agreement between a company and a client that specifies services and their expected performance, according to the ISO/IEC 20000-10:2018 standard. Here, the company serves as a provider, and the SLA is typically a clause in a contract for the delivery of services.

#Has a SLA been violated? When do we know there has been a breach of a SLA?
You must first read the small print in contracts. In order for the metrics to be measured on a single platform, some providers will only accept a SLA breach if it is reported to them and explicitly recorded on their service management system.

Additionally, it is typically the customer's responsibility to demonstrate that the SLA was indeed broken. A customer might need to employ their own monitoring system, for instance, to show that network latency was lower than the objective that had been provided.

It's the service provider organizationin the document processing industry using technologies such as OCR, PowerCapture, Doculator and WorldObjects. It's my project so I can not revel the company name 
SLA breaches are very common issue faced by customer facing organizations that provide product and services. To minimize the SLA breaches, it is important to identify
the factors affecting the breaches, using the attributes of the documents, customers, time of document processing, etc.
The goal of the project is to build machine learning model to predict the SLA breaches of the documents and the factors affecting the breaches in the SLA
 Data set contains 7 tables having information of the documents processed for various
clients of different fields from November 2021 to January 2022
 Data cleaning and EDA was performed on jobs, document monitor, question table,
and the cleaned data was used to build various machine learning models to predict
breaches in SLA.

# Problems that has been occured are as follows:
# 1.SLA Breach
SLA breaches are very common issue faced  by customer facing organizations. The objective of the analysis is to predict the document with SLA breaches
# 2.Time of document processing
This refers to the time when a job is assigned to an agent till the entire document is processed within the given time frame.
# 3.Root cause analysis 
It’s important to identify the factors that affect the breaches in the SLA of the documents.
# 4.Cost
The processing time of document is reduced which will intern reduce the cost.
# 5.Usability
The usability of the model will depend on the accuracy percentage. Therefore, to increase the chances of accuracy we are implementing 5 Models. 
# 6.Predicting the SLA breaches:
The important factors that influence the SLA breaches can be used to predict the high-risk document that are likely to have breaches.

# DATA PREPROCESSING
1.Establishing Connection with AZURE
Using Azure Data Studio, a connection was established with the database server to access the data. This data was then saved in csv formatand then used for the project.
2. Removing Null Values
Replacement of the null values with mean or median values in those columns. Furthermore, columns with higher null values were dropped.
3.Creating Dummy Variables
After careful consideration, the significant categorical values were ruled, and new dummy variables were created to be used in the models.
4.Number Formatting
Inappropriate data formats were handled and replaced with there corresponding values.

# EXPLORATORY DATA ANALYSIS
Missing values Analysis:
The DocumentMonitor table contains 38,831 rows and 20 columns. SLAMoment variable had 1% of its values missing and ErroredText variable had 99% missing values. SuggestedDocumentClass had missing values, if they were multiple document classes present in the uploaded document.
![image](https://user-images.githubusercontent.com/81670865/178589021-61c9572b-afea-4436-af1a-752ee0e30905.png)

Job Table:
The Job table has 3,75,218 rows and 20 columns. In total, 9 columns have missing values. FieldUUID, FieldName, FieldDataType Text, FieldLabel have 45% missing values. FeatureName, FeatureUUID, FeatureName and ParentjobId have 30% missing values. FinishedAt has around 20% missing values.
![image](https://user-images.githubusercontent.com/81670865/178589216-17c474ff-90c0-4cbd-85c4-ae3747ad99ea.png)

# EDA:
Correlation matrix of variables
The dependent variable SLA breach does not have very high correlation with any independent variable
However, SLA breach has the highest correlation with Entity 2 of 0.3, and ‘Page Feature Detection - Topdown’ question of 0.18
SLA breach is negatively correlated with ‘Entity 2’ and ‘Document Class’ with values -0.26 and -0.23 respectively
This indicates that SLA breach is less with documents from ‘Entity 1’ and in documents having multiple classes
Requested Human Revision is highly negatively correlated with ‘Entity 3’ indicating that ‘Entity 3’ requests of fewer number of revisions in the document
The variables ‘Number of pages’ is highly correlated with the number of questions, i.e., documents with higher number of pages have higher number of questions asked
![image](https://user-images.githubusercontent.com/81670865/178589411-9f5b4557-2bff-4dcc-b290-da9eb4a477c5.png)

![image](https://user-images.githubusercontent.com/81670865/178589645-3c95c2f1-19da-4597-b89d-892f8f3b1ba7.png)

![image](https://user-images.githubusercontent.com/81670865/178589557-f67200ae-3d21-4a01-a538-5311ca362748.png)
![image](https://user-images.githubusercontent.com/81670865/178589724-d655f574-1f43-446a-9fae-34718991bad4.png)
![image](https://user-images.githubusercontent.com/81670865/178589754-b3fed1ff-35a4-41a3-bc0e-e759b13f4307.png)
![image](https://user-images.githubusercontent.com/81670865/178589774-c90f1a0c-fa1f-4ca3-a43f-db344bee3966.png)
![image](https://user-images.githubusercontent.com/81670865/178589816-001b72ca-f0ed-4f60-b716-354c730327db.png)
![image](https://user-images.githubusercontent.com/81670865/178589860-38afb4f9-80bd-428c-98f7-1a8d6fe81101.png)

Conclusion:
1. Out of the five ML models built, Random Forest was the best model for predicting SLA violations with an accuracy of ~91%
2.The number and types of questions asked are the important factors that affect SLA breach
3.Documents with ‘Page feature detection – Poised’, ‘Page feature detection - top down’ and ‘extract field values’ questions are more likely to have SLA breach
4.Further efforts can be put in to optimize the model, and reduce the number of false negatives

# I'll update these once I've finished these projects, on which I'm still working.








