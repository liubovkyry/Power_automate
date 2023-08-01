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
1 Defining which dataset we want to run a query against - selecting workspace, datset and query
![image](https://github.com/liubovkyry/Power_automate/assets/118057504/57fd6347-1d92-47a2-ae0f-e76b524b0b38)

```
DEFINE
VAR _table = SELECTCOLUMNS(
'Orders Details',
"Order ID",'Order Details'[order_id],
"Order Created",'Order Details'[patient_created],
"Product name", RELATED('Products'[ProductName]),
"Category", RELATED('Categories'[CategoryName]),
"Order Date?", RELATED('Delivery Details'[delivery_date])
)
EVALUATE _table
```
