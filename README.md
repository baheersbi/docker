# docker
Explore containerization with our Docker Tutorials repository. Perfect for beginners and seasoned devs alike, it guides you from basic setups to advanced deployments, offering practical examples and best practices.

## Get Started
1. Download Docker from https://www.docker.com/products/docker-desktop/
   > Mac users should verify their chip type before downloading by going to the Apple icon on the top left corner and selecting ```About This Mac.```
2. Install it on [Windows](https://docs.docker.com/desktop/install/windows-install/) or [Mac](https://docs.docker.com/desktop/install/mac-install/)
3. Start Docker Desktop
   > Windows users may find a Desktop icon to Start Docker Desktop and the Mac users can find it at ```Applications``` folder
5. Open a terminal/command prompt:
   - Mac Users: Open a new Terminal window ```Applications -> Utilities -> Terminal```
   - Windows Users: Go to Search in ```Start``` menu and find ```Command Prompt```
6. Pull ```MySQL``` image: Once the Terminal or Command Prompt is opened, please type ```docker pull mysql``` and Press Enter
7. Run ```MySQL``` instances or containers: Based on our requirements, we need to initiate three MySQL servers, each using a distinct port number.
   - In you Terminal or Command Prompt window type the following command/s and presee Enter
     - Running Server 1: 
       - ```docker run --name server1 -e MYSQL_ROOT_PASSWORD=_your_password_ -p 3307 -d mysql```
     - Running Server 2: 
       - ```docker run --name server2 -e MYSQL_ROOT_PASSWORD=_your_password_ -p 3308 -d mysql```
     - Running Server 3: 
       - ```docker run --name server3 -e MYSQL_ROOT_PASSWORD=_your_password_ -p 3309 -d mysql```
     > You can run as many servers as you like using the above command but you should change the name and port number
8. Verify the running status of your MySQL servers by typing ```docker ps``` and it will return a list of servers which are currently running.
9. Login to the MySQL Servers:
   > The password is not visible when you type.
11. Open three Terminal or Command Prompt Windows and execute the following commands:
    - Terminal/Command Prompt 1: ```docker exec -it server1 mysql -P 3307 -u root -p``` and press enter and then your password. 
    - Terminal/Command Prompt 2: ```docker exec -it server2 mysql -P 3308 -u root -p``` and press enter and then your password.
    - Terminal/Command Prompt 3: ```docker exec -it server3 mysql -P 3309 -u root -p``` and press enter and then your password.
