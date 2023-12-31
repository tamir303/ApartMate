# README #

*Hello and welcome to Apartmate's README file!*

This README would help you to set up the project's application and running, please make sure you
follow the following steps precisely.

**Please be notified that the project has been edited in IntelliJ workspace**

### Initial Steps For Setting the Project's Environment ###

* Open IntelliJ IDE
* Press on 'File' on the left side of the screen
* Press the 'Open' option and afterward go to the extracted folder path and select it
* Right-click on the project's name and press 'Open Module Settings' at the bottom of the menu
* Go to tab 'Dependencies', press on the '+' sign, and import your Spring modules
* Select 'openjdk-19 (Oracle OpenJDK version 19.0.2)' or any jdk 17+
* Press on 'Apply' and then press 'Ok'

After you have done all the previous steps now let's configure the
resources root folder and the source root folder.

### Gradle setup ###

* Click on the 'File' in the upper left corner of the window
* Select the 'Settings' option
* Select the 'Build, Execution, Deployment' option
* Select 'Gradle'
* On 'Gradle JVM' option make sure you have checked for 'correcto-17'
* In case you don't have correcto-17 click on 'Download JDK'
* Under 'version' please select 17, and under 'vendor' please choose 'Amazon Correcto 17.0.6'

When hitting the run button, gradle should download all the dependencies by itself and tomcat should be up and running.


### Tests ###

* Make sure your `MongoDB` does ***NOT*** have any Test database on it, or that at least it's completely empty.
* The test database is created upon running the test's, no need to create it by yourselves.
* There are plenty of tests and some of them are for asynchronous methods, so please be patient until all tests are finished.
* ***IMPORTANT*** the test database is different from the original database, so no need to worry about that.
* Don't delete the original one by accident ;)

*Thank you for your time and enjoy our application! :)*
This repository is exclusive to the use of docker, it includes all miniapps except expenseTracker.

### Setup Steps 

* First, clone or download the project repository.

### 1 - Install Docker & docker-compose on linux

```
sudo apt update
sudo apt upgrade
sudo apt install lsb-release ca-certificates apt-transport-https software-properties-common -y
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt install docker-ce
sudo apt install docker-ce docker-ce-cli containerd.io docker-compose-plugin
```

### 2 - Run The docker-compose ###

* Enter the repository root directory
* Run ``` docker-compose up --build ```

### 3 - Use the project miniapps ###

* Server - ``` http://localhost:8083 ```
* Shop - ``` http://localhost:3000 ```
* Chat - ``` http://localhost:3001 ```
* Professionals - ``` http://localhost:3002 ```
