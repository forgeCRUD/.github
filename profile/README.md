```
  _____                      _____  _____   _    _  _____  
 |  ___|                    /  __ \|  _  \ | |  | ||  _  | 
 | |_  ___  _ __  __ _  ___ | /  \/| |_| | | |  | || | | | 
 |  _|/ _ \| '__|/ _` |/ _ \| |    |    /  | |  | || | | | 
 | | | (_) | |  | (_| |  __/| \__/\| |\ \  | |__| || |/ /  
 \_|  \___/|_|   \__, |\___|  \____/\_| \_|  \____/ |___/   
                  __/ |                                    
                 |___/                                     
```                               


<picture>
  <source media="(prefers-color-scheme: dark)" srcset="landing-page/public/img/logo/forgecrud-full-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="landing-page/public/img/logo/forgecrud-full-light.svg">
  <img alt="ForgeCRUD Logo" src="landing-page/public/img/logo/forgecrud-full-light.svg" width="280">
</picture>

### Low-Code Operations Platform

[![Website](https://img.shields.io/badge/Website-forgecrud.io-2a85ff?style=for-the-badge&logo=google-chrome&logoColor=white)](https://forgecrud.io)
[![Demo](https://img.shields.io/badge/Live-Demo-10b981?style=for-the-badge&logo=rocket&logoColor=white)](https://demo.v2.forgecrud.io)
[![Docs](https://img.shields.io/badge/Docs-Documentation-6366f1?style=for-the-badge&logo=gitbook&logoColor=white)](https://forgecrud.io/docs)

---

**ForgeCRUD** transforms your operational workflows into powerful digital applications - without writing a single line of code.

Build dynamic forms, design automated workflows, and create custom APIs in minutes. Perfect for purchase orders, leave management, invoice approvals, and any business process you can imagine.

---

## Features

<table>
<tr>
<td width="50%">

### Visual Form Builder
Build any form with drag-and-drop simplicity
- 15+ field types (text, select, date, file upload...)
- Auto-generated database tables
- Smart validation rules
- Relational field support
- Automatic code generation (PO-000001)

</td>
<td width="50%">

### Workflow Engine
Design approval flows visually with ReactFlow
- Multi-level approvals (Manager > Director > CEO)
- Conditional branching
- Scheduled triggers (cron-based)
- Email & real-time notifications
- Webhook integrations

</td>
</tr>
<tr>
<td width="50%">

### Custom API Builder
Create REST APIs without writing SQL
- Multi-table JOIN support
- Aggregation functions (SUM, COUNT, AVG)
- Window functions (ROW_NUMBER, RANK)
- Dynamic filtering & sorting

</td>
<td width="50%">

### Document Management
S3-compatible file storage with MinIO
- Version control
- Folder organization
- Access control
- File preview

</td>
</tr>
<tr>
<td width="50%">

### Real-time Notifications
Keep everyone informed instantly
- WebSocket-powered alerts
- Email integration
- Customizable templates
- In-app notification center

</td>
<td width="50%">

### Enterprise Security
Bank-grade security for your data
- 3-Level RBAC (User > Role > Organization)
- JWT authentication
- SQL Injection & XSS protection
- Rate limiting (100 req/min)
- Multi-tenant data isolation

</td>
</tr>
</table>

---

## How It Works

```
┌─────────────────┐     ┌─────────────────┐     ┌─────────────────┐     ┌─────────────────┐
│  1. DESIGN      │     │  2. AUTOMATE    │     │  3. SECURE      │     │  4. DEPLOY      │
│  ───────────    │     │  ──────────     │     │  ─────────      │     │  ─────────      │
│                 │     │                 │     │                 │     │                 │
│  Create forms   │────▶│  Build workflow │────▶│  Set roles &    │────▶│  Go live in     │
│  visually       │     │  with triggers  │     │  permissions    │     │  minutes        │
│                 │     │  & actions      │     │                 │     │                 │
└─────────────────┘     └─────────────────┘     └─────────────────┘     └─────────────────┘
```

---

## Use Cases

| Scenario | Description |
|----------|-------------|
| **Purchase Orders** | Request > Manager Approval > Budget Check > Director Approval > Procurement |
| **Leave Management** | Apply > Manager Review > HR Approval > Calendar Sync |
| **Invoice Approval** | Upload > Verification > Multi-level Approval > Payment Processing |
| **IT Support** | Ticket Creation > Assignment > Resolution > Feedback |
| **Expense Reports** | Submit > Receipt Upload > Approval > Reimbursement |

---

## Architecture

```
                                    ┌──────────────────────────────────────────────────────────┐
                                    │                      API GATEWAY                         │
                                    │            (Authentication · Rate Limiting)              │
                                    └────────────────────────────┬─────────────────────────────┘
                                                                 │
                    ┌────────────────────────────────────────────┼────────────────────────────────────────────┐
                    │                                            │                                            │
          ┌─────────▼─────────┐                       ┌──────────▼──────────┐                     ┌──────────▼──────────┐
          │   AUTH SERVICE    │                       │   FORM SERVICE      │                     │  WORKFLOW SERVICE   │
          │   ────────────    │                       │   ────────────      │                     │  ────────────────   │
          │   • JWT Tokens    │                       │   • Form Builder    │                     │  • Flow Designer    │
          │   • Session Mgmt  │                       │   • Data CRUD       │                     │  • Triggers         │
          │   • OAuth2        │                       │   • Validation      │                     │  • Actions          │
          └─────────┬─────────┘                       └──────────┬──────────┘                     └──────────┬──────────┘
                    │                                            │                                            │
                    │                    ┌───────────────────────┴───────────────────────┐                    │
                    │                    │                                               │                    │
          ┌─────────▼─────────┐   ┌──────▼──────┐   ┌──────────────┐   ┌────────▼────────┐   ┌───────▼───────┐
          │ PERMISSION SERVICE│   │ OPENAPI SVC │   │ DOCUMENT SVC │   │ NOTIFICATION SVC│   │ SCHEDULER SVC │
          │ ────────────────  │   │ ─────────── │   │ ──────────── │   │ ───────────────-│   │ ───────────── │
          │ • RBAC            │   │ • API Gen   │   │ • MinIO      │   │ • WebSocket     │   │ • Cron Jobs   │
          │ • Multi-tenant    │   │ • Query     │   │ • Versioning │   │ • Email         │   │ • Delayed     │
          └───────────────────┘   └─────────────┘   └──────────────┘   └─────────────────┘   └───────────────┘
                    │                    │                   │                   │                   │
                    └────────────────────┴───────────────────┴───────────────────┴───────────────────┘
                                                             │
                                    ┌────────────────────────▼────────────────────────┐
                                    │                   EVENT BUS                     │
                                    │                  (RabbitMQ)                     │
                                    └─────────────────────────────────────────────────┘
                                                             │
                         ┌───────────────────────────────────┼───────────────────────────────────┐
                         │                                   │                                   │
               ┌─────────▼─────────┐               ┌─────────▼─────────┐               ┌─────────▼─────────┐
               │    PostgreSQL     │               │      Redis        │               │      MinIO        │
               │    ──────────     │               │      ─────        │               │      ─────        │
               │    Primary DB     │               │    Cache/Queue    │               │   File Storage    │
               └───────────────────┘               └───────────────────┘               └───────────────────┘
```

---

## Tech Stack

<table>
<tr>
<td align="center" width="20%">
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/go/go-original-wordmark.svg" width="48" height="48" alt="Go" />
<br><strong>Go</strong>
<br><sub>Backend Services</sub>
</td>
<td align="center" width="20%">
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/react/react-original.svg" width="48" height="48" alt="React" />
<br><strong>React</strong>
<br><sub>Frontend</sub>
</td>
<td align="center" width="20%">
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/typescript/typescript-original.svg" width="48" height="48" alt="TypeScript" />
<br><strong>TypeScript</strong>
<br><sub>Type Safety</sub>
</td>
<td align="center" width="20%">
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/postgresql/postgresql-original.svg" width="48" height="48" alt="PostgreSQL" />
<br><strong>PostgreSQL</strong>
<br><sub>Database</sub>
</td>
<td align="center" width="20%">
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/redis/redis-original.svg" width="48" height="48" alt="Redis" />
<br><strong>Redis</strong>
<br><sub>Cache & Queue</sub>
</td>
</tr>
<tr>
<td align="center" width="20%">
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/docker/docker-original.svg" width="48" height="48" alt="Docker" />
<br><strong>Docker</strong>
<br><sub>Containerization</sub>
</td>
<td align="center" width="20%">
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/kubernetes/kubernetes-original.svg" width="48" height="48" alt="Kubernetes" />
<br><strong>Kubernetes</strong>
<br><sub>Orchestration</sub>
</td>
<td align="center" width="20%">
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/rabbitmq/rabbitmq-original.svg" width="48" height="48" alt="RabbitMQ" />
<br><strong>RabbitMQ</strong>
<br><sub>Message Queue</sub>
</td>
<td align="center" width="20%">
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nginx/nginx-original.svg" width="48" height="48" alt="Nginx" />
<br><strong>Nginx</strong>
<br><sub>API Gateway</sub>
</td>
<td align="center" width="20%">
<img src="https://min.io/resources/img/logo/MINIO_Bird.png" width="48" height="48" alt="MinIO" />
<br><strong>MinIO</strong>
<br><sub>Object Storage</sub>
</td>
</tr>
</table>

---

## Performance

| Metric | Value |
|--------|-------|
| API Response Time | < 100ms |
| Concurrent Users | 10,000+ |
| Uptime SLA | 99.9% |
| Microservices | 9 |
| Databases | 3 |
| Containerized | 100% |

---

## Quick Links

| Resource | Link |
|----------|------|
| Website | [forgecrud.io](https://forgecrud.io) |
| Live Demo | [demo.v2.forgecrud.io](https://demo.v2.forgecrud.io) |
| Documentation | [forgecrud.io/docs](https://forgecrud.io/docs) |
| Contact | [info@forgecrud.com](mailto:info@forgecrud.com) |

---

## Connect With Us

[![Twitter](https://img.shields.io/badge/Twitter-@forgecrud-1DA1F2?style=flat-square&logo=twitter&logoColor=white)](https://twitter.com/forgecrud)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-ForgeCRUD-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://linkedin.com/company/forgecrud)
[![GitHub](https://img.shields.io/badge/GitHub-forgecrud-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/forgecrud)

---

<p align="center">
  <strong>Transform Your Operations. Build Without Code.</strong>
  <br><br>
  <a href="https://forgecrud.io">
    <img src="https://img.shields.io/badge/Get_Started-ForgeCRUD-2a85ff?style=for-the-badge" alt="Get Started">
  </a>
</p>

---

<p align="center">
  Made with  by <a href="https://github.com/onuraltuntas">Onur Altuntas</a>
  <br>
  <sub>Copyright 2025 ForgeCRUD. All rights reserved.</sub>
</p>
