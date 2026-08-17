# Google-Cloud-Projects
# Google Cloud AI & Database Projects

A collection of three hands-on Google Cloud projects exploring **secure cloud database connectivity, Model Context Protocol (MCP), AlloyDB, AI agents, and multi-agent systems**.

These projects demonstrate the progression from a traditional cloud application architecture to AI-powered database interaction and finally to a collaborative multi-agent AI system.

---

## 📌 Projects Overview

| Project       | Focus                         | Main Technologies                                           |
| ------------- | ----------------------------- | ----------------------------------------------------------- |
| **Project 1** | Secure Cloud SQL connectivity | Compute Engine, Cloud SQL, Private IP, Cloud SQL Auth Proxy |
| **Project 2** | AI-to-database communication  | AlloyDB, MCP, AI Agents, IAM                                |
| **Project 3** | Multi-agent AI application    | ADK, MCP Toolbox, AlloyDB, Python                           |

---

# 🚀 Project 1: Connecting to Cloud SQL

### Compute Engine + Private IP + Cloud SQL Auth Proxy

The first project demonstrates how to securely connect a **Compute Engine VM** to a **Cloud SQL MySQL database** without exposing the database to the public internet.

### Architecture

```text
Application
     │
     ▼
Compute Engine VM
     │
     ▼
Cloud SQL Auth Proxy
     │
     ▼
Private IP / VPC
     │
     ▼
Cloud SQL (MySQL)
```

### Key Concepts

* Google Compute Engine
* Cloud SQL
* MySQL
* VPC networking
* Private IP
* Private Service Access
* Cloud SQL Auth Proxy
* IAM authentication

### What Was Implemented

1. Created a Compute Engine virtual machine.
2. Created a Cloud SQL MySQL instance.
3. Configured Private Service Access.
4. Assigned a Private IP to Cloud SQL.
5. Connected the VM and Cloud SQL through the same VPC.
6. Installed and configured Cloud SQL Auth Proxy.
7. Configured the required IAM permissions.
8. Executed SQL commands to verify the connection.

The final setup allowed database access without exposing Cloud SQL through the public internet.

### Problems & Solutions

| Problem                       | Solution                                            |
| ----------------------------- | --------------------------------------------------- |
| Private IP connection failed  | Configured VPC peering and Private Service Access   |
| Proxy authentication failed   | Granted the Cloud SQL Client IAM role               |
| Database connection timed out | Verified firewall rules and VPC configuration       |
| Proxy failed to start         | Used the correct Cloud SQL instance connection name |

### Applications

This architecture can be used in:

* Banking systems
* Healthcare applications
* Enterprise ERP systems
* Government applications
* SaaS platforms
* E-commerce backends
* Internal company dashboards

---

# 🤖 Project 2: Google Cloud MCP for AlloyDB

### Connecting AI Agents with Enterprise Data

The second project demonstrates how **Model Context Protocol (MCP)** can be used to allow AI agents to securely interact with an **AlloyDB** database.

Instead of giving an AI agent direct access to the database, MCP acts as a standardized communication layer between the agent and AlloyDB.

### Architecture

```text
AI Agent
    │
    ▼
MCP Server
    │
    ▼
AlloyDB
```

### Key Concepts

* AlloyDB
* Model Context Protocol (MCP)
* AI Agents
* IAM
* SQL
* Python
* Google Cloud
* Vertex AI integrations

### What Was Implemented

1. Provisioned an AlloyDB cluster.
2. Configured networking and IAM permissions.
3. Deployed an MCP server.
4. Connected MCP to AlloyDB.
5. Exposed database operations as MCP tools.
6. Configured an AI agent to communicate through MCP.
7. Executed SQL queries through the AI agent.
8. Retrieved structured information from AlloyDB.

### Problems & Solutions

| Problem                              | Solution                                               |
| ------------------------------------ | ------------------------------------------------------ |
| AI agent could not detect MCP server | Verified server endpoint configuration                 |
| Database authentication failed       | Updated credentials and IAM permissions                |
| SQL queries failed                   | Corrected SQL syntax and table names                   |
| Network timeout                      | Verified AlloyDB networking and firewall configuration |

### Applications

* AI customer support
* Financial analytics
* Healthcare assistants
* HR management
* Supply chain optimization
* AI-powered dashboards
* Business intelligence
* Enterprise data assistants

---

# 🧠 Project 3: Multi-Agent Application

### MCP Toolbox + AlloyDB + Google ADK

The third project builds on the previous MCP architecture by introducing **multiple specialized AI agents**.

Instead of relying on a single AI agent to handle every task, different agents are assigned different responsibilities such as query execution, reasoning, and response generation.

