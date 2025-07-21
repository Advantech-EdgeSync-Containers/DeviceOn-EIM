# EdgeMind-Manager Overview
EdgeMind Manager is a one-stop industrial IoT solution dedicated to addressing remote device management, device monitoring and operation & maintenance, as well as industrial data collection and visualization. The
management interface is web-based, offering a simple, convenient, and feature-rich experience that is easy to
integrate. It effectively enhances the management and maintenance efficiency of edge devices in industrial
environments, significantly reducing operational costs.
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/b15de991-5d0c-49fa-a19f-4285fd3b5b66" />
<img width="960" alt="EdgeMind-Manager-Diagram" src="https://github.com/user-attachments/assets/51685087-d58b-47c7-aa3c-0aacbff9849f" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/2c21592d-4935-441e-be37-4cc3cd89769b" />


# Demo
![EdgeMind-Manager_demo_1](https://github.com/user-attachments/assets/6ad47b07-c5ae-449e-8b1c-b8e3fb70b285)





# EdgeMind Manager Deployment Guide

## Supported Environments
Deployable to:
- On-premise Linux servers  
- Local virtual machines (VMs)  
- Cloud VMs (Alibaba Cloud, Microsoft Azure, AWS, etc.)  

## 1. System Requirements
### Minimum Specifications:
- **CPU**: 2 vCPU cores   
- **Memory**: 4GB RAM  
- **Storage**: 32GB SSD  
- **OS**: Ubuntu 18.04 or newer 

> Other Linux distributions also can be supported 

## 2. Network Configuration
### Required Open Ports:

| Port  | Protocol  | Service               |
|-------|-----------|-----------------------|
| 8080  | HTTP      | Web Interface         |
| 8082  | HTTP      | Message and ithing      |
| 30001 | HTTP      | For OTA               |
| 9000  | HTTP      | For OTA               |
| 1883  | TCP       | MQTT Broker           |
| 5500  | TCP       | VNC Server            |
| 9191  | Websocket | VNC                   |
| 8024,50500-50510  | TCP       | Terminal           |

## 3. Installation Procedure

### 3.1 Install Prerequisites
```bash
# Update system packages
sudo apt update && sudo apt upgrade

# Install Git
sudo apt install git

# Install Docker (official script)
curl -fsSL https://get.docker.com | sudo sh

# Install Docker-Compose
sudo apt install docker-compose

# Verify installations
docker --version
docker-compose version
```
### 3.2 Deploy EdgeMind-Manager
```bash
git clone https://github.com/Advantech-EdgeSync-Containers/EdgeMind-Manager.git
cd EdgeMind-Manager   
chmod +x  start.sh
# Execute installation (may take 10-20 minutes)
./start.sh 
```
> Note: The script will:
>  Pull Docker images
>  Configure container networks
>  Initialize database schemas

## 4. Accessing EdgeMind-Manager
 After successful installation, access the web interface:  
`http://<SERVER_IP>:8080`  

You will see the login page with following default credentials: 

**Default Account**:  
- Username: `admin`  
- Password: `admin`  


