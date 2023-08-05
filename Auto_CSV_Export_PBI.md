## Schedule Exports from Power BI AUTOMATICALLY 
<!-- https://www.youtube.com/watch?v=ZTkbC8zhA5k -->


How to set up scheduled export from PBI avoiding 1000 row limit using Power Automate.

Let's say task was to extract tables from PBI report on monthly basis for own reporting purposes. Report is build and already had been published on PBI Service. We need different column from different tables.

The first step is to either write or create the DAX query which will be used to extract the data into a CSV.

### Creating the DAX Query to extract the data
NOTE: The limitation is 100,000 rows or 1 Million Values, which ever comes first
<!-- https://www.youtube.com/watch?v=WsbIXJDhC_o&list=PLDz00l_jz6zze26MVT-0YV7qcjismMFFo&index=2 
https://www.fourmoo.com/2022/06/15/exporting-a-power-bi-visual-data-to-a-csv-file-in-sharepoint/
-->
<!-- Run PA, Click Dataset Refresh, When analyzing is done open name of desired visual - down click on copy query - compare with actual data selected and all filters applied -->

I will use the Performance Analyzer built into Power BI desktop to get the query I need.

 - I click on View in the ribbon and then clicked on Performance analyzer.
 - Then in the visual I clicked on the “Analyze this visual” which would then refresh the visual.
 - Next, in the Performance analyzer window I expanded the “VisualName” where I could then see the option to <b>Copy query</b>.
 - I then copied this query to my notepad. This allowed me to get the DAX I required without having to write any DAX.

### Power Automate to SharePoint Folder Data Exporting

Before I started the Power Automate flow, I made sure that I had access to a SharePoint site and folder where I wanted to extract the data to.

Start by creating New <b>Scheduled Cloud Flow</b> in Power Automate.

Name your export. Set time and frequency of exporting. Create.
![image](https://github.com/liubovkyry/Power_automate/assets/118057504/67bbdd05-5598-4138-9c9d-e6ea05604a0f)

Next is where I now wanted to extract the data from my Power BI report/dataset into the CSV file.
![image](https://github.com/liubovkyry/Power_automate/assets/118057504/198c5546-fe7b-486d-989f-1c1597dcb2fe)

There are several option to choose for the cloud flow.
Some options (like export to file) there work only for Premium Capacity, so we select <b>Run a query against a dataset</b>

 Defining which dataset we want to run a query against - selecting workspace, datset and query.

 Now, in the Query text I copied my DAX query I had copied earlier from the Performance analyzer.
 Syntax for query starts with "DEFINE VAR ... EVALUATE VAR.." 
 Hit Save.
![image](https://github.com/liubovkyry/Power_automate/assets/118057504/06cd4910-2408-4e4d-80ce-818e5b6768da)


In the next step -Add Data operation -  <b>creating a CSV file</b>, based on a <b>First table rows</b> - 
![image](https://github.com/liubovkyry/Power_automate/assets/118057504/a81a5550-5d0e-4fd8-a8ce-54e6a8b10171)


Then we create a step defining where to save our - <b>Create a file - SharePoint</b>

Note: What happens every week when file is extracted - it overwrites previous one if name is the same. We can add an expression <code>utcNow</code> to the name, so each extraction will have name with current date included or Expression <code> formatDateTime(utcNow(),’MM-dd-yyyy’) </code> for short date format.

That will make sure that file name always different.
Lastly, the file content will be the Output. 

![image](https://github.com/liubovkyry/Power_automate/assets/118057504/934f26c9-5410-400a-b3e6-42c84c5d5038)

Save. Can test it - run manually.


## Change column names when exporting data from Power BI 

![image](https://github.com/liubovkyry/Power_automate/assets/118057504/078ce70e-22df-43bb-a2ae-09d4708ff416)

Can add a step in between of our flow, add new step <b>Select</b>

![image](https://github.com/liubovkyry/Power_automate/assets/118057504/49ed4105-2896-4acc-bff4-8fd1a23b2411)


Map the Name we want to give with actual one by adding expression:
![image](https://github.com/liubovkyry/Power_automate/assets/118057504/d1f5c97c-6070-49b7-a2ad-2b05bad14fef)

![image](https://github.com/liubovkyry/Power_automate/assets/118057504/5cffb583-0ccb-46b1-982f-476f191248b0)

If we do this we have to move to our next step and change the CSV to the Output:

![image](https://github.com/liubovkyry/Power_automate/assets/118057504/218975d0-8268-442f-9140-297a82751995)

The names of colums are changed:

![image](https://github.com/liubovkyry/Power_automate/assets/118057504/5bfcd437-dd12-4357-94f0-e83077cfc9d7)


