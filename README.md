# Next-Gen University ERP – Fast, Scalable, Student-First

A modern, cloud-native **University ERP system** designed to stay fast, reliable, and responsive during real-world peak usage such as exam registrations, result announcements, and fee deadlines.

---

## Problem Set

This project is being built for the **S1 – WEBAPP** problem set.

> Build any product with a clean web or mobile interface. Focus on data flow, backend APIs, authentication, and real-time interactions. Solutions should feel production-ready with stable routing and storage layers.

Our ERP fits S1 because:
- It has a clean, responsive **web interface** built with React.
- It uses **backend APIs** hosted on AWS EC2.
- It relies on **scalable storage layers** (DynamoDB and S3).
- It focuses on **stable client-side routing** (React SPA) and production-style architecture.

---

## Problem Statement

Most universities rely on ERP systems that are supposed to quietly handle everything in the background — attendance, results, fees, exam forms, notices, and more.  
In reality, these systems struggle the moment real traffic shows up.

During peak times like:
- Online exam registrations
- Result announcements
- Fee payment deadlines

students and faculty face:
- Pages that take too long to load or time out  
- Systems that crash mid-submission  
- Clunky workflows where every click reloads a heavy page  

Instead of simplifying campus life, ERPs often:
- Cause missed deadlines and incomplete submissions  
- Create long queues at admin offices  
- Force staff to handle manual workarounds  

This project aims to fix that experience instead of accepting it as normal.

---

## Why This Project Exists

Ask students or faculty about their ERP and the reaction is usually the same — slow, awkward, and unreliable when it matters most.

On result days and form deadlines:
- Simple pages take ages to load  
- Sessions randomly break or log users out  
- Every action feels like click → redirect → reload → wait  

A system meant to be the digital backbone of a university ends up being something users fight with rather than rely on.

We wanted to fix the **foundation**, not just redesign the UI.

---

## What We Are Building

A **fast, modern, cloud-native university ERP** designed to behave correctly under real-world load, not just ideal demo conditions.

---

## Tech Stack (Brief)

### Frontend
- **React (Single Page Application)**  
  Enables client-side routing, reusable components, and smooth navigation without full page reloads.

### Backend
- **API-based backend (Phase 2)**  
  Handles business logic and data access, keeping the frontend lightweight and scalable.

### Compute
- **AWS EC2**  
  Hosts backend services and allows scaling during traffic spikes.

### Database
- **Amazon DynamoDB**  
  Provides low-latency, scalable storage for core ERP data such as students, courses, attendance, and results.

### File Storage
- **Amazon S3**  
  Stores documents like marksheets and notices, preventing heavy file traffic from overloading servers.

---

## Frontend: React SPA with Stable Routing

- Built as a **Single Page Application**
- Navigation between modules happens via client-side routing
- Avoids unnecessary full-page reloads

### UI Characteristics
- Modular dashboard cards, tables, and forms
- Fully responsive across laptops, tablets, and phones
- Designed for daily academic use, not just demos

---

## System Architecture

### High-Level Architecture

![Uni ERP System Architecture Diagram](uni_erp_architecture.png)

### Data Flow

