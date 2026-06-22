# Module 3: Cloud Services Management

## 4. Cloud Services Management

---

# Introduction

Cloud Services Management refers to the process of managing, monitoring, securing, and optimizing cloud-based services after deployment.

Cloud me application deploy karne ke baad sirf deployment hi important nahi hota, balki uski availability, reliability, security, performance, scalability aur cost management bhi equally important hote hain.

### Simple Definition

Cloud Services Management is the practice of managing cloud resources and services to ensure they remain reliable, available, secure, scalable, and cost-effective.

### Real-Life Example

Explore Bharat Website:

```text
Frontend → Vercel
Backend → Render
Database → Supabase
```

Deployment ke baad hume ensure karna hota hai:

* Website always available ho
* Data secure rahe
* Performance achhi ho
* Users badhne par scale kare
* Cost control me rahe

---

# Characteristics of Cloud Services Management

## 1. Reliability

Service kitni trustworthy hai.

Example:

```text
1000 Users
↓
Website Works Properly
```

Reliable service user requests ko successfully complete karti hai.

---

## 2. Availability

Service kitne time tak users ke liye accessible rahti hai.

Example:

```text
24 Hours
7 Days
```

High availability means service anytime and anywhere accessible ho.

---

## 3. Security

Data aur applications ko unauthorized access se protect karna.

Examples:

* Password Protection
* Encryption
* HTTPS
* Firewalls

---

## 4. Scalability

User load badhne par resources automatically increase ho sake.

Example:

```text
100 Users
↓
10000 Users
```

Application still works smoothly.

---

## 5. Performance

Application kitni fast response karti hai.

Example:

```text
Click
↓
Response in 1 Second
```

---

## 6. Cost Effectiveness

Pay only for resources actually used.

---

## 7. Monitoring

Cloud resources continuously monitor kiye jate hain.

Examples:

* AWS CloudWatch
* Azure Monitor
* Google Cloud Monitoring

---

## 8. Automation

Cloud automatically scaling aur resource provisioning perform karta hai.

Example:

```text
Traffic Increase
↓
Auto Scaling
↓
New Server Created
```

---

# 4.1 Reliability, Availability and Security of Services Deployed from Cloud

---

# 4.1.1 Cloud Service Reliability Modelling and Evaluation

## Definition

Cloud Service Reliability is the probability that a cloud service can successfully complete a user request within a specified period of time.

### Reliability Requirements

Cloud reliability ke liye:

1. User request successfully process honi chahiye.
2. Computing resources available hone chahiye.
3. Data resources available hone chahiye.
4. Network communication operational hona chahiye.

---

## Types of Failures

### Group 1: Request Stage Failures

Request execute hone se pehle failures.

#### Overflow

Too many requests arrive.

Example:

```text
Capacity = 100 Users
Actual = 10000 Users
```

#### Timeout

Response expected time me nahi aata.

Example:

```text
Request Sent
↓
No Response
↓
Timeout
```

---

### Group 2: Execution Stage Failures

Request execution ke dauran failures.

#### Examples

* Data Resource Failure
* Computing Resource Failure
* Software Failure
* Database Failure
* Hardware Failure
* Network Failure

---

## User Expectations from Cloud Services

When using cloud services, users expect:

* App always running ho
* Access from any device
* No downtime
* Secure connection
* Successful task completion

---

## Improving Reliability

### Proper Planning

* Backup Strategy
* Monitoring
* Recovery Plan

### Virtualization

Virtualization ki help se resources quickly add kiye ja sakte hain.

---

## Benefits of Reliable Systems

### Redundant Resources

```text
Server A Fails
↓
Server B Takes Over
```

### Continuous Availability

Services remain available.

### Better Productivity

Employees continue working without interruption.

---

## Importance of Reliability

Poor reliability leads to:

* Lost Productivity
* Lost Revenue
* Lost Customer Trust

---

# 4.1.2 Availability

## Definition

Availability means cloud services remain accessible anytime, anywhere, and from any device.

### Goal of Cloud Computing

High Availability is one of the main goals of moving to the cloud.

---

## Example

```text
Customer
↓
Online Store
↓
Checkout
```

Store available hona hi kaafi nahi hai.

Checkout bhi properly work karna chahiye.

---

## Relationship Between Availability and Reliability

```text
Availability
+
Reliability
=
Useful Service
```

