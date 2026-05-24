# A9 Express – Transport Booking Platform
## Software Requirement Specification

**By**

| Name | Index |
|---|---|
| Thevarasa Dayastan | SE/2022/007 |
| Arulanantham Mathumithan | SE/2022/015 |
| Vasanthakumar Arushanth | SE/2022/016 |
| Surenthiran Sathurjan | SE/2022/035 |
| Ensilirukman Ronald | SE/2022/043 |

*A report submitted in partial fulfilment of the requirements for the degree of Bachelor of Science Honours in Software Engineering (B.Sc.SE)*

Software Engineering Teaching Unit  
Faculty of Science  
University of Kelaniya  
Sri Lanka  
2026

---

## Version History

| Version | Date | Description | Author |
|---|---|---|---|
| 1.0 | 2026-03-21 | Initial SRS draft | Team |

---

## Table of Contents

- [Chapter 1: Introduction](#chapter-1-introduction)
- [Chapter 2: Project Scope and Stakeholders](#chapter-2-project-scope-and-stakeholders)
- [Chapter 3: Functional Requirements](#chapter-3-functional-requirements)
- [Chapter 4: Non-Functional Requirements](#chapter-4-non-functional-requirements)
- [Chapter 5: Business Rules, Constraints and Assumptions](#chapter-5-business-rules-constraints-and-assumptions)
- [Chapter 6: Use Case Diagrams](#chapter-6-use-case-diagrams)
- [Chapter 7: Use Case Descriptions](#chapter-7-use-case-descriptions)
- [Chapter 8: Activity & Sequence Diagrams](#chapter-8-activity--sequence-diagrams)
- [Chapter 9: External Interface Requirements](#chapter-9-external-interface-requirements)
- [Chapter 10: Data Requirements](#chapter-10-data-requirements)
- [Chapter 11: Alternative Solutions Considered](#chapter-11-alternative-solutions-considered)
- [Chapter 12: Feasibility Study](#chapter-12-feasibility-study)

---

## Chapter 1: Introduction

The **A9 Express – Transport Booking Platform** is a unified digital transportation management system designed to modernize and simplify transport service bookings in Sri Lanka. The platform integrates private bus ticket reservations, airport transfer services, and customizable tour package bookings into a single online system.

Currently, many transport operators rely on fragmented booking systems, manual coordination methods, and third-party platforms that provide limited flexibility, weak operator branding, and poor customer relationship management. Existing solutions mainly focus on basic seat reservations and lack integrated support for airport transfers and personalized tour services.

The proposed system centralizes transport operations by enabling operators to manage routes, schedules, pricing, bookings, and customer interactions through a dedicated platform. Customers can conveniently reserve transport services, customize Sri Lankan tour packages by selecting tourist destinations, and receive real-time booking updates through a user-friendly interface.

The system aims to improve operational efficiency, strengthen operator brand identity, provide flexible transport solutions, and enhance overall customer experience.

### 1.1 Purpose

The purpose of this document is to provide a detailed description of the functional and non-functional requirements of the A9 Express – Transport Booking Platform.

This document serves as a reference for developers, stakeholders, project supervisors, and clients to understand the system requirements, functionalities, constraints, and expected behavior before development begins.

The system is intended to provide a centralized transport booking solution that supports:

- Private bus ticket reservations
- Airport pickup and drop booking services
- Customizable Sri Lankan tour packages
- Real-time booking management
- Operator branding and pricing control

Additionally, the system allows users to select tourist attractions within Sri Lanka and automatically generate customized travel packages with calculated pricing based on selected destinations and services.

**Intended Audience:**

- Customers / Passengers
- Company Owners / Managers
- Drivers and Staff
- Tour Operators
- System Administrators
- Software Developers

### 1.2 Scope

**System Name:** A9 Express – Transport Booking Platform

**In scope:**

- Manage customer registrations and user accounts
- Enable real-time private bus seat booking
- Manage routes, schedules, and transport availability
- Provide airport pickup and drop booking services
- Allow customers to create customizable Sri Lankan tour packages
- Calculate package pricing based on selected tourist destinations
- Support online booking management and cancellation
- Provide operator branding and pricing customization
- Generate booking confirmations and notifications
- Maintain customer booking history
- Provide analytics and reporting features for operators
- Manage vehicles, drivers, and staff schedules

**Out of scope:**

- International transport booking services
- Airline ticket reservations
- Hotel reservation management
- Multi-country tour management
- Cryptocurrency payment processing

### 1.3 Definitions, Acronyms, and Abbreviations

| Term | Definition |
|---|---|
| Admin | System administrator responsible for managing the platform |
| Customer | User who books transport or tour services |
| Operator | Company managing transport services |
| Driver | Staff member responsible for transportation services |
| Booking | Reservation made by a customer |
| Tour Package | Customized travel package created using selected destinations |
| Airport Transfer | Transport service for airport pickup and drop |
| Real-Time Booking | Instant availability and booking updates |
| GPS | Global Positioning System used for tracking |
| SRS | Software Requirement Specification |
| UI | User Interface |
| Database | Organized collection of application data |
| API | Application Programming Interface |

### 1.4 Document Overview

- **Chapter 1** presents an introduction to the system, including its purpose, scope, definitions, and document overview.
- **Chapter 2** describes the project scope, existing problems, proposed solutions, stakeholders, and target users.
- **Chapter 3** defines the functional requirements of the system.
- **Chapter 4** specifies the non-functional requirements related to performance, security, usability, reliability, and scalability.
- **Chapter 5** outlines the business rules, assumptions, and system constraints.
- **Chapters 6 to 8** present the system models, including use case diagrams, use case descriptions, and activity diagrams.
- **Chapter 9** defines the external interface requirements.
- **Chapter 10** describes the data requirements.
- **Chapter 11** discusses alternative solutions and their limitations.
- **Chapter 12** evaluates the technical, operational, economic, and schedule feasibility of the system.

---

## Chapter 2: Project Scope and Stakeholders

### 2.1 Project Scope

The A9 Express – Transport Booking Platform aims to develop a web-based integrated transport management and booking system that modernizes transportation services in Sri Lanka. The platform consolidates private bus reservations, airport transfer bookings, and customizable tour package management into a single, unified digital solution.

**Key goals of the system include:**

- Eliminate fragmented and manual booking processes used by transport operators
- Provide customers with a convenient, real-time online booking experience
- Enable operators to manage routes, schedules, pricing, and vehicles through a centralized dashboard
- Allow customers to build personalized Sri Lankan tour packages by selecting destinations, with automated pricing calculation
- Strengthen operator brand identity through a dedicated platform
- Improve operational efficiency in managing drivers, staff, and vehicle schedules
- Provide analytics and reporting tools to support data-driven decision-making by operators

### 2.2 Stakeholders

| Stakeholder | Role |
|---|---|
| Company Owner | Primary decision maker and platform owner; controls operator branding, pricing, routes, and business operations |
| System Administrator | Manages platform-wide configurations, user permissions, system health, and technical operations |
| Passengers | End users who register, search, and book bus tickets, airport transfers, or customized tour packages |
| Drivers | Staff responsible for executing transport services; managed through the platform for scheduling and assignments |
| Tour Operators | Manage and configure tour packages, destinations, and associated pricing |
| Support Staff | Assist in managing day-to-day bookings, customer queries, and operational coordination |
| Development Team | Responsible for designing, building, testing, and maintaining the platform |
| Project Supervisors / Clients | Oversee project progress, validate requirements, and ensure deliverables align with business objectives |

### 2.3 Target Users

| Target User | Description |
|---|---|
| University Students | Students traveling between cities such as Colombo and Jaffna for academic purposes require affordable, reliable, and easy-to-book transport options. |
| Business Travelers | Professionals and entrepreneurs who frequently travel for meetings, conferences, or business operations and require punctual, comfortable, and bookable transport services. |
| Regular Jaffna–Colombo Travelers | Individuals who frequently commute or travel along the Colombo–Jaffna route and need a convenient platform to reserve seats in advance and track schedules in real time. |
| Tourists & Travelers | Local and international visitors who wish to explore Sri Lankan destinations through customizable tour packages offered on the platform. |
| Airport Travelers | Passengers requiring reliable airport pickup and drop services coordinated through the platform. |

**Key characteristics shared across all target users:**

- Need for advanced seat reservations to avoid last-minute unavailability
- Preference for digital booking over manual or phone-based methods
- Requirement for real-time updates on schedules, availability, and booking confirmations
- Expectation of transparent pricing and flexible cancellation options

---

## Chapter 3: Functional Requirements

### 3.1 User & Access Management

| ID | Description | Priority | Source | Status |
|---|---|---|---|---|
| FR001 | The system shall support multiple user roles: Customer, Operator, Driver, Staff, and Admin, with access controlled using a role-permission matrix. | High | System | Proposed |
| FR002 | User accounts shall be created, updated, and deactivated by the Admin. | High | Admin | Proposed |
| FR003 | Role-based permissions shall be configurable and enforceable across all system modules. | High | Admin | Proposed |
| FR004 | Users shall be authenticated using a valid email and password. | High | System | Proposed |
| FR005 | Users shall be redirected to role-specific dashboards after successful authentication. | High | System | Proposed |
| FR006 | User accounts shall be locked after five consecutive failed login attempts. | High | System | Proposed |
| FR007 | Password reset shall be performed via a time-limited email link. | High | System | Proposed |
| FR008 | User sessions shall be terminated after 30 minutes of inactivity. | Medium | System | Proposed |

### 3.2 Customer Registration & Profile Management

| ID | Description | Priority | Source | Status |
|---|---|---|---|---|
| FR009 | Customers shall be able to register by providing their name, email, phone number, and password. | High | Customer | Proposed |
| FR010 | Customer profiles shall be updatable including contact details and preferences. | High | Customer | Proposed |
| FR011 | Customer booking history shall be viewable from the customer profile. | High | Customer | Proposed |

### 3.3 Bus Ticket Booking

| ID | Description | Priority | Source | Status |
|---|---|---|---|---|
| FR012 | Customers shall be able to search for available buses by selecting origin, destination, and travel date. | High | Customer | Proposed |
| FR013 | The system shall display available seats in real-time for each bus route. | High | System | Proposed |
| FR014 | Customers shall be able to select one or more seats and confirm a booking. | High | Customer | Proposed |
| FR015 | The system shall prevent double-booking of the same seat. | High | System | Proposed |
| FR016 | Booking confirmation shall be sent to the customer via email or SMS upon successful reservation. | High | System | Proposed |
| FR017 | Customers shall be able to cancel a bus booking within the permitted cancellation window. | High | Customer | Proposed |
| FR018 | Booking status shall be maintained as Confirmed, Cancelled, or Completed. | High | System | Proposed |
| FR019 | An incomplete bus booking shall be automatically cancelled by the system if payment or confirmation is not completed within 15 minutes of initiation. | High | System | Proposed |

### 3.4 Route & Schedule Management

| ID | Description | Priority | Source | Status |
|---|---|---|---|---|
| FR020 | Admin shall be able to create, update, and deactivate bus routes including origin, destination, and stops. | High | Admin | Proposed |
| FR021 | Admin shall be able to configure schedules including departure times, days of operation, and seat capacity. | High | Admin | Proposed |
| FR022 | The system shall automatically update seat availability when bookings are made or cancelled. | High | System | Proposed |
| FR023 | Admin shall be able to set and adjust ticket pricing per route. | High | Admin | Proposed |

### 3.5 Airport Transfer Booking

| ID | Description | Priority | Source | Status |
|---|---|---|---|---|
| FR024 | Customers shall be able to book airport pickup and drop-off services by specifying date, time, location, and flight details. | High | Customer | Proposed |
| FR025 | The system shall display available vehicles and estimated transfer pricing for airport transfers. | High | System | Proposed |
| FR026 | Airport transfer booking confirmation shall be sent to the customer upon successful reservation. | High | System | Proposed |
| FR027 | Customers shall be able to cancel an airport transfer booking. | High | Customer | Proposed |
| FR028 | Admin shall be able to assign a driver and vehicle to confirmed airport transfer bookings. | High | Admin | Proposed |

### 3.6 Tour Package Customization

| ID | Description | Priority | Source | Status |
|---|---|---|---|---|
| FR029 | Customers shall be able to create customized Sri Lankan tour packages by selecting from a list of available tourist destinations. | High | Customer | Proposed |
| FR030 | The system shall automatically calculate tour package pricing based on selected destinations, vehicle type, and duration. | High | System | Proposed |
| FR031 | Customers shall be able to save, review, and confirm their customized tour packages before booking. | High | Customer | Proposed |
| FR032 | Tour package booking confirmation shall be generated and sent to the customer upon successful reservation. | High | System | Proposed |
| FR033 | Admin shall be able to manage the list of tourist destinations and associated pricing. | High | Admin | Proposed |
| FR034 | Customers shall be able to view and cancel their tour package bookings. | High | Customer | Proposed |

### 3.7 Vehicle, Driver & Staff Management

| ID | Description | Priority | Source | Status |
|---|---|---|---|---|
| FR035 | Admin shall be able to add, update, and deactivate vehicles including type, capacity, and registration details. | High | Admin | Proposed |
| FR036 | Admin shall be able to manage driver profiles including personal details, license information, and status. | High | Admin | Proposed |
| FR037 | Admin shall be able to assign drivers to specific routes, airport transfers, or tour bookings. | High | Admin | Proposed |
| FR038 | Staff schedules shall be manageable by the Operator. | Medium | Admin | Proposed |
| FR039 | Vehicle availability shall be updated automatically when assigned to a booking. | High | System | Proposed |

### 3.8 Operator Branding & Pricing Control

| ID | Description | Priority | Source | Status |
|---|---|---|---|---|
| FR040 | Admin shall be able to configure their brand identity including logo, company name, and contact details on the platform. | Medium | Admin | Proposed |
| FR041 | Admin shall be able to set and update pricing for bus routes, airport transfers, and tour packages independently. | High | Admin | Proposed |
| FR042 | Admin-specific pricing and branding shall be visible to customers during the booking process. | High | System | Proposed |

### 3.9 Booking Management & Notifications

| ID | Description | Priority | Source | Status |
|---|---|---|---|---|
| FR043 | Customers shall be able to view all their current and past bookings from their dashboard. | High | Customer | Proposed |
| FR044 | The system shall send real-time booking confirmation and cancellation notifications to customers via email or SMS. | High | System | Proposed |
| FR045 | Admin shall receive notifications when a new booking is made or cancelled. | High | System | Proposed |
| FR046 | Booking details shall include service type, date, time, passenger details, and payment status. | High | System | Proposed |

### 3.10 Reporting & Analytics

| ID | Description | Priority | Source | Status |
|---|---|---|---|---|
| FR047 | Admin shall be able to generate reports on bookings, revenue, and vehicle utilization. | High | Admin | Proposed |
| FR048 | The system shall provide an analytics dashboard showing booking trends, popular routes, and revenue summaries. | Medium | Admin | Proposed |
| FR049 | System-wide reports and audit logs shall be accessible to the Admin. | High | Admin | Proposed |

---

## Chapter 4: Non-Functional Requirements

### 4.1 Performance

| ID | Requirement | Measurable Acceptance Criterion | Priority | Source | Status |
|---|---|---|---|---|---|
| NFRP01 | Homepage and search results performance | Homepage and search results load within 2 seconds on a standard 4G/broadband connection. | High | Client (A9 Express) | Proposed |
| NFRP02 | Seat selection and booking confirmation speed | Pages respond within 3 seconds when 500 concurrent users are active. | High | Patient | Proposed |
| NFRP03 | High concurrency support | System sustains 500 concurrent users with no more than 5% error rate during load tests. | High | Admin | Proposed |
| NFRP04 | Airport hire and tour search speed | Search results returned within 3 seconds for any query. | Medium | System Design Team | Proposed |
| NFRP05 | Payment processing performance | Transactions complete within 5 seconds under normal load; users notified of failure within 10 seconds. | High | Dev Team | Proposed |
| NFRP06 | Mobile app data efficiency | Active use consumes no more than 50 MB of mobile data per hour. | Medium | Mobile UX Best Practices | Proposed |
| NFRP07 | Dashboard and analytics performance | Dashboard loads within 4 seconds for datasets up to 10,000 booking records. | Medium | Admin | Proposed |

### 4.2 Reliability

| ID | Requirement | Measurable Acceptance Criterion | Priority | Source | Status |
|---|---|---|---|---|---|
| NFRR01 | System availability | Measured uptime >= 99.5% per calendar month, verified via uptime monitoring tools. | High | Client (A9 Express) | Proposed |
| NFRR02 | Server failure handling | Automated failover activates within 60 seconds of any single node failure with no data loss. | High | Cloud Infrastructure (AWS) | Proposed |
| NFRR03 | Backup management | Automated daily backups completed successfully; backups retained for 30 days and restorable within 2 hours. | High | System Design Team | Proposed |
| NFRR04 | Disaster recovery | RTO <= 2 hours; RPO <= 1 hour of data loss for any unplanned outage. | High | System Design Team | Proposed |
| NFRR05 | Failed payment recovery | 100% of failed payments are rolled back and users notified within 30 seconds. | High | Stripe/PayPal Integration Spec | Proposed |
| NFRR06 | Error monitoring and alerts | Critical errors trigger automated alerts to the dev team within 2 minutes via monitoring service. | Medium | System Design Team | Proposed |
| NFRR07 | Maintenance scheduling | All scheduled maintenance occurs between 12 AM – 4 AM with 24-hour advance notification to users. | Medium | Operational Policy | Proposed |

### 4.3 Usability

| ID | Requirement | Measurable Acceptance Criterion | Priority | Source | Status |
|---|---|---|---|---|---|
| NFRU01 | Easy booking for new users | First-time users complete booking in under 5 minutes in usability testing with no assistance. | High | User Survey (118 responses) | Proposed |
| NFRU02 | Multi-language support | Sinhala, Tamil, and English are fully supported; language switchable from any screen. | High | Client (A9 Express) / Target Market | Proposed |
| NFRU03 | Accessibility support | Passes WCAG 2.1 Level AA automated and manual audit with zero critical violations. | Medium | System Design Team | Proposed |
| NFRU04 | Timely user notifications | SMS and in-app notifications delivered within 60 seconds of booking confirmation, cancellation, or schedule change. | High | Client Requirement | Proposed |
| NFRU05 | Easy operator management | Operators complete fleet, route, schedule, and pricing setup within 10 minutes during onboarding testing. | High | Client (A9 Express) | Proposed |
| NFRU06 | Clear error messages | All error messages pass user comprehension testing: >= 90% of test users understand the error and next step. | Medium | System Design Team | Proposed |
| NFRU07 | Hybrid booking support | Phone-assisted booking option available; confirmed bookings processed within the same system in under 5 minutes. | Medium | Target Market Analysis | Proposed |

### 4.4 Security

| ID | Requirement | Measurable Acceptance Criterion | Priority | Source | Status |
|---|---|---|---|---|---|
| NFRS01 | Secure data transmission | All endpoints use HTTPS/TLS 1.2+; HTTP requests are redirected to HTTPS. Verified via SSL Labs scan score >= A. | High | System Design Team / OWASP | Proposed |
| NFRS02 | Secure authentication | Clerk-managed authentication with OTP/MFA enabled; zero authentication bypass incidents in penetration testing. | High | Technology Stack (Clerk) | Proposed |
| NFRS03 | Secure payment processing | PCI-DSS compliant payment flow via Stripe/PayPal; no raw card data stored on platform servers — confirmed by security audit. | High | Stripe/PayPal Integration Spec | Proposed |
| NFRS04 | Role-based access control | RBAC enforced: passengers, operators, agents, and admins cannot access unauthorised resources — validated by role-based test suite. | High | System Design Team | Proposed |
| NFRS05 | Fraud detection | Fraud detection flags >= 95% of simulated fraudulent transactions in testing; blocked accounts notified within 30 seconds. | High | Risk Analysis | Proposed |
| NFRS06 | Secure password storage | All passwords hashed with bcrypt (cost factor >= 12); verified by code review — plaintext passwords absent from all storage layers. | High | Security Best Practices | Proposed |
| NFRS07 | Agent verification | 100% of agent accounts require document upload and admin approval; unverified agents cannot process bookings. | High | Client Requirement / Risk Analysis | Proposed |
| NFRS08 | Session timeout | Sessions automatically expire after 30 minutes of inactivity on all platforms; user prompted to re-authenticate. | Medium | System Design Team | Proposed |

### 4.5 Scalability

| ID | Requirement | Measurable Acceptance Criterion | Priority | Source | Status |
|---|---|---|---|---|---|
| NFRSC01 | Independent service scaling | Each service (booking, payment, notifications) scales independently; verified by load test showing no cascading failures. | High | System Design Team | Proposed |
| NFRSC02 | Automatic scaling during traffic spikes | AWS Auto Scaling provisions additional capacity within 3 minutes of CPU/load threshold breach with no downtime. | High | Cloud Infrastructure (AWS) | Proposed |
| NFRSC03 | Large database handling | Query response time remains under 2 seconds with 1 million booking records in the database. | High | System Design Team | Proposed |
| NFRSC04 | Easy onboarding of new operators | A new transport operator or service type can be onboarded within 2 developer-days without core architecture changes. | Medium | Client (A9 Express) Growth Plan | Proposed |
| NFRSC05 | Data caching efficiency | Cache hit rate >= 70% for routes, schedules, and seat availability queries — measured via Redis monitoring. | Medium | System Design Team | Proposed |
| NFRSC06 | High API request handling | API sustains >= 1,000 requests/minute per operator with < 1% error rate under load testing. | Medium | System Design Team | Proposed |

### 4.6 Maintainability

| ID | Requirement | Measurable Acceptance Criterion | Priority | Source | Status |
|---|---|---|---|---|---|
| NFRM01 | Consistent and documented codebase | ESLint/Prettier pass with zero errors on CI; >= 80% of functions have inline documentation comments. | High | System Design Team | Proposed |
| NFRM02 | Automated testing and deployment | CI/CD pipeline (GitHub Actions) executes all tests and deploys to staging on every pull request merge with zero manual steps. | High | Technology Stack (GitHub) | Proposed |
| NFRM03 | Automated test coverage | Unit and integration test coverage >= 70% across booking, payment, and authentication modules — measured by Jest coverage report. | Medium | System Design Team | Proposed |
| NFRM04 | API documentation | OpenAPI/Swagger documentation published and up to date; new developers complete onboarding within 5 working days. | Medium | System Design Team | Proposed |
| NFRM05 | Logging and audit support | Structured JSON logs retained for >= 90 days; log search returns results for any event within 10 seconds. | Medium | Operational Policy | Proposed |
| NFRM06 | Dependency maintenance | Dependency audit run quarterly; critical/high severity vulnerabilities patched within 14 days of disclosure. | Low | System Design Team | Proposed |

### 4.7 Portability

| ID | Requirement | Measurable Acceptance Criterion | Priority | Source | Status |
|---|---|---|---|---|---|
| NFRPO01 | Cross-browser compatibility | Fully functional on Chrome, Firefox, Safari, and Edge (latest 2 versions); zero critical browser-specific bugs in QA. | High | System Design Team | Proposed |
| NFRPO02 | Cross-platform mobile support | Single React Native codebase deployed to Android (v8.0+) and iOS (v13+); all core features functional on both platforms. | High | Technology Stack | Proposed |
| NFRPO03 | Responsive web design | Layout renders correctly and all features are usable at screen widths from 360px to 1920px — verified by device emulation testing. | High | System Design Team / Target Market | Proposed |
| NFRPO04 | Cloud deployment portability | Services containerised with Docker; deployment to a different cloud provider (e.g., GCP) achievable within 1 working day. | Medium | System Design Team | Proposed |
| NFRPO05 | Database migration support | Schema documented and migration scripts prepared; estimated migration effort to PostgreSQL <= 2 weeks. | Low | System Design Team | Proposed |
| NFRPO06 | External configuration management | All secrets and environment variables stored in .env files / secret manager; zero hardcoded credentials in the codebase confirmed by code scan. | Medium | DevOps Best Practices | Proposed |

---

## Chapter 5: Business Rules, Constraints and Assumptions

### 5.1 Business Rules

| ID | Rule Description |
|---|---|
| BR001 | User passwords shall comply with defined security and complexity requirements, and passwords shall be stored using secure hashing mechanisms. |
| BR002 | Each customer shall be assigned a unique customer identifier within the system. |
| BR003 | User accounts shall be temporarily locked after five consecutive failed login attempts. |
| BR004 | Customers shall be permitted to book buses, airport transfers, and tour packages only after successful authentication. |
| BR005 | Operators shall be permitted to manage routes, schedules, and pricing but shall not be permitted to modify system-level settings. |
| BR006 | Drivers shall only be permitted to access assigned trips and schedules. |
| BR007 | Administrative users shall be responsible for managing users, bookings, routes, pricing, and system reports. |
| BR008 | Password reset operations shall be performed through a secure email verification process. |
| BR009 | A customer shall not be allowed to reserve a seat that has already been booked by another customer. |
| BR010 | Incomplete bookings shall be automatically cancelled if payment or confirmation is not completed within 15 minutes. |
| BR011 | Customers shall be allowed to cancel bookings only within the permitted cancellation period defined by the company. |
| BR012 | Real-time booking confirmation notifications shall be sent to customers through email or SMS after successful booking completion. |
| BR013 | Ticket pricing for bus routes, airport transfers, and tour packages shall be configurable by the Admin. |
| BR014 | Tour package pricing shall be automatically calculated based on selected destinations, vehicle type, and duration. |
| BR015 | All user activities related to bookings and administrative actions shall be recorded in the system audit logs. |

### 5.2 Technology Constraints

| ID | Constraint |
|---|---|
| CON001 | The system shall be implemented as a web-based application accessible through modern web browsers such as Chrome, Edge, Firefox, and Safari. |
| CON002 | The system frontend shall be developed using React.js and the backend shall be developed using Node.js. |
| CON003 | The system database shall be implemented using MySQL. |
| CON004 | The system shall support responsive user interfaces for desktop and mobile devices. |
| CON005 | Internet connectivity shall be required for accessing online booking services and notifications. |

### 5.3 Legal Constraints

| ID | Constraint |
|---|---|
| CON006 | Customer personal information shall be handled according to applicable data privacy and protection regulations. |
| CON007 | Access to booking and customer information shall be restricted to authorized users only. |
| CON008 | Payment and transaction data shall be securely stored and protected from unauthorized access. |
| CON009 | Customer booking records shall be retained according to company and legal retention policies. |

### 5.4 Operational Constraints

| ID | Constraint |
|---|---|
| CON010 | The system shall support multiple transport services including bus booking, airport transfers, and tour package management. |
| CON011 | The system shall maintain operational continuity under moderate internet connectivity conditions. |
| CON012 | Real-time seat availability updates shall be supported during high booking activity periods. |
| CON013 | Booking and payment confirmation notifications shall depend on third-party email or SMS gateway availability. |

### 5.5 Assumptions

| ID | Assumption Description |
|---|---|
| ASM001 | Customers and staff are assumed to possess basic computer and smartphone literacy to operate the system effectively. |
| ASM002 | Reliable internet connectivity is assumed to be available for accessing the online booking platform. |
| ASM003 | Transport operators are assumed to provide accurate route, schedule, and pricing information to the system. |
| ASM004 | Administrators are assumed to regularly maintain and update booking schedules, vehicles, and driver details. |
| ASM005 | Secure hosting infrastructure and regular database backups are assumed to be available for the system. |
| ASM006 | Email and SMS notification services are assumed to be operational and accessible when sending booking confirmations and alerts. |
| ASM007 | Customers are assumed to provide valid personal and payment information during registration and booking processes. |

---

## Chapter 6: Use Case Diagrams

> **Note:** Use case diagram images should be placed in a `/diagrams` folder and referenced below.

### 6.1 Customer Booking Flow

![Customer Booking Flow](diagrams/uc_customer_booking_flow.png)

### 6.2 Authentication and Account Access

![Authentication and Account Access](diagrams/uc_authentication.png)

### 6.3 Admin Route & Vehicle Management

![Admin Route & Vehicle Management](diagrams/uc_admin_route_vehicle.png)

### 6.4 Notification and System Events

![Notification and System Events](diagrams/uc_notifications.png)

### 6.5 Admin Reporting and Analytics

![Admin Reporting and Analytics](diagrams/uc_admin_reporting.png)

---

## Chapter 7: Use Case Descriptions

### 7.1 Customer Booking Flow

#### UC-001: Search Available Buses

| Field | Details |
|---|---|
| **Use Case ID** | UC-001 |
| **Use Case Name** | Search Available Buses |
| **Actor(s)** | Customer |
| **Description** | Customer searches for available buses by selecting origin, destination, and travel date. |
| **Preconditions** | Customer is logged in. Bus routes and schedules have been configured by Admin. |
| **Postconditions – Success** | Customer views available buses and proceeds to booking. |

**Main Flow:**
1. Customer navigates to the bus search section.
2. Customer selects origin, destination, and travel date.
3. System queries available buses.
4. System displays list of available buses with seat availability.
5. Customer selects a preferred bus.

---

#### UC-002: Book Bus Ticket

| Field | Details |
|---|---|
| **Use Case ID** | UC-002 |
| **Use Case Name** | Book Bus Ticket |
| **Actor(s)** | Customer, System |
| **Description** | Customer selects and confirms a seat reservation on an available bus route. |
| **Preconditions** | Customer is logged in. Customer has searched and selected an available bus. Seats are available. |
| **Postconditions – Success** | Seat(s) reserved. Booking confirmation sent. Seat availability updated. |
| **Postconditions – Failure** | Booking not confirmed. Seat reservation released after timeout. |

**Main Flow:**
1. Customer selects one or more available seats.
2. System temporarily reserves seat(s) for 15 minutes.
3. Customer reviews and confirms booking.
4. System processes and confirms the booking.
5. Confirmation sent via email or SMS.

**Alternative Flow 1:** At step 1: If no seats are available, system displays a 'Sold Out' message and suggests alternative times or routes.

**Alternative Flow 2:** At step 3: If customer does not confirm within 15 minutes, system releases the temporary reservation.

**Business Rules:** BR-01: Seat reservations expire after 15 minutes. BR-02: Booking confirmation must be sent within 2 minutes of confirmation.

---

#### UC-003: Book Airport Transfer

| Field | Details |
|---|---|
| **Use Case ID** | UC-003 |
| **Use Case Name** | Book Airport Transfer |
| **Actor(s)** | Customer, Admin |
| **Description** | Customer books an airport pickup or drop-off by providing travel details. |
| **Preconditions** | Customer is logged in. Airport transfer services are available. |
| **Postconditions – Success** | Transfer booked and confirmed. Customer receives notification. |

**Main Flow:**
1. Customer navigates to airport transfer section.
2. Customer provides date, time, location, and flight details.
3. System displays available vehicles and estimated pricing.
4. Customer selects vehicle and confirms booking.
5. System generates confirmation and notifies customer.

---

#### UC-004: Customise Tour Package

| Field | Details |
|---|---|
| **Use Case ID** | UC-004 |
| **Use Case Name** | Customise Tour Package |
| **Actor(s)** | Customer, System |
| **Description** | Customer creates a personalised Sri Lankan tour package by selecting tourist destinations. |
| **Preconditions** | Customer is logged in. Tourist destinations and pricing configured by Admin. |
| **Postconditions – Success** | Tour package created and confirmed. Booking visible in customer history. |

**Main Flow:**
1. Customer navigates to tour package section.
2. Customer selects destinations from available list.
3. Customer selects vehicle type and specifies duration.
4. System calculates total package price.
5. Customer reviews, saves, and submits the tour booking.
6. System generates confirmation and notifies customer.

---

#### UC-005: Cancel Booking

| Field | Details |
|---|---|
| **Use Case ID** | UC-005 |
| **Use Case Name** | Cancel Booking |
| **Actor(s)** | Customer, System |
| **Description** | Customer cancels an existing bus, airport transfer, or tour booking within the permitted cancellation window. |
| **Preconditions** | Customer is logged in. Customer has an active confirmed booking. Cancellation is within the permitted time window. |
| **Postconditions – Success** | Booking status updated to Cancelled. Notifications sent. Availability restored. |
| **Postconditions – Failure** | Cancellation not permitted. Customer notified of cancellation window violation. |

**Main Flow:**
1. Customer navigates to booking history.
2. Customer selects the booking to cancel.
3. System validates cancellation is within permitted window.
4. Customer confirms cancellation.
5. System updates booking status to Cancelled.
6. System sends cancellation confirmation to customer and Admin.
7. System restores seat or vehicle availability.

**Alternative Flow 1:** At step 3: If cancellation window has expired, system displays an error message and denies the cancellation request.

**Business Rules:** BR-03: Cancellations must be requested at least 2 hours before scheduled departure.

---

### 7.2 Authentication & Account Access

#### UC-006: Register / Login

| Field | Details |
|---|---|
| **Use Case ID** | UC-006 |
| **Use Case Name** | Register / Login |
| **Actor(s)** | Customer |
| **Description** | A new customer registers an account or an existing customer authenticates to access the platform. |
| **Preconditions** | User has access to the A9 Express platform. User has a valid email address. |
| **Postconditions – Success** | Customer account created or authenticated. Session initiated. Customer redirected to dashboard. |
| **Postconditions – Failure** | Account not created or login denied. Error message displayed. |

**Main Flow:**
1. New customer navigates to registration page and provides name, email, phone, and password.
2. System validates details and creates the account.
3. Existing customer enters valid email and password.
4. System authenticates the user.
5. System initiates session and redirects to dashboard.

**Alternative Flow 1:** At step 1 (Registration): If email is already registered, system notifies user and prompts login instead.

**Alternative Flow 2:** At step 3 (Login): If credentials are invalid after 3 attempts, account is temporarily locked for 15 minutes.

**Business Rules:** BR-06: Passwords must be at least 8 characters with one uppercase letter and one number. BR-07: Account lockout after 3 failed login attempts.

---

#### UC-007: Validate Credentials

| Field | Details |
|---|---|
| **Use Case ID** | UC-007 |
| **Use Case Name** | Validate Credentials |
| **Actor(s)** | System |
| **Description** | System validates the email and password provided by the customer during login. |
| **Preconditions** | Customer has submitted login credentials. |
| **Postconditions – Success** | Credentials validated; authentication proceeds. |
| **Postconditions – Failure** | Invalid credentials; error message returned to customer. |

**Main Flow:**
1. System receives email and password input.
2. System checks credentials against stored records.
3. If valid, authentication proceeds.
4. If invalid, system returns an error message.

---

#### UC-008: Initiate Session

| Field | Details |
|---|---|
| **Use Case ID** | UC-008 |
| **Use Case Name** | Initiate Session |
| **Actor(s)** | System |
| **Description** | System creates an authenticated session for the customer after successful login. |
| **Preconditions** | Credentials have been successfully validated. |
| **Postconditions – Success** | Active session created. Customer has access to the platform. |

**Main Flow:**
1. System generates a session token for the authenticated user.
2. Session is stored and associated with the customer account.
3. Customer is granted access to protected platform features.

---

#### UC-009: View Booking History

| Field | Details |
|---|---|
| **Use Case ID** | UC-009 |
| **Use Case Name** | View Booking History |
| **Actor(s)** | Customer |
| **Description** | Customer views all current and past bookings from their dashboard after login. |
| **Preconditions** | Customer is logged in. |
| **Postconditions – Success** | Customer views complete booking history. Booking details displayed accurately. |

**Main Flow:**
1. Customer navigates to booking history section on dashboard.
2. System retrieves all current and past bookings.
3. Customer views booking details including service type, date, time, and payment status.
4. Customer selects a specific booking to view full details.

---

### 7.3 Admin Route & Vehicle Management

#### UC-010: Manage Routes & Schedules

| Field | Details |
|---|---|
| **Use Case ID** | UC-010 |
| **Use Case Name** | Manage Routes & Schedules |
| **Actor(s)** | Admin |
| **Description** | Admin creates, updates, and deactivates bus routes and configures schedules. |
| **Preconditions** | Admin is logged in with appropriate permissions. |
| **Postconditions – Success** | New route and schedule are active and bookable. Seat availability initialised. |

**Main Flow:**
1. Admin navigates to route management section.
2. Admin creates a new route by defining origin, destination, and stops.
3. Admin configures schedules including departure times and days of operation.
4. Admin sets ticket pricing per route.
5. System saves and makes the route available for customer booking.

---

#### UC-011: Manage Vehicles & Drivers

| Field | Details |
|---|---|
| **Use Case ID** | UC-011 |
| **Use Case Name** | Manage Vehicles & Drivers |
| **Actor(s)** | Admin |
| **Description** | Admin manages the fleet of vehicles and driver profiles on the platform. |
| **Preconditions** | Admin is logged in with appropriate permissions. |
| **Postconditions – Success** | Vehicle and driver profiles saved and available for assignment. |

**Main Flow:**
1. Admin navigates to vehicle management section.
2. Admin adds a new vehicle with type, capacity, and registration details.
3. Admin navigates to driver management section.
4. Admin creates or updates a driver profile with personal details and licence information.
5. Admin sets driver status as active or inactive.
6. System saves vehicle and driver information.

---

#### UC-012: Assign Driver to Booking

| Field | Details |
|---|---|
| **Use Case ID** | UC-012 |
| **Use Case Name** | Assign Driver to Booking |
| **Actor(s)** | Admin, Driver |
| **Description** | Admin assigns a driver and vehicle to a confirmed airport transfer or tour booking. |
| **Preconditions** | Admin is logged in. A confirmed booking exists requiring a driver. An available driver and vehicle exist. |
| **Postconditions – Success** | Driver and vehicle assigned to booking. Vehicle availability updated. Driver notified. |

**Main Flow:**
1. Admin views confirmed bookings requiring driver assignment.
2. Admin selects a booking to assign.
3. Admin selects an available driver and vehicle.
4. System assigns driver and vehicle to the booking.
5. System updates vehicle availability.
6. Driver is notified of the assignment.

---

### 7.4 Notification & System Events

#### UC-013: Send Booking Notifications

| Field | Details |
|---|---|
| **Use Case ID** | UC-013 |
| **Use Case Name** | Send Booking Notifications |
| **Actor(s)** | System |
| **Description** | System automatically sends real-time notifications to customers and Admin on booking events. |
| **Preconditions** | A booking, cancellation, or assignment event has occurred. Customer contact details are available. |
| **Postconditions – Success** | Customer receives booking or cancellation confirmation. Admin notified of relevant events. |

**Main Flow:**
1. System detects a booking confirmation, cancellation, or driver assignment event.
2. System retrieves customer contact details.
3. System generates the appropriate notification message.
4. System dispatches notification via email or SMS.
5. System notifies Admin of relevant booking events.

---

#### UC-014: Booking Confirmation Event

| Field | Details |
|---|---|
| **Use Case ID** | UC-014 |
| **Use Case Name** | Booking Confirmation Event |
| **Actor(s)** | System |
| **Description** | System triggers a notification when a new booking is successfully confirmed. |
| **Preconditions** | A booking has been successfully created and confirmed. |
| **Postconditions – Success** | Customer notified of confirmed booking. |

**Main Flow:**
1. System detects booking status set to Confirmed.
2. System triggers Send Booking Notifications use case.
3. Customer receives booking confirmation with details.

---

#### UC-015: Cancellation Event

| Field | Details |
|---|---|
| **Use Case ID** | UC-015 |
| **Use Case Name** | Cancellation Event |
| **Actor(s)** | System |
| **Description** | System triggers a notification when a booking is cancelled by the customer. |
| **Preconditions** | A booking has been successfully cancelled. |
| **Postconditions – Success** | Customer and Admin notified of cancellation. |

**Main Flow:**
1. System detects booking status updated to Cancelled.
2. System triggers Send Booking Notifications use case.
3. Customer and Admin receive cancellation confirmation.

---

#### UC-016: Driver Assignment Event

| Field | Details |
|---|---|
| **Use Case ID** | UC-016 |
| **Use Case Name** | Driver Assignment Event |
| **Actor(s)** | System |
| **Description** | System triggers a notification when a driver is assigned to a confirmed booking. |
| **Preconditions** | A driver has been successfully assigned to a booking by Admin. |
| **Postconditions – Success** | Driver notified of booking assignment. |

**Main Flow:**
1. System detects driver assignment to a confirmed booking.
2. System triggers Send Booking Notifications use case.
3. Driver receives assignment notification with booking details.

---

### 7.5 Admin Reporting & Analytics

#### UC-017: Generate Reports

| Field | Details |
|---|---|
| **Use Case ID** | UC-017 |
| **Use Case Name** | Generate Reports |
| **Actor(s)** | Admin |
| **Description** | Admin generates operational reports and views analytics on bookings and revenue. |
| **Preconditions** | Admin is logged in. Booking and operational data exists in the system. |
| **Postconditions – Success** | Report generated and displayed to Admin. |

**Main Flow:**
1. Admin navigates to reporting and analytics section.
2. Admin selects report type (bookings, revenue, vehicle utilisation).
3. Admin specifies date range and filters.
4. System generates and displays the report.
5. Admin views analytics dashboard with booking trends and revenue summaries.

---

#### UC-018: Access Audit Logs

| Field | Details |
|---|---|
| **Use Case ID** | UC-018 |
| **Use Case Name** | Access Audit Logs |
| **Actor(s)** | Admin |
| **Description** | Admin optionally accesses detailed audit logs for deeper review of system activity. |
| **Preconditions** | Admin has generated a report. Admin requires detailed activity tracking. |
| **Postconditions – Success** | Audit logs displayed and accessible for review. |

**Main Flow:**
1. Admin selects the audit log option from the reporting section.
2. System retrieves audit log entries.
3. Admin applies filter by vehicle or route.
4. System displays filtered audit log results.

---

#### UC-019: Export Report

| Field | Details |
|---|---|
| **Use Case ID** | UC-019 |
| **Use Case Name** | Export Report |
| **Actor(s)** | Admin |
| **Description** | Admin optionally exports a generated report for external use or record keeping. |
| **Preconditions** | Admin has generated a report. |
| **Postconditions – Success** | Report exported and downloaded by Admin. |

**Main Flow:**
1. Admin selects the export option after viewing a report.
2. Admin chooses the preferred export format.
3. System generates the export file.
4. Admin downloads the file.

---

## Chapter 8: Activity & Sequence Diagrams

> **Note:** Diagram images should be placed in a `/diagrams` folder and referenced below.

### 8.1 Activity Diagrams

#### 8.1.1 Activity Diagram – Book Bus Ticket

![Activity Diagram – Book Bus Ticket](diagrams/activity_book_bus_ticket.png)

#### 8.1.2 Activity Diagram – Airport Transfer Booking

![Activity Diagram – Airport Transfer Booking](diagrams/activity_airport_transfer.png)

#### 8.1.3 Activity Diagram – Customize & Book Tour Package

![Activity Diagram – Customize & Book Tour Package](diagrams/activity_tour_package.png)

#### 8.1.4 Activity Diagram – Manage Fleet, Routes & Pricing

![Activity Diagram – Manage Fleet, Routes & Pricing](diagrams/activity_manage_fleet.png)

#### 8.1.5 Activity Diagram – Online Payment Processing

![Activity Diagram – Online Payment Processing](diagrams/activity_payment_processing.png)

### 8.2 Sequence Diagrams

#### 8.2.1 Customer Booking Flow

![Sequence Diagram – Customer Booking Flow](diagrams/seq_customer_booking.png)

#### 8.2.2 Authentication & Account Access

![Sequence Diagram – Authentication & Account Access](diagrams/seq_authentication.png)

#### 8.2.3 Admin Route & Vehicle Management

![Sequence Diagram – Admin Route & Vehicle Management](diagrams/seq_admin_route_vehicle.png)

#### 8.2.4 Notification & System Events

![Sequence Diagram – Notification & System Events](diagrams/seq_notifications.png)

#### 8.2.5 Cancel Booking

![Sequence Diagram – Cancel Booking](diagrams/seq_cancel_booking.png)

#### 8.2.6 Admin Reporting & Analytics

![Sequence Diagram – Admin Reporting & Analytics](diagrams/seq_admin_reporting.png)

---

## Chapter 9: External Interface Requirements

### 9.1 User Interface Requirements

The A9 Express – Transport Booking Platform shall provide a responsive, user-friendly, and accessible interface for customers, transport operators, drivers, and administrators.

**The interface shall:**
- Be accessible through desktop and mobile devices
- Provide responsive layouts for different screen sizes
- Display real-time booking availability and updates
- Support simple navigation and efficient booking workflows
- Provide dashboards for customers, operators, and administrators

**Customer Interface Requirements** — Customers shall be able to:
- Register and log into the platform
- Search available transport services
- Book private bus tickets
- Reserve airport transfer services
- Create customized Sri Lankan tour packages
- Select tourist destinations and transportation options
- View booking confirmations and booking history
- Cancel or modify bookings based on service policies
- Receive notifications and travel updates

**Operator and Administrator Interface Requirements** — Operators and administrators shall be able to:
- Manage buses, routes, and schedules
- Configure pricing and availability
- Manage drivers and vehicles
- Monitor bookings and cancellations
- Access customer and operational reports
- Manage notifications and system settings
- View analytics dashboards

### 9.2 Hardware Interface Requirements

| Hardware Component | Purpose |
|---|---|
| Smartphones | Customer, driver, and operator access |
| Desktop / Laptop Computers | Administrative and operational management |
| GPS-enabled Devices | Real-time location and route tracking |
| Cloud Servers | Application hosting and data storage |
| Internet Routers / Network Devices | Communication and network connectivity |

### 9.3 Software Interface Requirements

| Software Interface | Purpose |
|---|---|
| Payment Gateway API | Online payment processing |
| Google Maps API | Route calculation and location services |
| SMS Gateway | Sending booking and notification messages |
| Email Service | Sending booking confirmations and alerts |
| Database Management System | Data storage and retrieval |
| Authentication Service | User login and access management |

**Proposed Technology Stack:**

| Component | Technology |
|---|---|
| Frontend | HTML, CSS, JavaScript, React |
| Backend | Node.js / Express |
| Database | MySQL / PostgreSQL |
| Mobile Application | React Native |

### 9.4 Communication Interface Requirements

- HTTPS shall be used for secure web communication.
- SSL/TLS encryption shall be implemented for secure data transmission.
- REST APIs shall be used for communication between frontend and backend components.
- SMS and email services shall support customer notifications and confirmations.
- Real-time booking and availability updates shall be supported through internet-based communication.
- Minimum 4G mobile data or broadband internet connectivity shall be required.
- Communication with third-party APIs shall use secure authenticated connections.

---

## Chapter 10: Data Requirements

### 10.1 Data Entities and Attributes

#### 10.1.1 Customer

| Field | Data Type | Constraints | Description |
|---|---|---|---|
| customer_id | VARCHAR(10) | PRIMARY KEY, UNIQUE, NOT NULL | Unique customer identifier |
| first_name | VARCHAR(100) | NOT NULL | Customer first name |
| last_name | VARCHAR(100) | NOT NULL | Customer last name |
| email | VARCHAR(150) | UNIQUE, NOT NULL | Customer email address |
| phone_number | VARCHAR(15) | NOT NULL | Contact number |
| password_hash | VARCHAR(255) | NOT NULL | Encrypted password |
| address | TEXT | NULLABLE | Residential address |
| registered_date | DATETIME | DEFAULT NOW() | Registration date |
| account_status | ENUM('Active','Inactive','Blocked') | DEFAULT 'Active' | Customer account status |

#### 10.1.2 User (System Users)

| Field | Data Type | Constraints | Description |
|---|---|---|---|
| user_id | INT | PRIMARY KEY, AUTO_INCREMENT | Unique user ID |
| username | VARCHAR(50) | UNIQUE, NOT NULL | Login username |
| password_hash | VARCHAR(255) | NOT NULL | Encrypted password |
| role | ENUM('Admin','Operator','Driver','Staff') | NOT NULL | User role |
| email | VARCHAR(150) | UNIQUE, NOT NULL | User email |
| is_active | BOOLEAN | DEFAULT TRUE | Account status |
| failed_attempts | INT | DEFAULT 0 | Failed login attempts |
| locked_until | DATETIME | NULLABLE | Account lock expiry |
| last_login | DATETIME | NULLABLE | Last login timestamp |

#### 10.1.3 Bus Route

| Field | Data Type | Constraints | Description |
|---|---|---|---|
| route_id | INT | PRIMARY KEY, AUTO_INCREMENT | Unique route ID |
| origin | VARCHAR(100) | NOT NULL | Starting location |
| destination | VARCHAR(100) | NOT NULL | Destination location |
| stops | TEXT | NULLABLE | Intermediate stops |
| distance_km | DECIMAL(6,2) | NULLABLE | Route distance |
| status | ENUM('Active','Inactive') | DEFAULT 'Active' | Route availability |

#### 10.1.4 Schedule

| Field | Data Type | Constraints | Description |
|---|---|---|---|
| schedule_id | INT | PRIMARY KEY, AUTO_INCREMENT | Unique schedule ID |
| route_id | INT | FOREIGN KEY → Bus Route | Assigned route |
| departure_time | DATETIME | NOT NULL | Departure date and time |
| arrival_time | DATETIME | NOT NULL | Expected arrival time |
| seat_capacity | INT | NOT NULL | Total seat capacity |

#### 10.1.5 Booking

| Field | Data Type | Constraints | Description |
|---|---|---|---|
| booking_id | INT | PRIMARY KEY, AUTO_INCREMENT | Unique booking ID |
| customer_id | VARCHAR(10) | FOREIGN KEY → Customer | Customer making booking |
| schedule_id | INT | FOREIGN KEY → Schedule | Selected trip |
| booking_date | DATETIME | DEFAULT NOW() | Booking timestamp |
| total_amount | DECIMAL(10,2) | NOT NULL | Total booking amount |
| booking_status | ENUM('Confirmed','Cancelled','Pending','Completed') | DEFAULT 'Pending' | Booking status |
| payment_status | ENUM('Paid','Unpaid','Refunded') | DEFAULT 'Unpaid' | Payment status |

#### 10.1.6 Seat

| Field | Data Type | Constraints | Description |
|---|---|---|---|
| seat_id | INT | PRIMARY KEY, AUTO_INCREMENT | Unique seat ID |
| schedule_id | INT | FOREIGN KEY → Schedule | Related schedule |
| seat_number | VARCHAR(10) | NOT NULL | Seat number |
| booking_id | INT | FOREIGN KEY → Booking, NULLABLE | Assigned booking |
| seat_status | ENUM('Available','Reserved','Booked') | DEFAULT 'Available' | Seat availability |

#### 10.1.7 Vehicle

| Field | Data Type | Constraints | Description |
|---|---|---|---|
| vehicle_id | INT | PRIMARY KEY, AUTO_INCREMENT | Unique vehicle ID |
| registration_number | VARCHAR(20) | UNIQUE, NOT NULL | Vehicle registration number |
| vehicle_type | VARCHAR(50) | NOT NULL | Bus/Van/Car type |
| capacity | INT | NOT NULL | Passenger capacity |
| status | ENUM('Available','Maintenance','Assigned') | DEFAULT 'Available' | Vehicle status |

#### 10.1.8 Driver

| Field | Data Type | Constraints | Description |
|---|---|---|---|
| driver_id | INT | PRIMARY KEY, AUTO_INCREMENT | Unique driver ID |
| first_name | VARCHAR(100) | NOT NULL | Driver first name |
| last_name | VARCHAR(100) | NOT NULL | Driver last name |
| license_number | VARCHAR(50) | UNIQUE, NOT NULL | Driving license number |
| contact_number | VARCHAR(15) | NOT NULL | Driver contact number |
| status | ENUM('Available','Assigned','Inactive') | DEFAULT 'Available' | Driver availability |

#### 10.1.9 Tour Package

| Field | Data Type | Constraints | Description |
|---|---|---|---|
| package_id | INT | PRIMARY KEY, AUTO_INCREMENT | Unique package ID |
| customer_id | VARCHAR(10) | FOREIGN KEY → Customer | Customer creating package |
| destinations | TEXT | NOT NULL | Selected destinations |
| duration_days | INT | NOT NULL | Tour duration |
| vehicle_type | VARCHAR(50) | NOT NULL | Selected vehicle |
| total_price | DECIMAL(10,2) | NOT NULL | Package price |
| package_status | ENUM('Pending','Confirmed','Cancelled') | DEFAULT 'Pending' | Package status |

#### 10.1.10 Audit Log

| Field | Data Type | Constraints | Description |
|---|---|---|---|
| log_id | INT | PRIMARY KEY, AUTO_INCREMENT | Unique log ID |
| user_id | INT | FOREIGN KEY → User | User performing action |
| action_type | VARCHAR(100) | NOT NULL | Type of action |
| entity_type | VARCHAR(100) | NULLABLE | Affected entity |
| entity_id | VARCHAR(50) | NULLABLE | Related record ID |
| description | TEXT | NULLABLE | Action description |
| timestamp | DATETIME | DEFAULT NOW() | Action timestamp |

### 10.2 Data Relationships

- A Customer can have many Bookings (one-to-many).
- A Bus Route can have many Schedules (one-to-many).
- A Schedule can have many Bookings (one-to-many).
- A Booking can contain multiple Seats (one-to-many).
- A Vehicle can be assigned to many Schedules (one-to-many).
- A Driver can be assigned to many Schedules or Tour Packages (one-to-many).
- A Customer can create multiple Tour Packages (one-to-many).
- A User can perform many system actions recorded in the Audit Log (one-to-many).
- A Schedule references one Bus Route.
- A Booking references one Customer and one Schedule.

### 10.3 Data Storage and Retention

- All data shall be stored in a MySQL 8.0 relational database.
- Customer and booking records shall be retained for a minimum of 5 years.
- Audit logs shall be retained for a minimum of 90 days for security monitoring.
- Automated database backups shall be performed every 24 hours.
- Cancelled booking records shall not be permanently deleted to maintain historical tracking.
- Payment and booking transaction data shall be securely stored for auditing purposes.
- Sensitive information such as passwords shall be encrypted before storage.
- Tour package and airport transfer records shall be retained for reporting and analytics purposes.

### 10.4 Data Integrity and Validation Rules

- Customer IDs and booking IDs must be unique and system-generated.
- Email addresses must be unique for each registered customer and user.
- Seat bookings must prevent double booking of the same seat.
- Booking dates and departure times must not be set in the past.
- Available seat counts must never become negative.
- All monetary values shall use DECIMAL(10,2) data types.
- Foreign key constraints shall be enforced to maintain relational integrity.
- Passwords must be securely hashed before storage.
- Route, booking, and payment updates shall create corresponding Audit Log entries.
- Only authenticated users with valid roles shall access protected system modules.

---

## Chapter 11: Alternative Solutions Considered

| Alternative | Description | Reason for Rejection |
|---|---|---|
| Manual / Paper-Based Booking System | Continue managing bus bookings, schedules, customer details, and tour reservations using paper records and registers. | Prone to human errors; difficult to track bookings and schedules; no real-time seat availability; inefficient data management; time-consuming. |
| Phone-Based Booking System | Customers make bookings through phone calls without using an online booking platform. | High chance of booking errors and double bookings; difficult to manage large booking volumes; no automated confirmations or notifications. |
| Spreadsheet-Based Management System | Use spreadsheet software to manage routes, bookings, vehicles, and customer records. | Not suitable for multi-user environments; lacks real-time updates; difficult to maintain data consistency; no automation features. |
| Separate Systems for Bus Booking, Airport Transfers, and Tours | Use independent systems for different transport services instead of a unified platform. | Lack of integration; duplicate data management; inefficient operations; difficult reporting and administration. |
| Mobile Application Only | Develop only a native mobile application without a web-based system. | Higher development and maintenance costs; requires separate applications for Android and iOS; limited accessibility for some users and administrators. |
| Admin Approval for Every Booking | Require admin approval before confirming every customer booking request. | Causes delays in booking confirmation; increases administrative workload; reduces customer convenience and booking efficiency. |
| Offline Booking Management System | Manage bookings and schedules without internet connectivity. | No real-time synchronization; difficult to update seat availability and notifications; limited accessibility for customers and operators. |
| Cash-Only Payment Method | Allow customers to make payments only through cash transactions. | Reduces convenience for online users; limits digital booking capabilities; not suitable for customers preferring online payment methods. |
| Manual Tour Package Planning | Staff manually prepare customized tour packages for each customer request. | Time-consuming; difficult to calculate pricing accurately; inefficient for handling multiple customer requests simultaneously. |

---

## Chapter 12: Feasibility Study

### 12.1 Technical Feasibility

#### 12.1.1 Technology Stack Assessment

| Component | Proposed Technology | Justification |
|---|---|---|
| Frontend | React.js | Component-based architecture, responsive UI, and strong community support |
| Backend | Node.js | Scalable, secure, and suitable for REST API development |
| Database | MySQL 8.0 | Reliable relational database suitable for booking and transaction management |
| Authentication | JWT + BCrypt | Secure authentication and password encryption |
| Containerization | Docker | Consistent deployment and environment management |
| Notifications | Email API / SMS API | Supports booking confirmations and alerts |
| API Documentation | Swagger / OpenAPI | Standardized and auto-generated API documentation |

#### 12.1.2 Technical Feasibility Assessment

- The development team has prior experience with React.js, Node.js, and MySQL through academic projects and coursework.
- All selected technologies and frameworks are open-source and widely documented.
- The system architecture separates frontend, backend, and database layers for easier maintenance and scalability.
- Docker can be used to ensure consistent deployment environments across development and production systems.
- Real-time seat booking and availability management introduce moderate technical complexity but are achievable using database synchronization and API validation techniques.
- Integration with email or SMS notification services can be implemented using existing third-party APIs.

> **Conclusion:** The project is technically feasible. The selected technologies are modern, reliable, and within the technical capabilities of the development team.

### 12.2 Economic Feasibility

#### 12.2.1 Cost Estimate

| Cost Item | Estimated Cost (LKR) |
|---|---|
| Development Cost (student project – no labour cost) | 0 |
| Cloud Hosting (12 months) | ~60,000 – 120,000 |
| Domain Name Registration (1 year) | ~3,000 – 5,000 |
| SSL Certificate (Let's Encrypt – free) | 0 |
| SMS / Email Notification Service | ~10,000 – 20,000 per year |
| Software Licenses (Open-source stack) | 0 |
| **Total Estimated Annual Operational Cost** | **~73,000 – 145,000 LKR** |

### 12.3 Benefit Analysis

- The system reduces manual booking and scheduling operations.
- Real-time booking management minimizes booking conflicts and double bookings.
- Automated notifications improve customer communication and service reliability.
- Digital records improve route, vehicle, and customer management efficiency.
- Online booking capabilities improve customer convenience and business accessibility.
- Reporting and analytics features help operators make better business decisions.

> **Conclusion:** The system is economically feasible. The operational costs are reasonable compared to the expected improvements in efficiency, customer satisfaction, and business management.

### 12.4 Operational Feasibility

- Customers and staff are assumed to possess basic computer and smartphone literacy.
- The system interface is designed to be simple and user-friendly.
- Key operations such as booking tickets, managing schedules, and viewing reports require minimal training.

#### 12.4.1 Organizational Impact

- Existing manual booking processes will be replaced with digital workflows.
- Initial staff training sessions will be required before system deployment.
- The system does not require significant hardware changes beyond existing computers and internet access.
- Admin users can manage schedules, pricing, vehicles, and user accounts without advanced technical skills.

> **Conclusion:** The system is operationally feasible. The interface design and automation features support smooth adoption by customers and transport operators.

### 12.5 Schedule Feasibility

#### 12.5.1 Estimated Project Timeline

| Phase | Description | Duration | Milestone |
|---|---|---|---|
| 1 | Requirements Analysis & SRS Documentation | 3 Weeks | SRS Approved |
| 2 | System Design (Architecture, Database, UI Mockups) | 3 Weeks | Design Completed |
| 3 | Frontend Development (React.js Modules) | 5 Weeks | UI Prototype |
| 4 | Backend Development (APIs, Authentication, Database Integration) | 5 Weeks | APIs Tested |
| 5 | Integration Testing & Bug Fixing | 3 Weeks | Test Reports |
| 6 | User Acceptance Testing (UAT) | 2 Weeks | UAT Sign-off |
| 7 | Deployment & Final Documentation | 2 Weeks | System Deployment |
| 8 | Buffer Time / Contingency | 2 Weeks | Project Completion |

**Total Estimated Duration: 25 Weeks**

#### 12.5.2 Schedule Risk Factors

- A multi-member development team allows parallel frontend and backend development.
- Academic workload and examinations may temporarily affect development progress.
- Modular system architecture supports phased implementation and testing.
- Clearly defined project scope helps reduce scope creep and scheduling delays.

> **Conclusion:** The schedule is feasible. The estimated timeline is achievable provided that tasks are properly managed and project scope is controlled effectively.
