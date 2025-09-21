# userdata
ec2 modules and security group modules with apache2 userdata

# Task (1)
### Login to your aws and ssh to your terminal
<img width="1035" height="682" alt="Screenshot 2025-09-21 at 6 20 13 pm" src="https://github.com/user-attachments/assets/e7f33672-02c9-4f9d-830a-d175bfc8af6e" />

### create a directory call terraform-ec2-apache and cd in to it 
<img width="655" height="46" alt="Screenshot 2025-09-21 at 5 51 13 pm" src="https://github.com/user-attachments/assets/cd5f76d9-9782-4f89-9912-ed83a4eb5531" />

### make an other directory call modules/ec2 to make this directory you need run mkdir -p modules/ec2
<img width="946" height="85" alt="Screenshot 2025-09-21 at 5 54 16 pm" src="https://github.com/user-attachments/assets/3be63c96-727b-41d8-85b6-e1314d29f462" />


### cd in to the modules and also cd into the ec2 inside the ec2 create a file with touch main.tf
<img width="901" height="276" alt="Screenshot 2025-09-21 at 6 01 10 pm" src="https://github.com/user-attachments/assets/80625d25-e032-4795-bba7-0764a90ca9b0" />

### open the file with vim main.tf and write a terraform code
<img width="1262" height="900" alt="Screenshot 2025-09-21 at 6 02 47 pm" src="https://github.com/user-attachments/assets/11c1b095-89f9-4496-a567-8e673d8bea19" />

### Now create a security group.
<img width="1210" height="533" alt="Screenshot 2025-09-21 at 6 10 22 pm" src="https://github.com/user-attachments/assets/2f0af4a1-f372-4f29-9cd6-216a52c20432" />

# Task (2)

### Now create a new directory on the project directory and name it modules/security_group use the come mkdir -p modules/security_group

### cd into the cd security_group ls to check it and use touch command to create your main.tf

<img width="998" height="280" alt="Screenshot 2025-09-21 at 6 40 27 pm" src="https://github.com/user-attachments/assets/ceb16b23-4cba-4877-a8ee-ffa704d575a4" />

### open the main.tf file and write your terraform code inside the file "vim main.tf"


<img width="1262" height="900" alt="Screenshot 2025-09-21 at 6 48 27 pm" src="https://github.com/user-attachments/assets/10a2bc4e-7762-4574-8ae3-e6164f298876" />

# Task (3)

### Let create a file sparately by using touch apache_userdata.sh

<img width="1063" height="101" alt="Screenshot 2025-09-21 at 7 07 18 pm" src="https://github.com/user-attachments/assets/c9b614a8-29a0-4392-bb4c-b954335efcae" />

### On this part you need to install apache2 and start the apache and enable the apache using the command below
#!/bin/bash
sudo apt update
sudo apt install -y apache2
sudo systemctl start apache2
sudo systemctl enable apache2
echo "<h1>Hello from Apache on EC2</h1>" | sudo tee /var/www/html/index.html

<img width="1262" height="766" alt="Screenshot 2025-09-21 at 7 12 10 pm" src="https://github.com/user-attachments/assets/47fe35c0-092b-4829-93a3-e66d814286a7" />


# Task (4)


### Let create a file sparately by using touch apache_userdata.sh
<img width="1063" height="101" alt="Screenshot 2025-09-21 at 7 07 18 pm" src="https://github.com/user-attachments/assets/c9b614a8-29a0-4392-bb4c-b954335efcae" />

### open the file call with vim apache_userdata.sh


<img width="1262" height="900" alt="Screenshot 2025-09-21 at 7 51 45 pm" src="https://github.com/user-attachments/assets/7b7290c7-72c0-47f2-be00-718aea31b390" />


### Now we have to install terraform 


<img width="881" height="291" alt="Screenshot 2025-09-21 at 7 40 38 pm" src="https://github.com/user-attachments/assets/ed410757-d362-491e-b0af-9f5f0cb38be3" />

### next step Install required dependencies
<img width="1128" height="173" alt="Screenshot 2025-09-21 at 7 41 13 pm" src="https://github.com/user-attachments/assets/a5f8e608-61c0-45e9-975f-a8288b586f5d" />

### Add the HashiCorp GPG key (so apt can verify packages)

<img width="1050" height="58" alt="Screenshot 2025-09-21 at 7 42 07 pm" src="https://github.com/user-attachments/assets/996c15a0-4029-4987-a999-097022d27278" />

### Add the official HashiCorp Linux repository

<img width="1440" height="383" alt="Screenshot 2025-09-21 at 7 42 48 pm" src="https://github.com/user-attachments/assets/b5fba750-27e8-4afc-9aae-aec8b7f6cd6f" />

### now you have to update by runing this command sudo apt update 
<img width="1440" height="249" alt="Screenshot 2025-09-21 at 7 43 36 pm" src="https://github.com/user-attachments/assets/e4d0d5eb-58c7-4880-a91d-b4c2cbfe446f" />

### Install Terraform "sudo apt install terraform -y"

<img width="1030" height="390" alt="Screenshot 2025-09-21 at 7 44 06 pm" src="https://github.com/user-attachments/assets/aff29fa4-01f6-4785-8ba0-44282813e7f2" />

### run terraform -version to know if the terraform is fully installed 

<img width="1241" height="82" alt="Screenshot 2025-09-21 at 7 44 35 pm" src="https://github.com/user-attachments/assets/ed3171bf-817c-4684-b1fa-98cc006cb150" />


