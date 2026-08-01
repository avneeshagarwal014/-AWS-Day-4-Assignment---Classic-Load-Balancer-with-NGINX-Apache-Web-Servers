# 🚀 AWS Classic Load Balancer (CLB) with NGINX & Apache Web Servers

## 📌 Project Overview

This project demonstrates how to implement **High Availability** and **Traffic Distribution** in AWS using a **Classic Load Balancer (CLB)** with multiple backend web servers.

As part of my **Multi-Cloud DevOps Learning Journey**, I deployed two EC2 instances running different web servers (NGINX and Apache HTTPD) and configured an AWS Classic Load Balancer to distribute incoming traffic between them.

The primary goal of this project was to understand how Load Balancers improve application availability, reliability, and fault tolerance in a cloud environment.

---

## 🏗️ Solution Architecture

Client Request

⬇️

AWS Classic Load Balancer (CLB)

⬇️

NGINX Web Server (EC2 Instance 1)

Apache HTTPD Web Server (EC2 Instance 2)

---

## 🎯 Project Objectives

* Deploy multiple EC2 instances.
* Configure different web servers.
* Implement AWS Classic Load Balancer.
* Configure Health Checks.
* Test traffic distribution across servers.
* Understand High Availability concepts.
* Eliminate Single Point of Failure.

---

## 🛠️ Services & Technologies Used

### AWS Services

* Amazon EC2
* AWS Classic Load Balancer (CLB)
* VPC
* Security Groups

### Web Servers

* NGINX
* Apache HTTPD

### Operating System

* Ubuntu Linux

---

## 📋 Implementation Steps

### Step 1: Launch EC2 Instances

Created two Amazon EC2 instances within the same VPC.

| Instance | Purpose                 |
| -------- | ----------------------- |
| EC2-1    | NGINX Web Server        |
| EC2-2    | Apache HTTPD Web Server |

---

### Step 2: Configure NGINX Web Server

Installed and configured NGINX on the first EC2 instance.

```bash
sudo apt update -y
sudo apt install nginx -y
sudo systemctl start nginx
sudo systemctl enable nginx
```

---

### Step 3: Configure Apache HTTPD Server

Installed and configured Apache HTTPD on the second EC2 instance.

```bash
sudo apt update -y
sudo apt install apache2 -y
sudo systemctl start apache2
sudo systemctl enable apache2
```

---

### Step 4: Create Custom Web Pages

Configured custom landing pages on both servers to identify traffic routing through the Load Balancer.

Example:

NGINX Server

```html
<h1>Welcome to NGINX Server</h1>
```

Apache Server

```html
<h1>Welcome to Apache HTTPD Server</h1>
```

---

### Step 5: Create AWS Classic Load Balancer

Configured a Classic Load Balancer with:

* Listener Port: 80 (HTTP)
* Registered Backend Instances
* Health Check Configuration
* Availability Monitoring

---

### Step 6: Test Traffic Distribution

Used the Load Balancer DNS Endpoint to verify:

✅ Requests were distributed across both servers

✅ Health Checks were working correctly

✅ Application remained accessible through the Load Balancer

---

## 📸 Project Screenshots

### AWS EC2 Instances Running

![Ec2 Instance](screenshots/EC2 Instances List.png)

### Nginx Service Status – Server 1

![Nginx Status](screenshots/nginx status running.png)

### Apache HTTPD Service Status - Server 2

![Apache HTTPD Status](screenshots/httpd status running.png)

### Custom Web Page on Server-1 Nginx

![Web Page - Nginx](screenshots/Custom Web Page on Server-1 Nginx.png)

### Custom Web Page on Server-2 Apache HTTPD

![Web Page - Apache HTTPD](screenshots/Custom Web Page on Server-2 httpd.png)

### Classic Load Balancer Configuration

![LB Configuration](screenshots/Load Balancer Configuration.png)

### Health Check Status

![Health Check](screenshots/Registered Targets &Instances.png)

### NGINX Server Output

![NGINX Server](screenshots/Load Balancer Traffic Distribution - Nginx.png)

### Apache HTTPD Server Output

![Apache Server](screenshots/Load Balancer Traffic Distribution - httpd.png)

---

## 🔍 Key Concepts Learned

### Load Balancing

Distributes incoming traffic across multiple servers to improve performance and availability.

### Health Checks

Continuously monitor backend servers and route traffic only to healthy instances.

### High Availability

Ensures applications remain accessible even when one server becomes unavailable.

### Fault Tolerance

Reduces the impact of server failures by maintaining redundant backend resources.

---

## 🚀 Skills Demonstrated

* AWS EC2 Administration
* AWS Classic Load Balancer (CLB)
* Linux Server Management
* NGINX Configuration
* Apache HTTPD Configuration
* Health Check Configuration
* VPC Networking
* High Availability Design
* Troubleshooting & Testing

---

## 📚 Key Takeaways

✔️ Load Balancers improve application reliability.

✔️ High Availability is a critical cloud architecture principle.

✔️ Health Checks help ensure traffic reaches healthy servers only.

✔️ Multiple backend servers eliminate single points of failure.

✔️ AWS Load Balancers simplify traffic management and scalability.

---

## 👨‍💻 Author

### Avneesh Agarwal

**Learning Journey:**

Linux → Git → AWS → Docker → Kubernetes → Terraform → Jenkins → Ansible

⭐ If you found this project useful, consider giving this repository a Star.
