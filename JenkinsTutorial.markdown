### Jenkins Tutorial
---
 Author: Monil Jhaveri 
 Version History 



| Version #  | Date |
|:-----------:|:-------------:|
| 1.0.0     | 2/3/2017 |


#### Purpose
- To guide a developer to create a simple Jenkins build server   
#### Installation (Ubuntu)
- Installing Jenkins 
```bash  
wget -q -O - https://pkg.jenkins.io/debian/jenkins-ci.org.key | sudo apt-key add -
sudo sh -c 'echo deb http://pkg.jenkins.io/debian-stable binary/ > /etc/apt/sources.list.d/jenkins.list'
sudo apt-get update
sudo apt-get install jenkins
```   
- Check if installation is running  
	- On local machines navigate to 
	```bash 
	localhost:8080 
	``` 
	- On host machines navigate to 
	```bash 
	HostMachineIP:8080	
	```
- Setting Up Jenkins 
	- Jenkins Password - located in 
	```
	/var/log/jenkins/jenkins.log
	```
	- Copy password and paste password into login screen in browser  
	- Install Plugins 
		- Install suggested plugins  
		- Custon Install plugins 
			- Email Extension Plugin
			- Mailer Plugin 
			- SSH Slaves Plugin 
			- Github Plugin 
			- Ant Plugin 
			- Gradle Plugin 
			- build timeout Plugin 
			- Config File Provider Plugin 
			- Credentials Binding Plugin 
			- Folders Plugin 
			- OWASP Markup Formatter Plugin 
			- Matrix Authorization Strategy Plugin 
			- PAM Authentication Plugn 
			- LDAP Plugin 
- Setup Administrator Account 
- Setting Up a Test Project 		
	- Configuring Project 
		- Setting up Github integration 
			- add project url and github url:  
			<img src="/home/nextdroid/develop/jenkins/ContinousIntegrationTestRepo/githubIntegration.jpeg" width="400" lenght="200">
		- Add Github authenication 
	- Adding build steps 
		- Jenkins supports bash integration 
	- Running Test Build 
		- Hit build now button:

		 <img src="/home/nextdroid/develop/jenkins/ContinousIntegrationTestRepo/Buildnow.png" width="400" length="200">
	- Finished Basic Setup! 
	
- Triggering Build on Every Push 
	- Setting Up localhost tunnelling 
		- Install ngrok 
		- [Download](https://ngrok.com/download)
		- Installing ngrok in Ubuntu and tunneling to localhost			
	``` 
	unzip  /path/to/ngrok.zip  && ./ngrok http 8080 
	```

	- copy new *.io address 
	-  go to the github repo and hit settings
	- hit webhooks and paste the *.io/github-webhook/ into the payload url 		

	<img src="/home/nextdroid/develop/jenkins/ContinousIntegrationTestRepo/webhooks.png" width="400" length="200">

	- Configuring Jenkins 
		- Navigate to project 
		- Hit Configure 
		- Check the Github hook trigger for GITScm polling 
 
	<img src="/home/nextdroid/develop/jenkins/ContinousIntegrationTestRepo/GITScm.png" width="400" length="200">
	
		
		 
	
			
 
