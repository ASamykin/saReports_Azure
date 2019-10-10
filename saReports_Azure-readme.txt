[10-10-2019]
* RingBuffer_Overview :  new report created to analyze content of sys.dm_os_ring_buffers 
* AzureDB_main : added link to RingBuffer_Overview report

[08-10-2019]
* ElasticJobs_Jobs : updated query to show status of "Last Run"; now it shows "not executed yet" for the jobs created recently and not run yet
* Sessions : added link to QueryStore information for an active query (click on SPID)

[03-10-2019]
* QueryStore_Overview : new report to analyze QueryStore configuration and content
* QueryStore_Queries : new report to see content of QueryStore and execution stats 
* QueryStore_Plans : new report to analyze execution plans per query
* QueryStore_PlanDetails : new report to see execution plan

[01-10-2019]
* DBEvents : change of service tier is added to the recent operations section

[27-08-2019]
* AzureDB_main : added analysis of connected sessions which have RESOURCE_SEMAPHOR waits in sys.dm_exec_session_wait_stats.
* Azure_Master : added second Database column for better UX
* 

[26-08-2019]
* AzureDB_main :  added Indicator of processes pending for memory
* ElasticJobs_Overview : minor formatting enhancements
* ElasticJobs_Jobs : added link to ElasticJobs_Targets
* ElasticJobs_Targets : new report is created to show targets 

[20-08-2019]
* Sessions:
	- added link to Sessions_PreviousQuery report 
* Sessions_PreviousQuery : new report is created to show previous query of a session

[19-08-2019]
* DBObjectSizes: 
	- added "Created" column with highlighting if create_date<>modified_date.
* ElasticJobs_Overview : new report created 2 weeks ago to help with Elastic Jobs 
	- column "Next Start" now has tooltip text with time left before execution
* ElasticJobs_Jobs : new report is created to show list of jobs

[27-06-2019]
* ObjectStats : added sorting to several columns

[20-06-2019]
* StatsHistogram : new report created to show statistics histogram
* ObjectStats : added link to "StatsHistogram" report
* MissingIndexes : misc formatting enhancements
* AzureDB_main : misc formatting enhancements

[18-06-2019]
* AzureDB_main :
	- Firewall link is now grey if there are no database level firewall rules
* AutomaticTuning :
	- addded support of "DBParameterization" recommendations
	- misc formatting enhancements

[17-06-2019] 
* IndexUsage :	new report created to show usage of indexes
* DBObjectSizes: 
	- added column "Index Usage" and link to IndexUsage report

[14-06-2019]
* DBEvents :
	- axis range and interval is adjusted (min, max)

* ElasticPool :
	- axis range and interval is adjusted (min, max)

[04-06-2019]
* ObjectStats :
	- minor formatting enhancements
	- column "Sample %" is added

[03-06-2019]
* ElasticPool :
	- added DTU level, list of databases and link to DBEvents report
* PerfmonCounters :
	- report migrated from another project

[31-05-2019]
* Azure_Master :
	- minor formatting changes
* ElasticPoolHistory : created by renaming original ElasticPool
* ElasticPool : new report is created to show current state of elastic pool and its workload today (+baseline).
	- added link to ElasticPoolHistory report

[29-05-2019]
* DBEvents :
	- general optimization (remove excessive queries)
	- added separate graph for Data I/O and Log Writes
	- minor formatting enhancements

* ElasticPool : work in progress 

[28-05-2019]
* ElasticPool : new report, work in progress 

[23-05-2019]
* Azure_Master :
	- minor formatting changes

* AzureDB_main :
	- offline cpus are moved to tooltip text of online cpus
	- target RAM is now visible
	- fixed Automatic tuning section (bugs with lookup)

* AutomaticTuning : work in progress.

[22-05-2019]
* Sessions :
	- minor formatting changes

* BufferObjects :
	- added column "Overall Fragmentation" and the link to "Fragmentation" report.
	- added link to "AutomaticTuning" report

* FirewallSettings :
	- added column "# IPs" which shows amount of IP addresses between Start and End IPs

* AutomaticTuning : new report is created to show automatic tuning settings and current status of autotuning efforts.


[21-05-2019]
* Azure_Master :
	- added "Logins and users"
	- added "Firewall settings" and link to the report

* FirewallSettings : new report is created to show firewall settings on server and database level

[20-05-2019]
* PricingTier :
	- minor design and source query changes

* DBPermission :
	- minor design changes

* BufferObjects :
	- added three columns "Fragmented", "Clean" & "Dirty"
	- minor formatting changes

[16-05-2019]
* Azure_Master : 
	- grouping by pools has been introduced
	- minor query changes

[15-05-2019]
* AzureDB_main :
	- added instance workload information (third graph)

[13 May 2019]
* PricingTier :
	- minor enhancements

[09 May 2019]
* PricingTier : new report has been created to show changes in pricing tier.
* Azure_Master : 
	- added a link to PricingTier report

[08 May 2019]
* Azure_Master : 
	- built-in query optimization

[26 April 2019]
* Azure_Master :
	- new column "Deadlocks" is added with conditional highlighting

[25 April 2019]
* Azure_Master :
	- fixed one of datasources (scope) 

[18 April 2019]
* AzureDB_main :
	- amended query which collects db information; tempdb now has "Data Used (MB)" values

[15 April 2019]
* Sessions :
	- amended connection dataset (scope is limited to the current database only)

[11 April 2019]
* ColumnstoreStats : 
	- minor formatting changes
* DBObjectSizes :
	- minor formatting changes

[10 April 2019]
* ColumnstoreStats : new report created to show columnstore rowgroups info
* DBObjectSizes :
	- added link to ColumnstoreStats report

[09 April 2019]
* XESessionBuffer : 
	- added number of rows and number of pages
* DBObjectSizes :
	- Table type column is added (heap/clustered/clustered columnstore)

[08 April 2019]
* Sessions :
	- "logical reads", "Dop" columns are added.
* MissingIndexes :
	- Tooltip notes are added to clarify column meanings.

[04 April 2019]
* DBPermissions :
	- redesigned "role membership" part
	- added filters and highlighting
	- minor enhancements

[02 April 2019]
* Sessions :
	- amended sql query to show actual resources consumed by active sessions

[01 April 2019]
* AzureDB_main :
	- fixed issue with long running queries (int overflow)
	- amended definition of ExtendedEvents session "" and filtered out 2 types of messages ("Changed database context to '%.*ls'.", "Changed language setting to %.*ls.")
* XESessionBuffer :
	- added counter of records

[28 March 2019]
* AzureDB_main :
	- database options are sorted now

* Azure_Master :
	- new column "Operations" is added; it shows either amount of active operations for a db, or current progress % if it's only one operation + tooltip details.
	- "Service Tier" cell is highlighted if there was a up- or downscale of it today. Tooltip text provides additional details.

[27 March 2019]
* AzureDB_main :
	- added creation of ExtendedEvents session (stopped by default) to trace error messages sent to the client. Target is ring buffer, max size is 200MB.
	- added start/stop function for a session
	- added view content of a session's ring buffer  (new report XESessionBuffer)
* XESession : 
	- minor formatting changes
* XESessionBuffer :  
	- new report which shows content of ring buffer of an ExtendedEvent session

[26 March 2019]
* DBEvents :
	- minor enhancements

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