# Introductio to Power automate
Objectives will include:

 * Describing the different types of flows
 * How to identify and choose the proper type of flow triggers
 * How to find and use templates to run or modify a flow
 * How to use data connectors and how to change them
 * Be able to describe templates, connectors, loops and conditions, expressions, and approvals
 * And finally, create and modify a flow
   
Power Automate can connect to a wide variety of applications within Microsoft, and outside. Here are some examples of what Power Automate can accomplish.

 * Press a button on your mobile phone to check the weather or your GPS location and bring up a map
 * Update your social media from a pre-approved SharePoint list of future posts
 * Run complex approval workflows combined with forms, documents, and notifications
 * Move documents that meet a certain criteria to another location with more storage space
 * Output items from a form to a SharePoint list or Excel Spreadsheet
 * And Flag a quality issue to shut down production across the world. Notify all production managers and require a mitigation form be filled out before resuming production

## Identifying Flow Types

 In Power Automate we have three types of flows we can use to accomplish our automations. 
 The three flows we will describe are cloud flows, business process or guided flows, and desktop or RPA flows.


 So we head into Power Automate and on the left-hand menu, we choose My flows. Cloud Flows. 
 The first of these flows is what we would call event-driven, triggered flows, or you'll see them listed as cloud flows.
 Within the cloud flows, there are three more types. These types really indicate the type of activation of the cloud flow.
