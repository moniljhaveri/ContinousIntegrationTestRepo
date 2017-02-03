### Jenkins Tutorial 
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
			![](/home/nextdroid/develop/jenkins/ContinuousIntegrationTestRepo/githubIntegration.jpeg)
		- Add Github authenication 
	- Adding build steps 
		- Jenkins supports bash integration 
	- Running Test Build 
		- Hit build now button: ![](/home/nextdroid/develop/jenkins/ContinuousIntegrationTestRepo/buildnow.png)
	- Finished Basic Setup! 
- Triggering Build on Every Commit 
	
	
	