### Architecture

```text
                    User
                     │
                     ▼
              Coordinator Agent
                     │
          ┌──────────┼──────────┐
          ▼          ▼          ▼
    Database Agent  Reasoning  Response
          │          Agent      Agent
          │
          ▼
     MCP Toolbox
          │
          ▼
       AlloyDB
```

### Key Technologies

* Google Cloud Platform
* AlloyDB
* Google Agent Development Kit (ADK)
* Model Context Protocol (MCP)
* MCP Toolbox
* Python
* PostgreSQL
* IAM
* Cloud Shell

### What Was Implemented

1. Configured the AlloyDB database.
2. Connected AlloyDB with MCP Toolbox.
3. Created multiple AI agents using Google ADK.
4. Assigned specialized roles to each agent.
5. Configured communication through MCP Toolbox.
6. Created a coordinator agent to distribute requests.
7. Executed database queries against AlloyDB.
8. Processed retrieved information using the appropriate agents.
9. Returned the final response to the user.

### Problems & Solutions

| Problem                           | Solution                                                  |
| --------------------------------- | --------------------------------------------------------- |
| Agents failed to communicate      | Verified MCP Toolbox configuration and agent registration |
| Tool invocation failed            | Corrected tool configuration and permissions              |
| Database queries returned no data | Validated schema, table names and SQL queries             |
| Authentication issues             | Configured IAM roles and Google Cloud credentials         |

### Applications

Multi-agent AI systems can be used for:

* Enterprise AI assistants
* Automated customer service
* Intelligent banking systems
* Healthcare decision-support
* Legal document analysis
* Research assistants
* Smart manufacturing
* Logistics
* AI-driven business process automation

---

# 🔐 Security Considerations

Security is a major focus across all three projects.

### Project 1

Uses:

* Private IP networking
* VPC
* IAM
* Cloud SQL Auth Proxy
* Encrypted communication

### Project 2

Uses:

* MCP as an intermediary layer
* IAM
* Secure database authentication
* Controlled tool access

### Project 3

Uses:

* MCP Toolbox
* IAM
* Authenticated Google Cloud environment
* Controlled agent-to-tool communication

The progression demonstrates how cloud infrastructure can evolve from secure database connectivity to controlled AI access and finally to secure multi-agent database interaction.

---

# 🛠️ Overall Technology Stack

### Cloud

* Google Cloud Platform
* Compute Engine
* Cloud SQL
* AlloyDB
* VPC
* IAM
* Cloud Shell

### AI

* AI Agents
* Google Agent Development Kit (ADK)
* Model Context Protocol (MCP)
* MCP Toolbox
* Vertex AI integrations

### Programming & Database

* Python
* SQL
* MySQL
* PostgreSQL

---

# 📈 Project Progression

```text
PROJECT 1
Secure Cloud Database
        │
        ▼
Compute Engine + Cloud SQL
        │
        ▼
Private IP + Cloud SQL Proxy
        │
        ▼
PROJECT 2
        │
        ▼
AI Agent + MCP + AlloyDB
        │
        ▼
AI-powered Database Access
        │
        ▼
PROJECT 3
        │
        ▼
Multiple AI Agents
        │
        ▼
ADK + MCP Toolbox + AlloyDB
        │
        ▼
Multi-Agent AI System
```

Together, the three projects demonstrate a progression from **secure cloud infrastructure → AI-powered database interaction → collaborative multi-agent AI systems**.

---

# 🎯 Learning Outcomes

Through these projects, the following concepts were explored:

* Cloud computing fundamentals
* Virtual machines
* Managed relational databases
* VPC networking
* Private IP connectivity
* IAM permissions
* Secure database access
* Cloud SQL Auth Proxy
* AlloyDB
* Model Context Protocol
* AI agents
* Agent Development Kit
* MCP Toolbox
* Multi-agent architecture
* Database querying through AI agents
* Secure AI-to-database communication

---

# 📂 Repository Structure

```text
Google-Cloud-AI-Projects/
│
├── Project-1-Cloud-SQL/
│   └── README.md
│
├── Project-2-AlloyDB-MCP/
│   └── README.md
│
├── Project-3-Multi-Agent-ADK/
│   └── README.md
│
├── system-design/
│   ├── project-1.png
│   ├── project-2.png
│   └── project-3.png
│
└── README.md
```

---

# 👩‍💻 Author

**Avishi Gupta**

B.Tech Computer Science & Engineering

---

## ⭐ Acknowledgement

These projects were developed as part of hands-on exploration of **Google Cloud infrastructure, databases, AI agents, and modern AI application architectures**.
