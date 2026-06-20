# Module 2: Cloud Applications

## 3. Cloud Applications

---

# Introduction

Cloud Application ek aisi application hoti hai jo cloud infrastructure par run karti hai aur internet ke madhyam se users ko services provide karti hai. Cloud applications scalability, flexibility, reliability aur cost-effectiveness provide karti hain.

---

# A Brief History

* Traditional applications local servers par host hoti thi.
* Internet ke growth ke saath web applications ka use badha.
* Cloud Computing ne applications ko cloud infrastructure par deploy karna possible banaya.
* AWS, Azure aur Google Cloud jaise providers ne cloud application development ko popular banaya.

---

# Definition of Cloud Application

A cloud application is a software application that runs partly or entirely on cloud infrastructure and can be accessed through the internet.

### Examples

* Gmail
* Google Drive
* Dropbox
* Netflix
* Zoom

---

# Cloud Application Design

Cloud applications ko design karte samay scalability, availability, performance aur security ko dhyan me rakha jata hai.

### Design Goals

* High Availability
* Scalability
* Reliability
* Security
* Cost Optimization

---

# Cloud Application Categories

## 1. Infrastructure as a Service (IaaS)

Cloud provider infrastructure provide karta hai.

### Examples

* AWS EC2
* Azure Virtual Machines
* Google Compute Engine
* DigitalOcean

### Advantages

* Full Control
* High Flexibility
* Customization

### Disadvantages

* Maintenance Responsibility
* Security Management
* System Administration Knowledge Required

---

## 2. Platform as a Service (PaaS)

Cloud provider infrastructure aur platform dono manage karta hai.

### Examples

* Render
* Railway
* Heroku
* Vercel
* Netlify

### Advantages

* Easy Deployment
* Faster Development
* Automatic Scaling

### Disadvantages

* Limited Customization
* Vendor Restrictions

---

## 3. Software as a Service (SaaS)

Complete software service internet ke through provide ki jati hai.

### Examples

* Gmail
* Google Docs
* Zoom
* Canva
* ChatGPT

### Advantages

* No Maintenance
* Ready to Use
* Easy Access

### Disadvantages

* Limited Control
* Vendor Dependency

---

# Benefits of Cloud Applications

* Scalability
* Cost Reduction
* High Availability
* Easy Maintenance
* Global Accessibility
* Disaster Recovery Support

---

# How Cloud Applications Work

```text
User
 ↓
Internet
 ↓
Cloud Application
 ↓
Database
 ↓
Response
```

Components:

* Frontend
* Backend
* Database
* Cloud Infrastructure

---

# Cloud Applications vs Web Applications

| Cloud Application                      | Web Application              |
| -------------------------------------- | ---------------------------- |
| Cloud Infrastructure par run karti hai | Web Server par run karti hai |
| Highly Scalable                        | Limited Scalability          |
| Multi-region Deployment Possible       | Usually Single Region        |
| Cloud Services Use karti hai           | Traditional Hosting          |

---

# Top Cloud Computing Technologies

## 1. Virtualization

Physical resources ko virtual resources me convert karne ki technology.

### Types of Virtualization

#### Hardware Virtualization

Ek physical machine par multiple virtual machines run karna.

Example:

* VirtualBox
* VMware

#### Operating System Virtualization

Ek hi operating system par isolated environments create karna.

Example:

* Docker Containers

#### Server Virtualization

Ek physical server ko multiple virtual servers me divide karna.

#### Storage Virtualization

Multiple storage devices ko ek logical storage unit ke roop me present karna.

---

## 2. Service-Oriented Architecture (SOA)

Application ko multiple reusable services me divide karna.

### Components

* Service Provider
* Service Consumer
* Service Registry

### Advantages

* Reusability
* Scalability
* Flexibility

---

## 3. Grid Computing

Multiple computers milkar ek large task complete karte hain.

### Advantages

* Faster Processing
* Resource Sharing
* Cost Effectiveness

### Applications

* Scientific Research
* Weather Forecasting
* Data Analysis

