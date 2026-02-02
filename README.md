# Ansible Project 3 – LAMP Stack Automation

## 📌 Project Overview
This project automates the deployment of a complete **LAMP stack (Linux, Apache, MariaDB, PHP)** using Ansible on AWS EC2.

Along with installing and managing services, the project also deploys a **PHP test application** to verify the stack end-to-end.

This project represents a **real-world infrastructure automation use case**, not just package installation.

---

## 🛠️ Tools & Technologies
- Ansible
- Linux (Amazon Linux 2023)
- AWS EC2
- Apache (httpd)
- MariaDB
- PHP

---

## 📂 Project Structure
```text
ansible-lamp-stack-automation/
├── inventory/
│   └── hosts
├── playbooks/
│   └── lamp.yml
└── README.md
```

## ▶️ How to Run the Project
### 1️⃣ Inventory

- The Ansible controller is used as the managed node (localhost) for learning purposes.
```
[web]
localhost ansible_connection=local
```

### 2️⃣ Run LAMP Playbook
```
ansible-playbook -i inventory/hosts playbooks/lamp.yml

```

## ✅ What This Playbook Automates

- Installation of Apache web server

- Installation of MariaDB database server

- Installation of PHP and required modules

- Starting and enabling all services

- Deployment of a PHP test application (phpinfo())

- Restarting Apache to apply PHP configuration


## 🔍 Verification Steps

**Apache Status**
```
systemctl status httpd
```

**MariaDB Status**
```
systemctl status mariadb
```

**PHP Application Test**
```
curl localhost
```


OR open in browser:

http://<EC2_PUBLIC_IP>


A PHP info page confirms successful LAMP deployment.

---

## 📸 Screenshots

### 🔹 Ansible Playbook Execution
Shows successful execution of the LAMP automation playbook.

![Playbook Execution](/img/Screenshot%20(1060).png)


---

### 🔹 Apache Web Server Status
Confirms Apache service is running and enabled.

![Apache Status](/img/Screenshot%20(1061).png)

---

### 🔹 MariaDB Database Status
Confirms MariaDB service is running successfully.

![MariaDB Status](/img/Screenshot%20(1062).png)

---

### 🔹 PHP Application Verification
PHP info page confirms end-to-end LAMP stack deployment.

![PHP Info](/img/Screenshot%20(1066).png)

---
## Author: 
**Vivek Chopde | Aspiring DevOps Engineer**

---
   🎇🎇🎇