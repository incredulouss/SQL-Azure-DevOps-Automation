
# SQL Script deployment using Azure DevOps

## Objective
The main objective of this repo to automate the SQL scripts deployment to Azure SQL servers using Azure DevOps CICD pipeline

### Tech Stack

- Azure SQL server
- Python odbc drivers
- Python scripts
- Azure devOps
- SQL scripts

### Prerequisite

- Azure SQL Server
- Azure DevOps organization
- IP of agent (Azure Devops) should be whitelisted to SQL server firewall (Networking)



### Steps to setup code

    1. Clone the repo
    
    2. Upload all the sql script you want to deploy inside the sql folder

    3. Open the sql-requirements.txt file inside the sql folder and update the name of the sql script you wanted to deploy. Also maintain the order in which you want to deploy

### Steps to setup Azure DevOps Pipeline

    1. Inside you Azure DevOps organization create the variable group, to store all the Environemnt variables.
    ex - database,  ODBC_driver = {ODBC Driver 17 for SQL Server}, password, server, username, workingDirectory = $(System.DefaultWorkingDirectory)/5214-AIW-SQL

    Note - Provide database, password, server and username values
    2. Now create the new Pipeline and connect to your repo and branch.
    3. Give the path of your application.yaml file for pipeline to do the deployment
    4. Finally run the pipeline and deploy the sql scripts to your SQL Server
## Other Common Github Profile Sections
👩‍💻 I'm currently working on writing the Blob with detailed descirption of the project

🧠 I'm currently learning Data engineering

🤔 I'm looking for help with any issues reagrding the repo


## FAQ

#### How to resolve Authentication issue to SQL server through pipeline ?

You will have to whitelist the IP address of the runner to the networking (firewall rule) of the SQL server


## Authors

- [@incredulouss](https://github.com/incredulouss)


## Feedback

If you have any feedback, please reach out to me at utkarsh.gupta1994@gmail.com


## Environment Variables

To run this project, you will need to add the following environment variables to your variable group in Azure DevOps

`database`

`ODBC_driver`

`password`

`server`

`username`

`workingDirectory`
