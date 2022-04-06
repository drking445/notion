Notion Javascript Client- this scripts reads in data from a csv file, calculates the average book ratings and the number of favorites for each book, and then displays the book data

Step 1: Create an integration.


Go to https://www.notion.com/my-integrations.
Click the "+ New integration" button.
Give your integration a name - I chose "Vacation Planner".
Select the workspace where you want to install this integration.
Select the capabilities that your integration will have.
Click "Submit" to create the integration.
Copy the "Internal Integration Token" on the next page and save it somewhere secure, e.g. a password manager.

Step 2: Share a database with your integration


Integrations don't have access to any pages (or databases) in the workspace at first. A user must share specific pages with an integration in order for those pages to be accessed using the API. This helps keep you and your team's information in Notion secure.

Start from a new or existing page in your workspace. Insert a new database by typing /database and selecting a full page table. Give it a title. I've called mine "Weekend getaway destinations". Click on the Share button and use the selector to find your integration by its name, then click Invite.

Your integration now has the requested permissions on the new database. Once an integration is added to a workspace, any member can share pages and databases with that integration - there's no requirement to be an Admin for this step.

Before moving on, you need the ID of the database you just created.
Copy the URL of your Notion database. Make sure you're viewing the database as a full page if you're using an inline database.
If you're using the Notion desktop app, click on the Share button and select Copy link.

The database ID is the part of the URL after your workspace name (if you have one) and the slash (myworkspace/) and before the question mark (?). The ID is 32 characters long, containing numbers and letters. Copy the ID and paste it somewhere you can easily find later.

Now open terminal/command prompt and go to the notion folder:

First run:

    export NOTION_KEY=secret_...
    export NOTION_DATABASE_ID=...

Second run:

    npm install
    
Third run:
   
    node index.js
    
- Was there anything you got stuck on, and if so what did you do to resolve it?

I was stuck on how to insert into the table and I figured it out by printing out the data to find the ids of the columns. I was also stuck on reading the data into memory from the csv and I resolved this by manually reading in the data.


- Do you have any suggestions for improving the API documentation to make it clearer or easier to use?

No, I think it was fairly straightforward


- A list of links to any major sources you relied on, if any (e.g. a StackOverflow response about how to structure Node CLI applications)

None used

- A list of major open-source libraries you chose to use and their purpose, if any (e.g. "Axios for networking")

None used
