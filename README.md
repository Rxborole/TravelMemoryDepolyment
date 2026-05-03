# 🌍 Travel Memory App — Full Stack Deployment (MERN + DevOps)

## 🚀 Project Overview

Travel Memory is a full-stack MERN application that allows users to record and manage their travel experiences, including trip details, images, and personal stories.

This project demonstrates **end-to-end deployment of a production-grade application** using modern DevOps practices on AWS.

---

## 🧠 Tech Stack

### 🔹 Frontend

* React.js
* Axios
* CSS

### 🔹 Backend

* Node.js
* Express.js
* MongoDB (Atlas)
* Mongoose

### 🔹 DevOps & Infrastructure

* AWS EC2 (Compute)
* AWS Application Load Balancer (ALB)
* Nginx (Reverse Proxy + Static Hosting)
* PM2 (Process Manager)
* Cloudflare (DNS, CDN, SSL)

---

## 🏗️ Architecture

<img width="681" height="741" alt="My_Travelapp_Arch drawio" src="https://github.com/user-attachments/assets/14f8d5ae-45d0-43fb-8545-70bbe1134fbe" />


---

## 🔁 Request–Response Flow

1. User sends request via browser
2. Request goes through Cloudflare (DNS + CDN + SSL)
3. Forwarded to AWS Load Balancer
4. Load Balancer distributes traffic to EC2 instances
5. Nginx:

   * Serves React frontend
   * Proxies API calls to backend
6. Node.js backend processes request
7. Data fetched from MongoDB Atlas
8. Response flows back to user via same path

---

## ⚙️ Features

* Add travel experiences
* View trip history
* Store trip details (dates, cost, places, notes)
* Responsive UI
* Backend API with MongoDB integration
* Scalable deployment with load balancing

---

## 🖥️ Local Setup

### 1. Clone Repository

```bash
git clone https://github.com/<your-username>/My_Travel_App.git
cd My_Travel_App
```

---

### 2. Backend Setup

```bash
cd backend
npm install
```

Create `.env`:

```env
PORT=3000
MONGO_URI=your_mongodb_connection_string
```

Run backend:

```bash
npm start
```


<img width="1259" height="170" alt="MongoDbConnect (2)" src="https://github.com/user-attachments/assets/cb05b8e5-9a8e-4081-a848-1ac819980eba" />

---

### 3. Frontend Setup

```bash
cd ../frontend
npm install
npm start
```
<img width="1277" height="566" alt="Frontsetup" src="https://github.com/user-attachments/assets/e49bc1b0-5803-4b50-a957-a79883056ea4" />


---

## ☁️ Deployment Steps (Summary)

### 🔹 Backend Deployment

* Hosted on EC2
* Managed using PM2
* Connected to MongoDB Atlas
<img width="1234" height="240" alt="MongoDbConnect" src="https://github.com/user-attachments/assets/7d37a06f-d0bb-4b20-b9dc-53d7d2712310" />



### 🔹 Frontend Deployment

* Built using `npm run build`
* Served via Nginx

### 🔹 Reverse Proxy

<img width="1270" height="606" alt="ngnix" src="https://github.com/user-attachments/assets/fa6591b5-9dde-43ad-a16c-e78028d1e1b1" />

* Nginx routes:

  * `/` → React frontend
  * `/api` → Node backend

<img width="1265" height="535" alt="Nginx routes" src="https://github.com/user-attachments/assets/54402e26-7568-4b6c-861d-c79a27944bac" />

### 🔹 Load Balancing

* AWS Application Load Balancer
* Multiple EC2 instances for scalability
  
<img width="1255" height="530" alt="Load Balancing" src="https://github.com/user-attachments/assets/88475342-32f3-4b76-9238-20f91eed4d79" />

#### Testing Load Balancer.
  *Stoped an EC2 instance

<img width="1262" height="521" alt="Testing Load Balancer" src="https://github.com/user-attachments/assets/d45dd301-c8cd-4609-9d59-858ccd56d4bb" />

 * Browse the DNS of Load Balancer, The site should load fine.
  

  <img width="1215" height="630" alt="DNS of Load Balancer" src="https://github.com/user-attachments/assets/8dbf3d8b-b3f3-4192-a7d3-aae807f18f73" />


### 🔹 Domain & SSL

* Domain configured via Cloudflare

<img width="1919" height="820" alt="Domain" src="https://github.com/user-attachments/assets/b39e12ba-3a6b-4a7a-9e45-406f5ccf9437" />

  
* SSL enabled using:

  * Cloudflare (edge)
  * AWS ACM (origin)
<img width="1820" height
<img width="1919" height="820" alt="Domain" src="https://github.com/user-attachments/assets/b42fcb0d-0292-45dc-a8f6-4ad0aad7325d" />


---

## 🌐 Live URL

```
https://cloudcraft-lab.com
```

## 📦 Key DevOps Concepts Demonstrated

* Infrastructure setup on AWS
* Reverse proxy using Nginx
* Load balancing with ALB
* Domain + DNS management
* SSL/TLS configuration
* Process management using PM2
* Production deployment of MERN stack

---

## 🔮 Future Improvements

* CI/CD pipeline (GitHub Actions)
* Auto Scaling Group
* Docker containerization
* Monitoring (CloudWatch / Prometheus)
* Logging improvements

---

## 👤 Author

**Rupesh Borole**

---

## 💼 Project Summary

This project demonstrates the ability to:

* Deploy full-stack applications in production
* Design scalable cloud architecture
* Configure networking, DNS, and SSL
* Debug real-world infrastructure issues

---
