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
  
### Select your Subscription, Resource Group, and Azure Reqion

### Select the Consumption Plan

### Select Create

  
  <img width="746" alt="LogicApp Creation" src="https://github.com/ANFTechTeam/Snapshot-Scheduler/assets/63759009/ea18f713-78ec-4f6f-bae5-89636ad62758">


### 

## Open the Logic App and set the System Assigned Idenity for the Security

<img width="1701" alt="System Assigned Identity" src="https://github.com/ANFTechTeam/Snapshot-Scheduler/assets/63759009/ea44821c-3a8a-4ac7-8e58-de539c7c9ca3">


### Assign an Azure RBAC utilizing the system assigned managed Identity to the ANF Resource at either the ANF Account or Capacity Pool Resource Level

<img width="1200" alt="Azure RBAC for Logic App" src="https://github.com/ANFTechTeam/Snapshot-Scheduler/assets/63759009/ee1ac3a4-ed2a-46be-9a45-0c4e864f83c6">

### 
### 

## Replace the code from the Logic app code view, section with the code in github (https://github.com/ANFTechTeam/Snapshot-Scheduler/SnapshotCode.git)

<img width="1331" alt="Replace Code fromGithub" src="https://github.com/ANFTechTeam/Snapshot-Scheduler/assets/63759009/31bf59e9-50ae-4dab-8788-22222224549c">


###
### 

## Lastly Open the Designer view in the Logic App and set the Retention Period, Capacity Pool

<img width="1583" alt="Set Retention and Capacity Pool" src="https://github.com/ANFTechTeam/Snapshot-Scheduler/assets/63759009/8bbf69a2-0ba8-4c92-920b-c5b976f9669a">


### 

## Run a manual Test to ensure all is working correctly
   


 
