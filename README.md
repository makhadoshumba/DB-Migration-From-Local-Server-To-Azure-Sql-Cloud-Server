# Database Migration From Local Server To Azure Sql Cloud Server
Database migration project showcasing Azure SQL Database deployment, secure SSMS connectivity, and successful migration from on-prem SQL Server to Cloud server(Azure). This will enable my website to connect to database online once it live, since a local sql serevr is only limited to local use, only good for testing purposes.


<br>
First we create an SQL database in Azure(this is where we are migrating to):
<br>
<img src=".assets/01.png">


Create Resource group and name the Database(NB! this should be the same as the local database you want migrate):
<img src=".assets/02.png">

Now I created a server that I will later use to connect Azure Database to SQL Server Management Studio (SSMS) allowing me o manage it form there:
<img src=".assets/03.png">

I used "SQL authentication" as a authentication method. This will later make connecting the server to SSMS seamless later on:
<img src=".assets/04.png">

Reviewing my configs:
<img src=".assets/05.png">

I am deploying now:
<img src=".assets/06.png">

Closely monitoring deployment to see if everything is deploying correctly:
<img src=".assets/07.png">

Deployment was a success:
<img src=".assets/08.png">

I made sure the resources were really deployed: 
<img src=".assets/09.png">

Here I was configuring my Network settings to allow me to connect to this database via SQL Server Management Studio, basically making it publicly accessible:
<img src=".assets/10.png">

I added an IPv4 address which will allow me to connect to connect and communicate with this server:
<img src=".assets/11.png">

Network Settings were succesfully configured:
<img src=".assets/12.png">

Connecting to local Server to prepare for exporting/migration:
<img src=".assets/13.png">

Looking for my Database:
<img src=".assets/14.png">

Making sure all the tables I want are there:
<img src=".assets/15.png">

Now we connect to the Azure SQL server to SSMS start migrating the database:
<img src=".assets/16.png">

Azure SQL server connected to SSMS successfully:
<img src=".assets/17.png">

Checking if the Database we created in the begining is present
<img src=".assets/18.png">

Now we go back to the local server:
<img src=".assets/19.png">

Locating the database I want to migrate:
<img src=".assets/20.png">

Right clicked to go to tasks and then find "Export Data...", this is where the migration happens:
<img src=".assets/22.png">

SQL Server Import and Export Wizard (the migration tool) opens:
<img src=".assets/23.png">

Here I had to lacate the data source which is my local server and the database I am migrating
<img src=".assets/24.png">


<img src=".assets/25.png">

<img src=".assets/26.png">

<img src=".assets/27.png">

<img src=".assets/28.png">

<img src=".assets/29.png">

<img src=".assets/30.png">

<img src=".assets/31.png">

<img src=".assets/32.png">

<img src=".assets/33.png">

<img src=".assets/34.png">

<img src=".assets/35.png">

<img src=".assets/36.png">

<img src=".assets/37.png">

<img src=".assets/38.png">

