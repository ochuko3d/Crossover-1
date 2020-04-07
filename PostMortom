# PostMortem/Root Cause Analysis of the AES EDI jira AESEDI-53447 #1

## Date
4-07-2020

## Authors
*Ochuko Agbigbe*
* Senior Cloud Operations Engineer*

## Status
Complete, resolved

## Summary
The customer data was not sent from AES EDI. The investigation showed that 
the file with the data was sent, but it did not get processed due to an issue with the AES CIS service.

## Impact
486,000 records were affected and the EDI to CIS monitoring service too.

## Root Causes
While running the patch script a larger number of record files were sent in to which cause a disruption in the service resulting in customer data not been processed and it also affected EDI to CIS monitoring service working on the CIS side. The missed records were not discovered automatically. 

## Trigger
A large amount of customer data being sent..

## Resolution
Reloading the *AES CIS* monitoring service allowed us to spot the missed records that were not discovered automatically. 

## Detection
Our customer create this Jira to alert us on this failure. *Please refer to (AESEDI-53447)*


## Action Items
| Action Item | Type | Owner | Bug |
| ----------- | ---- | ----- | --- |
| Writing of monitoring policy to detect records missings | prevent | LMP | **DONE** |
| Monitor the data ingesters and processors (ETL) | prevent | LMP | (Jira Issue No: AESCIS-38263)**TODO** |

## Lessons Learned
Addition of more monitoring plugins and modules to watch this critical part of the infrastructure. 

## Timeline

04-07-2020 (*all times UTC*)

| Time  | Description |
| ----- | ----------- |
| 11:56 | Discovering of the missing files |
| 12:00 | Restarting of the AES CIS monitoring module |
| 12:15 | Starting of the data processing of the records files |
| 13:00 | Completion of the data processing of all the 486,000 records files |
