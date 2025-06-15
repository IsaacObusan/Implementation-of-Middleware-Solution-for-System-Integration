# 📡 Middleware Integration: EBPPro ↔ BUMS

A system integration project designed to automate and streamline the data transfer between Camarines Norte State College's Electronic Budget Planning Process (EBPPro) and Budget Utilization and Monitoring System (BUMS) using RESTful APIs and RabbitMQ.



![Screenshot_15-6-2025_22445_](https://github.com/user-attachments/assets/f16e0650-2068-4a7e-ae46-deb5b326e40e)


## 📌 Project Overview

This middleware solution addresses the inefficiencies in the manual transfer of budget data between EBPPro and BUMS. The system ensures real-time synchronization, data integrity, and scalability while minimizing human error.

## 🧩 Features

- 🔄 Automated Budget Data Transfer
- 🚀 RESTful API via Flask (Python)
- 📨 Asynchronous Messaging using RabbitMQ
- 📋 JSON-formatted Budget Payloads
- 🔧 Middleware hosted on Ubuntu
- 🧪 Tested with Postman

## 🛠 Technologies Used

| Component      | Technology         |
|----------------|--------------------|
| API Framework  | Flask (Python)     |
| Message Broker | RabbitMQ           |
| Data Format    | JSON               |
| OS Environment | Ubuntu             |
| Testing Tool   | Postman            |

## ⚙️ System Architecture

- **Architecture Style**: Microservices + Client-Server + Event-Driven + Three-Tier
- **Data Flow**:
  1. EBPPro sends budget via POST API.
  2. RabbitMQ queues data asynchronously.
  3. BUMS listens for data and pulls it when ready.

## 🔁 API Endpoints

| Method | Endpoint       | Description                        |
|--------|----------------|------------------------------------|
| GET    | `/api/budget`  | Retrieve latest budget             |
| POST   | `/api/budget`  | Send new budget data               |
| PUT    | `/api/budget`  | Update existing budget             |
| DELETE | `/api/budget`  | Remove outdated budget info        |

## 📂 Repository Structure

```bash
.
├── rest_api_server.py    # Flask RESTful API implementation
├── rabbitmq_config/      # RabbitMQ setup & queue configurations
├── payloads/             # Sample JSON budget payloads
└── README.md             # Project documentation
