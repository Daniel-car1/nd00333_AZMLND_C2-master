![YouTube Video Views](https://img.shields.io/youtube/views/ntwpQAADKUk?style=social)       ![YouTube Video Likes](https://img.shields.io/youtube/likes/ntwpQAADKUk?style=social)  (Beta Version) \ 
![GitHub Repo stars](https://img.shields.io/github/stars/Daniel-car1/nd00333_AZMLND_C2-master?style=social) \
![GitHub language count](https://img.shields.io/github/languages/count/Daniel-car1/nd00333_AZMLND_C2-master) \
![GitHub commit activity](https://img.shields.io/github/commit-activity/m/Daniel-car1/nd00333_AZMLND_C2-master?style=flat-square)


# Operationalizing Machine Learning

This project was all about investigating the [Bank Marketing dataset](https://automlsamplenotebookdata.blob.core.windows.net/automl-sample-notebook-data/bankmarketing_train.csv) with cloud-based Machine Learning methods using the Microsoft Azure ML studio and the Python SDK with the focus on deploying an Auto ML model, consuming the REST endpoint and using pipeline automation to launch the model automated into production, automating the Machine Learning process to consume the endpoint from customers. \
A screencast [ML Engineer with Microsoft Azure - Udacity - Machine Learning Operations](https://www.youtube.com/watch?v=b_VmyyrZD40) was recorded, showing the key steps and the performance of the model, generated in this project.


## Architectural Diagram

![Architectural Diagram](https://github.com/Daniel-car1/nd00333_AZMLND_C2-master/blob/master/starter_files/Images/project_flow/overview.png) 

The provided architectural diagram of the project shows the main steps, to deploy and consume an endpoint of a Machine Learning model in the Azure cloud. \
Steps 1 to 5 are mainly done by using the Azure ML studio and the Terminal (GitBash) - like creating an Auto ML model, deploying the best generated model and consuming it's endpoint. While in step 6 the the best model was created, selected, published/deployed and consumed automatically - unsing the Python SDK and Jupiter Notebook - by running the steps in a pipeline, which enhances the performance of Machine Learning Engineers to work on new projects due to time savings caused of the automated generation and deployment workflow.  \
Each single step 1-6 has it's own work processes:


| 1. Authentication | 2. Auto ML model | 3. Deploy the best model | 4. Enable logging | 5. Consume model endpoints |
| --- | --- | --- | --- | --- |
| Create a compute principle. <br /> Enable security, and complete authentication. | Upload the dataset. <br /> Create an Auto ML run. | Select the best model. <br /> Enable Authentication. <br /> Deploy the model using ACI (Azure Container Instance) | Write and run code to enable Applicatin Insights | Display the model's API. <br /> Consume and benchmark the REST endpoint. |
| ![](https://github.com/Daniel-car1/nd00333_AZMLND_C2-master/blob/master/starter_files/Images/project_flow/Authentication.PNG) | ![](https://github.com/Daniel-car1/nd00333_AZMLND_C2-master/blob/master/starter_files/Images/project_flow/AutoMLmodel.PNG) | ![](https://github.com/Daniel-car1/nd00333_AZMLND_C2-master/blob/master/starter_files/Images/project_flow/deploy%20model.PNG) | ![](https://github.com/Daniel-car1/nd00333_AZMLND_C2-master/blob/master/starter_files/Images/project_flow/enable%20logging.PNG) | ![](https://github.com/Daniel-car1/nd00333_AZMLND_C2-master/blob/master/starter_files/Images/project_flow/consume%20endpoint.PNG) | \


| 6. Create and publish a pipeline |
| --- |
| Combine the steps above in a pipeline. |
| ![](https://github.com/Daniel-car1/nd00333_AZMLND_C2-master/blob/master/starter_files/Images/project_flow/create%20and%20publish%20a%20pipeline.png) |


## Key Steps
*TODO*: Write a short discription of the key steps. Remeber to include all the screencasts required to demonstrate key steps.\ 

**Authentication** provides access control of Service Principal for specific workspaces. \
In Microsoft Azure *Service Principals* are non-interactive accounts, their permissions are managed with Azure Active Directory. 
1. *Login* using the terminal (GitBash or Azure PowerShell)
2. Creating a Service Principal (SP). The permission is managed by the Acitve Directory (AD). <br/> The *objectId* is important to give that specific user the user role in the next step. <img src="https://github.com/Daniel-car1/nd00333_AZMLND_C2-master/blob/master/starter_files/Images/1_Authentication/3.PNG" height="80%" width="80%"> <br/>
3. Share the workspace. The user got the user role of an owner. <br/> (Note: Note: All steps were performeded in the provided VM, which causes an error due to nonexistent user rights.) <img src="https://github.com/Daniel-car1/nd00333_AZMLND_C2-master/blob/master/starter_files/Images/1_Authentication/4.PNG"> <br/>

<br/> <br/>

**Automated ML Experiment** generates the best model fitted to the database input. \
1. Upload the Bankmarketing dataset - a tabular dataset - to ML Studio, making it a available for ML projects. <br/> <img src="https://github.com/Daniel-car1/nd00333_AZMLND_C2-master/blob/master/starter_files/Images/2_Automated_ML_Experiment/1.PNG"> <br/>
2. Crate and run a Auto ML experiment using Classification. <br/> The completed Automated ML Run 1 (bank-automl > Run 1) took less than 22 minutes in total and generated a best model algorithm *VotingEnsemble* with an AUC_weighted of 0.94768.  <br/> <img src="https://github.com/Daniel-car1/nd00333_AZMLND_C2-master/blob/master/starter_files/Images/2_Automated_ML_Experiment/4.PNG"> <br/>
3. Select the best model, after the Auto ML run ins completed. <br/> Voting Ensemble was the last run (66) of the classification task. <br/> <img src="https://github.com/Daniel-car1/nd00333_AZMLND_C2-master/blob/master/starter_files/Images/2_Automated_ML_Experiment/7.PNG"> <br/>

<br/> <br/>

**Deploy the best model**.
1. Select *VotingEnsemble*
2. Deploy *VotingEnsemble* using Azure Container Instance (ACI) and enable Authentication. <br/> <img src="https://github.com/Daniel-car1/nd00333_AZMLND_C2-master/blob/master/starter_files/Images/3_Deploy_the_best_model/1.PNG"> <br/>

<br/> <br/>

**Enable Looging** <br/>
In the previous step, VotingEnsemble was deployed. To retrieve logs, Applicatin Insights has to be enabled. Which can be done in Azure Studio by setting a checkbox or using the Azure Python SDK.
1. Enable Application Insights says 'true'.  <br/> Consuming the [*Application Insights url*](https://github.com/Daniel-car1/nd00333_AZMLND_C2-master/blob/master/starter_files/Images/4_Enable_Application_Insights/3.PNG) leads to a statistical overview of *Failed requests*, *Server response time* and *Server requets* which can be can be evaluated in much more detail like Smart Detection, Live metrics, Failures, Performance, etc.  <br/> <img src="https://github.com/Daniel-car1/nd00333_AZMLND_C2-master/blob/master/starter_files/Images/4_Enable_Application_Insights/2.PNG"> <br/>
2. Retrieve the logs, like:  <br/>
    - Listing ip and port
    - Initializing logger
    - Swagger GET methods etc.
<br/> <img src="https://github.com/Daniel-car1/nd00333_AZMLND_C2-master/blob/master/starter_files/Images/4_Enable_Application_Insights/1.PNG"> <br/>

<br/> <br/>

**Swagger Documentation** <br/>
The in Azure deployed model provides a Swagger JSON file, which contains information about methods and the schema which has to be used to consume the REST endpoint of the ML model. Swagger provides a service called Swagger-UI which allows to explore the Swagger JSON file in a user friendly way. <br/> Therefore the latest Swagger-UI Docker image has to run, follow after:  
1. Download the swagger.json file from the endpoint section.
2. Interact with the swagger instance running with the documentation for the HTTP API of the model. Running on localhost.
3. Display the contents of the API for the model.  <br/> The terminals show the executed scripts, which make it possible to consume the downloaded in swagger.json file in the Swagger-UI. Interaction between a service and the deployed model is done via the REST API exchanging JSON documents. Here the API specification for the Azure Machine Learning service 'automl-bank-deploy' has version 1.0. The Schemes are presented in HTTPS and the API methods are GET (displays the health status of the API) and POST, the interaction method.
<br/> <img src="https://github.com/Daniel-car1/nd00333_AZMLND_C2-master/blob/master/starter_files/Images/5_Swagger_Documentaion/7.PNG"> <br/>
The POST requests expects a JSON object as payload for executing the real-time machine learning service.
<br/> <img src="https://github.com/Daniel-car1/nd00333_AZMLND_C2-master/blob/master/starter_files/Images/5_Swagger_Documentaion/2.PNG"> <br/>

<br/> <br/>

**Consume Model Endpoints** <br/>
In the previous step 'Swagger Documentation' the methods and payloads interacting with the deployed Auto ML model was progressed. Using these information, consumption of the model's REST endpoint, can be progressed.
1. Select the scoring uri (= REST endpoint) of the automl-bank-deploy model, this is the target of the POST request.
2. Because authentication is necessary and the model is deployed as a ACI, 'using key' is the authentication type. There fore select the Primary key.
3. Construct a JSON data object using the schema obtained before. Here two requestas of a very young (17 years old) and a very old (87 years old) person were produced.
4. POST request the JSON object.
5. Obtain the resonse JSON object. <br/>
      - {"result": ["no", "no]} 
      - Both requests were denied.
<br/> <img src="https://github.com/Daniel-car1/nd00333_AZMLND_C2-master/blob/master/starter_files/Images/6_Consume_Model_Endpoints_and_Benchmark/2.PNG"> <br/>

<br/> <br/>

**Benchmark Model Endpoints** using Apache bench, an open source benchmark tool for load-testing the deployed Machine Learning model. Load-testing a model is done by sending an amount of POST requests to the model's API and measure it's performance like, *failed requests*, *Time taken for tests*, etc. If a request failed because of a too long taken time for a test, the performance of the compute target may have to be increased. <br/>
The model successfully passed the benchmark test. <br/>
1. Update the benchmark script.
2. Run the scripts against the HTTP API using the authentication keys to retrieve performance results.


| Starting the benchmark script | Final logs | Statistics in detail |
| --- | --- | --- |
| Request and first responses. | Last response with code 200 OK and statisticas. | Details of the benchmark metrics. <br/> - Time taken for tests: 1.705 seconds <br/> - Complete requests: 10 <br/> - **Failed requests: 0** |
| ![](https://github.com/Daniel-car1/nd00333_AZMLND_C2-master/blob/master/starter_files/Images/6_Consume_Model_Endpoints_and_Benchmark/3.PNG) | ![](https://github.com/Daniel-car1/nd00333_AZMLND_C2-master/blob/master/starter_files/Images/6_Consume_Model_Endpoints_and_Benchmark/4.PNG) | ![](https://github.com/Daniel-car1/nd00333_AZMLND_C2-master/blob/master/starter_files/Images/6_Consume_Model_Endpoints_and_Benchmark/5.PNG) | 

<br/> <br/>

**Create, Publish and Consume a Pipeline** using Jupyter Notebook. \ 
Automating the ML workflow to create, publish and consume a Machine Learning model using pipeline mechanism in Azure ML leads to the following: <br/>
1. Pipeline has been created.
<br/> <img src="https://github.com/Daniel-car1/nd00333_AZMLND_C2-master/blob/master/starter_files/Images/7_Create_Publish_Consume_Pipeline/6.PNG"> <br/>
2. Pipeline Endpoint has been created.
<br/> <img src="https://github.com/Daniel-car1/nd00333_AZMLND_C2-master/blob/master/starter_files/Images/7_Create_Publish_Consume_Pipeline/10.PNG"> <br/>
Regarding the Pipeline endpoint, the last run status is finished and the status is active, that means the endpoint is ready for cosumption.
<br/> <img src="https://github.com/Daniel-car1/nd00333_AZMLND_C2-master/blob/master/starter_files/Images/7_Create_Publish_Consume_Pipeline/active_pipeline.PNG"> <br/>
3. The Bankmarketing dataset with the AutoML module. 
<br/> <img src="https://github.com/Daniel-car1/nd00333_AZMLND_C2-master/blob/master/starter_files/Images/7_Create_Publish_Consume_Pipeline/1.PNG"> <br/>
4. In the 'Published Pipeline overview' the REST endpoint is shown and the status of ACTIVE.
<br/> <img src="https://github.com/Daniel-car1/nd00333_AZMLND_C2-master/blob/master/starter_files/Images/7_Create_Publish_Consume_Pipeline/3.PNG"> <br/>
5. Jupyter Notebook, shows the step runs using the 'Use RunDetailsWidget'.
<br/> <img src="https://github.com/Daniel-car1/nd00333_AZMLND_C2-master/blob/master/starter_files/Images/7_Create_Publish_Consume_Pipeline/4.PNG"> <br/>
<br/> <img src="https://github.com/Daniel-car1/nd00333_AZMLND_C2-master/blob/master/starter_files/Images/7_Create_Publish_Consume_Pipeline/5.PNG"> <br/>
6. In ML stuido, the scheduled run is shown. The total run of the Jupyter Notebook took 1.5 hours.
<br/> <img src="https://github.com/Daniel-car1/nd00333_AZMLND_C2-master/blob/master/starter_files/Images/7_Create_Publish_Consume_Pipeline/10.PNG"> <br/>

<br/> 
The focus of that project was understanding the ML automation process using pipelines, with all additional tasks and steps.
<br/>

## Screen Recording
See the project in action on my youtube channel [ML Engineer with Microsoft Azure - Udacity - Machine Learning Operations](https://www.youtube.com/watch?v=b_VmyyrZD40) and don't forget to give me a like.

## Standout Suggestions
The optional items about load-testing the endpoint was done an documented detailed in the section *Benchmark Model Endpoints*.

## Future Improvements
- Expanding the script, using a Parallel Run Step in a pipeline.
- Test a local (Docker) container with a downloaded model.
- Export the best best model to ONNX.

## Sources
[Udacity - Machine Learning Engineer for Microsoft Azure](https://www.udacity.com/course/machine-learning-engineer-for-microsoft-azure-nanodegree--nd00333) <br/>
[Azure Machine Learning documentation](https://docs.microsoft.com/en-us/azure/machine-learning/) <br/>
[Authentication in MS Azure using SP ](https://docs.microsoft.com/en-us/powershell/azure/authenticate-azureps?view=azps-5.4.0) <br/>
[Azure machine Learning SDK - MLOps](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-create-machine-learning-pipelines) <br/>
[Swagger API Development](https://swagger.io/) <br/> 
[Apache HTTP server benchmarking tool](http://httpd.apache.org/docs/2.4/programs/ab.html) <br/>
[Jupyter Notebook](https://jupyter.org/)


