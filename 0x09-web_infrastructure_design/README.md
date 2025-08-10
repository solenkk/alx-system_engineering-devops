# Web Infrastructure Design Evolution

This repository documents the progressive enhancement of a web infrastructure from basic single-server setup to fully scaled and monitored architecture.

## Table of Contents
1. [Simple Web Stack](#0-simple-web-stack)
2. [Distributed Web Infrastructure](#1-distributed-web-infrastructure)
3. [Secured & Monitored Infrastructure](#2-secured--monitored-web-infrastructure)
4. [Scale-Up Infrastructure](#3-scale-up-web-infrastructure)

---

<a id="0-simple-web-stack"></a>
## 🔧 0. Simple Web Stack
![Simple Web Stack Diagram](https://imgur.com/a/R2yHXIp)

### Architecture

graph LR
    U[User] --> D[DNS]
    D --> S[Single Server]
    S --> WS[Web Server]
    S --> APP[Application]
    S --> DB[Database]

graph TD
    U[User] --> LB[Load Balancer]
    LB --> WS1[Web Server 1]
    LB --> WS2[Web Server 2]
    WS1 --> DB[Primary DB]
    WS2 --> DB
    DB --> REPLICA[Replica DB]

https://imgur.com/a/uzl7qPv
