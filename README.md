# CMPE-272-Assignments-labs

<li>Lab HW 1</li>

<li>Lab HW 2 - Web Env Site</li>

<li>Lab HW 3 - Secure Site</li>

# SSh your ec2 instance:

Install apache and php server to have the enivronment to host php website 

sudo yum install httpd php

Now cd /var/www/html 


# Open your local cmd and use scp to copy your locally developed php website files to the ec2 server

cd path in pem key and php files.

scp -i demo281.pem -r ./phphw/* ec2-user@52.91.65.223:/var/www/html

Now ls and verify the files transfered from local to the server.

![image](https://github.com/Skillz619/CMPE-272-Homework/assets/43133388/e9c842b5-16ba-48fc-abe3-de4867187789)

Now open the public ip address of your ec2 instance

![image](https://github.com/Skillz619/CMPE-272-Homework/assets/43133388/2b533ac8-ed12-4774-a821-3f5f5e71bf47)

you can see the website hosted on your ip 

![image](https://github.com/Skillz619/CMPE-272-Homework/assets/43133388/f73d33e1-a2f4-49d4-ae3a-393aa01f976d)

Now configure your route53 

![image](https://github.com/Skillz619/CMPE-272-Homework/assets/43133388/499385d5-e324-4f66-9e6a-ff57f6bce64a)

Add the required Nameservers and Cname and A servers in your hosting service.

![image](https://github.com/Skillz619/CMPE-272-Homework/assets/43133388/ce891b1e-f6cf-44f0-8dbd-205cddade6e4)


Once they are mapped you can see your website hosted on your domain - Shreekatsjsu.co
![image](https://github.com/Skillz619/CMPE-272-Homework/assets/43133388/14ad9c87-83f6-4b26-ab0d-4eefaa792dfa)


<h2>PHP HW - 3 Adding Secure Connection </h2>

sudo yum install certbot python2-certbot-apache

sudo certbot --apache

open editor 
sudo nano /etc/httpd/conf/httpd.conf

Add virual host for port 80:

<VirtualHost *:80>
    ServerName your-domain.com
    DocumentRoot /var/www/html
    # Additional configuration options (if needed)
</VirtualHost>


Restart Apache 

sudo systemctl restart httpd   # For CentOS/RHEL

sudo systemctl restart apache2  # For Ubuntu/Debian

Run the certbot again
![image](https://github.com/Skillz619/CMPE-272-Class-HW-Labs/assets/43133388/5b736cba-1c97-41a1-8e81-d7ede06dfb48)

sudo certbot --apache


We now have our HTTPS site secured

![image](https://github.com/Skillz619/CMPE-272-Class-HW-Labs/assets/43133388/dfbeaadd-15fa-4c4f-9251-e33fbe5df4c1)

admin

password123

Domain Used - [Shreekatsjsu.co](Https://Shreekatsjsu.co)

[Https://Shreekatsjsu.co](Https://Shreekatsjsu.co)


admin

password123
