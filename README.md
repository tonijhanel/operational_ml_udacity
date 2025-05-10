# Project: Operationalizing Machine Learning

## Project Summary:
This project aimed to develop a binary classification model to predict qualified leads for a bank marketing campaign focused on term deposit subscriptions. Utilizing the Bank Marketing dataset (comprising 10,000 customer records with features like age, employment, marital status, and education), the goal was to accurately classify whether a customer would subscribe ('yes' or 'no'). The project leveraged the Azure Machine Learning SDK and Studio, specifically employing Azure Automated Machine Learning Pipelines to efficiently identify and configure the optimal predictive model.

### Best Model Performance:
An Automated ML run, lasting 20 minutes, explored 15 different models. The best performing model identified was a VotingEnsemble, achieving a weighted Area Under the ROC Curve (AUC) of 0.94610.

### Potential Future Improvements:
**Two key areas for potential model improvement were identified:**
1.	**Addressing Data Imbalance:** The Bank Marketing dataset exhibits an imbalance, with only 11% of the target variable indicating a 'yes' subscription. Strategies to address this imbalance, such as oversampling the minority class or undersampling the majority class, could potentially lead to a more robust and better-performing model.

2.	**Increasing Automated ML Run Time:** The Automated ML process was limited to 20 minutes to manage computational costs. Extending the run time to 45 minutes or an hour could allow the system to explore a wider range of models and hyperparameter configurations, potentially leading to further improvements in model performance.

### Architectural Diagram:
![Architectural Diagram](images/archdiagram.png) Architectural Diagram

### Screencast

[Screen Cast](https://drive.google.com/file/d/19AehQU7S3-omNJG8SonqOZqBMhNxobq1/view?usp=sharing)

#### Step 1: Authentication

##### Create Service Principal
![RBAC command](images/auth_rbac.png) Create the Service Principal


##### Capture Object ID
![Show Client](images/show_client_id.png) Capture Object ID


##### Share Command
![Share command](images/rolecombined.png) Assign the role to the new Service Principal for the given Workspace, Resource Group and User

#### Step 2: Automated ML Experiment

##### Registered Dataset
![Bank Marketing Dataset](images/bankdataset.png) Bank Marketing Dataset

![Bank Marketing Dataset](images/bankdataset2.png) Bank Marketing Dataset Rows

##### AutoML Experiment

![Auto ML Pipeline Completed](images/pipelinecomplete.png) Auto ML Run Completed

![Auto ML Summary](images/pipelinesummary.png) Auto ML Run Summary

![Auto ML Best Model](images/automl_completed.png) Auto ML Best Run

#### Step 3: Deploy the Best Model
![Auto ML Best Model Summary](images/automl_bestmodel.png) Auto ML Best Run Summary

#### Step 4: Enable Logging

![log.py file](images/log_changes.png) Changes to log.py

![Logs](images/logsrun.png) Logs from running log.py

![App Insights Enabled](images/appinsights_truev2.png) Application Insights enabled on best run endpoint



#### Step 5: Swagger Documentation

![Swagger API Definition](images/swaggerdef1.png) Swagger API Definition for Best Model Endpoint

![Swagger API Definition _ Score](images/swaggerpost.png) Score method 

![Swagger Response ](images/endpointspy.png) Result of consuming the endpoint by running endpoint.py


#### Step 6: Consume Model Endpoints

![Swagger Response ](images/endpointspy.png) Result of consuming the endpoint by running endpoint.py

![Benchmark ](images/benchmark_page1.png) Output from Running Apache Benchmark - Page 1

![Benchmark ](images/benchmarkpage2.png) Output from Running Apache Benchmark - Page 2



#### Step 7: Create, Publish and Consume a Pipeline

![Notebook ](images/notebookautoml.png) Auto ML via SDK notebook

![Run Detail ](images/rundetail.png)  AutoML Run Details

![Pipeline Run in noteboook ](images/runidforpipelienendpoint.png)

![Endpoint Pipeline ](images/endpointpipeline.png) Submit Auto ML Pipeline via SDK

![Pipeline Active ](images/pipelinerestendpointstatus.png) Auto ML Pipeline Run

![Pipeline completed ](images/pipelineendpoint_completed.png) Auto ML Pipeline Completion

![Pipeline Active ](images/pinelineactive.png) Auto ML Pipeline Status


