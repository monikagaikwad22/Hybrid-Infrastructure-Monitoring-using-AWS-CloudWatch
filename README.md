# 🚀 **Hybrid Infrastructure Monitoring using AWS CloudWatch**

Designed and implemented a hybrid monitoring solution by integrating an on-premise virtual machine with AWS CloudWatch using the CloudWatch Agent. Built centralized dashboards and configured real-time alerting using SNS to monitor both cloud and on-prem environments efficiently.

---

## 📌 Project Overview

This project showcases a Hybrid Monitoring System where an on-premise server (Virtual Machine) is connected with AWS CloudWatch for unified monitoring.

The solution gathers metrics from:

- ☁️ AWS EC2 Instance  
- 🖥️ On-Premise Virtual Machine  

All metrics are visualized in a single CloudWatch dashboard, along with automated alerting through SNS notifications.

---
<img width="1536" height="1024" alt="ChatGPT Image Mar 27, 2026, 05_43_09 PM" src="https://github.com/user-attachments/assets/b8930c86-1207-4bff-ba34-4b0be445ee88" />


## 🧠 Architecture

On-Prem VM → CloudWatch Agent → AWS CloudWatch  
                                     ↓  
EC2 Instance → Metrics → Dashboard + Alarms → SNS (Email Alerts)

---

## 🛠️ Technologies Used

- AWS CloudWatch  
- AWS EC2  
- AWS SNS  
- IAM Roles & Policies  
- Ubuntu (Virtual Machine)  
- CloudWatch Agent  

---

## ⚙️ Implementation Steps

### 🔹 1. On-Premise VM Setup

- Created an Ubuntu VM using VirtualBox  
- Installed and configured CloudWatch Agent  

![WhatsApp Image 2026-03-23 at 4 13 41 PM](https://github.com/user-attachments/assets/9836d9d0-aac7-4570-aa33-0cdee8295f6b)



![WhatsApp Image 2026-03-23 at 4 14 14 PM](https://github.com/user-attachments/assets/0dca1e32-9ef8-4e5b-a9db-ecaae9c2df59)


---

### 🔹 2. EC2 Instance Configuration

- Launched an Ubuntu EC2 instance  
- Attached IAM Role with CloudWatch access permissions  

![WhatsApp Image 2026-03-23 at 4 16 00 PM](https://github.com/user-attachments/assets/2743474b-7364-4644-9462-f088374316c5)



![WhatsApp Image 2026-03-23 at 4 27 45 PM](https://github.com/user-attachments/assets/c77eed2c-ce51-417e-a9fd-cfe4446c8e62)

---

### 🔹 3. CloudWatch Agent Setup

- Configured CloudWatch Agent on both VM and EC2  

Metrics collected:
- CPU utilization  
- Memory usage  
- Disk usage  

![WhatsApp Image 2026-03-26 at 10 03 36 PM](https://github.com/user-attachments/assets/8db44d26-e8e5-4d21-8d72-0edcb43fc247)



![WhatsApp Image 2026-03-26 at 10 20 06 PM](https://github.com/user-attachments/assets/82185fd3-0071-4d17-8920-60fc8fb14c8c)

---

### 🔹 4. Agent Status Verification

- Started CloudWatch Agent service  
- Verified successful execution  

![WhatsApp Image 2026-03-26 at 10 20 06 PM](https://github.com/user-attachments/assets/906b7324-f26d-4018-973b-a0d3fda9bef3)


---

### 🔹 5. Metrics Validation

- Verified metrics in CloudWatch console  

Examples:
- EC2 → CPUUtilization  
- VM → mem_used_percent  


![WhatsApp Image 2026-03-26 at 10 08 27 PM](https://github.com/user-attachments/assets/349aca2e-9b50-424b-bc46-0f539a77e476)

---

### 🔹 6. Dashboard Creation

- Created a unified CloudWatch Dashboard including:
  - EC2 CPU metrics  
  - VM Memory usage  
  - VM Disk utilization  

![WhatsApp Image 2026-03-26 at 10 05 40 PM](https://github.com/user-attachments/assets/44e4a22e-b8c2-4979-a206-1c0b3aafcc52)

---

### 🔹 7. SNS Alert Setup

- Created SNS Topic  
- Subscribed email for receiving alerts  

![WhatsApp Image 2026-03-26 at 10 24 54 PM](https://github.com/user-attachments/assets/a7df0aac-b49c-4a3a-8c0c-0a5275222171)

---

### 🔹 8. Alarm Configuration

Configured CloudWatch Alarms:

- EC2 CPU Utilization > 70%  
- VM Memory Usage > 70%  


![WhatsApp Image 2026-03-26 at 10 06 26 PM](https://github.com/user-attachments/assets/7453b3a2-115a-497a-90f7-e137292222f4)


---

### 🔹 9. Testing & Validation

- Generated load using `stress` command  
- Observed:
  - Metric spikes  
  - Alarm triggering  
  - Email notification received  


![WhatsApp Image 2026-03-26 at 10 15 41 PM](https://github.com/user-attachments/assets/ad64a310-726b-42e8-b8ed-04e9693c79c7)


---

## 📊 Final Outcome

- Unified monitoring for hybrid infrastructure  
- Real-time performance tracking  
- Automated alerting via SNS  
- Successfully validated monitoring through stress testing  

---

## 💬 Key Learnings

- Designing hybrid cloud monitoring architecture  
- CloudWatch Agent setup & troubleshooting  
- Custom metrics collection  
- Dashboard creation & alert configuration  
- Handling real-world monitoring scenarios  

---

## 🎯 Conclusion

This project demonstrates an effective approach to integrating on-premise systems with AWS CloudWatch, enabling centralized monitoring and proactive alerting across hybrid environments.

---

## 👨‍💻 Author
Monika Gaikwad
