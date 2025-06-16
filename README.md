# AltSchool Landing Page – Semester Project

This repository contains the implementation of a dynamic landing page built as part of the second semester AltSchool Cloud Engineering project.

## Project Overview

This project showcases a professionally deployed, responsive landing page enhanced with animations and interactive sections. It is hosted on a Linux server environment using Nginx and was created to demonstrate deployment, system setup, and frontend development skills.

>  Live Project URL: [http://172.17.136.103/dynamic-landing-page/](http://172.17.136.103/dynamic-landing-page/)
>  URL: http://altschool.chickenkiller.com

---

## Screenshot

![Landing Page Screenshot](assets/landing-page.png)

---

##Tech Stack

- HTML5 & Tailwind CSS
- AOS.js for animations
- Nginx Web Server
- Git & GitHub for version control
- Ubuntu (WSL2) for local server environment

---

##  Setup & Deployment Steps

### 1. **Install and Configure WSL2**

- Install Ubuntu via WSL2 on Windows
- Update and upgrade system packages
  ```bash
  sudo apt update && sudo apt upgrade -y

# Install and Start Nginx
- sudo apt install nginx -y
- sudo service nginx start

# Project folder structure
/var/www/html/
└── dynamic-landing-page/
    ├── index.html
    └── assets/
        ├── tailwind.min.css
        ├── aos.css
        ├── aos.js
        └── landing-page.png

# Cloning and Configureing the Repo
- git clone git@github.com:ogbemi-ejegi/altschool-landing-page.git
- cd altschool-landing-page

# Deployment on AZURE + UBUNTU NGINX

1. SSH into Azure VM
   - ssh ogbemi@74.249.26.71
     
2. Install and start Nginx
   - sudo apt update
   - sudo apt install nginx -y

3. Upload project files from WSL2
   - scp -r ~/dynamic-landing-page/* ogbemi@74.249.26.71:/tmp

4. Move files to Nginx web root
   - sudo mv /tmp/* /var/www/html/
     
5. Restart Nginx
   - sudo systemctl restart nginx


Domain Setup
Domain: altschool.chickenkiller.com
Configured using FreeDNS (freedns.afraid.org)
A record pointed to Azure VM public IP
DNS propagation verified successfully

# SSL Setup with Encrypt
- sudo apt install certbot python3-certbot-nginx -y
- sudo certbot --nginx -d altschool.chickenkiller.com

TODO
Retry SSL setup after rate limit resets

Consider changing to a less-used FreeDNS domain

Add contact form integration

Add more sections like portfolio and testimonials

Push codebase to GitHub with documentation

Author
Ogbemi Mene-Ejegi
http://altschool.chickenkiller.com

