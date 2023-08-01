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
### Learning Loops and Conditions
### Exploring Expressions
### Understanding Approvals
