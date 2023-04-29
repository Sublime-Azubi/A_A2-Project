# A_A2-Project
```diff
+ This is an upgraded version of of guest list application
```
--- 
## TEAM MEMBERS:

1. [Brian Gitau](https://www.linkedin.com/in/brian-gitau-520430137/)
2. [Amos M ogaka Nyaburi](https://www.linkedin.com/in/amos-nyaburi/)
3. [Christopher Yongo](https://www.linkedin.com/in/chris-yongo-a6178527/)
4. [Ifeanyi Okeibunor](https://www.linkedin.com/in/ifeanyi-ambrose-okeibunor/)
4. [Eva Naomi Njoroge](https://www.linkedin.com/in/eva-naomi-njoroge-ab26944b/)
5. [Nana Esi Ashun-Cobbina](https://www.linkedin.com/in/nana-esi-a-2341aa157/)
6. [Emmanuel Bassey](https://www.linkedin.com/in/drillebassey/)
7. [Uwimana Alphonsine](https://www.linkedin.com/in/uwimana-alphonsine-90023b108/)
8. [Ebenezer Kuku](https://www.linkedin.com/in/thekukuebenezer/)


## PROJECT OVERVIEW
In project 1 version 2, we have created a simple web page that allows visitored to register and submit their information through a UI. In this project , we will create a dynamic webpage that will automatically populate a backend databae with the users informations. Terraform will be uses to automate the deployment of DynamoDB tables and would to dynamically populate a backend database with the users' log in information with the help of php-composer.

![Architecture](https://user-images.githubusercontent.com/104580680/235295691-9b1091e2-1236-4065-a836-753ab7051895.JPG)

#### We will begin this project by revamping the UI of our web page from V2 Project. Thereafter, dockerize the  application and save the image in docker hub.
![Architecture](/artifacts/login%20page.png)

## PROJECT MANAGEMENT TOOL
 For this project, Gitbub project is used as a project management tool to track progresses on project tasks and manage sprints and& timelines
![project](/artifacts/github%20project.JPG)
   
## TASK LIST
- [x] Automate Dynamodb deployment using Terraform
- [x] Link Dynamo to webpage using aws SDK and php-composer
- [x] Package and deploy project version 3  


## CHALLENGES ACOUNTERED:
1. **Docker Installer error:** <br>
```diff
- _Creating “rootNode” subnodes: constructing “BackendServices” in “rootNode”: writing locks to lock-directories: reading path to AppData\Roaming\Docker\locked-directories: parsing JSON: invalid character "\x00". looking for the beginning of value_
```
** SOLUION:**<br>
 Located and deleted the locked directories file and when docker desktop started again, a new locked file was created.
 
2. Terraform failure due to symantic and syntax error: we werer able to resolve this after several hours of concerted troubleshooting effort from teammates.
3. Also the decralring multiple Attributes of the dynamodb in the teraform file caused the terraform plan to fail. the was reuired that the attributes be indexed first. <br>
**SOLUTION**: Instead of indexing the intire list of attributes, Onely one attribute was declared. this is because dynamodb does not neccessarily require declaration of all table attribles during table creation. Atrributes can be addded on demand

## DEPLOYMENT OF DYNAMODB TABLE
### What is Dynamodb
* **Amazon DynamoDB** is a fully managed NoSQL database service that provides fast and predictable performance with seamless scalability.
* Terraform was used to automate the deployment of Amazon dynamodb table which would serve as storage for the application and also used to insert set of data in the table
* Source code is available in the repository
* A major requirement for a susccessful deployment of dynamodb Table is an access to AWS Account. We Configure Aws account Identity and Access Management to allow programmatic access and access to DynamoDb.

* Obtain the secret keys and access ID. Store them in a separate file locally

### What is Terraform?
* **Terraform** is an open-source infrastructure as code software tool that provides a consistent CLI workflow to manage hundreds of cloud services (resources). Terraform codifies cloud APIs into declarative configuration files.

### Basic Terraform Commands
<html>
<body>
 <p><p>terraform init  – initialize the plugin as per the code</p>
 <p>terraform fmt      – neatly formats the terraform code</p>
 <p>terraform plan     – highlights on the code to be implemented and whether the configurations are correct</p>
 <p>terraform apply    – applies/runs the code to create our resources</p>
 <p>terraform destroy  - to kill and remove all the code and infrastructure build. Totally remove the programs built by terraform.</p> 
</body>
</html>

## LINK DYNAMODB
Using AWS SDK and php-composer the dynamodb is linked to the application. the composer automatically populated the dynamodb table with uder information from the web application  page

The **php-composer** is a dependency manager for PHP. It also has its own autoloader to enable autoloading.
1. Download composer https://getcomposer.org
Make composer globally or locally.
Require your first package.
2. Create a composer.json file that will declare to composer, the vendor's name you would like to install.
composer.lock will point to the version currently installed.
Composer Install
This looks for a Composer.lock file exists. If none exists, “composer update” will automatically run to create the composer.lock file. If composer.lock file exists, then install the declared dependencies from here (working directory).

1. Download composer https://getcomposer.org
Make composer globally or locally.
Require your first package.

## PACKAGE AND DEPLOY APPLICATION
This involved dockerizing the entire application and shipping to a public repository. dockerhub is used in this case.
First step is to write a docker file for the entire application and build  using the "docker build" command

## 4 Simple steps to push  image to docker hub:
docker login --username username
prompts for password. If you omit --password which is recommended as it does not store it in your command history.
docker tag my-image username/my-repo. 
docker tag docker-web-app:3.0 username/docker-web-app:3.0
docker push username/my-repo.
docker push username/docker-web-app:3.0


