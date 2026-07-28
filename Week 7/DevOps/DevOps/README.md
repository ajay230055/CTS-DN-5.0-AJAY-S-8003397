# DevOps Fundamentals

A detailed reference guide covering the core concepts of DevOps.

---

## Table of Contents
1. [What is DevOps?](#1-what-is-devops)
2. [Core Principles](#2-core-principles)
3. [The DevOps Lifecycle](#3-the-devops-lifecycle)
4. [Key DevOps Tools by Category](#4-key-devops-tools-by-category)
5. [CI/CD Explained](#5-cicd-explained)
6. [Benefits of DevOps](#6-benefits-of-devops)
7. [Common DevOps Metrics (DORA Metrics)](#7-common-devops-metrics-dora-metrics)

---

## 1. What is DevOps?
DevOps is a set of practices, culture, and tools that combines **Software Development (Dev)** and **IT Operations (Ops)**. Its goal is to shorten the software development lifecycle (SDLC) and deliver high-quality software continuously, by improving collaboration between development and operations teams.

DevOps is not a single tool or job title — it's a **cultural shift** that encourages shared responsibility for building, testing, deploying, and maintaining software throughout its entire lifecycle.

## 2. Core Principles
- **Collaboration** — Breaking down silos between developers, testers, and operations teams so everyone works toward the same goal.
- **Automation** — Automating repetitive tasks like builds, tests, and deployments to reduce human error and speed up delivery.
- **Continuous Integration (CI)** — Frequently merging code changes into a shared repository, with automated builds/tests on each merge.
- **Continuous Delivery/Deployment (CD)** — Automatically preparing (or deploying) code changes to production after passing CI.
- **Monitoring & Feedback** — Continuously monitoring applications and infrastructure to catch issues early and feed insights back into development.
- **Infrastructure as Code (IaC)** — Managing and provisioning infrastructure through code/config files instead of manual processes (e.g., Terraform, Ansible).
- **Fail Fast, Learn Fast** — Encouraging small, frequent changes so failures are caught and fixed quickly rather than discovered late.

## 3. The DevOps Lifecycle
```
Plan → Code → Build → Test → Release → Deploy → Operate → Monitor → (back to Plan)
```
This is often visualized as an **infinity loop**, emphasizing that DevOps is a continuous, iterative process rather than a linear one.

- **Plan** — Define requirements, roadmap, and goals.
- **Code** — Write and review application code.
- **Build** — Compile code and package it into deployable artifacts.
- **Test** — Run automated tests (unit, integration, security).
- **Release** — Prepare the tested build for deployment.
- **Deploy** — Push the release to production or staging environments.
- **Operate** — Manage the running application and infrastructure.
- **Monitor** — Track performance, errors, and user feedback to inform the next planning cycle.

## 4. Key DevOps Tools by Category
| Category | Tools |
|---|---|
| Version Control | Git, GitHub, GitLab, Bitbucket |
| CI/CD | Jenkins, GitHub Actions, GitLab CI, CircleCI, Azure DevOps |
| Configuration Management | Ansible, Chef, Puppet |
| Infrastructure as Code | Terraform, AWS CloudFormation, Pulumi |
| Containerization | Docker, Podman |
| Orchestration | Kubernetes, Docker Swarm |
| Monitoring & Logging | Prometheus, Grafana, ELK Stack, Datadog |
| Collaboration | Jira, Slack, Confluence |

## 5. CI/CD Explained
- **Continuous Integration (CI):** Developers merge code into a central repo frequently (multiple times a day). Automated builds and tests run on every commit to catch bugs early.
- **Continuous Delivery (CD):** Code is automatically prepared for a release to production, but the final deployment step may require manual approval.
- **Continuous Deployment:** Every change that passes automated tests is automatically deployed to production — no manual step required.

### Example CI/CD Pipeline (GitHub Actions)
```yaml
name: CI Pipeline

on:
  push:
    branches: [main]

jobs:
  build-and-test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - name: Install dependencies
        run: npm install
      - name: Run tests
        run: npm test
      - name: Build application
        run: npm run build
```

## 6. Benefits of DevOps
- Faster time to market
- Improved deployment frequency
- Reduced failure rate of new releases
- Faster recovery time (Mean Time to Recovery)
- Better collaboration and communication across teams
- Higher quality software due to continuous testing

## 7. Common DevOps Metrics (DORA Metrics)
1. **Deployment Frequency** — How often code is deployed to production.
2. **Lead Time for Changes** — Time from code commit to production deployment.
3. **Change Failure Rate** — Percentage of deployments causing failures.
4. **Mean Time to Recovery (MTTR)** — Time taken to recover from a failure.

---

*For deeper learning, refer to official resources like the [AWS DevOps guide](https://aws.amazon.com/devops/what-is-devops/) or [Atlassian's DevOps guide](https://www.atlassian.com/devops).*
