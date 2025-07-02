# Real-Time Intrusion Detection System for SDN Optimized by Fed-Adam 

## Overview

**RTIDS-FedAdam** is an advanced, privacy-preserving cybersecurity threat detection framework for Software-Defined Networking (SDN) environments. Leveraging **federated learning** with the **FedAdam optimizer** and real-time data streaming via **Apache Kafka**, this project enables distributed, collaborative model training and real-time intrusion detection without centralizing sensitive network data.

The system is designed to detect a wide range of attacks—including DDoS, Probe, DoS, BFA, Web-Attack, BOTNET, and U2R—by combining deep learning, distributed systems, and real-time analytics in a scalable, production-ready architecture.

---

## Table of Contents

- [Features](#features)
- [System Architecture](#system-architecture)
- [Technologies Used](#technologies-used)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Running the System](#running-the-system)
- [Project Structure](#project-structure)
- [Usage](#usage)
- [Results](#results)
- [Future Work](#future-work)
- [References](#references)

---

## Features

- **Federated Learning**: Distributed model training across multiple SDN clients without sharing raw data.
- **FedAdam Optimization**: Adaptive, momentum-based optimizer for fast and stable federated convergence.
- **Real-Time Detection**: Kafka-powered streaming for live network traffic simulation and instant threat analysis.
- **Multi-Class Attack Detection**: Identifies DDoS, Probe, DoS, BFA, Web-Attack, BOTNET, U2R, and Normal traffic.
- **Privacy-Preserving**: No centralized data collection; only model updates are shared.
- **Scalable & Modular**: Easily extendable to more clients, new attack types, or additional real-time analytics.
- **Comprehensive Monitoring**: Enhanced alerting, statistics, and real-time dashboard.

---

## System Architecture

![image alt](https://github.com/Govindds1/RTIDS-FedAdam/blob/main/System_Architecture.png?raw=true)


---

## Technologies Used

- **Python 3.8+**
- **PyTorch** (Deep Learning, Federated Learning)
- **scikit-learn** (Preprocessing, Metrics)
- **pandas, numpy** (Data Handling)
- **matplotlib, seaborn** (Visualization)
- **Apache Kafka** (Real-Time Streaming) [1]
- **kafka-python** (Kafka Producer/Consumer)
- **Jupyter Notebook** (Development & Analysis) [2]
- **VS Code** (Recommended IDE)

---

## Getting Started

### Prerequisites

- Python 3.8 or higher
- Java 8+ (for Kafka)
- Apache Kafka 2.8+ (download from [kafka.apache.org](https://kafka.apache.org/downloads))
- Recommended: 8GB+ RAM, modern CPU, optional CUDA GPU

### Installation

1. **Clone the Repository**
   ```bash
   git clone https://github.com/Govindds1/RTIDS-FedAdam.git
   cd RTIDS-FedAdam
   ```
