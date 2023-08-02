## BUILDING AND MANAGING FLOWS

### Building Your Flow

You’ve now learned enough that we’re going to build your own flow. In one of our first lectures, we talked about how to start flows with a button, automated, or scheduled.

If starting with a Button, it could look like this on my mobile device. I click to find out the weather and I am prompted to select the date. It then displays the weather for me for the location that I put into the flow. Let’s build this flow.

 - Let’s start with an instant flow which gives us our button. Give it a name and select Manually trigger a flow.
 - Click on the manually trigger a flow. Notice you could put in a request for input of different types.
 - Click on New step.
 - Choose MSN weather, Get today’s weather.
 - Add your location.
 - Click on New step.
 - Choose to send email V2.
 - Fill in who to send it to.
 - In the subject let’s mix in some dynamic content for the location.
 - We then fill in the body with text and dynamic content from the actions above.
 - I am adding a location, a day summary, and a night summary.
 - Save the flow.
 - Go back one step.
 - From here we can click on Run. The first time running, it will get your permissions lined up. When the green checks are in place, you are good to go. Click continue.
 - Then run flow.
We should get an email that looks like this.

To see this same flow in a Scheduled cloud flow, we need to start a scheduled flow. First, I’m going to save some steps to my clipboard to use in our new flow.

 - Fill in the name and choose when you want to start the first instance of the flow. Let’s repeat it every day.
 - We click Create to see our new flow.
 - We add a new step from the clipboard and choose the forecast. Fill in the location.
 - We then add a new step for the email and bring it from our clipboard.
 - We then save the flow, and it will just run every day. It’s that simple.
 - Our last flow is an Automated flow. We will build a Twitter flow to retweet any tweet that includes the hashtag #cloudacademy.

Go to create and choose Automated cloud flow.
 - We name our file and then choose a trigger. Remember the name is not required at this stage but the trigger is.
 - Type in Twitter to see the When a new tweet is posted trigger and choose it. Then create.
 - In the search text we can put our hashtag, and anything that might be from cloudacademy.
 - Add a new step. Search for twitter. This time we see many actions.
 - Choose Get user. Fill in the Username with the dynamic content of the same.
 - Add a new step, search for variable, and choose Initialize variable.
 - Change the name to TweetCount and Type to Integer since this will be a number. I then set the initial number to 0. Twitter doesn’t like you automatically tweeting too many tweets in a day, so I am going to limit the number of times this flow runs.
 - Now we add a condition where the TweetCount variable is less than or equal to 10. This will be true for ten retweets then it will go to the NO side of the condition.
 - On the Yes side, add the Twitter action of Retweet.
  - In Tweet id, we will put the dynamic content of Tweet id.
 - I want to give credit to the user so I’m going to leave the option on no for Trim user.
 - Now we add another variable action called Increment variable.
 - We choose the name of our initialized variable, TweetCount.
 - And then enter the value of 1. Each time it retweets, it will add a 1.
 - Last step for the Yes branch of our control is another control called Terminate which will end the run. We will change the Status to Succeeded.
 - On the No branch, we add another variable called set variable. We have reached our limit of 10 if it comes down this No branch, so we are going to reset it back to 0.
 - So we pick our variable of TweetCount and set the value to 0.
Now, this would not stop it from posting again in the same day so we will add a delay which will wait to run this again for 1 day.
So we find the Delay action and put 1 as the count, and Day as the unit.
We save and we now can sit back and have our Twitter account tweet about information we are interested in.

