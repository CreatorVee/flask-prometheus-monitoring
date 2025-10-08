# 📊Flask Monitoring with Prometheus & Grafana

---

**CLICK ON TECH STACK TO SEE HOW  I USED THESE TOOLS IN MY WORK**


## ⚙️ Tech Stack

# Monitoring & Observability:
[![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=for-the-badge&logo=prometheus&logoColor=white)](https://github.com/CreatorVee/flask-prometheus-monitoring/tree/main/prometheus/prometheus.yml)
[![Grafana](https://img.shields.io/badge/Grafana-F46800?style=for-the-badge&logo=grafana&logoColor=white)](https://github.com/CreatorVee/flask-prometheus-monitoring/blob/main/docker-compose.yml)

---

# Backend Technologies:
[![Flask](https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=flask&logoColor=white)](https://github.com/CreatorVee/flask-prometheus-monitoring/blob/main/app.py)
[![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://github.com/CreatorVee/flask-prometheus-monitoring/blob/main/app.py)

---

# DevOps & Infrastructure:
[![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)](https://github.com/CreatorVee/flask-prometheus-monitoring/blob/main/Dockerfile)
[![Docker Compose](https://img.shields.io/badge/Docker%20Compose-2496ED?style=for-the-badge&logo=docker&logoColor=white)](https://github.com/CreatorVee/flask-prometheus-monitoring/blob/main/docker-compose.yml)

🧠 This project demonstrates real-time monitoring and observability using Prometheus, Grafana, Flask, and Docker Compose.
The goal is to show how monitoring tools can visualize live metrics from an application — helping engineers detect, analyze, and improve system performance.

📝 Project Overview

- Before implementing monitoring, there was no easy way to see how the Flask application behaved internally — metrics like request count, response time, and errors were hidden.

- After integrating Prometheus and Grafana, I could visually observe:

- How many times the app endpoints were accessed.

- Response durations and uptime.

- The overall health and performance of the service.

- This project highlights the importance of observability — knowing exactly what’s happening inside your systems through data.

---


# 🎯Key Features

- Real-time tracking of Flask metrics

- Prometheus scrapes metrics from the /metrics endpoint

- Grafana visualizes data with interactive dashboards

- Docker Compose manages all services together

- Demonstrates a full DevOps-style monitoring workflow

---


# 📂 Project Structure


monitoring-project /

├── app.py  /              # Flask application exposing /metrics

├── prometheus.ym l/       # Prometheus scrape configuration

├── docker-compose.yml/   # Defines Prometheus, Grafana, Flask containers

├── requirements.txt/   # Flask and Prometheus client dependencies

└── README.md /           

---


# 🎥 Demo
![Project Demo](assets/Monitoring-demo.gif)

**This demo shows how Grafana updates live metrics from the Flask app**

After refreshing the Flask app several times, Grafana’s graph instantly shows the increase — **moving from 1 to 16 requests.**
This proves that Prometheus is collecting data in real time and Grafana is displaying it visually, showing how activity on the app directly affects the monitoring dashboard.

---


# 🧰 Setup & Run

1️⃣ Clone the Repository

- git clone <repo-url>
- cd monitoring-project

  ---
  2️⃣ Build and Start the Services
  
- docker-compose up -d

---

3️⃣ Access the Services

- Flask app → http://localhost:5000

- Prometheus → http://localhost:9090

- Grafana → http://localhost:3000

  ---

  4️⃣ Stop Services
  
- docker-compose down

  ---


🧠 Problems & Solutions
🧱 Before (No Monitoring)

❌ Could not see if the app was running properly or how many users accessed it.
❌ No visibility into performance, errors, or uptime.

⚙️ After (With Prometheus + Grafana)

✅ Prometheus automatically collects live metrics from the app.
✅ Grafana visualizes them through graphs and dashboards.
✅ Engineers can now spot spikes, latency issues, and failures in real time.

---

🧩 Commands Used
# Check running containers
- docker ps

# View container logs
- docker-compose logs prometheus
- docker-compose logs grafana

# Restart containers
- docker-compose restart

# Stop and remove containers
- docker-compose down


---

# 🧠 What I Learned

- Prometheus → How it scrapes metrics from services and stores them for analysis.

- Grafana → How to visualize Prometheus metrics using dynamic dashboards.

- Flask → How to expose application metrics via the /metrics endpoint.

- Docker Compose → Running multiple services (app, Prometheus, Grafana) together easily.

- Observability Importance → Realized how monitoring helps detect, debug, and optimize services before issues impact users.

 
---


<img width="1600" height="656" alt="2025-10-08_16h55_11" src="https://github.com/user-attachments/assets/72137609-d86f-446d-a02f-b5546645e8c8" />

**Prometheus monitoring the Flask app on port 5000**

This screenshot shows that Prometheus successfully scraped and collected metrics from the Flask service, confirming that the application is healthy and being tracked in real time.

---

<img width="1548" height="233" alt="2025-10-08_22h24_07" src="https://github.com/user-attachments/assets/0d295615-8922-47ec-b99a-dced39b0f05c" />

**All containers running using Docker Compose**

This proves that Prometheus, Grafana, and the Flask app were all started together through Docker Compose — saving time and effort by running multiple containers with a single command.

---

<img width="1291" height="536" alt="2025-10-08_17h57_01" src="https://github.com/user-attachments/assets/226f24b4-f79e-45b3-abd0-aedb9ed474ca" />

**Flask app being monitored by Prometheus and Grafana**

This is the application whose metrics are being collected and visualized. It represents how modern DevOps teams track their running services using open-source monitoring tools.


----


