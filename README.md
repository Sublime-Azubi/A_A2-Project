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


We will begin this project by revamping the UI of our web page from V2 Project. Thereafter, dockerize the  application and save the image in docker hub.

   
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

## DEPLOYMENT OF Dynamodb 



## LINK DYNAMODB


## PACKAGE AND DEPLOY APPLICATION
   
