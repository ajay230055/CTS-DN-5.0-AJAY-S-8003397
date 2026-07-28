# Cloud Fundamentals

A detailed reference guide covering the core concepts of Cloud Computing.

---

## Table of Contents
1. [What is Cloud Computing?](#1-what-is-cloud-computing)
2. [Key Characteristics](#2-key-characteristics)
3. [Cloud Service Models](#3-cloud-service-models)
4. [Cloud Deployment Models](#4-cloud-deployment-models)
5. [Major Cloud Providers](#5-major-cloud-providers)
6. [Core Cloud Concepts](#6-core-cloud-concepts)
7. [Benefits of Cloud Computing](#7-benefits-of-cloud-computing)
8. [Common Cloud Terminology](#8-common-cloud-terminology)

---

## 1. What is Cloud Computing?
Cloud computing is the **on-demand delivery of computing resources** (servers, storage, databases, networking, software) over the internet ("the cloud") with pay-as-you-go pricing, instead of owning and maintaining physical infrastructure.

Rather than buying and maintaining physical servers, organizations rent computing power and storage from a cloud provider, paying only for what they use.

## 2. Key Characteristics
- **On-demand self-service** — Provision resources without human intervention from the provider.
- **Broad network access** — Accessible over the internet from various devices.
- **Resource pooling** — Provider resources are pooled to serve multiple customers (multi-tenancy).
- **Rapid elasticity** — Resources can scale up or down quickly based on demand.
- **Measured service** — Pay only for what you use, with usage monitored and billed accordingly.

## 3. Cloud Service Models
| Model | Description | Examples |
|---|---|---|
| **IaaS** (Infrastructure as a Service) | Provides virtualized computing resources (VMs, storage, networks) | AWS EC2, Azure VMs, Google Compute Engine |
| **PaaS** (Platform as a Service) | Provides a platform to build, run, and manage apps without managing infrastructure | AWS Elastic Beanstalk, Heroku, Google App Engine |
| **SaaS** (Software as a Service) | Fully managed software delivered over the internet | Gmail, Google Workspace, Salesforce, Dropbox |

**Analogy:**
- IaaS = Renting an empty plot of land (you build everything)
- PaaS = Renting a furnished apartment (you just move in and customize)
- SaaS = Staying in a hotel (everything is provided and managed)

## 4. Cloud Deployment Models
- **Public Cloud** — Owned/operated by third-party providers, shared among multiple organizations (e.g., AWS, Azure, GCP).
- **Private Cloud** — Dedicated infrastructure used exclusively by one organization, either on-premises or hosted.
- **Hybrid Cloud** — Combination of public and private clouds, allowing data/applications to move between them.
- **Multi-Cloud** — Using services from multiple cloud providers simultaneously to avoid vendor lock-in and increase resilience.

## 5. Major Cloud Providers
| Provider | Key Services |
|---|---|
| **AWS** (Amazon Web Services) | EC2, S3, Lambda, RDS, VPC |
| **Microsoft Azure** | Azure VMs, Blob Storage, Azure Functions, Azure SQL |
| **Google Cloud Platform (GCP)** | Compute Engine, Cloud Storage, Cloud Functions, BigQuery |

## 6. Core Cloud Concepts
- **Compute** — Virtual machines/instances that run applications (e.g., EC2, Azure VM).
- **Storage** — Object storage (S3), block storage (EBS), file storage.
- **Networking** — VPCs, subnets, load balancers, VPNs, CDN.
- **Databases** — Managed relational (RDS) and NoSQL (DynamoDB) databases.
- **Serverless Computing** — Running code without provisioning/managing servers (e.g., AWS Lambda, Azure Functions). You pay only for execution time.
- **Identity & Access Management (IAM)** — Controlling who can access what resources and what actions they can perform.
- **Auto Scaling** — Automatically adjusting compute resources based on load.
- **Load Balancing** — Distributing incoming traffic across multiple servers for reliability and performance.

## 7. Benefits of Cloud Computing
- Cost efficiency (no upfront hardware investment)
- Scalability and flexibility
- High availability and disaster recovery
- Global reach with low latency (via regions/edge locations)
- Faster innovation and deployment
- Reduced maintenance burden (provider manages hardware)

## 8. Common Cloud Terminology
| Term | Meaning |
|---|---|
| Region | A geographic location containing multiple data centers |
| Availability Zone (AZ) | An isolated data center within a region |
| CDN | Content Delivery Network — caches content closer to users |
| VPC | Virtual Private Cloud — isolated network within the cloud |
| SLA | Service Level Agreement — guaranteed uptime/performance |
| Elasticity | Ability to automatically scale resources up/down |
| Latency | Time delay between a request and a response |

---

*For deeper learning, refer to [AWS Documentation](https://docs.aws.amazon.com), [Azure Documentation](https://learn.microsoft.com/azure), and [Google Cloud Documentation](https://cloud.google.com/docs).*
