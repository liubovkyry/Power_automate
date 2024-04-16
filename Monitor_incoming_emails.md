## Monitor incoming emails

You can create a flow that automatically performs one or more actions after it's triggered by an event. For example, the flow can monitor your Outlook inbox and when an email with a specific subject line and email address arrives, the flow will take the attachment and save it to a SharePoint library.

### Prerequisites
Microsoft Office 365

### Specify the SharePoint site and library
You can use any SharePoint site of your choice and can also use an existing library.

In this scenario, we'll use the following SharePoint site and its default <b>Documents</b> library, which is available out-of-box.

### Specify an event to start the flow
First, you must select the trigger (event) that starts the flow.

 - Sign in to Power Automate by using your organizational account.
 - Select <b>My flows</b>.
 - Select <b>New flow</b>, and then select <b>Automated cloud flow</b>.
 - Under <b>Choose your flow's trigger</b>, enter Outlook, select the <b>When a new email arrives (V3)</b> trigger and select Create.


![image](https://github.com/liubovkyry/Power_automate/assets/118057504/91e4d451-e7a6-4168-9124-fad013877938)

 - Select the trigger and then select the <b>Show all</b> button.
 -  Add the following:
<b>From</b> - 'your org email address'
<b>Include Attachments</b> - 'Yes'
<b>Subject Filter</b> - 'Daily report'
<b>Importance</b> - 'Any'
<b>Only with Attachments</b> - 'Yes'
<b>Folder</b> - 'Inbox'

![image](https://github.com/liubovkyry/Power_automate/assets/118057504/0387185a-b51b-47d9-85de-2a4ba26639bf)

### Specify an action
 - Select <b>Insert a new step</b> and select Add an action.
 - Search for create file, and then select the <b>SharePoint create file</b> action.
 - For <b>Folder Path</b> select <b>/Shared Documents</b>
 - Select the <b>File Name</b> field and then select the Enter data from previous step button.
 - Select <b>Attachments Name</b> from Dynamic Content.

   ![image](https://github.com/liubovkyry/Power_automate/assets/118057504/b957e94e-79c6-4221-86f1-c05d161009ff)

 - Select the <b>File Content</b> field and then select the Enter data from previous step button.
 - Select <b>Attachments Content</b> from <b>Dynamic Content</b>
 - Once the Attachments Name is added the <b>Create file</b> action is automatically added in an <b>Apply to each</b>. This will take care of scenarios when an email comes in with multiple attachments.

   ![image](https://github.com/liubovkyry/Power_automate/assets/118057504/0d37a37b-62e8-41cb-82d7-23a5e5d6c532)
