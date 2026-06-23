# Database Migration From Local Server To Azure Sql Cloud Server
Database migration project showcasing Azure SQL Database deployment, secure SSMS connectivity, and successful migration from on-prem SQL Server to Cloud server(Azure). This will enable my website to connect to database online once it live, since a local sql serevr is only limited to local use, only good for testing purposes.

<br>
To begin this migration process, I had to create an SQL database in Azure(this is where we are migrating to):
<img src=".assets/01.png" style="width: 700px; height: 500px;" >

<br>
I created the resource group and named the Database(NB! this should be the same as the local database you want migrate):
<img src=".assets/02.png" style="width: 800px; height: 500px;">

<br>
Now I created a server that I will later use to connect Azure Database to SQL Server Management Studio (SSMS) allowing me o manage it form there:
<img src=".assets/03.png" style="width: 800px; height: 500px;">

<br>
I used "SQL authentication" as a authentication method. This will later make connecting the server to SSMS seamless later on:
<img src=".assets/04.png" style="width: 800px; height: 500px;">

<br>
Reviewed my configs:
<img src=".assets/05.png" style="width: 800px; height: 500px;">

<br>
I am deploying now:
<img src=".assets/06.png">

<br>
Closely monitoring deployment to see if everything is deploying correctly:
<img src=".assets/07.png">

<br>
Deployment was a success:
<img src=".assets/08.png">

<br>
I made sure the resources were really deployed: 
<img src=".assets/09.png">

<br>
Here I was configuring my Network settings to allow me to connect to this database via SQL Server Management Studio, basically making it publicly accessible:
<img src=".assets/10.png">

<br>
I added an IPv4 address which will allow me to connect to connect and communicate with this server:
<img src=".assets/11.png">

<br>
Network Settings were succesfully configured:
<img src=".assets/12.png">

<br>
Connecting to local Server to prepare for exporting/migration:
<img src=".assets/13.png">

<br>
Looking for my Database:
<img src=".assets/14.png">

<br>
Making sure all the tables I want are present:
<img src=".assets/15.png">

<br>
I connected the Azure SQL server to SSMS start migrating the database:
<img src=".assets/16.png">

<br>
Azure SQL server connected to SSMS successfully:
<img src=".assets/17.png">

<br>
Checking if the Database we created in the begining is present
<img src=".assets/18.png">

<br>
Now we go back to the local server:
<img src=".assets/19.png">

<br>
Locating the database I want to migrate:
<img src=".assets/20.png">

<br>
Right clicked to go to tasks and then find "Export Data...", this is where the migration happens:
<img src=".assets/22.png">

<br>
SQL Server Import and Export Wizard (the migration tool) opens:
<img src=".assets/23.png">

<br>
Here I had to locate the data source which is my local server where the database im migrating is residing in this case:
<img src=".assets/24.png">

<br>
Here I had to classify the destination in which I want to migrate the database to, in this case it was the Azure SQL server:
<img src=".assets/25.png">

<br>
And here I chose which database I am going to export my database into:
<img src=".assets/26.png">

<br>
Configuring for it to export more than one table:
<img src=".assets/27.png">

<br>
Presented with all my tables in my local server:
<img src=".assets/28.png">

<br>
Select all the the tables
<img src=".assets/29.png">

<br>
Now we are about to start exporting/migrating:
<img src=".assets/30.png">

<br>
Reviewing all my configurations before I begin exporting/migrating:
<img src=".assets/31.png">

<br>
The database was successfully migrated to the Azure SQL server:
<img src=".assets/32.png">

<br>
My database now resides in the Azure SQL server as a Azure SQL Database
(now my database is in the cloud allowing for online access):
<img src=".assets/33.png">

<br>
Checking Azure Query Editor to see if my admin_users table has been transfered successfully:
<img src=".assets/34.png">

<br>
Checking Azure Query Editor to see if my form_details table has been transfered successfully:
<img src=".assets/35.png">

<br>
Connecting to my Azure SQL server to view the migrated database in SSMS to make sure everything is alright:
<img src=".assets/36.png">

<br>
This assures me that the database was migrated successfully
<img src=".assets/37.png">
<br>


