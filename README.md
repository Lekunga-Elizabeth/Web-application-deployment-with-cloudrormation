# Web-application-deployment-with-cloudrormation

this is a 3 tier web application 
To successfull run this template we modify the code by adding the tag option so as to have the ec2 instance name. when running this code i had a roll back and discovered that my key under tag was writing in small letters so i changed it to capital letters "K"

to update your stack or instance name use the command: aws cloudformation update-stack --stack-name wokers1stack --template-body file://cloudformation-template.yaml 

 Looking at this at this image you will see the original instance name as compudemy-instance
![instance updated](https://user-images.githubusercontent.com/116527791/235403260-1d2c6e60-c471-4a8b-85e6-5f1e54b74986.jpg)

after changing the instance name, to family instance for example and runing the update command it will autommatically update in your console. see immage below

![family instance update](https://user-images.githubusercontent.com/116527791/235403546-73389b45-a446-4ad1-a5c7-44bc4eb69202.jpg)

it is a good practise to create your security group using the code.



The next step after we deploy the instance and it is up and runing is for us now to run the RDS resources but befor we do that we need to define the security groups idenfifying the inbound and outbound rule for each

- The immage below descripe the security group of our RDS, thsi indicate that the he RDS database  allows inbound traffic only from  the internet comming form our EC2 instance  that is why we open port 80 but with the security group id sources from ec2 and outbound traffic only to the Internet. 

![security-group](https://user-images.githubusercontent.com/116527791/235413198-d1c2a544-e669-418f-a941-6b60df459140.jpg)




