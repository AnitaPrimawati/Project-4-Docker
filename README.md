# Project-4-Docker

Tools : Docker and Python
Step by step to migrate data using Docker and Python: :

Step 1: Open and Start Docker Make sure Docker is installed on your computer and start Docker Desktop.
Step 2: Create docker-compose.yml Create the docker-compose.yml file and declare the services for MySQL and Postgres.
Step 3: Run MySQL and Postgres Container Run the docker-compose up -d command to make MySQL and Postgres Image run as containers separately. If you want them to run in the background, add the -d option.
Step 4: Log into the MySQL Container Terminal Use the docker exec -it <container_id> bash command to log into the MySQL container terminal.
Step 5: Login to MySQL Database Enter the mysql --local-infile=1 -uroot -pmysql operational < /docker-entrypoint-initdb.d/init.sql command to login to the MySQL database.
Step 6: Enable Local Infile If an error occurs regarding the local infile, run the SET GLOBAL local_infile = 1; query within the MySQL database, then re-run the LOAD DATA LOCAL INFILE query.
Step 7: Set up the Python Virtual Environment Open a terminal and enter the scripts directory. Create and activate the Python virtual environment using the python3 -m venv env and source env/bin/activate commands (or env/Scripts/activate in Windows).
Step 8: Install Python Requirements Install the required Python packages with the python3 -m pip install -r requirements.txt or pip install -r requirements.txt command.
Step 9: Create a Database in Postgresql Log into the Postgresql container with the docker exec -it <postgres_container_id> bash command. Next, log into the Postgresql database with the root user using the psql -Upostgres command. Create a new database named data_warehouse with the command CREATE DATABASE data_warehouse;.
Step 10: Select Database and Create Tables Select the new database that has been created with the \c data_warehouse command. Next, list the tables in the database with the \d command.
