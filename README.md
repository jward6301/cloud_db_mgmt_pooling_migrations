# cloud_db_mgmt_pooling_migrations
HHA 504 Assignment 4C - Migrations and Pooling

## 1. Connection Pooling Setup::
On Azure, open Database for MySQL servers. Next click create and select flexible server. Then either choose an existing resource group or create a new one. Create a server name and make sure to change the compute and storage option to the B1s option. Create a admin user name and passowrd. Under networking please select to add your current IP address and enter in 0.0.0.0 - 255.255.255.255. Click review and create and if all options look correct, select create. 
Before closing out of this, please make sure that under Service Parameters, the max_connections option is changed to 20 and the connect_timeout option is changed to 3.
On GCP, open SQL. Please click create instance and choose mysql. Create an ID and password. ensure that enterprise is selected as well as sandbox. Change the configuration to shared core with 1vCPU. Next, under connections add a network named AllowAll set to 0.0.0.0/0. Finally click create instance.

## 2a. Database Schema and Data: and 2b. Using MySQL Workbench to Generate ERD
All code was reused from a previous assignment and similar steps were followed. You can view the code used in the following repo: https://github.com/jward6301/flask_4_databases_mysql_vm. I have attached screenshots of the working ERDs for both Azure and GCP. The ERDs were created using the reverse engineer function on Workbench. 

## 3. SQLAlchemy and Flask Integration:
All code for this step was taken from a previous assignemnt as well. You can view the code in this repo. .gitignore and .ENV files were used to protect my informaiton to connect to GCP and Azure. 
I was originally able to run the code and create a flask application for Azure but once I tried to run it for GCP it stopped working for both
## 4. Database Migrations with Alembic:
I could not fix my error from the previous step, but I attempted to move onto these steps. I was able to successfully follow until steps 4-5 from Professor Williams' instructions. I kept receving the following error code: ImportError: cannot import name 'Base' from 'gcp' (./gcp.py). 

## 5. Errors
I ran into man few errors while completing this assignment that did not allow me to complete the assignment. I was unsure of how fix the errors. 
1. I could not open the flask section and kept receiving error codes of jinja2.exceptions.TemplateNotFound: base.html. I could not figure out what was causing this issue, as the code was taken from a previous assignment. i attached screenshots of the error code in the screenshots folder.
2. As explained in section 4, I could not run the Alembic section properly. I kept receving ImportError: cannot import name 'Base' from 'gcp' (./gcp.py) error code and attached screenshtos of it in the screenshots folder.



