# Nexcore ERP

Nexcore ERP is a backend-first, API-driven ERP core designed to be **generic, modular, and predictable**.

It focuses on building a **reliable business and financial core** before frontend polish, BI layers, or legacy-system coupling.

The architecture is intentionally **domain-agnostic**, making it adaptable to different industries through integration layers, ETL, and staging pipelines.

---

## Overview

Nexcore ERP was designed around a simple principle:  
**core business rules must be explicit, auditable, and stable**.

Instead of coupling the system to a specific operation or legacy flow, the project separates:

- **core domain logic**
- **integration and import flows**
- **financial events**
- **inventory traceability**

This allows the ERP core to evolve predictably while remaining reusable across multiple business contexts.

---

## Tech Stack

- Python 3.12
- FastAPI
- PostgreSQL
- SQLAlchemy
- Alembic
- Docker / Docker Compose
- React + TypeScript (frontend)

---

## Architecture

High-level flow:

**Client / Frontend / Swagger**  
→ **FastAPI API layer**  
→ **Domain services and business rules**  
→ **PostgreSQL**

External or legacy systems are integrated **outside the core** through ETL and staging processes.

---

## Core Principles

- **API-first architecture**
- **Explicit input/output contracts**
- **Clear separation of domain vs integration logic**
- **Immutable operational events where auditability matters**
- **Financial consistency through atomic transactions**
- **Database evolution managed through migrations only**
- **Predictable backend behavior over hidden side effects**

---

## Functional Scope

Current project scope includes:

- Authentication and access control
- Customer management
- Product and unit-of-measure management
- Order creation and editing
- Inventory movement tracking
- Purchase import flow (NF-e XML based)
- Accounts payable
- Accounts receivable
- Dashboard and operational visibility

---

## Business Highlights

### Inventory Traceability
Inventory is modeled with a traceable movement-based approach, prioritizing auditability and consistency over silent state mutations.

### Financial Synchronization
Operational events and financial records are tightly aligned to reduce divergence between business actions and accounting state.

### Purchase Import Flow
NF-e XML ingestion follows a structured flow with validation, preview, matching, and confirmation steps.

### Backend Authority
Critical calculations and validations are enforced on the backend to ensure consistency regardless of client behavior.

---

## Why this project matters

This project reflects how I think about software engineering:

- strong backend foundations first
- explicit business rules
- predictable state transitions
- auditability in financial and inventory operations
- modular design for long-term reuse

It is not just a CRUD app — it is an attempt to build an ERP core with **real operational discipline**.

---

## Current Status

The project is under active development and already supports real end-to-end operational flows across sales, purchases, inventory, and finance.

Current focus areas:

- API consistency
- domain refinement
- operational robustness
- scalable evolution of the core architecture

---

## Roadmap

Planned evolution includes:

- deeper financial workflows
- richer reporting and dashboarding
- stronger integration pipelines
- expanded ERP modules
- production-hardening of the platform

---

## Screenshots

### NF-e Import Flow
![NF-e Import](./Images/puschase_NFe_import.png)

### Dashboard
![Dashboard](./Images/dashboard.png)

### Purchases
![Purchases](./Images/purchase_detail.png)
![Purchases](./Images/purchases.png)

### Orders
![Orders](./Images/order_detail.png)

### Product Detail
![Product Detail](./Images/product_detail.png)

---

## Notes

This repository is intended as a **public showcase** of the project vision, architecture, and engineering direction.

The full private implementation contains the active development core and detailed internal structure.