![image](https://github.com/liubovkyry/Power_automate/assets/118057504/4df2525a-c251-4b4b-b6b9-809abcdf3109)

![image](https://github.com/liubovkyry/Power_automate/assets/118057504/338a39a3-017c-477d-a4cc-edc6794d5a21)

![image](https://github.com/liubovkyry/Power_automate/assets/118057504/9c714c60-2ff2-4c5a-9a13-d90306df8b51)

![image](https://github.com/liubovkyry/Power_automate/assets/118057504/53085366-b727-4544-b043-9ee32dd6f3c6)

![image](https://github.com/liubovkyry/Power_automate/assets/118057504/1d730e69-e017-4117-83d8-0a9d966c1d74)

![image](https://github.com/liubovkyry/Power_automate/assets/118057504/38e1ca37-eaf3-4bfd-92da-4bce0a08f739)

![image](https://github.com/liubovkyry/Power_automate/assets/118057504/31fe7709-443d-4982-98f4-fa92a6446aef)

![image](https://github.com/liubovkyry/Power_automate/assets/118057504/6680c253-93bd-4433-ba20-1c9269616002)

![image](https://github.com/liubovkyry/Power_automate/assets/118057504/5ca98401-c5a9-4d1a-950c-d9cadeed4bfc)


![image](https://github.com/liubovkyry/Power_automate/assets/118057504/69f2a12f-6574-47a9-9755-1d300de07916)

![image](https://github.com/liubovkyry/Power_automate/assets/118057504/edac68c1-8d9e-4448-a457-fd7c07aa6d32)

![image](https://github.com/liubovkyry/Power_automate/assets/118057504/0de9d28c-5733-4f5e-8052-08950acccd3c)

![image](https://github.com/liubovkyry/Power_automate/assets/118057504/6f0a8643-a52c-4ecb-941a-2ca83fc8a045)

![image](https://github.com/liubovkyry/Power_automate/assets/118057504/8e56e0ee-e7b0-4544-b778-778e331c2f2d)

![image](https://github.com/liubovkyry/Power_automate/assets/118057504/4e4f3159-15c3-4cc8-a64e-c1e89d8176d2)

![image](https://github.com/liubovkyry/Power_automate/assets/118057504/8be3263e-828b-4c50-b96a-8d7bd9f4cbc8)

![image](https://github.com/liubovkyry/Power_automate/assets/118057504/3fe86f6c-e95f-42c9-b9bf-4ca15e29393e)

![image](https://github.com/liubovkyry/Power_automate/assets/118057504/f951d6d1-92d5-4426-a3cd-584802dadbe6)

![image](https://github.com/liubovkyry/Power_automate/assets/118057504/1c6bfe35-1eb8-48f6-a74d-dbd9cb39f3f8)

![image](https://github.com/liubovkyry/Power_automate/assets/118057504/043148fa-ee7f-4f80-a178-a7e23d39d399)

![image](https://github.com/liubovkyry/Power_automate/assets/118057504/a0592e76-ca52-4c1d-86d9-1554ad7a3a0e)









## Data Operations

Data operations are a way to manipulate our data in flows. We will look at three different data operations. The Compose data operation, Join, and the Filter Array.

I’m going to show you these by creating a flow that watches for changes to our SharePoint list.<i> When the amount in stock reaches below 5 items, we want to change the status to “Reorder”, and get an email telling us to reorder the item in any or all cities affected.</i> Let’s see what that might look like. 

First of all we create <b>an automated cloud flow</b>. We search for triggers by <b>SharePoint</b> And find the trigger for when an item is created or modified. Make sure that you choose the one that says item instead of file. Files that are modified refer to document libraries not lists. And we give this flow a name. We then click on create.
![image](https://github.com/liubovkyry/Power_automate/assets/118057504/dc8566e6-cb13-4776-8aac-94a0405ecc51)

We go ahead and add our site address and our list name to the trigger. We are going to add a new step and we will search for connectors and actions with word data. Choose data operation and you will see the different data operation actions available. Let's go ahead and choose the <b>Compose data</b> operation.

![image](https://github.com/liubovkyry/Power_automate/assets/118057504/39a4f401-7ee1-4a9f-83fc-2ce479bca4bd)
![image](https://github.com/liubovkyry/Power_automate/assets/118057504/d2aa4b08-5b21-45f2-8a0a-9e2592769368)


Compose lets us put in an array of items that we can use in a dynamic content called, output at a later step. So, I'm going to add an array of cities. Next, we will add a new step and this time we'll add the <b>data operations<b/> action for Join. We have two boxes to fill in here first, it wants to know where we are bringing the information from and we're going to bring that from our Compose action that we already did.

We do that by choosing the dynamic content that's called <b>outputs</b> right under the Compose item. We then put in the formatting that we want to Join each of those items with so remember in our Compose we have a list of cities. They only have a comma between them. When I finally output these, <i>I want them to come out as the name of the city, and then the word<b> “city” </b>after them, followed by a comma.</i> Don't forget to lead off with a space. Anything you type we'll end up here even if it's a hidden character like a space. 
![image](https://github.com/liubovkyry/Power_automate/assets/118057504/eb581464-ef7b-446e-88f8-078b50e2ea87)

Our next step is to add a <b>condition control</b> which we worked with earlier on. We're going to put in the condition control with a condition of the <b>amount in stock</b> being less than five. Going down the yes path we will put in an <b>update item</b>. We must put in our site address our list name an ID and a title. Everything else should be left empty except for the thing that you want to update. I'm going to update my status value to “Reorder”.


![image](https://github.com/liubovkyry/Power_automate/assets/118057504/156fed73-8935-4f30-aa77-3e87fd2164f9)


I then add an action to send an email with the subject of reorder items. In the body, using dynamic content, we say the following locations need manufacturers name and then model reordered. Underneath that I'm going to put the output from the Join command. Make sure you're using the right output and not using the one from the Compose like we did earlier.

![image](https://github.com/liubovkyry/Power_automate/assets/118057504/4041be4f-2f00-40d8-9105-bcb962195112)


![image](https://github.com/liubovkyry/Power_automate/assets/118057504/084e65db-4767-48e7-871e-07199a7d5df8)


Now the way we've written this it would cause a loop that would continue because it would go an update an item to say reorder if the stock amount was under 5. Power Automate notices that something was modified when the flow changed the status, so it starts again. So, we're going to use another data operation to limit how the trigger will work. Remember from an earlier lecture we put a condition on the trigger. At that time, we used an expression and I told you that I would tell you later an easy way to get those expressions.

![image](https://github.com/liubovkyry/Power_automate/assets/118057504/5d19747c-f769-407f-85a9-49d124cf0783)


We click on the menu for our trigger, and we go to settings. We then go down to the trigger conditions and click on add. Now you can type in an expression right here if you know how to do it. Let me show you how I find these expressions. Click on the + to add <b>an action</b> and add the data operation of <b>Filter Array</b>. Using the Filter Array click on choose a value and put in our status value then click on is "not equal to” and enter in the word “Reorder”. Now here's where the magic happens just simply click on <b>edit in advanced mode</b> and copy the expression that you see there.

![image](https://github.com/liubovkyry/Power_automate/assets/118057504/9f6abbed-1852-47b3-acf4-dedd3ec3529b)

![image](https://github.com/liubovkyry/Power_automate/assets/118057504/6a204117-92ef-4653-800e-fed8175f50f1)

![image](https://github.com/liubovkyry/Power_automate/assets/118057504/03cb5585-7223-4ba1-9845-721503250e65)



We go back into our trigger settings, and we paste that expression. Now this trigger will not fire if it finds that the status is already at reorder which will stop our loop from happening. <i>You can now get rid of the Filter Array. We could also use the Filter Array somewhere down below if we wanted to filter out the output that we had from the Compose data operation where we wanted to just find the city of Tokyo for instance.</i>

![image](https://github.com/liubovkyry/Power_automate/assets/118057504/7e19c5e3-57db-4090-9583-44ce2c08021a)

We then save our flow, and we go into our list. When we change any of these items to an amount less than five, and its status does not equal reorder, our flow will start. 

![image](https://github.com/liubovkyry/Power_automate/assets/118057504/06a8e7d1-548a-41b5-b4a3-f6e2771b6872)

Let's look at the email that comes from our flow.

![image](https://github.com/liubovkyry/Power_automate/assets/118057504/d6d3474b-635b-489b-af43-4b233b1772c8)

It looks like it was very successful it put the word city in a comma and a space for each one of the items that was in our array in the Compose data operation.

So, to sum it up, data operations are a great way to manipulate our data. Compose can take an array of terms and create an output item we can use later on. Join can take an array item and join them together with a different character, symbol, or words. And a Filter Array is not only a secret weapon that helps us to write expressions, but it can also filter items out of a whole array of information.

### Modifying Your Flow

Let’s look at modifying your flow. You've now built your own flow and you find that something could be added, or something could be taken away, or maybe you just want to make things run a little smoother. In order to add extra actions to a flow you always look for the place that says <b> “add an action”</b>. That can be found between actions and within an action. 
![image](https://github.com/liubovkyry/Power_automate/assets/118057504/1ca6f0a4-04fc-4fee-b0e1-24ec573cf8f8)

![image](https://github.com/liubovkyry/Power_automate/assets/118057504/f845b79e-f40b-49de-9773-f313c24d9075)


When we click on add an action, and put in SharePoint, notice that there are actions and triggers. Things like <b>controls</b> only have actions and do not have triggers. You might find yourself adding a lot to your flow if you started with a template. Sometimes 3/4 of the template works just great but you need to change 1/4 of it. So, lengthening it with more steps can be part of that change.
![image](https://github.com/liubovkyry/Power_automate/assets/118057504/fae8f7a6-6858-4cc5-9973-e5d02e4f330a)


Another way we can modify our flow is by changing actions that already exist. There are a lot of things that can be changed on an action and, depending on the action itself, there are multiple advanced options or different settings for that action. Many times, when we are using connections to SharePoint, there is one important piece in the <b>advanced options</b> that really helps out.

![image](https://github.com/liubovkyry/Power_automate/assets/118057504/7aec4605-ca9c-42f7-8a4d-3a0b58e26e98)

When we turn on advanced options, you'll notice a new field comes into play called <b>“limit columns by view”</b>. Some of our SharePoint lists are very long and to be able to grab all the data from a SharePoint list is either cumbersome or it just fails. This advanced option helps us to gather just what we need by using a view that you've already created in your list to bring in only the things you want to change. For instance, if I'm only changing the status value, the manufacturer, and model, then I would create a view that only includes those things. That will make your flow much faster and more efficient. Other fields may come in because they are required but it does cut down a lot of our data management. 

Another good way to change your actions is to rename them. In this course we mostly looked at flows that were not very long. I have some flows that have over 100 different actions in them. If I don't rename each action to mean something to me, I can easily lose my place in what things are doing and why they are where they are. By clicking on the ellipse menu, we can choose to rename the action.

One other item that we can use to change, or update our flows is very helpful and you may have seen me do it earlier. When you click on the ellipse menu for an action you can choose to “copy to my clipboard”. That allows you to bring this back into another action or another step with all the information already pre-configured for you. That only stays in your clipboard while active in this session. You can copy an action from one flow to another, but it has to be done in the same online session.

![image](https://github.com/liubovkyry/Power_automate/assets/118057504/353c5ea4-b3d7-4a2b-b365-b784d8e4d5c8)

By now you should be noticing the flexibility in our power automate environment. Changes can be made at any point in our flow. Then by testing we can find other areas that might need more efficiency or corrections as we go forward. 
