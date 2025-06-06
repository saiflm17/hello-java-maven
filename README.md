# hello-java-maven   TASK-8  EXPLANATION 

#STEP-1 : Am taking a New server with server configurations like server_name, AMI : amazon linux kernel 5.10, Instance_type : t2.micro, key_pair, security_group : All Traffic, EBS : 10 GIB .  After launching the server and am connecting the server through SSH .

#STEP-2 : to chnage the root user by using command .

- COMMAND : sudo -i - To change the root user .

- #STEP-3:- am installing jenkins. so jenkins before am installing java-17 version because of jenkins dependency java so am installing java-17 version.

- so am collecting jenkins.io there are two repos am collecting there.

- COMMAND: yum install java-17-amazon-corretto -y.

- COMMAND: yum install jenkins -y.

- so now actually jenkins it is a service so we have to start the jenkins service.

- COMMAND: systemctl start jenkins - To start the jenkins service.

- COMMAND: systemctl status jenkins - To check the status of the jenkins service.

- COMMAND: yum install git -y .

- Now am Accessing jenkins dashboard with publicIP:8080 . And 8080 is a jenkins port number .

- After i will give some credentials to login jenkins dashboard .

- Now am creating a New Repository and the Repository_Name : hello-java-maven .

- here am taking two files .

   1 . pom.xml
   2 . src/main/java/HelloWorld.java .

- am taking java project source code hello world .

- After i Came jenkins dashboard .

- Now am creating a New Job and Job_Name : deployment . am selecting a FreeStyle Project.

- Afetr Go to manage jenkins 🡢 Global Tool Configuration 🡢 Add Maven 🡢 Name: mymaven   version : 3.8.6 .

- Now am configure to Job .

- select the job 🡢 go to configure 🡢 select Git and give repository_url 🡢 branch : main .

- After in Build Section , select : Invoke top-level Maven targets .

- Name : mymaven  ,  GOAL : clean package .

- save and build the job .

- so my build is successful and also checks the Console Output .

- and target folder also created and inside the target folder jar file is created .

- java/Maven projects deployed in TOMCAT application server .

- And artifacts stored in NEXUS REPOSITORY .

- Artifacts means war, ear, jar files .

- cd /var/lib/jenkins - jenkins default path .
