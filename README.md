# Steps to Create a Case Template in theHive.

Today we are going to talk about making quick and simple Custom Case Templates in thHive.

The best thing about a case template is the time it saves the analyst when responding to a case in theHive. Providing an analyst with simple to select options in a drop down saves time determining what a manager is looking for, allowing the analyst more time to provide observables or even… analysis. If a case manager, crew lead or team lead is asking for similar responses for every case, creating a template in the description or providing drop downs will simplify the task and everyone spends less time editing. And if you know your analyst will be conducting the same tasks (more or less) for similar cases, you can template in a task list to help answer the case, closing the case faster and freeing up even more time for your analysts to analyze.

The first thing you need to do is know what you want your ticket to contain. This is important. I know it sounds ‘important’, as in “in a perfect world, I’d know what I want, but this isn’t a perfect world so I’ll just start building a case template and add what I want as I go”. The ‘building-the-plane-in-flight’ mentality goes right out the window with theHive. Separations of duty help solve that problem for the Organization Admin by creating new problems for theHive admin. 

See, an Organization Admin knows what they need for their organization, or at least knows what they want… or most of the time knows what they don’t want at least. But theHive Admin is the only account that can decide what data fields can contain. Which means that the Organization Admin has to talk to theHive Admin with any fresh ideas. Sure, this might be some overhead for both parties, but every user gets to enjoy a standard as a result.

# 1.	Decide What You Want.  
Think about how you want to divide up cases. Is it by MITRE ATT&CK tactics? Is it by common adversarial actions that fit a killchain? In this example, we will use a hybrid of observable adversarial actions that fit a broad MITRE tactic but within the template, we might see several sub-tactics. This way, the analyst has the flexibility of starting a case quickly rather than needing to pinpoint a tactic that may be flawed or single sided. For example, an analyst may start a ticket to the lead that indicates C2, but it turns out that is not ONLY C2, but C2 for exfil instructions. It doesn’t matter what your preference is; what matters is you set a standard that works for the flow of accomplishing the mission at hand.

# 2.	Talk to theHive Administrator.
You have a great idea where you want to put every end point on the network you are currently focused on in a drop down. The host analyst love this idea so they can create a case and start slinging out IOCs. It’ll make cases easy to search. Or the network analysts have petitioned the Network Lead to open cases with a drop down of ports, divided in open and closed and the protocols associated with them. They are tired of typing it out themselves. So, you as the lead, go to theHive Admin and tell them what you want. And they laugh at you and tell you to (respectfully) kick rocks. They don’t have time for that. There is no dedicated work-role to theHive. Or they tell you to provide them with a return delimited text file for the list you are asking for. “Oh – I don’t have time for that!”, you say. But let’s say you do give them that list. They will take it and laugh as they realize that to use such an insanely long list means your analysts might spend more time scrolling through a drop down than doing… analysis.

When you present an idea, try to think of subjects, items or actions that you will want universally – things that will fit most of the time. Any outliers can have notes made in the Details section if need be. And if the “outliers” become commonplace enough, fields can be created to identify them.

At this point, you have an idea that you want to tackle lateral movement actions. You realize that there is a MITRE tactic for lateral movement and sub tactics. Those would be good, since your organization uses the MITRE anyway. TheHive Admin agrees.

# 3.	Create Custom Fields – theHive Admin 
You state the things you want in your custom case template, theHive Admin agrees and then they turn away and start typing. You should walk away now. See, only they can create the custom fields you want to use. But only the Organization Admin can put those fields in a Custom Case Template and implement it. So they will tell you when they are done and you can get to making the template later. 
But in case you find yourself saddled with creating a template you know your analysts will need but no one created (and you have those theHive Admin creds), here is how you do it:

Log in as the admin:
https://github.com/33v3rp3ss/theHive-Custom-Templates/images/main/1_signin.png 

On the top right, click on “Admin” and drop down will appear. Choose “Case custom fields”.
 

On the top left of the page, you will see a button, “Add custom field”:
 


You will see the “Add custom field” screen. Each “*” is a necessary field that needs information. Fill out the name and you will notice the “Internal Reference” will autofill; it is best to keep this default for simplicity sake when exporting/importing custom case templates. Provide a description to assist analysts, or HQ folks, in understanding in plain language what is expected. And then “Type”. We’ll choose “string”:
 