---

## 4. Utility Computing

Pay-As-You-Use model.

### Features

* On-Demand Resources
* Scalability
* Cost Savings

### Examples

* AWS
* Azure
* Google Cloud

---

# Practice for Deploying Your Apps in the Cloud

Cloud deployment ke dauran best practices follow karni chahiye.

---

## Choose Between IaaS, PaaS and SaaS

Application developers ke liye generally PaaS recommended hota hai kyunki infrastructure management provider handle karta hai.

---

# Application Scaling

## Vertical Scaling (Scale Up)

Existing server ke resources increase karna.

Example:

```text
4 GB RAM → 16 GB RAM
```

### Advantages

* Easy Management
* Simple Upgrade

### Disadvantages

* Limited Growth
* Single Point of Failure

---

## Horizontal Scaling (Scale Out)

Multiple servers add karna.

Example:

```text
Server 1
Server 2
Server 3
```

### Advantages

* High Availability
* Better Reliability
* Unlimited Growth

### Disadvantages

* Complex Setup
* Higher Management Effort

---

## Manual Scaling

Developer manually servers add karta hai.

---

## Automatic Scaling

Cloud automatically load ke according servers add ya remove karta hai.

---

# Application State

## Stateful Applications

Server user ki information maintain karta hai.

Examples:

* Login Sessions
* Shopping Cart

### Problems

* Difficult Scaling
* Session Loss Risk

---

## Stateless Applications

Server user state maintain nahi karta.

Data external storage me save hota hai.

### Benefits

* Easy Scaling
* Better Cloud Support
* High Availability

---

# Database for Cloud Applications

### Best Practices

* Database ko separate server par deploy karo.
* Same region me database rakho.
* Database independently scalable hona chahiye.

### Options

#### Remote VPC Connection

Cloud application securely database se connect karti hai.

#### REST Service Access

Database ko APIs ke through access kiya jata hai.

---

# Multiple Geographies

Application ko multiple regions me deploy karna.

### Benefits

* Reduced Latency
* Better Performance
* High Availability
* Disaster Recovery
* Global Scalability

### Example Regions

* Mumbai
* Singapore
* London
* Virginia

---

# REST-Based Web Services

Frontend aur backend ko separate karne ke liye REST APIs use ki jati hain.

### Architecture

```text
Frontend
 ↓
REST API
 ↓
Database
```

### Benefits

* Better Security
* Reusability
* Independent Scaling
* Easier Maintenance

---

# Continuous Integration and Continuous Delivery (CI/CD)

### CI (Continuous Integration)

Code changes ko frequently merge aur test karna.

### CD (Continuous Delivery)

Application ko automated process ke through deploy karna.

### Workflow

```text
Code
 ↓
Git Push
 ↓
Build
 ↓
Test
 ↓
Deploy
```

### Benefits

* Faster Deployment
* Better Quality
* Reduced Errors

---

# Vendor Lock-In

Kisi ek cloud provider par excessively dependent ho jana.

### Avoid Using

* Proprietary APIs
* Vendor-Specific Technologies

### Prefer Using

* PostgreSQL
* REST APIs
* Docker
* Standard Technologies

---

# Develop Locally or in the Cloud

### Local Development

```text
Laptop
 ↓
VS Code
 ↓
Localhost
```

### Cloud Development

```text
Cloud IDE
 ↓
Cloud Server
 ↓
Application
```

### Benefits of Cloud Development

* Production-like Environment
* Better Collaboration
* Easier Deployment

---

# Choosing an IDE

Aisa IDE choose karo jo cloud plugins support karta ho.

### Examples

* VS Code
* IntelliJ IDEA
* Eclipse
* PyCharm

### Important Features

* Cloud Integration
* Hot Deployment
* Remote Debugging
* Breakpoints

---

# Future of Cloud Providers

### Focus Areas

#### Containers

Examples:

* Docker
* Rocket Containers

#### Container Orchestration

Examples:

* Kubernetes
* Docker Swarm

### Recommendations


