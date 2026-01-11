# Next-Gen University ERP – Fast, Scalable, Student-First

A modern, cloud-native **University ERP system** designed to remain fast, reliable, and responsive during real-world peak usage such as exam registrations, result announcements, and fee deadlines.

---

## Problem Set

This project is being built for the **S1 – WEBAPP** problem set.

> Build any product with a clean web or mobile interface. Focus on data flow, backend APIs, authentication, and real-time interactions. Solutions should feel production-ready with stable routing and storage layers.

Our ERP fits S1 because:
- It provides a clean, responsive **web interface** using React.
- It uses **backend APIs** instead of static or mock data.
- It relies on **cloud-based storage and compute** (AWS).
- It focuses on **stable routing** and production-style system design.

---

## Problem Statement

Most universities rely on ERP systems that are expected to quietly manage attendance, results, fees, exam forms, notices, and other academic workflows.  
In practice, these systems struggle the moment real traffic appears.

During peak times such as:
- Online exam registrations  
- Result announcements  
- Fee payment deadlines  

students and faculty face:
- Pages that take too long to load or time out  
- Systems crashing during important submissions  
- Clunky workflows with full page reloads on every action  

Instead of simplifying campus operations, ERPs often:
- Cause missed deadlines and incomplete forms  
- Create long queues at admin offices  
- Force staff to rely on manual workarounds  

This project aims to fix these foundational issues instead of accepting them as normal.

---

## Why This Project Exists

For students and faculty, ERP systems are often:
- Slow
- Difficult to navigate
- Unreliable during critical periods

On result days and submission deadlines:
- Simple actions take several seconds
- Sessions randomly expire
- Each click triggers a redirect and full reload

A system meant to be the digital backbone of a university ends up being something users struggle against instead of rely on.

We wanted to build an ERP where **performance and reliability are the default**, not a bonus.

---

## What We Are Building

A **fast, modern, cloud-native university ERP** designed to behave correctly under real-world usage conditions, not just ideal demo scenarios.

---

## Tech Stack (Detailed)

### Frontend – React (Single Page Application)

The frontend is built as a **Single Page Application (SPA)** using React.

**Why React SPA?**
- Enables **client-side routing**, eliminating unnecessary full page reloads.
- Improves perceived performance, especially on slower networks.
- Allows modular, reusable UI components suitable for large systems like ERPs.
- Keeps navigation smooth even when moving between complex modules such as attendance, results, and fees.

**Frontend Responsibilities**
- UI rendering and layout
- Client-side routing between ERP modules
- Handling form inputs and validations
- Communicating with backend APIs

---

### Backend – API-Based Architecture

The backend is structured as a separate **API layer** (introduced in Phase 2).

**Why a dedicated backend?**
- Separates business logic from UI concerns.
- Allows the frontend to remain lightweight.
- Makes the system easier to scale and maintain.
- Enables future support for authentication, authorization, and role-based access.

**Backend Responsibilities**
- Handling requests from the frontend
- Validating and processing data
- Interacting with the database and storage services
- Acting as the central control layer of the ERP

---

### Compute – AWS EC2

Backend services are hosted on **Amazon EC2**.

**Why EC2?**
- Provides flexibility to scale vertically or horizontally during peak loads.
- Avoids the limitations of single, fixed on-prem servers.
- Suitable for production-style deployments rather than academic demos.

EC2 allows the system to remain responsive during sudden traffic spikes such as result releases or exam form deadlines.

---

### Database – Amazon DynamoDB

Core ERP data is stored in **Amazon DynamoDB**, including:
- Student records
- Course data
- Attendance information
- Results and fee records

**Why DynamoDB?**
- Designed for **high-concurrency access**.
- Offers low-latency reads and writes at scale.
- Eliminates the need for manual database tuning during traffic spikes.

This makes it well-suited for university systems where thousands of users may access data simultaneously.

---

### File Storage – Amazon S3

Documents such as:
- Marksheets
- Admit cards
- Notices
- Other static files  

are stored in **Amazon S3**.

**Why S3?**
- Offloads heavy file traffic from application servers.
- Highly reliable and scalable.
- Ensures document downloads do not affect core application performance.

---

## Frontend Design & UX

- Built with reusable, modular components
- Fully responsive across laptops, tablets, and mobile devices
- Designed for dense academic data without overwhelming users
- Avoids legacy ERP patterns such as cluttered tables and constant reloads

The goal is not just functionality, but usability for daily academic workflows.

---

## System Architecture

### High-Level Architecture

Here's how the entire system is structured and how data flows through it:


![Uni ERP System Architecture Diagram](uni_erp_architecture.png)


The system is designed with clear separation between:
- Presentation layer (React frontend)
- Application logic (backend APIs)
- Data storage (DynamoDB)
- File storage (S3)

---

## Backend & Infrastructure Philosophy

University traffic patterns are not uniform:
- Normal usage most of the semester
- Extreme spikes during deadlines and announcements

This system is designed with those spikes as a **baseline assumption**, not an edge case.

- Compute scales independently
- Database handles concurrent access
- File downloads are isolated from core logic

---

## Current Progress (Hackathon – Round 1)

### Completed
- Core React SPA structure
- Stable client-side routing
- Responsive UI across devices
- Partial backend API integration
- Deployment using AWS EC2, DynamoDB, and S3

### Observations
- Navigation between sections feels instant
- No unnecessary full page reloads
- Implemented modules behave like a real product rather than a prototype

### Demo Video
https://drive.google.com/file/d/1l0t6YZ99RNTzE2yT_DiJyQyueOVngCpq/view

---

## What’s Left Before the Final Round

- Make all modules fully dynamic via backend APIs
- Complete remaining core backend endpoints
- Improve error handling and loading states
- Harden the system for production-like reliability

---

## Why This Project Matters

This is not a simple CRUD application or a demo ERP.

It addresses a real, recurring problem:
- University systems failing under peak usage
- Students and staff losing trust in core infrastructure
- “Server down” becoming an accepted norm

By combining:
- A React SPA frontend
- A dedicated backend API layer
- Scalable cloud compute
- High-concurrency data storage
- Reliable file handling

this project aims to build a university ERP that is designed to **stay up, stay fast, and scale** when it matters most.

It represents the kind of ERP system we wish our own universities actually had.