In the “Possible values” field, we need to provide content for our future drop-down menu. Notice the instructions in gray on the input field – “Possible values, one per line”. We take a list of common techniques to apply and type them in here. When complete, click the “Save field” button on the bottom right:
 

# 4.	Create a Custom Case Ticket – Organization Admin
TheHive Admin is done and can go about doing whatever their primary and secondary jobs are at this point. Or if you were sneaky and did that yourself, you can go back to making that great, new case template that will save a few hours of analysts time, and maybe a few hours of editing time trying to whip the right information out of them so you can get your report in on time. In any case, log out of theHive admin and into the Organizational Admin account.
You’ll notice the top right corner is slightly different:
 

Click on “Organisation” and you’ll see your users pane by default. We don’t care. We want templates. So click on the “Case Templates” tab:
 

On this screen, you’ll see a list of current templates on the left sidebar and the menu of whatever selected template on taking up the rest of the screen. What we are concerned with is the “+New template” button here:
 

Here is the blank template screen. There are only a couple areas that need to be filled out (“Template name” and “Description”). But you can create tasks, identify a default Severity, and even apply tags for tracking.
 

After the mandatory and “administrative” fields have been filled out how you like (as below), we are ready to add custom fields by clicking on the “+” icon right of the “Custom field”:
 

You’ll be presented with a drop down menu with all the Custom Fields theHive Admin created. You can choose one and keep clicking the “+” icon to add more until you are satisfied that you have made your analysts job as easy as possible (and ensure that you are getting as many answers as it takes to make your job easy without dragging it out of them). You can add tasks as well, or come back and add them later, based on the organizational TTPs/playbook you have. Once done, be sure to click the “+Save case template” button on the lower right of the screen:
 

Immediately you will see your Custom Case Template populate the left hand bar, joining the other high-speed templates you have loaded/created:
 


# 5.	Sharing is Caring. – Organisation Admin
Have you noticed that there is another organization using theHive but they have case templates that aren’t like yours? Maybe… maybe they are better?! And you want them! Or maybe they are not as good. Maybe you want to share them, especially if you work closely with that organization and don’t want to look through poorly crafted theHive cases should you have to. Well, for both altruistic AND selfish purposes, you can easily share your templates.

From the “Case Templates” tab (where we created a custom case template above), highlight the template you want to share. In this case, we’ll select our great “Lateral Movement” template and click the “Export case Template” button on the lower right:
 

I have created a new folder on my machine, and here I can either rename or choose to save to that new folder:
 

I decide that theHive knows its naming conventions better than me, and since it tends to be particular, we’ll keep the default and drive on by clicking the “Save” button:

 

We can navigate to the template’s save file (a .json formatted file) and when we open it (if we are curious and want to see it or if we want to edit it before sharing/importing) we can see it here:
 

Now we are ready to share! And everyone has a big tea party and celebrates as we come together!
Except they don’t. The ashy taste of failure looms…

# 6.	Importing Custom Case Templates: Time to Talk to theHive Admin…Again.
You gave your template to the friendly organization across the way and everyone was happy. Then they went to import it. Now they aren’t friendly anymore. They don’t return your calls. They don’t write. They barely look at you, and when they do, you can tell… they are judging you. 
“You template doesn’t work!” they say. What?! It works just fine you try to tell them.

The problem is, those custom fields in your template… The admin for their instance of theHive hasn’t made them yet. To get rid of the error message, you need to get theHive Admin to create the Custom Fields you used on your theHive instance.

From theHive Admin account you are transferring FROM, navigate to the “Case custom fields”:
 

Scroll to the custom field(s) you need for the template you are wanting to import (in this case, Lateral Movement Techniques):
 

Open a text editor and make sure to grab all the info you need to create a Case Custom Field in the RECEIVING theHive instance. This example holds all the relevant fields:
 

Take the text document and the exported .JSON, and transport that (whatever means you prefer) to your theHive instance. 

Follow the direction in “Step 3. Create Custom Fields”, copy/paste the text document to ensure you get the proper syntax (especially the “Internal Reference” field).

Switch to the Organization Admin. Navigate to the Case Templates by clicking on the “Organization” button and going to the “Case Templates” tab:
 

Click the “Import template” button:
  
When the “Import Case Template” window opens, you can drop one or more JSON  files (or navigate to it) to prepare for the import:
 

If your template uploads successfully, there will be green notification bars in the lower left; these will be red if there is an error, along with a brief statement pertaining to the error. 