# 3.2 Deploying a Web Service from Inside and Outside a Cloud Architecture

## Introduction

Java Web Deployment in Cloud Computing me kai challenges hote hain jaise:

* Performance Issues
* Cost Issues
* Security Issues
* Reliability Issues

Jab Java application ko cloud par deploy kiya jata hai to expected performance milni chahiye, lekin cloud environment ki limitations aur performance challenges ko bhi dhyan me rakhna padta hai.

Cloud Computing ko network ke madhyam se service provide karne wali technology ke roop me dekha ja sakta hai. Yeh users ko on-demand resources provide karti hai.

### Features of Cloud Computing

* On-Demand Self Service
* Resource Pooling
* Rapid Elasticity
* Broad Network Access
* Measured Service

### Popular Cloud Platforms

* Google App Engine
* Microsoft Azure
* Amazon Web Services (AWS)

---

## Deploying Web Service Applications onto Application Servers

Web Services ko Application Servers par deploy kiya ja sakta hai.

### Process

```text
Application
      ↓
EAR File
      ↓
Application Server
      ↓
Deployment
```

### EAR File

EAR (Enterprise Archive) Java Enterprise Applications ka deployment package hota hai.

### Examples of Application Servers

* IBM WebSphere
* JBoss
* WebLogic
* Apache Tomcat

---

## Using a Third-Party JAX-WS Web Services Engine

Kayi situations me third-party JAX-WS engine use karna padta hai.

### JAX-WS

Java API for XML Web Services

### Popular JAX-WS Engines

* Apache CXF
* Apache Axis2
* Metro

### Benefits

* Web Services Development
* Service Deployment
* XML Based Communication

---

## Deploying Web Service Client Applications

Web Service Client Applications bhi deploy ki ja sakti hain.

### Process

```text
Client Application
       ↓
EAR File
       ↓
Application Server
       ↓
Deployment
```

Client applications deployed services ko consume karti hain.

---

## Making Deployed Web Services Available to Clients

Deployment ke baad services ko clients ke liye accessible banana padta hai.

### WSDL

WSDL = Web Services Description Language

WSDL service ke baare me information provide karti hai:

* Service Name
* Available Operations
* Request Format
* Response Format

### Purpose

Client applications WSDL ka use karke web services se connect kar sakti hain.

---

## Running an Unmanaged Web Services JAX-RPC Client

### JAX-RPC

Java API for XML Remote Procedure Call

JAX-RPC clients hosted web services ko invoke kar sakte hain.

### Benefits

* Remote Service Invocation
* Distributed Communication
* Enterprise Integration

---

# 3.3 Advantages and Disadvantages

## Positive Aspects (Advantages of Cloud Computing)

### 1. Service Based

Cloud Computing services ke roop me resources provide karti hai.

#### Benefits

* Simplified Usage
* Reduced Management Effort
* Automated Service Delivery

---

### 2. Elastic

Cloud resources demand ke hisab se automatically scale ho sakte hain.

#### Benefits

* Dynamic Scaling
* Better Resource Utilization
* Cost Optimization

---

### 3. Shared

Resources multiple users ke beech share kiye ja sakte hain.

#### Benefits

* Economies of Scale
* Efficient Resource Usage
* Lower Operational Costs

---

### 4. Metered by Use

Cloud services usage ke according charge karti hain.

#### Pricing Models

* Pay-As-You-Go
* Subscription Based
* Fixed Plans
* Free Plans

#### Benefits

* Cost Control
* Flexible Billing

---

### 5. Uses Internet Technologies

Cloud services internet standards ka use karti hain.

### Technologies

* URL
* HTTP
* HTTPS
* IP
* REST

#### Benefits

* Universal Access
* Easy Connectivity
* Platform Independence

---

# Benefits of Cloud Computing

The most commonly cited benefits are:

### Agile Deployment

* Fast Deployment
* Easy Provisioning
* Faster Time to Market

### Reduced Costs

* Pay for What You Use
* Reduced Infrastructure Costs

### Reduced In-House IT Costs