![image](https://github.com/liubovkyry/Power_automate/assets/118057504/9f045e64-8686-4cf4-ae4f-7af9b6378bfc)

![image](https://github.com/liubovkyry/Power_automate/assets/118057504/d20caf12-8d90-471b-a574-edccb89bdb9f)

 <b>An Automated flow</b> is a flow that is triggered based on some criteria. For instance, if a SharePoint list item is updated the flow will start, or when an email is received, the flow starts.

<b>Instant flows</b> are the type that you can start with a button. This button could be attached to a web page or used within a cell phone Power Automate app. 

<b>Scheduled flows</b> are the type that run based on a specific schedule, like once per day or once a week, they might start up to remind somebody of something or run a process that needs to be done every week.

<b>Desktop</b> or <b>Robotic Process Automation (RPA)</b> flows are automations that you create for your desktop or for using the web. They are created in another interface on your desktop and saved in the cloud. A good example might be starting up your web browser and opening a page of that website to keep up to date on new additions.


<!--I'm gonna go ahead and click on Cloud Fundamentals, which will take us into its properties. And I'm going to edit that, which will launch our application for the Power Automate desktop app.

This is a desktop flow that I created to launch Cloud Academy's site then take me into the learning paths of the cloud fundamentals section. You can automate this by recording your steps and then adding this flow to your startup process. I could also record steps to move larger files like videos and pictures to another hard drive with more room.-->

<b>Business process</b> or <b>guided flows</b> are made to guide a person through a business process flow. The best examples of these are flows that are used in dynamics 365 sales actions. A phone salesperson may go through a script and a specific task list. A new employee may go through a set of documents that are presented one after another as they fill them out. Most of the integration does happen with Dynamics 365.

You will often hear the terms “team flow” and “my flows”. My flows will show you all of your flows: cloud, desktop, and business process flows. You will notice there's a place that says, <b>“shared with me”</b>. Team flows are what you find under the shared with me menu. Those are flows that you have shared with someone else and, someone else has shared with you, turning them into team flows. So we covered three types of flows: cloud flows, business process or guided flows, desktop or RPA flows. We also talked about the three different types of cloud flows, of automated, instant, and scheduled. Our next lecture will be on using templates.

## COMPONENTS OF POWER AUTOMATE

### Using Templates
![image](https://github.com/liubovkyry/Power_automate/assets/118057504/d9b14abf-14eb-4ba1-a010-934a87adf544)

Templates are a really great way to get started quickly on your automation development. There are hundreds of templates already created that will do almost anything you want to do. You can start from a template and customize it to fit your needs. If it doesn't do everything you want, customize or repurpose it. 
You'll notice we can access templates from the home page right in the middle. 

There are also different ways to find the template we need.

By category is one of those ways.

Within the templates, we can find things by categories. Categories are showing across the top of the screen and when we click on the ellipses menu, we see a couple more. 

Some categories that I have found useful are remote work, approval, and some of the most used templates being email templates. 

Sorting templates is also very helpful.

A template doesn’t always fit our process perfectly so we may need to do some Customizing and Repurposing.

If you want to have Power Automate do some of the work for you, pick a template and then open the template and change the items that you wish to change. In a search for SharePoint templates, I find one that sends an email when a SharePoint list is modified. I can open this template and put in my site and list information.  The subject and body content of the email are not really what I want to send, so I can change those things and then save it as my own.
![image](https://github.com/liubovkyry/Power_automate/assets/118057504/0406f4ab-f782-4572-940a-6aff1961530f)

![image](https://github.com/liubovkyry/Power_automate/assets/118057504/109c27b1-5489-402f-aed7-0afe8dbe9ee7)


So, using templates can be very helpful in starting with Power Automate. Not only can you learn from them, but you can customize them as well. We saw how we could find templates through categories, searches, and sorting. We also saw that we could customize and repurpose those templates to meet our needs, then save them as our own.

### Power Automate Connectors
You might notice that throughout Power Automate you will not only see Microsoft connections being made but you'll see connections to all sorts of different third-party vendors. Connectors make this possible by creating a link to that third-party provider of some service. When we want to connect two different things that don't speak the same language, we need some kind of connector in the middle and that's what Microsoft has built. There are hundreds of connectors built into Power Automate. At this time, there are close to 500 different connectors. 
![image](https://github.com/liubovkyry/Power_automate/assets/118057504/a44e58c9-1790-4875-acc0-5a9e451e2a9f)


Let’s talk a little about accounts you will need and pre-built content that comes with a connector

Each one of these connectors helps us to actually make a connection between two different services. In some cases, you need to have an account with the service that you're connecting with, for instance in the case of Cognito forms, they offer a free membership where you can build simple forms.

If I want to have somebody fill out a survey from Cognito, and have that information flow to a SharePoint list, then email someone, then I use a connector from Cognito forms, a connector from SharePoint, and I use a connector to Outlook. With the connector comes some prebuilt content so when I do link up with Cognito forms it already knows that it's going to go and find my forms and the fields of that form, with the type of data for each field. I then connect the form that I've created and pull different information out of it. This is why Power Automate is called a “no code, or low code solution”, because it does most of the work.

Notice that some connectors have the word Premium under them. Premium connectors look like all the rest of the connectors and can do the same things as other connectors, but the difference is in the level of service, licensing, and price. So, I can link up my MailChimp account to pull new subscribers into SharePoint, but I need to put in credentials for MailChimp and be able to use their premium content which requires me to purchase more than their free account.

I also need to have a proper license with Microsoft for Power Automate. Since licensing changes from time to time, please check your license to see if Premium accounts are included. When you see the item that says premium that means there's a charge on one end or the other, and, sometimes premium can mean that we need a higher license within Power Automate or other services.


One note I would like to share is that there are connectors and there are connections. <b>Connectors</b> are what get two different services talking together, <b>connections</b> are the credentials that we use to connect with the different services. Connectors are found under the connectors link in the left-hand navigation. Connections are found underneath the data link in left-hand navigation. There at the bottom, you see my latest connection with Adobe.



### Learning Loops and Conditions
Loops and conditions are helpful when our process flow is not just one straight line or argument. Loops help us to continue to process things until some condition is met. Conditions help us act on certain criteria or take action on other criteria.

Loops can include counters that help them to start from a position and end when counters reach another position. When each loop happens, counters can be incremented. For example, retweet a message until the Retweet count reaches 10.

 Loops can continually run without counters until a condition is met. For example, sending a reminder every day until the status reaches “Approved”. Let’s look at some ways to use conditionals and loops.

Within Power Automate, we will start with a simple flow that emails someone when we have a change to an inventory list item. We add a new action between our list and the email, and we select Control. The loops and conditionals all fall within here. The first one of these we will look at is a Switch Control.

Notice we get three input boxes, a Switch, Case, and Default. In the Switch box we are turning the switch on to watch our status value. When the status equals “Out of Stock”, then the next step runs.
![image](https://github.com/liubovkyry/Power_automate/assets/118057504/7f3f909a-2b3b-4ece-924c-dd6c14247d5d)

 I am going to add an email action and then put it as our next action in the Case. This would send an alert email to someone. If status equals anything else, then it does nothing more. 

I’m going to copy our email so we can use it again. Now let’s add a Condition Control in the same place. Notice that we also get three boxes but, in this case, we can do more inputs than a switch which was for a single input. We can still add our status value and what it is equal to, but we could also add multiple other conditions that must be met. When a condition is met, we travel down the Yes side of the condition. If the condition is not met, then we go down the No path. Let’s add our email as an action of the Yes path.
![image](https://github.com/liubovkyry/Power_automate/assets/118057504/1ca8ed57-072d-4a52-bbc8-6b2fe62bb1c7)
![image](https://github.com/liubovkyry/Power_automate/assets/118057504/21477b10-5551-45df-82a3-ff3f5d40d525)

On our No path, we could add another condition control to split the status values even further. For example, let’s add a condition that still sends an email but only if it is not out of stock, and it is not in the status of “Available”. That way, we can send a different email to notify people that stock is low. We could go on doing this until we break down everything we need to accomplish. So, Condition Controls will help us to do multiple conditions.

For the Do Until Control, we can use our same example, but you might see an issue. I would like to send a reminder to order an item when the Status is equal to “Out of Stock”.  Let’s put the Do Until into place and select our Status Value equal to Ordered. Now by itself, the do until creates some problems. First, it will continue to send emails or change things until we reach our condition or until it times out. The default time out is set at 1 hour.

You can see that we would have to make some changes, or we would have this running for ever if we don’t be careful. We would most likely want to start with a scheduled cloud flow and run it every day or once a week. Then, we would have a conditional control that would include the Do Until control within it. Then we would not get into a loop that would drive others crazy or time out.
![image](https://github.com/liubovkyry/Power_automate/assets/118057504/8b54b7e8-cd12-4972-b7fa-66097370394f)


Our next control is the Apply to each. Notice the lighter color of these two controls. That is an indicator that they should be in another control. Apply to Each will apply an action to a group of items. If I wanted to have all items in my inventory that were ordered changed to the status of “Available”, then I would need to do two things. First would be to add a condition control or switch. Since we are only looking for one item, I will use a switch control to look for those items that are equal to the status value of “Received”. Then I embed the Apply to each control to update the status value on just those that say” Received” to the status value of “Available”. It will continue to run until all items that were received are updated.
### Exploring Expressions

 What is an Expression? An expression is a small code function that might help us to concatenate text, perform math functions, date functions, or logical functions against our data. When we talked about our conditions, we were looking for something to be equal to something else and we did that with just dropping down boxes and making choices. We can also write the expressions from scratch.
 ![image](https://github.com/liubovkyry/Power_automate/assets/118057504/54b49ab5-3ec3-4ca7-872a-d81b7b22b5f2)


You can find expressions by going to any place in our flow and clicking to bring up the dynamic content. Dynamic content comes from the fields and properties of our data and is packaged for us. Right next to the Dynamic content tab is the Expression tab.

There are endless ways to add expressions in advanced mode or basic mode. Let’s add an expression to our trigger to only trigger if the inventory status is equal to Reorder or Out of Stock. We click on our trigger menu, choose settings, and Add a Trigger Condition. Our condition is going to be an OR expression where either the status can equal Reorder, or Out of Stock. Our flow is going to run every time the SharePoint list is modified but the first step will be to validate this trigger condition. If neither of those statuses are there, the flow stops. 

We could also change this by adding another expression where our Amount in Stock is less than, or equals the number 5.  
![image](https://github.com/liubovkyry/Power_automate/assets/118057504/d73b956e-f26c-45c2-a7ff-69be69631922)

### Understanding Approvals
Approval flows are a way to have one or more people approve content, documents, or maybe even calendar items like days off. We can have many cycles of approvals where one person approves one step, then the next person approves the next step and so on. Our ultimate goal is to automate the process of sending emails and documents back and forth and reducing time to results.

One of the Common Starting Points as we learned earlier, is to start with a template. There is a specific category for Approvals so that is where we can find many premade approval flows.

Here are some common components of approval flows. Of course, some trigger that starts the flow when a file is changed, created, or modified. An approval action. Emails to approve and to update the submitter of status. Updates to files like status changes, copy, move, attach can all be part of the approval. You will most likely see some of the other items we have covered like conditions, loops, and expressions. 

The results may look something like this.
![image](https://github.com/liubovkyry/Power_automate/assets/118057504/300b1018-2687-4d97-9080-8e09405bf690)

This is a flow that looks for a new file to appear in a document library. It then creates an approval for the first person to respond. It gives them information about what they are approving as well as a link to the item so they can review it. Once approved, we copy the file to another library for approved documents and send an email to the originator to let them know that it is being approved.

This is an example of the email received by the approver. It has a button to approve which presents a comment section which could be used in an email. Once submitted, it sends another email with the results.
![image](https://github.com/liubovkyry/Power_automate/assets/118057504/d8a8cd31-7432-4ff6-b1a7-c7505b9dc65b)

We could of course, make this much more complicated. Let’s look at an approval for an item created in OneDrive which interacts with email, Teams, and approvals.

It starts with a trigger for a file being created, it creates a share link, then it gets my profile and holds that in memory so I can use it down further in the flow. 

![image](https://github.com/liubovkyry/Power_automate/assets/118057504/461c7a4d-8db0-4cd1-a5bf-46006323f032)

We then see our approval with all the options filled in. We then see something a little new in a parallel branch which lets two processes happen at the same time. Down the first branch, we find an Apply to Each loop that creates cards for Microsoft Teams. We then wait for the approval to happen.
![image](https://github.com/liubovkyry/Power_automate/assets/118057504/0a15ef48-c937-498e-bc7d-229c2c64bc35)

Notice the condition that we learned about being used to find out if it was approved or rejected. Depending on the approval outcome, the user gets a note in Teams.

Down the other branch is an error action that just looks like an email is being sent. This is really a special item that has been set to run after a failure. When we click on the ellipse’s menu, we can click on Configure Run After to see when the email is actually being sent. The next step just terminates the flow.
![image](https://github.com/liubovkyry/Power_automate/assets/118057504/5c1604f2-a46d-49d9-bd9e-a152a4f6ab53)


