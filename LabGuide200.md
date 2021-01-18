## Part 2 - Autonomous Database Startup Guide

## Creating Autonomous Database

1. Sign into your Cloud account and you will be presented with your dashboard. Select Autonomous Transaction Processing, Create an Autonomous Data Warehouse database.

TODO:Image of clicking Cread ADW

2. Enter a Display name as well as a Database name. Add a password to the Administrator Credentials section. Move the Always Free selector to the right.

- Display Name: A user-friendly description or other information that helps you easily identify the resource. The display name does not have to be unique, and you can change it whenever you like. Avoid entering confidential information. Recommend using ADW+your initials + 01

- Database Name: The database name must consist of letters and numbers only, starting with a letter. The maximum length is 14 characters. Avoid entering confidential information. You can use the same as Displayname without Spaces! *I suggest that you give your database name that is easy to remember. I use something like BRADW01 where “BR” are my initials.*

TODO: Image of Dispay Nanme and Database Name

3. Verify the defaults for the remaining fields below.

- Workload Type: Data Warehousing

- Deployment Type: Shared Infrastructure.

- Always Free: Move this selector to the right so that the provisioning workflow shows only the Always Free
configuration options. Note that the Core CPU count and Storage configuration fields are disabled when provisioning an Always Free Autonomous Database. Your database will have 1 OCPU, 8 GB of memory, and 20 GB of storage.m*Note: if failing to select Always Free your credits will be charged*