* Less Hardware Maintenance
* Lower Administrative Overhead

### Reduced Capital Investment

* No Large Initial Investment
* Operational Expense Model

### Access to Latest Technology

* Continuous Updates
* New Features
* Modern Infrastructure

### Increased Accessibility

* Access from Anywhere
* Support for Mobile Devices
* Better Collaboration

---

# Disadvantages of Web Services

## 1. Matching Requirements

A single web service may not satisfy every customer requirement.

### Issues

* Different Customer Needs
* Specialized Requirements

---

## 2. Availability Issues

Web Services may not always be available.

### Problems

* Server Downtime
* Network Failures
* Service Interruptions

---

## 3. Security Issues

Since web services are accessible over public networks, they may face security threats.

### Risks

* Unauthorized Access
* Data Theft
* Attacks on Services

### Solutions

* Authentication
* Authorization
* HTTPS
* Security Policies

---

## 4. Guaranteed Execution Problems

HTTP protocol does not guarantee delivery of requests.

### Issues

* Network Failures
* Lost Requests
* Communication Delays

---

# Quick Revision

## Web Service Deployment

```text
Application
      ↓
EAR File
      ↓
Application Server
      ↓
WSDL
      ↓
Client Access
```

### Technologies

* JAX-WS
* JAX-RPC
* WSDL
* WebSphere
* JBoss
* WebLogic

---

## Advantages of Cloud Computing

1. Service Based
2. Elastic
3. Shared Resources
4. Metered by Use
5. Internet Based
6. Agile Deployment
7. Reduced Cost
8. Reduced IT Cost
9. Reduced Capital Investment
10. Latest Technology Access

---

## Disadvantages of Web Services

1. Matching Requirements
2. Availability Issues
3. Security Issues
4. Guaranteed Execution Problems

* Use Industry Standards
* Avoid Proprietary Solutions
* Prefer Docker and Kubernetes Support

---

# Cloud Deployment Best Practices (Summary)

1. Use PaaS for development.
2. Support horizontal scaling.
3. Design stateless applications.
4. Use scalable databases.
5. Deploy across multiple geographies.
6. Use REST-based web services.
7. Implement CI/CD.
8. Avoid vendor lock-in.
9. Use industry-standard technologies.


# 3.2 Deploying a Web Service from Inside and Outside a Cloud Architecture

## Introduction

Java Web Deployment in Cloud Computing me kai challenges hote hain jaise:

* Performance Issues
* Cost Issues
* Security Issues
* Reliability Issues

Jab Java application ko cloud par deploy kiya jata hai to expected performance milni chahiye, lekin cloud environment ki limitations aur performance challenges ko bhi dhyan me rakhna padta hai.

Cloud Computing ko network ke madhyam se service provide karne wali technology ke roop me dekha ja sakta hai. Yeh users ko on-demand resources provide karti hai.

### Features of Cloud Computing

* On-Demand Self Service
* Resource Pooling
* Rapid Elasticity
* Broad Network Access
* Measured Service

### Popular Cloud Platforms

* Google App Engine
* Microsoft Azure
* Amazon Web Services (AWS)

---

## Deploying Web Service Applications onto Application Servers

Web Services ko Application Servers par deploy kiya ja sakta hai.

### Process

```text
Application
      ↓
EAR File
      ↓
Application Server
      ↓
Deployment
```

### EAR File

EAR (Enterprise Archive) Java Enterprise Applications ka deployment package hota hai.

### Examples of Application Servers

* IBM WebSphere
* JBoss
* WebLogic
* Apache Tomcat

---

## Using a Third-Party JAX-WS Web Services Engine

Kayi situations me third-party JAX-WS engine use karna padta hai.

### JAX-WS

Java API for XML Web Services

### Popular JAX-WS Engines

* Apache CXF
* Apache Axis2
* Metro

### Benefits

* Web Services Development
* Service Deployment
* XML Based Communication

---

## Deploying Web Service Client Applications

Web Service Client Applications bhi deploy ki ja sakti hain.

### Process

