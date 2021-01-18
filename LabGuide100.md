## Part 1 - Getting Setup with Oracle Free Tier for Education

Students in this course will be using Oracle Cloud Free Tier Account for Education. This cloud service provides Free Oracle Autonomous Database instances that will be used in class. Additionally, once registered you get 365 days and $300 free money to use on Paid Cloud Services that will also be used in class. Please note that this Free Tier is different from the Normal Oracle Free Tier in that you are not required to provide a credit card and you have 365 days instead of 30 days of use for non-free services.

If you already have a registered Oracle Free Tier for Education account and you have more than 30 days left on the account you can proceed to Part 2.

[Part 2: Autonomous Database Startup Guide](/Oracle-Cloud-Free-Tier-Education-Setup/?lab=part-2-autonomous-database-startup-guide)

## Setup Oracle Free Tier for Education

In order to get the Oracle Cloud Free Tier with 365 days of $300 you will get an email from Oracle Academy asking you to register.

The email will come from Oracle Academy or no_reply@oracle.com. The email will indicate that your instructor has requested your account and will look something like the one instructors get, shown in Figure 1.

TODO: Figure 1 Email

This email has the link the you need to follow to register for the account. Before clicking on the link and registering you need to determine the email address that is linked to the Education Program. Your instructor should have sent you an email telling you which email address you should use. You MUST use that email account. It is the only one that gives you 365 days to use the Free $300 credits.

Since KU email accounts can have several aliases you need to determine which email was given to Oracle. Go to the email and click on or right click on the actual email address that Oracle used. As you can see in Figure 2 the email used is shown and circled. Check your email find the email and get the email used. *Make note of this email. You will need it for the next steps.*

TODO: Figure 2 Email Address


Once you have the email address click on the “Click Here” link on the email. You will now go to the Cloud Sign-up Page (Figure 3)

TODO: Figure 3 Cloud Sign-up Page

Enter the email address that Oracle Academy used to send you the email. *Do not use any other email address or you will be signing up for a 30 day account instead of the 365 day education account.*

Click Next to continue with the registration.

You should now see this next screen in Figure 4. This is notification that you are eligible for the Special 365 day Program.

**If you do not see this screen STOP! Verify your Email Address again and try again. Do not continue if you don't see this dialog box. Contact your instructor if you cannot fix this.**

**Do not give Oracle a credit card number, as it is not required for the Student account.**

TODO: Figure 4 Student Program Qualification

Click the `OK` button and then click `Next` to continue.

You will be asked for an Account Name and this is not your email address. 

Enter one that unique to you. A recommendaation is to use your first initial and last name.

**Remember this as you will always need it to sign in.**

Next you will be asked to choose a region. Ashburn or Phoenix are the proper options.

Now fill out the rest of your information.

After you enter this information you will see a PASSWORD button. Click that and the password screen will be shown.

TODO: Passowrd box

Enter a valid Password (Remember / write it down) and click on Next.

TODO: Image of completion

Now your account will be provisioned. When the process is finished it will eventually bring up the Login Screen .
Remember to write down the account name and username (your email address used to register) and password.

TODO: Oracle CLoud Login

FIXME: Suggest Single Sign-On or login password? I believe single sign on is required later.

You need to enter your username and password to log you in to the Oracle Cloud home page.

It will take a while to provision, maybe as much as an hour or so, to complete and you will see that you have a Trial Balance of $300 that is good for 365 days. 

Sign out of your account now and wait for at least 1 hour. 

Sign back in using the following login method:
- Go to oracle.com URL
- Click on Menu Item > View Accounts

TODO: Image of where to click

Click on Sign-in to Cloud

