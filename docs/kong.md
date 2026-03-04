# Kong

## What is Kong?
Kong is a high-performance API Gateway built on top of:

🔹 Nginx
🔹 OpenResty
🔹 🔹 Lua (for plugin execution)

<br />

## Kong Architecture Overview

There are 5 core components in Kong architecture:

- Proxy Layer
- Admin API
- Control Plane (Optional - Hybrid Mode)
- Data Plane
- Database (Optional in DB-less)

## Core Kong Entities

These are critical to understand architecture:

| Entity   | Purpose                    |
| -------- | -------------------------- |
| Service  | Backend API                |
| Route    | Path matcher               |
| Consumer | API client                 |
| Plugin   | Behavior modifier          |
| Upstream | Load-balanced target group |
| Target   | Actual backend instance    |

## Why Kong is So Fast?

- Built on Nginx event loop
- Uses non-blocking I/O
- Config stored in memory
- No DB lookup per request
- Lua runs inside Nginx worker

## Load Balancing Architecture

When you define:

```
Upstream
  ├── Target 1
  ├── Target 2
  ├── Target 3
```

Kong handles:
- Round robin
- Least connections
- Hash-based
- Health checks
- Circuit breaking

All handled inside Nginx worker processes.

## Real Production Architecture
```
Internet
   ↓
Load Balancer
   ↓
Multiple Kong Data Planes
   ↓
Microservices Cluster
   ↓
Databases
```
Control plane lives separately.