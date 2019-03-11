# saReports_Azure
SSMS-based dashboards for Azure SQL database 

This set of SSMS-reports is developed as a free and customizable solution to monitor SQL Azure DB on ad-hoc basis.
It also can be useful for SQL developers and other who work with SQL server but has lack of SQL server knowledge.

There are two main reports :
1) Azure_Master
2) AzureDB_Main

Other reports depend on the main ones.

Azure_Master
This report should be invoked from master database and shows workload on all databases hosted on the server. 
Data shown is aggregated by 5 mins intervals.

AzureDB_Main
This report should be invoked from a user database and shows lots of db-related information.
Performance data is more granular but is hosted only for the last 1 hour.

Link:
https://sites.google.com/view/sareports/eng/azuredb
