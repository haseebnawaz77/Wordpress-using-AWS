# Wordpress-using-AWS
Hosting a Wordpress site using AWS Technology (RDS instance and EC2 instance)

</br></br></br>
### EC2 Instance
###### Pass the bootstrap script in the resources in the "user data" section when configuring an instance
![image](https://user-images.githubusercontent.com/52587103/75938983-12468a80-5e57-11ea-8aae-15358ad7a3d9.png)
</br>
###### Allow port 80 and SSH from only your IP address for safer practice 
![image](https://user-images.githubusercontent.com/52587103/75942023-53429d00-5e5f-11ea-8291-7d4e15e5323b.png)

![image](https://user-images.githubusercontent.com/52587103/75942028-576eba80-5e5f-11ea-8c00-2e5ddf58a523.png)

</br></br></br>
________________________________________________________________________________________________________________________________________
________________________________________________________________________________________________________________________________________
### RDS Instance
Configure the settings of the RDS system and launch it 

![image](https://user-images.githubusercontent.com/52587103/75939077-402bcf00-5e57-11ea-86ef-bcf9ee009521.png)
</br></br>

##### Caution - remember to give your database a name or it will NOT be created. 
###### We will need the name of the database and its password and also the user of the database and its password for future reference
![image](https://user-images.githubusercontent.com/52587103/75941189-052c9a00-5e5d-11ea-9b4e-ceafe5c3f2e8.png)

</br>

![image](https://user-images.githubusercontent.com/52587103/75941801-9e0fe500-5e5e-11ea-9338-d1c0e2771738.png)
</br></br></br>

________________________________________________________________________________________________________________________________________
________________________________________________________________________________________________________________________________________


### Security Groups
###### The security groups for the Web Server and RDS instance
![image](https://user-images.githubusercontent.com/52587103/75942036-5d649b80-5e5f-11ea-8fd3-aff8deca04db.png)



###### Edit the security group of the RDS instance to only allow communication from the webserver’s Security group on port 3306
![image](https://user-images.githubusercontent.com/52587103/75942052-6bb2b780-5e5f-11ea-90e3-5121e7d462b6.png)

</br></br></br>
________________________________________________________________________________________________________________________________________
________________________________________________________________________________________________________________________________________
### Initializing

###### Head over to your webserver EC2 instance and grab the DNS and enter it in ur browser
![image](https://user-images.githubusercontent.com/52587103/75942068-72d9c580-5e5f-11ea-91f5-8d142a54bf74.png)


###### The following web page should be prompted


![image](https://user-images.githubusercontent.com/52587103/75941219-12e21f80-5e5d-11ea-870f-49d283ea86ce.png) </br></br>

##### Enter the correct information 
###### * Database Name = Initial database Name(RDS)
###### * Database Host = The endpoint of your RDS instance, grab the endpoint and paste it here
![image](https://user-images.githubusercontent.com/52587103/75941225-170e3d00-5e5d-11ea-8fde-98d60ce72eed.png)

</br></br></br>


###### We need to write this php file in our Web server instance. 
###### Copy the contents of this file

![image](https://user-images.githubusercontent.com/52587103/75941233-1b3a5a80-5e5d-11ea-8f50-4b7eb308ae15.png)</br>


###### SSH into your Web Server(EC2 instance)
![image](https://user-images.githubusercontent.com/52587103/75939213-93058680-5e57-11ea-851c-a063b4669a58.png)</br>

###### Paste the following contents in this file and save it with the name “wp-config.php”

![image](https://user-images.githubusercontent.com/52587103/75939230-9ac52b00-5e57-11ea-9878-bf10fe11be95.png)

</br></br></br>
________________________________________________________________________________________________________________________________________
________________________________________________________________________________________________________________________________________
### Finishing off

##### After you have done that, go back to the wordpress web page and click “Run the Installation”
If everything was done correctly, this page should be prompted 

![image](https://user-images.githubusercontent.com/52587103/75941246-21303b80-5e5d-11ea-9327-55177fe4bc4c.png)




###### Enter in the details and click confirm
![image](https://user-images.githubusercontent.com/52587103/75941255-255c5900-5e5d-11ea-8d02-47a6c37058d5.png)

</br></br></br>
________________________________________________________________________________________________________________________________________
________________________________________________________________________________________________________________________________________
### Your WordPress site is ready! Hosted on an AWS EC2 instance and RDS instance
![image](https://user-images.githubusercontent.com/52587103/75942079-7a996a00-5e5f-11ea-85bb-37b63552d50e.png)















