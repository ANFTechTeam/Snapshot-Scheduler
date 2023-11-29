# Snapshot-Scheduler
Schedule Snapshots at Frequency below Hourly



** **

## Description
# Snapshot-Scheduler

Utilizing an Azure Logic App, schedule ANF Snapshots at a frequency below hourly.  The Snapshot frequency is set within the Logic App (**default is 5 minutes**), suggested to not be lower than 3 minutes. Specify the number of Snapshots you want to maintain.  Lastly set the ANF Capacity Pool(s) that contains the volumes you want to Assign the Snapshot Schedule to.

Once set the Logic App will takeover the scheduling and rotation of the Snapshots at the frequency specified

** **
## Change Log
11/09/2023 - Initial Release

** **
## Prerequisites - One Time Setup

## Create the Logic App in the Azure Portal

### Go  https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FANFTechTeam%2FSnapshot-Scheduler%2Fmain%2Fdeploy-snapshot-scheduler.json
  
### Select your Subscription, Resource Group, and Azure Reqion

### Select the Consumption Plan

### Select Create

  
 <img width="746" alt="LogicApp Creation" src="https://github.com/ANFTechTeam/Snapshot-Scheduler/assets/63759009/0b435ff8-75c9-47f8-a773-e339c48a8e64">



### 

## Open the Logic App and set the System Assigned Idenity for the Security

<img width="1701" alt="System Assigned Identity" src="https://github.com/ANFTechTeam/Snapshot-Scheduler/assets/63759009/72daca10-166c-41ca-9749-a599d2fcc128">



### Assign an Azure RBAC utilizing the system assigned managed Identity to the ANF Resource at either the ANF Account or Capacity Pool Resource Level

<img width="1200" alt="Azure RBAC for Logic App" src="https://github.com/ANFTechTeam/Snapshot-Scheduler/assets/63759009/bd230feb-f99d-4c1a-a7bb-5aef825ee210">


### 
### 

## Replace the code from the Logic app code view, section with the code in github ( [SnapshotSchedulerCode] https://github.com/ANFTechTeam/Snapshot-Scheduler/blob/main/SnapshotCode.git )  

<img width="1331" alt="Replace Code fromGithub" src="https://github.com/ANFTechTeam/Snapshot-Scheduler/assets/63759009/aa989166-05e1-43d6-9ceb-6e7c5c4c957c">



###
### 

## Lastly Open the Designer view in the Logic App and set the Retention Period, Capacity Pool

<img width="1583" alt="Set Retention and Capacity Pool" src="https://github.com/ANFTechTeam/Snapshot-Scheduler/assets/63759009/8bbd871a-8091-46de-b9e3-680fc9948e83">



### 

## Run a manual Test to ensure all is working correctly
   


 
