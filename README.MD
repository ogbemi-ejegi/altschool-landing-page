# AltSchool Dynamic Landing Page Prototype 🚀

A professionally deployed, responsive landing page created as part of the **AltSchool Second Semester Exams**. This project demonstrates web development, server configuration, and deployment skills.

---

## 🌐 Live Demo

Access the project here: **http\://\<172.17.136.103>**

## 🎨 Project Preview

![Rendered Page Screenshot](assets/screenshot.png)

---

## 🔧 Steps Taken

### 1. **Server Setup**

* Used **WSL2 with Ubuntu** on Windows.
* Updated package list:

  ```bash
  sudo apt update && sudo apt upgrade
  ```
* Installed necessary packages:

  ```bash
  sudo apt install nginx git curl
  ```

### 2. **Web Server Configuration**

* Started and enabled Nginx:

  ```bash
  sudo systemctl start nginx
  sudo systemctl enable nginx
  ```
* Verified that Nginx listens on port 80:

  ```bash
  sudo netstat -tulpn | grep :80
  ```
* Checked server IP address using:

  ```bash
  ip addr show eth0
  ```

### 3. **Landing Page Development**

* Created a folder: `/var/www/html/dynamic-landing-page`
* Developed a single HTML page using:

  * Tailwind CSS (`assets/tailwind.min.css`)
  * AOS.js for animations (`assets/aos.css` and `assets/aos.js`)
  * Sections included:

    * Navbar
    * Hero Section
    * Services
    * Portfolio
    * Testimonials
    * Contact Form
    * Footer

### 4. **Making It Dynamic & Responsive**

* Ensured layout was responsive with Tailwind classes.
* Used `data-aos` attributes for scroll-based animations.
* Created a modern, investor-friendly layout.

### 5. **Deployment**

* Moved files into the Nginx default root:

  ```bash
  sudo cp -r * /var/www/html/
  sudo systemctl restart nginx
  ```
* Opened browser and accessed via `http://172.17.136.103`.

### 6. **Version Control & GitHub**

* Initialized a Git repo:

  ```bash
  git init
  git remote add origin git@github.com:ogbemi-ejegi/altschool-landing-page.git
  ```
* Added SSH key to GitHub for authentication.
* Pushed to remote:

  ```bash
  git add .
  git commit -m "Initial commit"
  git push -u origin main
  ```

---

## 📂 Repository Structure

```
/dynamic-landing-page
├── index.html
├── assets/
│   ├── tailwind.min.css
│   ├── aos.css
│   └── aos.js
└── README.md
```

---

## 💌 Contact

**Ogbemi Ejegi**
GitHub: [@ogbemi-ejegi](https://github.com/ogbemi-ejegi)
Email: [ejegi.ogbemi@gmail.com]

---

> **Note:** Replace `<YOUR_PUBLIC_IP>` and the screenshot path as needed.

