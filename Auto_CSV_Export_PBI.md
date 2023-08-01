## Schedule Exports from Power BI AUTOMATICALLY 

### Power Automate to SharePoint Folder Data Exporting

How to set up scheduled export from PBI avoiding 1000 row limit using Power Automate.

Let's say task was to extract tables from PBI report on monthly basis for own reporting purposes. Report is build and already had been published on PBI Service. We need different column from different tables.

Start by creating New Scheduled Cloud Flow in Power Automate.
![image](https://github.com/liubovkyry/Power_automate/assets/118057504/41edf256-e91f-4481-95e4-49af796f6bb8)

Name your export. Set time and frequency of exporting. Create.
![image](https://github.com/liubovkyry/Power_automate/assets/118057504/e40c3a37-fae5-4c1d-8438-29236d3f76f6)

Next. Add a new step - we are looking for Poer BI here.
Some options there work only for Premium Capacity, so we select <b>Run a query against a dataset</b>
![image](https://github.com/liubovkyry/Power_automate/assets/118057504/d0430561-2d2a-4bd3-b75d-77a72972dab0)

 Defining which dataset we want to run a query against - selecting workspace, datset and query
![image](https://github.com/liubovkyry/Power_automate/assets/118057504/57fd6347-1d92-47a2-ae0f-e76b524b0b38)

![image](https://github.com/liubovkyry/Power_automate/assets/118057504/d5dfa258-2cb4-4d9f-9b58-458c5bcaf767)

In the next step creating a CSV file, based on a First table rows - 
![image](https://github.com/liubovkyry/Power_automate/assets/118057504/e80a897e-e475-4f22-abec-b09b05ee021f)

![image](https://github.com/liubovkyry/Power_automate/assets/118057504/341b3ff1-c18b-4a23-86ac-df88aed33c5e)

Then we create a step defining where to save our - Create a file - SharePoint:

![image](https://github.com/liubovkyry/Power_automate/assets/118057504/b293f124-dbd5-4e7c-8069-a6df3f4ceb3e)

Note: What happens every week when file is extracted - it overrides previous one if name is the same. We can add an expression utcNow to the name, so each extraction will have name with current date included:

![image](https://github.com/liubovkyry/Power_automate/assets/118057504/ffbc1d37-0d27-438d-98f9-1d5f81b0822e)

That will make sure that file name always different.
Lastly, the file content will be the Output:
![image](https://github.com/liubovkyry/Power_automate/assets/118057504/040e6bea-0a45-4532-ad1b-701b8c309a51)

Save. Can test it - run manually.

Can update formula in Power automate and include filters if needed.

![image](https://github.com/liubovkyry/Power_automate/assets/118057504/266648be-6904-4f06-9eb4-cda203acafdb)




