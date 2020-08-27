## 1	Welcome to the Data Engineer Assessment .

Purpose is to provide us an assessment of your current skills, which is just another variable to be consider in the overall process interview.

### 1.1	OBJECTIVE:
You are responsible to perform a task for the customer company Wide World Importers, the objective is to 
* Replicate the **invoice report** provided by client, with the data in their On-Line Transaction Processing (OLTP) database named WideWorldImporters.
* Secondary objective: Perform a quick check up, that the invoice amounts in the invoice report have been correctly exported to their data warehouse (WideWorldImportersDW)

Invoice report description given by the customer:
> “The invoice report shows all the Supplier Invoice transaction type, in a given date range, Supplier Invoices are enriched with the Purchase Order information and their respective lines, is very useful since also provides relevant information about the Supplier and the Stock Items” 

### 1.2	WALKTHROUGH
Once you have read and understand the objective and the customer requirement
Step one you should get familiar with the data sources:
* Here is the Technical documentation, we strongly recommend check the OLTP   -> Database Cata-log
https://docs.microsoft.com/en-us/sql/samples/wide-world-importers-what-is?redirectedfrom=MSDN&view=sql-server-ver15
* Use the tools at hand like these native views to identify the possible objects to be use.
```
select * from INFORMATION_SCHEMA.TABLES order by TABLE_SCHEMA
select * from INFORMATION_SCHEMA.COLUMNS order by TABLE_SCHEMA, TABLE_NAME
```
### 1.3	PARAMETERS
Input: 
 * Transaction type: 5
 * Transaction Date filter: November 2015
Output:
See table below

### 1.4	EXPECTED RESULTS:
 * Query that generates the Invoice report with the given parameters
 * Bonus point: Proof of comparison between 
