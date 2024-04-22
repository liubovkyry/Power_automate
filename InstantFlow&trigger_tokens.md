## Build a flow that uses information like locations or date

You can build instant flows that use information like Global Positioning System (GPS) data, date information, or email. This information is available as trigger tokens. Trigger tokens are data points that are known and available to the device that an instant flow is running on. These tokens change, based on factors like the current time or the current geographic location of the device.

For example, if you run an instant flow on a phone, the phone probably knows the time at your current location, the date, and your current address. In other words, the time and date, and the address where the phone is located, are determined when the instant flow runs. They're automatically available for use in any instant flows that are run on the device.

You can use these trigger tokens to build useful flows that minimize repetitive tasks. Such tasks include providing your location to someone or tracking how much time you spent on a particular job or service call.

### List of instant trigger tokens 

![image](https://github.com/liubovkyry/Power_automate/assets/118057504/01179059-df47-41bb-bd97-779dd4dd2313)

### Create an instant flow that uses trigger tokens

Let's create an instant flow on a mobile device to let your colleagues know you're working from home today.

### Prerequisites
A work or school email address, or a Microsoft account that has access to Power Automate.

The Power Automate mobile app for Android or iOS.

### Create the Instant flow

 - From the Power Automate home page, select Templates from the left hand menu.
 - Search for Working from home today and select the Send a "Working from home today" email to your colleagues service.
 - ![image](https://github.com/liubovkyry/Power_automate/assets/118057504/58fbfa8f-a9ce-4388-a2d2-054e8c46f63b)
 - Make sure your connections have a green check mark next to them. You might need to sign in to the Office 365 Users connection and create a connection to Notifications. Select Continue.
 - Now we switch to Power Automate mobile to edit and run the flow.
 - Open the Power Automate mobile app and sign in with your organizational credentials.
 - ![image](https://github.com/liubovkyry/Power_automate/assets/118057504/c2f3481c-fad7-493e-bad5-c4e005acf836)
 - Select the three dots next to the flow name and select Edit.
 - Once the flow opens and you can see the actions, select the Apply to Each action and then select the Send an Email action that's inside of the Apply to Each. The Send an email action expands to show options to configure the email.
 - Select the Subject field, and enter WFH today. Notice that when you selected the Subject field, a list of tokens appeared below. While the cursor is still in the Subject field, scroll down until you see the Date field at the bottom in blue and select it. Notice that the date token now appears in the Subject field.

   ![image](https://github.com/liubovkyry/Power_automate/assets/118057504/5fdc32bc-32de-4c14-88bb-dbd76072c717)
 - Scroll to the Body field and select the default message so that you can add tokens there.
 - Scroll down to find the Full Address token and select it. The Full Address token is now in the body of the email.

![image](https://github.com/liubovkyry/Power_automate/assets/118057504/8e729217-fb39-445d-b57a-51ef5e4a0f7c)

 - Scroll down to the bottom of the flow and select Save.
 - You should receive a message that says Flow edited successfully.

### Run the Instant flow

![image](https://github.com/liubovkyry/Power_automate/assets/118057504/e3b7f2aa-e086-44af-802e-8bdad9a61242)

