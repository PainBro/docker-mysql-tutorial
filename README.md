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
  * Run 2 sql files on the sql server that will create and populate a database and table
  * Set up all environmental variables for the sql server to allow remote connections
  * Set variables for sqlpad that will create a connection to our sql server automatically

3. Open a browser to <code>localhost:3000</code> to open sqlpad (may need to wait a few seconds for the script to finish running)

Login using the email address and password that was setup in the <code>my.env</code> in the <code>sqlpad_env_file</code> folder
* admin@sql.pad
* password123

### Resources
* https://medium.com/codex/docker-compose-explained-3954baf495ec
* https://github.com/byuibigdata/docker_guide/blob/main/docker-compose.yml
* https://dagshub.com/blog/setting-up-data-science-workspace-with-docker/
* https://github.com/byuibigdata/docker_guide

#### Additional Resources for further Study
* Deploy a Docker container onto Heroku - https://medium.com/featurepreneur/how-to-deploy-docker-container-on-heroku-part-2-eaaaf1027f0b