A service that is available but not reliable is practically useless.

---

## Bringing It All Together

Three important cloud qualities:

### Availability

Service online ho.

### Reliability

Service correctly work kare.

### Scalability

Load badhne par scale ho.

---

## Role of IaaS

Infrastructure as a Service provides:

* Servers
* Storage
* Networking
* Automation

Examples:

* AWS EC2
* Azure VM
* Google Compute Engine

---

## Benefits of Availability

* Access from anywhere
* Better customer satisfaction
* Reduced downtime
* Business continuity

---

# 4.1.3 Security

## Definition

Cloud Security is a collection of technologies, controls, policies, and procedures used to protect cloud infrastructure, applications, and data.

### Objectives

Protect against:

* Data Leakage
* Data Theft
* Unauthorized Access
* Data Loss

---

# How to Manage Security in the Cloud

## 1. Firewall

Acts as a security barrier between internet and cloud resources.

```text
Internet
↓
Firewall
↓
Cloud Server
```

Benefits:

* Blocks unauthorized access
* Protects applications
* Filters malicious traffic

---

## 2. Access Control

Controls user permissions.

Example:

```text
Employee → Read Only

Manager → Edit

Admin → Full Access
```

---

## 3. VPN (Virtual Private Network)

Provides secure remote access.

```text
Employee
↓
VPN
↓
Cloud Network
```

---

## 4. Data Masking

Sensitive information is hidden.

Example:

```text
9876543210
↓
98******10
```

---

## 5. Disaster Recovery

Helps recover lost or stolen data.

Example:

```text
Database Failure
↓
Restore Backup
```

---

# Benefits of Cloud Security Systems

Cloud security helps by:

* Protecting businesses from dangers
* Protecting against internal threats
* Preventing data loss
* Defending against malware
* Defending against ransomware
* Maintaining business continuity

---

# Malware

Malicious software that damages systems.

Examples:

* Virus
* Trojan
* Spyware

---

# Ransomware

Locks data and demands payment for recovery.

Example:

```text
Data Locked
↓
Pay Money
↓
Get Access Back
```

---

# Data Redundancy

Multiple copies of data are maintained.

Example:

```text
Copy 1
Copy 2
Copy 3
```

---

# DDoS Security

## DDoS (Distributed Denial of Service)

Attackers flood a service with fake requests.

Example:

```text
Normal Traffic
100 Requests

Attack Traffic
100000 Requests
```

Effects:

* Slow Website
* Service Downtime
* Revenue Loss
* Reputation Damage

---

# Top 7 Advanced Cloud Security Challenges

---

## 1. Enlarged Surface

Cloud environments have large attack surfaces.

Risks:

* Malware
* Zero-Day Attacks
* Account Hijacking
* Data Theft

---

## 2. Lack of Visibility and Tracking

Customers do not have complete visibility into cloud infrastructure.

Problems:

* Difficult Monitoring
* Limited Control
* Increased Security Risks

---

## 3. Ever-Changing Workload

Cloud resources change dynamically.

Example:

```text
Morning → 2 Servers
Evening → 20 Servers
```

Security policies become difficult to manage.

---

## 4. DevOps, DevSecOps and Automation

Fast CI/CD deployments may introduce vulnerabilities.

Example:

```text
Code
↓
Build
↓
Deploy
```

Without proper security checks.

---

## 5. Granular Privileges and Critical Management

Improper access permissions create security risks.

Example:

```text
Normal User
↓
Database Delete Permission
```

Security issue.

---

## 6. Complex Environment

Organizations may use:

* Public Cloud
* Private Cloud
* Hybrid Cloud
* Multi-Cloud

Managing security becomes difficult.

---

## 7. Cloud Compliance and Governance

Organizations must comply with regulations.

Examples:

* PCI DSS
* HIPAA
* GDPR
* NIST 800-53

Maintaining compliance in dynamic cloud environments is challenging.

---

# Quick Revision

## Reliability

* Overflow
* Timeout
* Resource Failures
* Network Failures

## Availability

* Anytime Access
* Anywhere Access
* Any Device Access

## Security

* Firewall
* Access Control
* VPN
* Data Masking
* Disaster Recovery

## Security Challenges

1. Enlarged Surface
2. Lack of Visibility
3. Ever-Changing Workload
4. DevOps & Automation
5. Granular Privileges
6. Complex Environment
7. Compliance & Governance