FIXME:(At this screen you can Bookmark (Oracle Cloud Sign-on)

Enter your Account Name FIXME:(you wrote this down?). [you got an email with this on it also!]

TODO: Image of Oracle Cloud Login

Click Next

Now enter in your email address and password

TODO: Username and Password login

You should now see the Your Oracle Cloud Main Home Page

TODO: Main page

You are done!

Notice you should have money available in your trial credits and Trial Days should be more than 30.

TODO: Image of credits and days

Note: If you happen to see that you only have 30 days of Trial then you did not actually create the account using the proper education email address. Contact your Instructor Immediately. If you see this image then you don’t have the education account:

TODO: Free tier image?

you need to create a new cloud account using the email account that Oracle Academy send you.

Hint: You can bookmark this page and it will go directly to the prompt without having to go to oracle.com again.














<!-- 
This section focuses on getting started with OAC and introducing students to the interface.

Key takeaways from this lab:
- Starting an OAC instance
- Learning and getting acclimatized to the interface

## Oracle Analytics Cloud

Oracle Analytics Cloud is a cloud-first analytics platform, providing fast and flexible analysis of any data from any source. It is built on the industry-leading Oracle Business Intelligence platform and Oracle’s top tier cloud infrastructure.

Oracle Analytics Cloud delivers scalability, high availability, state-of-the-art security, and operational simplicity. This combination of proven technologies, world-class infrastructure, broad data access, and deep analytic capabilities makes Oracle Analytics Cloud the best solution for every user.

The goal of today’s workshop is to introduce you to the data visualization capabilities included in OAC. We will be analyzing data using local Excel files. OAC also allows you to analyze data based on a pre-built OAC subject area or coming directly from a wide variety of sources. These can include Oracle SaaS applications (e.g. ERP Cloud), databases, and 3rd party applications (e.g. Salesforce), amongst others.

## What are Oracle Analytics?

Oracle Analytics is a tool that enables you to explore analytical data visually and individually. The capabilities are available both via a web-based interface (OAC) as well as via a local client (Oracle Analytics Desktop).

Oracle Analytics makes it easy to visualize your data, so you can focus on exploring interesting patterns and outliers. Just upload your data files or connect to a data source, select the elements you are interested in, and let Oracle Analytics find the best way to visualize it. Of course, you can also choose from a wide range of visualizations yourself if you want to look at your data in a specific way.

- **Creating visualizations is easy**. Your data analysis work is an individual experience in exploration and discovery that can also be shared with other users. Oracle Analytics enables you to experiment with a wealth of different options for how to view your data. During this experimentation process, you can find correlations, discover patterns, and see trends in your content.

- Oracle Analytics provides you with tools for faster and simpler assembly of detailed reports arranged together in an appealing and meaningful display. Oracle Analytics goes even further, to give you dynamic views for focused, exploratory interaction with your data.

## Oracle Analytics provides the following:

>**Guidance**: Grammar-centric approach to visualizations combined with powerful keyword search and pattern detection to aid all users making new discoveries.

>**Richness**: Robust visualization library and streamlined dashboard construction provide all the tools needed for constructing sophisticated analysis across many different perspectives of data.

>**Visual Grammar**: Visualizations automatically created and updated by applying visual grammar to data selections made by user. All visualization types share foundation in visual grammar.

>**Keyword Search**: All relevant artifacts are indexed for search. Unfamiliar data models can be intuitively accessed using keywords.

>**Pattern Brushing**: Sophisticated technique to highlight correlations between visualizations. Patterns highlighted across all components on the canvas.

>**Data Blending**: Combining two or more data sources for analysis.

## Provisioning an Oracle Analytics Cloud Instance

1. From any browser go to oracle.com/cloud/sign-in.html to access the Oracle Cloud.

    [https://www.oracle.com/cloud/sign-in.html](https://www.oracle.com/cloud/sign-in.html)

    ![](images/login-screen.png " ")

2.  Sign into the **Single Sing-On (SSO)** by clicking **Continue**. This is required because the **Identify Provider** will be required to create our Oracle Analytics Cloud Instance.  
*NOTE:  Do NOT click the Sign-In button, this will sign you in without your Identify Provider and you will not be able to create the instance.*

    ![](images/single-sign-on.png " ")

3. Enter your username and password and click on **Sign In**.

    ![](images/oracle-cloud-signin.png " ")

4. Once you log in you will see a page similar to the one below.  Click on the hamburger icon in the upper left corner to reveal the menu.

    ![](images/hamburger.png " ")  

5. Click on **Analytics** -> **Analytics Cloud**

    ![](images/menu.png " ")

6. On the next screen, click on **Create Instance**.

    ![](images/create-analytics-instance.png " ")

7. Now, give your instance a **Name**.

    ![](images/100/img_1a_7_3.png " ")
    
    Next, we will configure our instance. Click on the **Feature Set** dropdown.

    ![](images/100/img_1a_7_1.png " ")

    Choose **Self-service Analytics**  and leave the rest of the options as is.

    ![](images/100/img_1a_7_2.png " ")

    

8. Review your selections. Make sure your fields match the fields mentioned in the previous step. In case of issues, return to the previous screen and make the required changes. Then click **Create**.

    ![](images/100/img_1a_8_1.png " ")

9. Now, wait for the instance to be created. This can take up to half an hour.

    ![](images/100/img_1a_9_1.png " ")

10. Once created select **Analytics Home Page**.

    ![](images/100/img_1a_10_1.png " ")

    Doing so will take you to the OAC home page which we will be reviewing in the next section.

    ![](images/100/img_1b_1.png " ")

11. It's important to note that once we're done using the instance we need to **Stop** the instance or else it could use multiple dollars a day of our trial credits. Restarting the instance at a later time takes roughly 5 minutes.

    ![](images/100/img_1a_10_3.png " ")
## Reviewing the Home page and the primary menus

On logging into OAC, you will see the home page.

![](images/100/img_1b_1.png " ")  

1. Start by clicking on the hamburger menu in the top-left of the UI. This will open the drawer menu.

    ![](images/100/img_1b_1_1v2.png " ")

2. You can use this menu to navigate through the application.

    ![](images/100/img_1b_2_1.1v2.png " ")

    ![](images/100/img_1b_2_1.2v2.png " ")

    The application follows standard web and application interface protocols, thus supporting both left and right click interactions. In terms of general navigation, there are 4 key menus accessible at the top of the screen or via a hamburger menu in the top left (not all screens will show the top menu bar but the hamburger navigation is always available).

    >**Home**: Application start up page from where you can view existing projects, data sets, data flows or create new ones.

    >**Catalog**:  Collections of visualizations and the underlying data sources. **Folders** are simply means by which to organize projects.

    >**Data**: Display or create **Data Sets** (instances of data such as a specific Excel file);
        >> **Connections** (connections to data sources such as a database or SaaS application to pull data files); or
        >> **Data Flows** (ability to curate data from data sources including adding calculations, merging multiple sources, and managing columns).

    >**Machine Learning**: This page shows all the available machine learning models ready for use in projects.

    >**Jobs**: This page shows all the status of data replication, data flow, and sequence operations.

    >**Console**: Administrative menu for managing **Custom Plugins** (e.g. new types of analyses obtained from the Oracle Analytics Store or custom built), **Maps** layers (e.g. new backgrounds for map-based analyses) and other administrative tasks.

    >**Academy**: Home to important links to the OAC documentation and videos that help you accomplish common tasks in the OAC.

3. At the top-right of the UI, click on the **Create** button.

    ![](images/100/img_1b_3_1v2.png " ")

    This window allows you to create a Visualization project, a data set, a connection to an external source, a data flow, or a sequence.

Now that you can start and navigate around OAC, let’s get started with some analyses!

[Continue to Part 2](/Oracle-Analytics-Cloud-Workshop/?lab=part-2--basic-introduction-core-features) -->