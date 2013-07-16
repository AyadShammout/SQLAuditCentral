SQL Audit Project Description
=============================

With SQL Server 2008, there is a powerful yet lightweight method to audit a SQL Server instance. But to manage and view the audits of your entire SQL Server environment, we have created the Centralized Auditing Framework that will parse, load, and report all of your audit logs. 

From a high-level perspective, the architecture to audit sensitive operations for your SQL Server environment will be to: 
-Turn on auditing on your various database and servers; you can find more information at http://msdn.microsoft.com/en-us/library/cc280386.aspx

-Have these audit logs go to one centralized location instead of a local folder 

-Included in the Centralized Audit Framework is an SSIS package that will Parse through all of these audit log files.

-Populate a centralized database (also included) with audit dimension data (class, type, server names, etc.) and audit fact data (audit events separated by category of server, database, DDL, and DML actions).

Once the data is loaded, a nightly job will process the data to product report tables. 
These report tables can be viewed by SSRS reports (included).

