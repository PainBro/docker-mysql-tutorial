# Docker Mysql Container Connection Tutorial

## The connection pattern is now very simple:

Docker must be functional on your device.
Clone the git repo to your computer.
Open a terminal/powershell/CommandPrompt window in the git repo.
Run the command docker-compose -p mycomposer -f docker-compose.yml up -d
Wait until the terminal says it's done, then wait about 40 seconds more.
Connect to sqlpad at localhost:3000 using admin@sql.pad and password123
The connection needed to connect to the mysql container is now preprogrammed into the sqlpad container under the name 'pickle' because I was making the names.