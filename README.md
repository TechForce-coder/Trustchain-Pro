# 🔐 TrustChain Pro

### Sovereign Identity • Policy-Based Access • Digital Asset Governance

**Blockchain-Based Secure Platform for Identity, Access Control, and Digital Asset Management**

**Smart India Hackathon 2026 • SIH26125 • Team Tech Force**

---

## 📌 Table of Contents

* [Overview](#-overview)
* [Problem Statement](#-problem-statement)
* [Our Solution](#-our-solution)
* [Key Features](#-key-features)
* [How It Works](#-how-it-works)
* [System Architecture](#-system-architecture)
* [Technology Stack](#-technology-stack)
* [Security Model](#-security-model)
* [Digital Asset Lifecycle](#-digital-asset-lifecycle)
* [Validator Network](#-validator-network)
* [Dashboard](#-dashboard)
* [Demo](#-demo)
* [Use Cases](#-use-cases)
* [Impact](#-impact)
* [References](#-references)

---

## 🚀 Overview

**TrustChain Pro** is an advanced security platform designed to combine **decentralized digital identity, dynamic policy-based access control, and tamper-evident digital asset management** into a unified ecosystem.

The platform addresses security challenges associated with centralized identity and asset-management systems by combining cryptographic authentication, policy-based authorization, digital asset ownership, hash-chained records, and distributed validation.

### Core Components

* **Decentralized Identifiers (DIDs)** for digital identities
* **ECDSA P-256 authentication** using the Web Crypto API
* **Hybrid RBAC + ABAC authorization**
* **NFT-based digital asset ownership**
* **Smart-contract governance logic**
* **SHA-256 hash chaining**
* **MongoDB Atlas** for persistent records
* **Socket.IO** for real-time synchronization
* **Distributed validator-node architecture**
* **Live audit and tamper-detection dashboard**

---

## 🎯 Problem Statement

### SIH26125

**Blockchain-Based Secure Platform for Identity, Access Control, and Digital Asset Management**

Traditional centralized systems can create several security and operational challenges:

| Challenge                              | Problem                                                  |
| -------------------------------------- | -------------------------------------------------------- |
| 🔐 **Centralized Identity**            | Dependence on a single administrative authority          |
| ⚠️ **Single Point of Failure**         | Central-system failure can affect the complete system    |
| 🕵️ **Identity Theft & Cyber Attacks** | Credential abuse, phishing, and unauthorized access      |
| 🚫 **Unauthorized Access**             | Improper privileges can lead to access misuse            |
| 📦 **Asset Ownership Verification**    | Difficult to verify ownership and asset history          |
| 📜 **Opaque Audit Trails**             | Difficult to maintain transparent and verifiable history |

---

# 💡 Our Solution

TrustChain Pro introduces a multi-layered security pipeline:

```text
┌─────────────────────────────┐
│            USER             │
│ Register / Login / Action   │
└──────────────┬──────────────┘
               │
               ▼
┌─────────────────────────────┐
│        DID IDENTITY         │
│    Decentralized Identity   │
└──────────────┬──────────────┘
               │
               ▼
┌─────────────────────────────┐
│      ECDSA P-256 SIGNING    │
│       Web Crypto API        │
└──────────────┬──────────────┘
               │
               ▼
┌─────────────────────────────┐
│         RBAC + ABAC         │
│   Role + Context Evaluation │
└──────────────┬──────────────┘
               │
        ┌──────┴──────┐
        ▼             ▼
┌──────────────┐ ┌───────────────┐
│ Access Check │ │ Asset Request │
└──────┬───────┘ └───────┬───────┘
       │                 │
       └────────┬────────┘
                ▼
┌─────────────────────────────┐
│    GOVERNANCE / NFT LOGIC   │
└──────────────┬──────────────┘
               │
               ▼
┌─────────────────────────────┐
│      SHA-256 HASH CHAIN     │
│     Tamper-Evident Ledger   │
└──────────────┬──────────────┘
               │
               ▼
┌─────────────────────────────┐
│   DISTRIBUTED VALIDATORS    │
│ Delhi • Bengaluru • Mumbai  │
└──────────────┬──────────────┘
               │
               ▼
┌─────────────────────────────┐
│     LIVE AUDIT DASHBOARD    │
└─────────────────────────────┘
```

---

# ✨ Key Features

## 🪪 1. Decentralized Identity

* DID-based identity model
* Self-sovereign identity concept
* Passwordless cryptographic authentication
* ECDSA P-256 key pairs
* Browser-side signing through Web Crypto API

---

## 🛡️ 2. Hybrid RBAC + ABAC

TrustChain Pro combines **Role-Based Access Control (RBAC)** with **Attribute-Based Access Control (ABAC)**.

Access decisions can consider:

* User role
* Clearance level
* Permissions
* Time
* Location
* Device/context
* Network conditions
* Dynamic risk score

This allows access decisions to consider both **who the user is** and **the context of the request**.

---

## 🧾 3. Digital Asset Ownership

The platform provides NFT-based digital asset representation for traceable ownership.

Features include:

* Unique asset representation
* DID-linked ownership
* Asset allocation
* Transfer workflows
* Ownership history
* Asset provenance tracking

---

## ⚙️ 4. Smart-Contract Governance

Governance logic controls:

* Asset creation
* Asset metadata binding
* Asset allocation
* Transfer authorization
* Multi-party approval
* Policy enforcement

---

## 🔗 5. Tamper-Evident Ledger

TrustChain Pro uses SHA-256 hash chaining to make unauthorized modification detectable.

```text
Previous Hash
      +
Transaction Data
      +
Metadata
      │
      ▼
   SHA-256
      │
      ▼
New Block Hash
```

Each block is linked with the previous hash.

Conceptually:

```text
Block 1
   │
   ├── Hash 1
   ▼
Block 2
   │
   ├── Previous Hash = Hash 1
   ├── Transaction Data
   ▼
   Hash 2
   │
   ▼
Block 3
```

If stored transaction data is modified, the resulting hash can differ from the expected chain value, allowing tampering to be detected.

---

## 🌐 6. Distributed Validation

The prototype demonstrates a three-node validator architecture:

| Validator Node               | Location  | Responsibility           |
| ---------------------------- | --------- | ------------------------ |
| **Government Registry Node** | Delhi     | Registry validation      |
| **Public Audit Node**        | Bengaluru | Audit verification       |
| **Independent Auditor Node** | Mumbai    | Independent verification |

---

## 📊 7. Live Audit Dashboard

The dashboard provides visibility into:

* ✅ Consensus status
* 🔗 Block hash verification
* 📜 Access history
* 🚨 Tamper detection
* 🟢 Node health
* 📦 Approved block data
* ⚡ Real-time updates

---

# 🔄 How It Works

### Step 1 — Request Generation

The user initiates an operation such as:

```text
Transfer
Read
Access
Asset Minting
```

### Step 2 — Cryptographic Signing

The request payload is signed locally using:

```text
DID + ECDSA P-256
```

The Web Crypto API handles the browser-side cryptographic operation.

### Step 3 — Zero-Trust Evaluation

The backend validates:

```text
Signature
    ↓
Identity
    ↓
Role
    ↓
Attributes
    ↓
Context
    ↓
Risk
```

### Step 4 — Authorization

The system produces an explicit:

```text
APPROVED
```

or

```text
DENIED
```

decision.

### Step 5 — Ledger Storage

Approved transactions are recorded using SHA-256 hash chaining.

### Step 6 — Network Broadcast

Socket.IO broadcasts relevant updates to the validator nodes.

### Step 7 — Audit & Verification

The live dashboard displays the updated system state and validation information.

---

# 🏗️ System Architecture

```text
┌─────────────────────────────────────────────────────────────┐
│                      CLIENT LAYER                           │
│                                                             │
│          React.js + Web Crypto API + Dashboard              │
└──────────────────────────┬──────────────────────────────────┘
                           │
                           ▼
┌─────────────────────────────────────────────────────────────┐
│                   APPLICATION LAYER                         │
│                                                             │
│                  Node.js + Express.js                       │
│                                                             │
│ Signature Verification │ RBAC │ ABAC │ Governance │ APIs    │
└──────────────────────────┬──────────────────────────────────┘
                           │
             ┌─────────────┴─────────────┐
             ▼                           ▼
┌──────────────────────────┐   ┌─────────────────────────────┐
│       DATA / LEDGER      │   │      REAL-TIME NETWORK      │
│                          │   │                             │
│      MongoDB Atlas       │   │         Socket.IO           │
│    SHA-256 Hash Chain    │   │    Node Synchronization     │
└────────────┬─────────────┘   └──────────────┬──────────────┘
             │                                │
             └────────────────┬───────────────┘
                              ▼
             ┌────────────────────────────────┐
             │     DISTRIBUTED VALIDATORS     │
             │                                │
             │ Delhi │ Bengaluru │ Mumbai     │
             └────────────────┬───────────────┘
                              │
                              ▼
             ┌────────────────────────────────┐
             │       LIVE AUDIT DASHBOARD     │
             └────────────────────────────────┘
```

---

# 🧰 Technology Stack

| Layer             | Technology           | Purpose                      |
| ----------------- | -------------------- | ---------------------------- |
| **Frontend**      | React.js             | User interface and dashboard |
| **Styling**       | Tailwind CSS         | Interface styling            |
| **Cryptography**  | Web Crypto API       | ECDSA P-256 signing          |
| **Backend**       | Node.js              | Server runtime               |
| **API Framework** | Express.js           | REST APIs and business logic |
| **Database**      | MongoDB Atlas        | Persistent data storage      |
| **Integrity**     | SHA-256              | Hash chaining                |
| **Identity**      | DID                  | Decentralized identity       |
| **Authorization** | RBAC + ABAC          | Access control               |
| **Asset Model**   | NFT                  | Digital asset ownership      |
| **Real-Time**     | Socket.IO            | Node synchronization         |
| **Governance**    | Smart-contract logic | Asset governance             |

---

##

---

>

---

# 🔐 Security Model

TrustChain Pro follows a layered security approach:

```text
┌──────────────────┐
│ Decentralized ID │
└────────┬─────────┘
         ▼
┌──────────────────┐
│   ECDSA P-256    │
│  Authentication  │
└────────┬─────────┘
         ▼
┌──────────────────┐
│   RBAC + ABAC    │
│  Authorization   │
└────────┬─────────┘
         ▼
┌──────────────────┐
│  Context / Risk  │
│    Evaluation    │
└────────┬─────────┘
         ▼
┌──────────────────┐
│    Governance    │
└────────┬─────────┘
         ▼
┌──────────────────┐
│  SHA-256 Ledger  │
└────────┬─────────┘
         ▼
┌──────────────────┐
│ Validator Nodes  │
└──────────────────┘
```

---

# 🪙 Digital Asset Lifecycle

```text
┌─────────────────┐
│ Asset Creation  │
└────────┬────────┘
         ▼
┌─────────────────┐
│  Authorization   │
└────────┬────────┘
         ▼
┌─────────────────┐
│   NFT Minting   │
└────────┬────────┘
         ▼
┌─────────────────┐
│    Allocation   │
└────────┬────────┘
         ▼
┌─────────────────┐
│ Transfer Request│
└────────┬────────┘
         ▼
┌─────────────────┐
│   Governance    │
└────────┬────────┘
         ▼
┌─────────────────┐
│ Ownership Log   │
└─────────────────┘
```

---

# 🌐 Validator Network

The prototype demonstrates a distributed validator architecture across three logical nodes:

| Validator                    | Location  | Role                     |
| ---------------------------- | --------- | ------------------------ |
| **Government Registry Node** | Delhi     | Registry validation      |
| **Public Audit Node**        | Bengaluru | Audit verification       |
| **Independent Auditor Node** | Mumbai    | Independent verification |

```text
                 ┌─────────────────┐
                 │  Delhi Registry │
                 │      Node       │
                 └────────┬────────┘
                          │
                          ▼
                 ┌─────────────────┐
                 │ Block / Data    │
                 │ Synchronization │
                 └────────┬────────┘
                          │
             ┌────────────┴────────────┐
             ▼                         ▼
   ┌─────────────────┐       ┌─────────────────┐
   │    Bengaluru    │       │     Mumbai      │
   │  Public Audit   │       │   Independent   │
   │      Node       │       │  Auditor Node   │
   └─────────────────┘       └─────────────────┘
```

---

# 📊 Dashboard

The TrustChain Pro dashboard provides:

### Consensus Monitoring

Displays the synchronization state of validator nodes.

### Block Verification

Provides visibility into SHA-256 hash verification.

### Access History

Records access requests and authorization events.

### Tamper Detection

Helps identify inconsistencies in hash-linked records.

### Node Health

Displays the status of participating validator nodes.

### Live Updates

Socket.IO provides real-time updates to the interface.

---

# 🎥 Demo

### Animation Video

https://www.youtube.com/watch?v=0Db1RHNCBF4

### Prototype Demonstration 

https://youtu.be/EiAhNy8VCxE

---
# 🌍 Use Cases

## 🛡️ Defense

* Sensitive digital asset management
* Classified document integrity
* Blueprint records
* Supply-chain data

## 🏛️ Government

* Cross-department asset governance
* Identity management
* Verifiable ownership records
* Audit workflows

## 🏢 Enterprise

* Digital credentials
* Licenses
* Intellectual property
* Supply-chain management
* Compliance-oriented audit workflows

---

# 📈 Impact

| Area                  | Expected Impact                         |
| --------------------- | --------------------------------------- |
| 🔐 **Security**       | Stronger identity and access protection |
| ⚙️ **Efficiency**     | Automated authorization and governance  |
| 📋 **Accountability** | Traceable transaction history           |
| 📈 **Scalability**    | Modular validator architecture          |
| 📜 **Compliance**     | Audit-oriented record keeping           |


---

# 📚 References

1. **W3C — Decentralized Identifiers (DIDs) v1.0**
   https://www.w3.org/TR/did-core/

2. **Ministry of Electronics and Information Technology — Data Protection Framework**
   https://www.meity.gov.in/data-protection-framework

3. **NIST SP 800-207 — Zero Trust Architecture**
   https://csrc.nist.gov/pubs/sp/800/207/final

4. **W3C — Web Cryptography API**
   https://www.w3.org/TR/WebCryptoAPI/

5. **Haber & Stornetta — How to Time-Stamp a Digital Document**
   https://www.anf.es/pdf/Haber_Stornetta.pdf

6. **Smart India Hackathon**
   https://www.sih.gov.in/