```text
Client Application
       ↓
EAR File
       ↓
Application Server
       ↓
Deployment
```

Client applications deployed services ko consume karti hain.

---

## Making Deployed Web Services Available to Clients

Deployment ke baad services ko clients ke liye accessible banana padta hai.

### WSDL

WSDL = Web Services Description Language

WSDL service ke baare me information provide karti hai:

* Service Name
* Available Operations
* Request Format
* Response Format

### Purpose

Client applications WSDL ka use karke web services se connect kar sakti hain.

---

## Running an Unmanaged Web Services JAX-RPC Client

### JAX-RPC

Java API for XML Remote Procedure Call

JAX-RPC clients hosted web services ko invoke kar sakte hain.

### Benefits

* Remote Service Invocation
* Distributed Communication
* Enterprise Integration

---

# 3.3 Advantages and Disadvantages

## Positive Aspects (Advantages of Cloud Computing)

### 1. Service Based

Cloud Computing services ke roop me resources provide karti hai.

#### Benefits

* Simplified Usage
* Reduced Management Effort
* Automated Service Delivery

---

### 2. Elastic

Cloud resources demand ke hisab se automatically scale ho sakte hain.

#### Benefits

* Dynamic Scaling
* Better Resource Utilization
* Cost Optimization

---

### 3. Shared

Resources multiple users ke beech share kiye ja sakte hain.

#### Benefits

* Economies of Scale
* Efficient Resource Usage
* Lower Operational Costs

---

### 4. Metered by Use

Cloud services usage ke according charge karti hain.

#### Pricing Models

* Pay-As-You-Go
* Subscription Based
* Fixed Plans
* Free Plans

#### Benefits

* Cost Control
* Flexible Billing

---

### 5. Uses Internet Technologies

Cloud services internet standards ka use karti hain.

### Technologies

* URL
* HTTP
* HTTPS
* IP
* REST

#### Benefits

* Universal Access
* Easy Connectivity
* Platform Independence

---

# Benefits of Cloud Computing

The most commonly cited benefits are:

### Agile Deployment

* Fast Deployment
* Easy Provisioning
* Faster Time to Market

### Reduced Costs

* Pay for What You Use
* Reduced Infrastructure Costs

### Reduced In-House IT Costs

* Less Hardware Maintenance
* Lower Administrative Overhead

### Reduced Capital Investment

* No Large Initial Investment
* Operational Expense Model

### Access to Latest Technology

* Continuous Updates
* New Features
* Modern Infrastructure

### Increased Accessibility

* Access from Anywhere
* Support for Mobile Devices
* Better Collaboration

---

# Disadvantages of Web Services

## 1. Matching Requirements

A single web service may not satisfy every customer requirement.

### Issues

* Different Customer Needs
* Specialized Requirements

---

## 2. Availability Issues

Web Services may not always be available.

### Problems

* Server Downtime
* Network Failures
* Service Interruptions

---

## 3. Security Issues

Since web services are accessible over public networks, they may face security threats.

### Risks

* Unauthorized Access
* Data Theft
* Attacks on Services

### Solutions

* Authentication
* Authorization
* HTTPS
* Security Policies

---

## 4. Guaranteed Execution Problems

HTTP protocol does not guarantee delivery of requests.

### Issues

* Network Failures
* Lost Requests
* Communication Delays

---

# Quick Revision

## Web Service Deployment

```text
Application
      ↓
EAR File
      ↓
Application Server
      ↓
WSDL
      ↓
Client Access
```

### Technologies

* JAX-WS
* JAX-RPC
* WSDL
* WebSphere
* JBoss
* WebLogic

---

## Advantages of Cloud Computing

1. Service Based
2. Elastic
3. Shared Resources
4. Metered by Use
5. Internet Based
6. Agile Deployment
7. Reduced Cost
8. Reduced IT Cost
9. Reduced Capital Investment
10. Latest Technology Access

---

## Disadvantages of Web Services

1. Matching Requirements
2. Availability Issues
3. Security Issues
4. Guaranteed Execution Problems
