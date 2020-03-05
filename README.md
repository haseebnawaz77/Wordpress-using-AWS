# Wordpress-using-AWS
Hosting a Wordpress site using AWS Technology (RDS instance and EC2 instance)

</br></br>
### EC2 Instance
###### Pass the bootstrap script in the resources in the "user data" section when configuring an instance
![image](https://user-images.githubusercontent.com/52587103/75938983-12468a80-5e57-11ea-8aae-15358ad7a3d9.png)
</br>
###### Allow port 80 and SSH from only your IP address for safer practice 
![image](https://user-images.githubusercontent.com/52587103/75939050-386c2a80-5e57-11ea-8d2a-346155145c98.png)

![image](https://user-images.githubusercontent.com/52587103/75939066-3bffb180-5e57-11ea-886b-9ce933bbdf5e.png)

</br></br>
### RDS Instance
Configure the settings of the RDS system and launch it 

![image](https://user-images.githubusercontent.com/52587103/75939077-402bcf00-5e57-11ea-86ef-bcf9ee009521.png)
</br>

##### Caution - remember to give your database a name or it will NOT be created. 
###### We will need the name of the database and its password and also the user of the database and its password for future reference
![image](https://user-images.githubusercontent.com/52587103/75941189-052c9a00-5e5d-11ea-9b4e-ceafe5c3f2e8.png)

</br>
###### The database is now available
![image](https://user-images.githubusercontent.com/52587103/75939099-50dc4500-5e57-11ea-8414-2751fb2a316b.png)
</br></br>

### Security Groups
The security groups for the web server and RDS instance
![image](https://user-images.githubusercontent.com/52587103/75939119-5afe4380-5e57-11ea-81c3-7ec46d1c5ed9.png)

Edit the security group of the RDS instance to only allow communication from the webserver’s Security group on port 3306
![image](https://user-images.githubusercontent.com/52587103/75939135-62bde800-5e57-11ea-8744-ac243dfdcb54.png)

</br></br>

### Initializing

###### Head over to your webserver EC2 instance and grab the DNS and enter it on ur browser
![image](https://user-images.githubusercontent.com/52587103/75939172-7701e500-5e57-11ea-897a-7465a2e8fb30.png)

###### The following Web page should be prompted


![image](https://user-images.githubusercontent.com/52587103/75941219-12e21f80-5e5d-11ea-870f-49d283ea86ce.png)

![image](https://user-images.githubusercontent.com/52587103/75941225-170e3d00-5e5d-11ea-8fde-98d60ce72eed.png)



###### We need to write this Php file in our Web server instance. 
###### Copy the contents of this file

![image](https://user-images.githubusercontent.com/52587103/75941233-1b3a5a80-5e5d-11ea-8f50-4b7eb308ae15.png)


###### SSH into the server
![image](https://user-images.githubusercontent.com/52587103/75939213-93058680-5e57-11ea-851c-a063b4669a58.png)

###### Paste the following contents in this file and save it with the name “wp-config.php”

![image](https://user-images.githubusercontent.com/52587103/75939230-9ac52b00-5e57-11ea-9878-bf10fe11be95.png)

</br></br>
### Finishing off

##### After you have done that, go back to the wordpress web page and click “Run the Installation”
If everything was done correctly, this page should be prompted 

![image](https://user-images.githubusercontent.com/52587103/75941246-21303b80-5e5d-11ea-9327-55177fe4bc4c.png)




###### Enter in the details and click confirm
![image](https://user-images.githubusercontent.com/52587103/75941255-255c5900-5e5d-11ea-8d02-47a6c37058d5.png)

</br></br>
### Your WordPress site is ready! Hosted on an AWS EC2 instance and RDS instance
![image](https://user-images.githubusercontent.com/52587103/75941266-2a210d00-5e5d-11ea-95d0-ac6ed2c58113.png)
 













