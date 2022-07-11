# Setting up a SQL Server in Docker

### Prerequisites
* Have a knowledge of Docker
* Have Docker installed
* Cloned this repository

### Creating the Docker Container
1. In a terminal (Bash/Shell/ect.) navigate to the directory with the <code>docker-compose.yml</code> file
2. Run the command <code>docker-compose -p mycomposer -f docker-compose.yml up -d</code>
  
  This will do many things:
  * Build a container for mysql_server and sqlpad
  * Run a 2 sql files on the sql server that will create and populate a database and table
  * Set up all environmental variables for the sql server to allow remote connections
  * Set variables for sqlpad that will create a connection to our sql server automatically

3. Open a browser to <code>localhost:3000</code> to open sqlpad (may need to wait a few seconds for the script to finish running)

### Resources
* 
