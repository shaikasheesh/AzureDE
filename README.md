# AzureDE Project README
Here is the Crisp detail on the project:

1) Raw Data is stored on the On-premise SQL Server

2) It is copied to Bronze Container using Azure Data Factory copy data activity

3) The idea behind Bronze Silver & Gold is

     1) Bronze to have a exact copy of raw data as it is present on SQL server

     2) Silver to have level 1 transformation data

     3) Gold to have Level 2 transformation data

4) These transformations are done using Databricks & spark functionality

5) Once have the data ready in gold container, we will load it into Synapse Analytics Serverless SQL

6) Using Power BI desktop we can connect to this Azure Synapse SQL and load the data and build visualizations on top it.

7) In real time, if any data is updated/modified onto the premise server, it should reflect on the BI reporting. so we are automating the pipeline trigger schedule which does the ETL tasks and update the reports in real time

![image](https://github.com/shaikasheesh/AzureDE/assets/63601317/3f6af4a5-8c33-4986-be54-dd061fd1df22)

