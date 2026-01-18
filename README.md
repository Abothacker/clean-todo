# 🚀 Deploying a Node.js Application on AWS EC2

A step-by-step guide to deploy a Node.js application on AWS EC2 using EC2 Instance Connect.

---

## 📌 Prerequisites

- AWS account

---

## 🛠️ Deployment Steps

### 1️. Create an AWS EC2 Instance

- Go to **AWS Console → EC2 → Launch Instance**
- Select **Ubuntu** as AMI
- Choose **t2.micro** instance type
- Click **Launch Instance**

---

### 2️. Connect to Your Instance

- Go to **EC2 → Instances**
- Select your instance → Click **Connect**
- Choose **EC2 Instance Connect** → Click **Connect**

---

### 3️. Update System Packages
```bash
sudo apt update
```

---

### 4️. Install Node.js, NPM, and Git
```bash
sudo apt install nodejs npm git -y
```

---

### 5️. Clone Your Repository
```bash
git clone https://github.com/Abothacker/clean-todo.git
```

---

### 6️. Navigate to Project Directory
```bash
cd clean-todo
```

---

### 7. Install Dependencies
```bash
npm install
```

---


### 8. Configure Security Group

- Go to **EC2 → Security Groups**
- Select your instance's security group
- Click **Edit Inbound Rules** → **Add Rule**
- **Type:** Custom TCP | **Port:** 5173 | **Source:** 0.0.0.0/0
- Click **Save Rules**

Opens port 5173 to allow external access to your application.

---

### 9. Start the Application
```bash
npm run dev -- --host
```

---
### 10. Access Your Application
```
http://YOUR_EC2_PUBLIC_IP:5173
```
Replace `YOUR_EC2_PUBLIC_IP` with your instance's public IP address.

---

##  What I Learned

- AWS EC2 instance setup and management
- Linux package installation and navigation
- Node.js deployment on cloud servers
- Security group configuration

---


## 🏷️ Tags

`#DevOps` `#AWS` `#EC2` `#NodeJS` `#CloudComputing` `#Deployment`

---

## 👤 Credits

Node.js To Do application originally developed by Guilherme Milreu.
