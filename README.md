# Next-Gen University ERP – Cloud-Native & Production-Ready

A full-stack, cloud-native **University ERP system** engineered to handle real academic workloads with predictable performance, scalable infrastructure, and clean system separation.  
Built and completed as part of the **S1 – WEBAPP final round**.

---

## Hackathon Track

**S1 – WEBAPP**

This project focuses on:
- Clean web interface
- Backend APIs
- Scalable storage
- Stable routing
- Production-style system design

This repository represents the **completed final-round submission**, not a prototype.

---

## System Overview

The ERP is implemented as a **layered, full-stack web application** with clear separation between frontend, backend, and storage.


This structure enables independent development, testing, and scaling of each layer.

---

## Core Objectives Achieved

- Eliminated full page reloads using SPA architecture
- Introduced a dedicated backend for business logic
- Designed storage layers based on access patterns
- Deployed using cloud infrastructure suitable for real traffic
- Ensured modularity and maintainability across the system

---

## Tech Stack – Detailed Implementation

### Frontend – React (Single Page Application)

The frontend is implemented as a **React SPA** responsible for all user interaction and navigation.

**Key Characteristics**
- Client-side routing for seamless navigation between ERP modules
- Persistent layout across pages to avoid redundant reloads
- Modular component design (dashboards, tables, forms)
- Responsive UI for desktop, tablet, and mobile usage

**Why this matters**
Traditional ERPs reload the entire page for every action, which degrades performance under load.  
The SPA approach ensures:
- Faster navigation
- Reduced network overhead
- Better user experience during peak usage

---

### Backend – Dedicated API Layer

A separate backend layer is implemented inside the `Backend/` directory.

**Responsibilities**
- Centralized business logic
- API endpoints for frontend consumption
- Request validation and processing
- Coordination between data and storage layers

**Why a dedicated backend**
- Prevents logic duplication in the frontend
- Improves maintainability and debugging
- Enables scalability independent of UI traffic
- Aligns with production ERP architecture patterns

This backend design allows the system to grow without restructuring the frontend.

---

### Compute – AWS EC2

Backend services are hosted on **Amazon EC2**.

**Rationale**
- Full control over runtime environment
- Suitable for long-running API services
- Can scale vertically or horizontally based on demand

EC2 ensures the system remains responsive during:
- Exam form openings
- Result announcements
- Fee deadline traffic spikes

---

### Database – Amazon DynamoDB

All core ERP data is stored in **Amazon DynamoDB**, including:
- Student records
- Course and subject mappings
- Attendance data
- Results and fee information

**Why DynamoDB**
- Designed for high-concurrency workloads
- Low-latency reads and writes
- Automatically handles traffic bursts
- No manual tuning required during peak periods

This avoids database bottlenecks commonly seen in legacy ERP systems.

---

### File Storage – Amazon S3

Documents such as:
- Admit cards
- Marksheets
- Notices
- Static assets

are stored in **Amazon S3**.

**Why S3**
- Separates file access from core application logic
- Scales independently from backend compute
- High durability and availability

This ensures file downloads never impact API responsiveness.

---

## System Architecture

### High-Level Architecture Diagram

Here's how the entire system is structured and how data flows through it:


![Uni ERP System Architecture Diagram](uni_erp_architecture.png)


The architecture enforces:
- Clear separation of concerns
- Independent scaling of layers
- Fault isolation between UI, logic, and storage

---

## Database Design Reference

The file `tableStructure.txt` documents the core data entities and relationships used in the system.

This demonstrates:
- Thoughtful data modeling
- Alignment with real ERP requirements
- Preparation for long-term system extension

---

## Frontend Design Principles

- Modular UI components for maintainability
- Layouts optimized for dense academic data
- Responsive behavior across devices
- Navigation optimized for frequent daily usage

The UI is designed for **actual institutional use**, not just demonstration.

---

## Backend Design Principles

- Clean API boundaries
- Centralized validation
- Consistent response structures
- Error handling at the service level

This backend structure supports long-term stability and extensibility.

---

## Deployment & Reliability

The system is deployed using:
- AWS EC2 for compute
- DynamoDB for structured data
- S3 for file storage

The infrastructure is designed to handle:
- Normal daily usage
- Sudden traffic spikes
- Concurrent access from large user groups

---

## Project Status – Final Round

### Completed
- React SPA frontend with stable routing
- Backend API layer
- Cloud deployment (EC2, DynamoDB, S3)
- Database design and storage integration
- Responsive UI verified across devices

### Validated Through Testing
- Smooth navigation across modules
- No unnecessary full page reloads
- Stable behavior under concurrent access
- Backend and frontend operate as independent layers

---

## Demo

🎥 Demonstration Video:  
https://drive.google.com/file/d/1l0t6YZ99RNTzE2yT_DiJyQyueOVngCpq/view

---

## Final Notes

This project represents a **completed, full-stack ERP system** built with production principles in mind.

It demonstrates:
- Architectural decision-making
- Scalable infrastructure usage
- Clear separation of concerns
- Awareness of real-world academic traffic patterns

The system is not a conceptual demo, but a **deployable foundation** suitable for real institutional environments.
