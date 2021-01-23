*NOTE:* This file is a template that you can use to create the README for your project. The *TODO* comments below will highlight the information you should be sure to include.\
![YouTube Video Views](https://img.shields.io/youtube/views/liJVSwOiiwg?style=social&color=red) -> badges of my screencast published on youtube \
![GitHub Repo stars](https://img.shields.io/github/stars/Daniel-car1/nd00333_AZMLND_C2-master?style=social) \
![GitHub all releases](https://img.shields.io/github/downloads/Daniel-car1/nd00333_AZMLND_C2-master/total?style=flat-square)
![GitHub commit activity](https://img.shields.io/github/commit-activity/m/Daniel-car1/nd00333_AZMLND_C2-master?style=flat-square)


# Operationalizing Machine Learning

*TODO:* Write an overview to your project.\
This project was all about investigating the [Bank Marketing dataset](https://automlsamplenotebookdata.blob.core.windows.net/automl-sample-notebook-data/bankmarketing_train.csv) with cloud-based Machine Learning methods using the Microsoft Azure ML studio and the Python SDK with the focus on deploying an Auto ML model, consuming the REST endpoint and using pipeline automation to launch the model automated into production.


## Architectural Diagram
*TODO*: Provide an architectual diagram of the project and give an introduction of each step.\
![Architectural Diagram](https://github.com/Daniel-car1/nd00333_AZMLND_C2-master/blob/master/starter_files/Images/project_flow/overview.png) \

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

*TODO* Remeber to provide screenshots of the `RunDetails` widget as well as a screenshot of the best model trained with it's parameters.\

## Screen Recording
*TODO* Provide a link to a screen recording of the project in action. Remember that the screencast should demonstrate:\

## Standout Suggestions
*TODO (Optional):* This is where you can provide information about any standout suggestions that you have attempted.\

## Sources
[Udacity - Machine Learning Engineer for Microsoft Azure](https://www.udacity.com/course/machine-learning-engineer-for-microsoft-azure-nanodegree--nd00333)\
[Azure Machine Learning documentation](https://docs.microsoft.com/en-us/azure/machine-learning/)

