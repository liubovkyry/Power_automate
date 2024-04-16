We'll build a flow for the Contoso event team that automatically pulls customer email addresses from a Microsoft Excel workbook on Microsoft OneDrive. 

We'll then set up the flow so that any email addresses that anyone adds to the workbook will receive an event information email once a day.

   ### Prerequisites
For this scenario, you’ll need to make an Excel file with a table that contains the following columns: ContactEmail, FirstName, and LastName. Save the Excel file in OneDrive for Business. You'll connect to this file in step 9. Use your organization email address as the ContactEmail, using your email will make testing the flow easier.

![image](https://github.com/liubovkyry/Power_automate/assets/118057504/1b8598a4-bac9-4118-991e-26659b9ee11a)

   ### Create a scheduled flow
 - Sign in to Power Automate by using your organizational account.
 - Select the correct environment.
 - Select <b>My flows</b>.
 - Select New, and then select Scheduled cloud flow.
 - By default you have the option to repeat every 1 minute, however, you have the option to change it and the options available are Minute, Week, Day, Hour and Second.

![image](https://github.com/liubovkyry/Power_automate/assets/118057504/fbd45960-a85c-4d1d-b57b-9eca4451b021)

 - Name your flow and under <b>Run this flow<b/> set the flow to repeat every one Day.
 - Select Create.
 - Select the <b>Insert a new step</b> button and then select <b>Add an action</b>.
 - In the search field, enter excel, select the <b>Excel Online (Business) List rows present in a table</b> action.
 - Select Sign in and sign in with your organization credentials, if prompted.
 - In the <b>Location</b> field, select the drop-down arrow and select <b>OneDrive for Business</b>.
 - In the <b>Document Library</b> field, select the drop-down arrow and select OneDrive.
 - In the <b>File name</b> field, select the folder button, and then select the Excel file to use.
 - In the <b>Table name</b> box, select the drop-down arrow, and then browse to and select the worksheet to use.

   ![image](https://github.com/liubovkyry/Power_automate/assets/118057504/274091d5-e6e0-46dd-8aef-33d6aff1ed87)
