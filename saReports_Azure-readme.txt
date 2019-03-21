[21 March 2019]
* Sessions :
	- added system sessions if they block user's ones
	- minor enhancements
* AzureDB_main :
	- fixed issue with data and tooltip text of "Blocked" column section "Connected"
	- added information about ad-hoc query plans with usecount=1 
* Fragmentation :
	- source query amended to show correct information about columnstore indexes

[20 March 2019]
* DBEvents : 
	- storage used is now shown in GBs 
	- minor formatting enhancements
* AzureDB_main :
	- sections "Tuning Actions" and "Tuning Settings" are combined into one "Automatic Tuning" with appropriate ToolTip text

[19 March 2019]
* AzureDB_main :
	- added "Tuning Actions" and "Tuning Settings" objects (analysis of sys.dm_db_tuning_recommendations and sys.database_automatic_tuning_options)

[18 March 2019]
* AzureDB_main :
	- amended built-in query dealing with db scoped configuration parameters
	- CPU/RAM/DataIO/LogWrites graphs can show more than last 1 hour of data if the following command is executed on the database
		ALTER DATABASE SCOPED CONFIGURATION SET GLOBAL_TEMPORARY_TABLE_AUTO_DROP = OFF
* DBPermissions : 
	- misc enhancements (sorting)

[14 March 2019]
* DBEvents : 
	- visual enhancements & formatting
	- queries rewritten using sp_executesql
	- new pie-chart is added
* Azure_Master :
	- added "Other Events" column with amount of events happened today (+tooltip text)  except failed connections
* ObjectStats : 
	- added highlighting for modrecs>20% & misc formatting

[13 March 2019]
* ExecutionPlan : added the following info
	- session sets 
	- recources consumed by the request
	- header of the report
* AzureDB_main : misc visual enhancements
* Sessions : misc visual enhancements
* Fragmentation :  new report created to show 
	- table indexes
	- sizes
	- compression
	- fragmentation
  Can be invoked from "DBObjectSizes" report.
* DBObjectSizes : added link to "Fragmentation" report. Misc visual enhancements.

[12 March 2019]
* AzureDB_main : added a warning message when resource utilization is more than 80% for more than 50% of time.
* Azure_Master : report is redesigned
	- resource graphs are grouped per db in one column
	- service tier is enriched with pool names
	- GeoReplica indication is added
	- "History" column is added to get historical information of utilization and db events
* DBEvents : report is redesigned
	- "Workload & Storage for the last 14 days" is added to show workload per weekday for comparative analysis.
	  It is possible to click on any day and get detailed information (workload, storage usage, db events).