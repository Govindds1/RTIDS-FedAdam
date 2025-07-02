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

```` ```````flowchart TD
    subgraph Client_Side["Federated Clients (SDN Domains)"]
        A1[Local Data<br>(Majority.csv/Minority.csv)]
        A2[Data Preprocessing<br>(Scaling, Encoding)]
        A3[Local Model Training<br>(CyberSecurityNet)]
        A4[Model Update<br>(FedAdam Delta)]
        A1 --> A2 --> A3 --> A4
    end

    subgraph Kafka_Stream["Real-Time Traffic Simulation"]
        B1[Kafka Producer<br>(Simulated/Real Traffic)]
        B2[Kafka Broker<br>(cybersecurity-stream)]
        B3[Kafka Consumer<br>(Threat Detector)]
        B1 --> B2 --> B3
    end

    subgraph Server_Side["Central Server"]
        C1[Model Aggregation<br>(FedAdam)]
        C2[Global Model Update]
        C1 --> C2
    end

    A4 -- Model Updates --> C1
    C2 -- Global Model --> A3

    B3 -- Feature Extraction & Prediction --> D1[Real-Time Inference<br>with Global Model]
    D1 -- Alerts & Metrics --> D2[Dashboard & Monitoring]`````` ```
