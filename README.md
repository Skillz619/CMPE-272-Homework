# CMPE-272-Assignments-labs


<p align="center"> 
  Visitor count<br>
  <img src="https://profile-counter.glitch.me/CMPE-272-Assignments-labs/count.svg" />
</p>



<li><a href="https://github.com/Skillz619/CMPE-272-Class-HW-Labs/tree/main/phphw1">Lab HW 1</li>

<li><a href="#env">Lab HW 2 - Web Env Site</li>

<li><a href="#secure">Lab HW 3 - Secure Site</li>

<li><a href="#curl">Lab HW 4 - CURL Calls</li>

<li>Lab HW 5- User creation and Searching DB</li>

<li><a href="#movievote">May 2nd Lab - Vote - Jquery Mobile</a></li>

<li><a href="#termproject">Cross Domain Enterprise Online Market Place</a></li>


<h2 id="env">Lab HW 2 - Web Env Site</h2

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


<h2 id="secure">PHP HW - 3 Adding Secure Connection </h2>

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


Domain Used - [Shreekatsjsu.co](Https://Shreekatsjsu.co)

[Https://Shreekatsjsu.co](Https://Shreekatsjsu.co)


Username: admin

Password: password123


<h2 id="curl">Lab HW-4 CURL Calls</h2>

Company A,B and C 

![image](https://github.com/Skillz619/CMPE-272-Class-HW-Labs/assets/43133388/b37bc022-4b1f-424a-a201-3ca842823802)


Inserted database and tables 

![image](https://github.com/Skillz619/CMPE-272-Class-HW-Labs/assets/43133388/b72d12d0-7bb3-4253-8a03-7a0e924270cf)

Fetched the data from the sql lite database on the php webpage displayed. - VIA CURL calls - Company A
![image](https://github.com/Skillz619/CMPE-272-Class-HW-Labs/assets/43133388/cd1aaf4c-d965-49fc-925c-b348ad1abf72)

Fetched Company B via Curl calls from the SQL db
![image](https://github.com/Skillz619/CMPE-272-Class-HW-Labs/assets/43133388/d0d9f5d1-93fb-4951-8d87-cb865be8e7a0)

Fetched Company C via Curl calls from the SQL db
![image](https://github.com/Skillz619/CMPE-272-Class-HW-Labs/assets/43133388/3b7540e0-9536-4e82-aff9-88f66a933116)


All three Company Website Links - (https://shreekatsjsu.co/index.php?page=lab4)

<li> [Company A](https://shreekatsjsu.co/company_a.php) </li>

<li> [Company B](https://shreekatsjsu.co/company_b.php) </li>

<li> [Company C](https://shreekatsjsu.co/company_c.php) </li>



<h2 id="movievote">Lab May-2nd - Movie Vote - Jquery Mobile</h2>

[May -2nd - Vote-JQuery](https://github.com/Skillz619/CMPE-272-Class-HW-Labs/tree/main/May-2nd-Lab)

![image](https://github.com/Skillz619/CMPE-272-Class-HW-Labs/assets/43133388/9dea5349-84e9-44fb-9f4c-a5efff81767d)


Pre - Loaded the choices upto 10 movies

![image](https://github.com/Skillz619/CMPE-272-Class-HW-Labs/assets/43133388/7f9f3e86-4afe-46e0-99cf-eaee9e1537b6)


![image](https://github.com/Skillz619/CMPE-272-Class-HW-Labs/assets/43133388/2d07a12f-172c-45c0-9ebb-f6124fef057d)


Build Deployed via Netlify and Link to access - https://272lab-movie-vote-shreekar.netlify.app/


<h2 id="termproject">Cross Domain Enterprise Online Market Place</h2>

Term Project - Cross Domain Enterprise Online Market Place - [Github Repo](https://github.com/Skillz619/272-project-Shopstop.git)