- Administrator Credentials: Set the password for the Autonomous Database Admin user by entering a
password that meets The USERNAME is always ADMIN – Remember this! the following criteria:
  
    1. Between 12 and 30 characters long
    2. Contains at least one lowercase letter
    3. Contains at least one uppercase letter
    4. Contains at least one number
    5. Does not contain the double quotation mark (")
    6. Does not contain the string "admin", regardless of casing

Use this password when accessing the Autonomous Database service console and when using an SQL client tool. WRITE THIS DOWN ALONG WITH THE USER NAME --- YOU WILL USE THIS A LOT!!!

- License Type: When you provision an Always Free Autonomous Database, the license type is set to License included and cannot be adjusted.

- Advanced Options

Tags: Optionally, you can apply tags. If you have permissions to create a resource, you also have permissions to apply free- form tags to that resource. To apply a defined tag, you must have permissions to use the tag namespace. For more information about tagging, see Resource Tags. If you are not sure if you should apply tags, skip this option (you can apply tags later) or ask your administrator. Avoid entering confidential information.

TODO: Screenshot of defaults

4. Click **Create Autonomous Data Warehous Database**.

TODO: Screenshot of Click Create

5. It may take several minutes for your database to be provisioned, while this is happening you will see this screen :

TODO: Screenshot of DB Creation

6. When this process is completed, you will now see the state set to available. This means that your database instance is created.

TODO: Screenshot of DB Started

7. Now that the database is running you should create the Wallet file which you will need to login using SQLDeveloper Desktop and Oracle Analytics (Cloud and Desktop)

8. Click on the DB Connection Button (Tab) and it will ask you to set a password and Download the file. Remember where you stored this wallet file you will need it later. (FYI it will call the file with your Instance name + wallet.zip) Also DO NOT UNZIP THIS FILE YOU WILL NEED THE ZIP FILE.

9. You now have a live database server!
At any point you can sign in to your Cloud account and return to your database by using the hamburger icon in the top left corner and selecting Autonomous Data Warehouse.

TODO: Select Autonomous Data Warehouse

10. This will return you to your database page where you can select your live database.

11. If you saved a shortcut to go directly to the Cloud Database Page you will see this screen:

TODO: Cloud Database Login

- Enter your Account Name (Cloud Tenant) and click continue 

- You will now be asked for you username and password

TODO: Sign in 

- Once you sign in you will be brought directly to the Database Page listing your configured Database Instances.

TODO: DB Instances Screenshot

- You can then manage your database instances. Note one of my databases is stopped. Simply click on the instance you want to manage and go to the database page to manage it.

- Now you can click on the various things like More Actions to Start/Stop/Terminate or Tools to use SQLDeveloper, change Admin Password or use Apex. You can click on the DB Connection button to create wallet file to connect to ADW using SQLNet or other tools, like SQLDeveloper Desktop or Oracle Analytics Desktop.

## Restarting your Autonomous Database if it has stopped due to inactivity:

- If your Always Free Autonomous Database has no activity for a period of 7 consecutive days, the Database service will stop the database automatically. You will also get an email from Oracle when they automatically turn off your Database.

TODO: Email about database paused from Oracle

- If this happens, you are allowed to restart the database and continue using it. If your Always Free Autonomous Database remains in a stopped state for 3 consecutive months, the resource will be reclaimed by the Database service.

1. Go to the ADW instance page and restart the Database click the Start button in the Other Options link.

TODO: Screenshot

2. Confirm that you would like to start the database by clicking Start in the confirmation window.

TODO: Screenshot

3. You will see a status of “Starting”

TODO: Screenshot

4. After a few moments the database status will change to “Available” and you are then free to continue use.

TODO: Screenshot











<!-- ## Part 2 - Analyzing Sales - Basic Introduction to Core Features

This section walks you through the analysis of a single data set.

Key takeaways from this lab:
- Creating projects with data sets and visualizations
- Understanding the visualization capabilities of Oracle Analytics
- Telling a story with annotated visualizations

## Creating a Project with a Data Source and Visualizations

**Scenario**

You are the Chief Marketing Officer (CMO) of KoolKart.

KoolKart is an e-Commerce company that sells 4 categories of products and is looking for innovative ways to increase revenues. As part of that initiative, you and your team have launched several social media campaigns within the past 6 months.

Given the level of investment your company has made, you are looking to ensure that resources are being effectively utilized. Hence, you are investigating the effectiveness of those campaigns.

After reaching out to the sales team, you have been provided with a spreadsheet with thousands of rows of information and are struggling to make heads or tails of what you are evaluating. Let’s see how Oracle Analytics can help you!

1. Review the spreadsheet containing the sales figures used in this lab.

     Download and open the <a href="/Oracle-Analytics-Cloud-Workshop/Exercise%20Files/KoolKart%20Sales%20Data.xlsx">**KoolKart Sales Data.xlsx**</a> file.

    ![](images/200/img_2a_1_1.png " ")

    >You should see that there are several thousand records of sales figures (e.g. **Revenue** and **Number of Orders**) broken down by **Date**, **Category**, **Age Group**, and **Gender**.

    You can close the spreadsheet.

2. Create a project to evaluate the sales data and upload the Excel file.

    Select **Create Project** from the Home screen.

    ![](images/200/img_2a_2_1.png " ")

    Every project requires a data source, so you will be prompted to add one.

    Select **Create Data Set** to load in the Excel file.

    ![](images/200/img_2a_2_2.png " ")

    >If you had created connections to external systems (e.g. an Oracle Database), you would see those as options here. For the purpose of this lab, we will just upload a file.

    ![](images/200/img_2a_2_3.png " ")

    Navigate to the **KoolKart Sales Data.xlsx** file and select it.

3. Validate the uploaded data.

    >Following the upload of the file, which will be available for other projects as a **Data Source**, you have the ability to make changes to the data so it can be easily used within analyses.

    ![](images/200/img_2a_3_1.png " ")

    ![](images/200/img_2a_3_2.png " ")

    The system will determine, if the columns are **Attributes** or **Measures**.

    >![](images/200/img_2a_3_3.png " ") **Attributes**: Indicated by **A**, attributes are generally non-numeric fields.

    >![](images/200/img_2a_3_4.png " ") **Measures**: Indicated by **#**, measures are generally numeric fields.

    >If a field is determined to be a **Measure**, the system will also determine the default aggregation method for when it is used in an analysis (e.g. average, sum, count). If desired, you can change an **Attribute** to a **Measure** and vice-versa. For **Measures**, you can also change the default aggregation rule.

    >![](images/200/img_2a_3_5.png " ") **Clock**: Fields may also be indicated by a **Clock** icon. These will be your date and time based fields, which can be handled differently in certain visualizations. However, they still need to be defined as **Attributes** or **Measures**. If the **Clock** icon appears, the date is being treated as an **Attribute** otherwise it will have a **#** icon.

    No changes are needed for this data.

4. Add data to your project.

    Click **Add** to begin creating visualizations.

    ![](images/200/img_2a_4_1.png " ")

5. Use **Recommendations** to enrich your data set for analysis.

    On creating the data set, you will be guided to the **Prepare** screen, where you can modify your data set. OAC uses its intelligence to recommend changes that can enrich the data set.

    ![](images/200/img_2a_4_2.png " ")

    Selecting a column will filter the recommendations to show only those related to that column.

    Select **Customer Country** to see the recommendations for the column..

    ![](images/200/img_2a_4_3.png " ")

    >Although, we won't be using the recommendations now, it is a very powerful feature and we will see that in the last lab.

6. Create an analysis of monthly revenues.

    Select the **Visualize** tab (top right of the screen).

    ![](images/200/img_2a_5_1.png " ")

    Select the **Data Elements** icon and select **Month**. Press and hold the **Control(Windows)** or **Command(Mac)** key and click on **Revenue** Then, right click and select **Create Best Visualization**.

    ![](images/200/img_2a_5_2.png " ")

    >As an intelligent analytics platform, the system is able to provide recommendations for how best to visualize information. The system has determined that a bar chart is a good way to display the information that you are evaluating.

    ![](images/200/img_2a_5_3.png " ")

    Before we continue, let’s take a step back and better understand the interface of the Visualize tab and its capabilities.

## Understanding the Visualize Interface

1. Review the **Visualize** interface and menus.

    >We have previously established that a **Project** comprises of data sources and visualizations related to those data sources. We have already walked through the process of adding a data source in the previous section. Now, we will learn some more about visualizations.

    >Visualizations are displayed on a canvas. A **Canvas** can contain multiple visualizations and a **Project** can include multiple Canvases.

    >When you open the **Visualize** interface, you should see the **Canvas** in addition to a few other menus. The **Project Components Menu** will be on the left hand side and the **Project Tabs** will appear at the center top of the screen.

    ![](images/200/img_2b_1_1.png " ")

    Let’s start by reviewing the **Project Tabs**, which allow you to switch between editing data sources, creating visualizations, and putting together a story about the visualizations.

    ![](images/200/img_2b_1_2.png " ")

    You can switch between the tabs as needed and each has a specific purpose:

    >**Prepare** – Validate and make changes to the data you wish to use in your visualizations.

    >**Visualize** – Create your visualizations.

    >**Narrate** – A nice feature where you can view, compile, and manage meaningful “stories” from your visualizations by picking certain ones to highlight and adding commentary.

    Next to the **Project Tabs**, you will find the **Project Menu** which allows you to manage various facets of your project.

    ![](images/200/img_2b_1_3.png " ")

    From left to right, the items are:

    >**Undo Last Edit** – Remove the last user change.

    >**Redo Last Edit** – Reapply the last user change rolled back by the above (greyed out, if there is nothing to redo).

    >**Share Project** – Bring up additional options for sharing the project as a file or to print.

    >**Save** – Provides ability to save the project.

    >**Home** – To return to the home screen.

    On the left hand side of the screen, the **Project Components Menu** displays the available Data Sources, **Data**, **Visualizations**, or **Analytics** within the project (depending upon which one has been selected). If you are on the **Prepare** tab, then it will display **Preparation Script** or **Data**.

    ![](images/200/img_2b_1_4.png " ")

    The icons on the left filter the items listed. From top to bottom they are:

    >**Data Elements** – Displays the actual data available for analysis (e.g. the columns from your data sources).

    >**Visualizations** – Visual elements available for use in the Canvas.

    >**Analytics** – Provides access to advanced analytics that can be added to visualizations such as trend lines, clusters, and outliers.

    Based on which icon is selected, you will see different results. The example below shows the **Data** in our current project.

    ![](images/200/img_2b_1_5.png " ")

    The **Search** box allows you to search through the data sets. For example, you can search for **Data** that are related to the customers by typing in customer.

    ![](images/200/img_2b_1_6.png " ")

    ![](images/200/img_2b_1_7.png " ") Click the **X** to remove any filters (please do so, now).

    Now that you have been exposed to the core features of the interface, let’s dive into some further analyses.

## Analyzing Sales Figures by Product and Customer Segments

>Thus far, you have brought data into Oracle Analytics and generated a basic analysis of revenues over the past six months. However, this is a fairly basic analysis and, as CMO, you really need and want to dig in to the data further. Specifically, you are interested in seeing how different product categories are performing and how different marketing segments (e.g. gender) have an impact on those figures.

1. Create a breakdown of revenue by product category.

    Drag and drop **Category** into the **Color** property of the previously created bar chart.

    ![](images/200/img_2c_1_1.png " ")

    You can now see monthly revenue broken out by product category.

    ![](images/200/img_2c_1_2.png " ")

    >Built-in intelligence can even attempt to determine the best way to add **Category** to your visualization by simply double clicking on it.

    >You can also interact with the results further by hovering over various categories. For example, if you move your mouse over the yellow portion of **2015-11** (which represents **Electronics & Computers**), you will see all other categories dimmed for easier viewing. You will also be able to see more detailed information on the actual data (e.g. the actual number of orders).

    ![](images/200/img_2c_1_3.png " ")

    ![](images/200/img_2c_1_4.png " ")

    >After looking at each product category, you can now see that Electronics & Computers and Clothing & Shoes categories are consistently the major contributors to sales in the past 6 months.

    >That helps in better understanding which categories drive the most revenues, but you still need to better understand your customer demographics.

2. Create a new type of visualization to evaluate revenues by age group.

    Select the **Data Elements** item and select **Customer Age Group**. Press and hold the **Control(Windows)** or **Command(Mac)** key and click on **Revenue**. Now, right click and select **Pick Visualization**.

    ![](images/200/img_2c_2_1.png " ")

    **Select Donut**.

    ![](images/200/img_2c_2_2.png " ")

    >As you can see, there is already a great variety of visualizations available and more are released in every new version of the tool. We won't be covering each and every one, but we have made an attempt to provide a few examples during the course of this workshop. 

    ![](images/200/img_2c_2_3.png " ")

    You should see the new visualization, automatically placed next to the bar chart.

    >It looks like our customers in the 25-31 and 32-39 age range are the largest contributors to our revenues in the past 6 months. Let’s take a look at revenues over time to see if there is a noticeable increase over time (which we’d hope based upon our investments in the social media campaigns).

3. Create a new type of visualization to evaluate revenues by date (e.g. to view a trend over time as opposed to just monthly totals).

    Select the **Data Elements** item and select **Date**. Press and hold **Control(Windows)** or **Command(Mac)**. Select **Revenue**. Now, right click and select **Create Best Visualization**.

    ![](images/200/img_2c_3_1.png " ")

    You should now see a canvas that looks like the following:

    ![](images/200/img_2c_3_2.png " ")

    >It looks like we have seen some increased revenues, though we will likely need to drill in even further to identify the impact of the social media campaigns. However, before we do that, let’s “clean-up” the canvas so it’s easier to digest, in case we need to share the results.

## Formatting Visualizations and the Canvas

1. Rearrange the visualizations to make them easier to view.

    Click on the **Revenue by Date** timeline visualization. A blue border will indicate that the image has been selected. Hover your cursor near the top border until you see a 4-way arrow icon.

    ![](images/200/img_2d_1_1.png " ")

    Left click and drag the visualization into the top right of the canvas above the **Revenue by Customer Age Group** visualization until you see a thick blue line.

    ![](images/200/img_2d_1_2.png " ")

    Make sure that the thick blue line does not extend above Revenue by Month, Category otherwise the visualization you are moving will appear above both the bar chart and donut.

    ![](images/200/img_2d_1_3.png " ")

    ![](images/200/img_2d_1_4.png " ")

    Now, click on the **Customer Age Group** visualization. Just like the previous time, the image will have a blue border when selected. Hover your cursor until you see a 4-way arrow icon.

    ![](images/200/img_2d_1_5.png " ")

    Left click and drag the visualization into the bottom left of the canvas under the **Revenue by Month, Category** visualization until you see a thick blue line.

    ![](images/200/img_2d_1_6.png " ")

    Your canvas should look like the following:

    ![](images/200/img_2d_1_7.png " ")

2. Expand one of the visualizations.

    Now, click on the **Revenue by Date** visualization. Hover your cursor over the left border until you see an arrow icon.

    Left click and drag the edge of the visualization to the left to increase the size. Your canvas should now look like the following:

    ![](images/200/img_2d_2_2.png " ")

3. Adjust the project colors used in the visualizations.

    Select the **Canvas Settings** option in the **Project Menu** in the top right of the screen and select **Project Properties**.

    ![](images/200/img_2d_3_1.png " ")

    Click on **Default** in the **Color Series** option.

    ![](images/200/img_2d_3_2.png " ")

    Scroll down and select **Tokyo**. Then select OK.

    ![](images/200/img_2d_3_3.png " ")

    All of the visualizations will now reflect the new color scheme, across all canvases!

    ![](images/200/img_2d_3_5.png " ")

    >You may have noticed that in addition to a wide variety of options and configurations, there is also the ability to create custom palettes, which enables users to display results however they wish. For the purpose of this example, we made changes at the project level for a quick and easy change but colors and display options are also available at the visualization level to allow for full flexibility.

4. Reset the color palette.

    To avoid confusion with coloring in prior exercises, let’s go ahead and reset the color palette.

    Select the **Canvas Settings** option in the **Project Menu** in the top right of the screen and select **Reset Colors**.

    ![](images/200/img_2d_4_1.png " ")

5. Rename the Canvas.

    Since **Projects** can have multiple **Canvases**, it usually makes sense to name them for the ease of reviewing down the line.

    Select the **arrow icon** in the **canvas tab** on the bottom left of the screen and click **Rename**.

    ![](images/200/img_2d_5_1.png " ")

    Give the **Canvas** a meaningful name such as **Revenue Analysis** by clicking in the box and typing it in. Select the checkmark to confirm your changes.

    ![](images/200/img_2d_5_2.png " ")

## Analyzing Visualizations with Trend Lines and Trellis Rows

>As mentioned earlier, as the KoolKart CMO, you have now started to evaluate your revenue data. However, you want to make sure that it has some relation to the social media campaigns that you launched during November, January, February, and April. At first glance, it does look like revenues are increasing following those campaigns but you want to make sure things are also trending upwards, overall.

Luckily, Oracle Analytics can help. So, let’s take a closer look at our numbers!

1. Add a trend line to your Revenue by Date visualization.

    **Right click** anywhere in the **Revenue by Date** visualization and select **Add Statistics** followed by **Trend Line.

    ![](images/200/img_2e_1_1.png " ")

    You should now see a trend line within the **Revenue by Date** visualization.

    Click anywhere in the visualization to remove the trend line properties menu.

    >Upon adding the trend line, hopefully you also notice the ability to add other types of analyses such as: reference lines, clusters, forecasts, as well as the ability to fine tune those analyses. The platform is highly intelligent and robust, and allows for the deepest levels of analysis, some of which we will cover in later labs.

    >It looks like revenues are trending upwards and have been healthy for the past 6 months! But let’s see if that holds true for all product categories or if our campaigns have had more success in certain areas than others.

2. Further analyze your **Revenue by Date** visualization by breaking it out, according to product category.

    >Trellis Rows and Trellis Columns are mechanisms by which we can breakdown an analysis by creating multiple versions of that analysis for distinct entities. In the example being used, there is an initial line chart looking at revenues over time. Adding a Trellis Row for product category creates a line chart of revenues for each product category. See below for a screenshot.

    ![](images/200/img_2e_2_1.png " ")

    Make sure the **Revenue by Date** visualization is selected by clicking on it. Now, select **Category** from the **Project Components Menu** on the left (make sure to select the **Data Elements**, if you do not see **Category** listed). Drag and drop it into the **Trellis Rows** property of the visualization.

    ![](images/200/img_2e_2_2.png " ")

    Your line chart should now be comprised of 4 rows, each of which is its own line chart for a specific product category.

     ![](images/200/img_2e_2_3.png " ")

    >Now, this is interesting!

    >We knew overall revenues were trending upward and that certainly seems true for the Books & Audible and Movies & Music categories. However, Clothing & Shoes seems to have remained flat and Electronics & Computers is actually trending down! Electronics & Computers makes up a good portion of our overall revenues too, so we should really take a closer look at all of this.

    >We should talk with our team, but what is the best way to share this information?

## Narrating a Story with Visualizations and Insights

1. Add an Insight to your project.

    Click on **Narrate** in the **Project Tabs** in the top right of the screen.

     ![](images/200/img_2f_1_1.png " ")

     You will see the following screen:

     ![](images/200/img_2f_1_2.png " ")

2. Create a narration for your Insight.

    Click on the hamburger icon and select **Add To Story**.

    ![](images/200/img_2f_2_1.png " ")

    You should see the ability to add information into a text box at the top of the screen. Click into the **Description** text box and type in **Clothing & Electronics are not following the overall sales trend**. Click anywhere outside the box.

    ![](images/200/img_2f_2_2.png " ")

    Let’s also give the **Canvas** tab a meaningful name. Double-click the Title Box (currently labeled "Revenue Analysis") and type **Clothing & Electronics**.

    ![](images/200/img_2f_2_3.png " ")

    The **Canvas** is now ready to be shared, which we will cover later on. Let’s make sure to save our work at this point.

3. Save your project.

    Select the **Save** disk from the **Project Menu** in the top right of the screen. Select **Save As** in the pop-up menu.

    ![](images/200/img_2f_3_1.png " ")

    Type in "KoolKart Sales - " followed by your initials as the Name and click **Save**.

    ![](images/200/img_2f_3_2.png " ")

Congratulations! You have now successfully created compelling visualizations with Oracle Analytics.
## Modifying Properties in the Data Panel

Now, let's go over the data panel in the bottom left of the UI for accessing properties. You will find yourself using them in the upcoming labs, so now is a good time to visit them. Click on the **Visualiza** tab and click inside the **Revenue by Date** line charts.

![](images/200/img_2g_1.png " ")

This section will cover the functions of each of these options.

![](images/200/img_2g_2.png " ")

![](images/200/img_2g_3.png " ")

>![](images/200/img_2g_4.png " ") **General**: Allows you to edit the title, visualization type, and line type.

>![](images/200/img_2g_5.png " ") **Edge Labels**: Allows you to edit labels within your visualizations such as Trellis Rows or Trellis Columns.

>![](images/200/img_2g_6.png " ") **Axis**: Allows you to adjust the labels for different axes on your visualization. This includes the labels axis, values axis, and secondary values axis.

>![](images/200/img_2g_7.png " ") **Values**: Allows you to adjust the measures you have included in your data set. This includes the aggregation method, number format, and Y2 axis (if it applies).

>![](images/200/img_2g_8.png " ") **Date/Time Format**: Allows you to adjust how date/time column data is shown in your visualizations.

>![](images/200/img_2g_9.png " ") **Analytics**: Allows you to add different analytics options to your visualization. This includes Clusters, Outliers, Reference Lines, and Forecasts.

[Continue to Part 3](/Oracle-Analytics-Cloud-Workshop/?lab=part-3--data-blending-wrangling) -->