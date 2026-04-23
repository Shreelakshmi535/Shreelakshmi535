# Shreelakshmi Doddaaladahalli Manjunatha

**MS Information Technology & Management — Illinois Institute of Technology '25**

📍 Atlanta, GA &nbsp;|&nbsp; 📧 shreelakshmidm18@gmail.com &nbsp;|&nbsp; 💼 [linkedin.com/in/shreelakshmidm](https://www.linkedin.com/in/shreelakshmidm)

---

## About Me

I am an engineer with a background spanning infrastructure operations, cloud data engineering, and database administration — actively building toward an OpenShift SRE / Platform Engineering role.

At TCS I supported production database environments, monitored systems with Splunk, automated workflows with Bash, and collaborated with DevOps teams on containerised deployments. At InsOps I build and maintain Azure cloud data pipelines for enterprise insurance migration. In parallel I am building production-grade SRE projects using Red Hat OpenShift, Tekton, Prometheus, Grafana, and HashiCorp Vault — the exact tooling used by enterprise engineering teams.

I am open to roles in **OpenShift SRE**, **Platform Engineering**, **DevOps**, and **Data Engineering**.

---

## Technical Skills

| Area | Tools & Technologies |
|---|---|
| **Container & Platform** | Red Hat OpenShift (OCP), Kubernetes, Docker, RBAC, SCCs, PersistentVolumes, StatefulSets |
| **CI/CD** | Tekton Pipelines & Triggers, Harness (concepts), Jenkins, GitLab CI/CD, GitHub Actions |
| **Observability** | Prometheus, PromQL, Grafana, Alertmanager, Splunk, ELK Stack, Datadog, AppDynamics |
| **OpenShift AI** | RHOAI, KServe InferenceService, ModelMesh, Data Science Pipelines, Jupyter on OCP |
| **Cloud & IaC** | Azure (ADF, SQL, Data Lake), AWS (EC2, S3, VPC, IAM, EKS), Terraform, Ansible |
| **Security & Secrets** | HashiCorp Vault (K8s auth + Agent sidecar), CyberArk (concepts), RBAC, OAuth2, AWS KMS |
| **Data Engineering** | Azure Data Factory, PostgreSQL, MSSQL, MySQL, ETL Pipelines, Pentaho PDI, Power Query |
| **Analytics & BI** | Power BI, Tableau, DAX, Star Schema, Data Warehousing |
| **Languages** | Python (pandas, scikit-learn, K8s client), SQL, Bash |
| **SRE** | SLI/SLO/Error Budgets, Incident Response, Postmortem/RCA, Toil Reduction, CAB Governance |

---

## SRE Projects

### Project 1 — OpenShift SRE Operations Platform
`OpenShift` `Prometheus` `Grafana` `Alertmanager` `HashiCorp Vault` `RHOAI` `KServe` `Python` `Docker`

**Status: Completed 2025 &nbsp;|&nbsp; Cost: $0 — 100% open source**

A production-grade SRE platform built on Red Hat OpenShift demonstrating the full reliability engineering lifecycle — deployment, monitoring, alerting, secret management, AI model serving, and incident response.

**What I built:**
- Deployed a Python Flask microservice on Red Hat OpenShift with RBAC, custom SCCs, resource limits, liveness/readiness probes, and a TLS-terminated Route
- Configured HashiCorp Vault Agent sidecar using Kubernetes auth method for secret injection — zero hardcoded credentials anywhere
- Instrumented the app with Prometheus metrics (Counter, Histogram, Gauge) and deployed Prometheus with ServiceMonitor CRD for automatic scraping
- Built a 6-panel Grafana dashboard — request rate, error rate, p50/p95/p99 latency, pod restarts, CPU, memory
- Defined 3 SLOs (availability 99.9%, p99 latency < 2s, error rate < 0.1%) with PromQL and configured Alertmanager rules
- Deployed a scikit-learn model as a KServe InferenceService on Red Hat OpenShift AI (RHOAI)
- Simulated an OOMKill incident, triaged via Grafana, resolved, and wrote a complete postmortem with RCA

**Repository structure:**
```
app/            ← Flask app with Prometheus metrics + non-root Dockerfile
openshift/      ← Deployment, Service, Route YAML manifests
monitoring/     ← Prometheus config, Grafana dashboard JSON, alert rules
postmortem/     ← Full incident postmortem document
```

---

### Project 2 — Tekton CI/CD Pipeline on OpenShift
`Tekton Pipelines` `Tekton Triggers` `Trivy` `Buildah` `Quay.io` `OpenShift` `GitHub webhooks`

**Status: In Progress — 2025 &nbsp;|&nbsp; Cost: $0 — 100% open source**

A Kubernetes-native CI/CD pipeline built with Tekton — demonstrating automated build, security scanning, and deployment triggered automatically on every GitHub push.

**What I am building:**
- 4-stage Tekton Pipeline: git-clone → Trivy security scan (blocks on critical CVEs) → Buildah build/push → OpenShift rolling deploy
- Tekton Triggers with EventListener, TriggerBinding, TriggerTemplate — git push fires pipeline automatically
- Security gate: pipeline fails if any CRITICAL CVE found in the container image
- Final Task deploys KServe InferenceService on RHOAI — complete MLOps flow from commit to production model serving

---

## Data Engineering & Analytics Projects

### Data Integration & ETL Pipeline — Pentaho PDI
`Pentaho PDI` `PostgreSQL` `ETL` `SQL` `Data Warehousing`

- Orchestrated ETL consolidating sales data from 5 sources, processing 100K+ records with 95% data quality score
- Applied validation rules, type enforcement, and deduplication delivering clean tables into a centralised PostgreSQL data warehouse
- Implemented data validation rules catching 500+ quality issues before downstream processing

---

### Business Intelligence & Streaming Analytics — Power BI
`Power BI` `DAX` `Power Query` `Star Schema` `Time Intelligence`

- Built dashboards with DAX measures for Total Views, Hours Watched, Avg Completion %, Avg Rating, and Genre Share
- Authored time-intelligence measures (YoY/QoQ/MTD via DATEADD) with drill-through from Region → Genre → Title
- Applied Row Level Security (RLS) by Region and Language for stakeholder-specific data access

---

## Work Experience

### Data Engineer Intern — InsOps Inc
**Apr 2025 – Present &nbsp;|&nbsp; United States**
`Azure ADF` `Azure SQL` `Data Lake` `Python` `SQL` `Guidewire`

- Build and maintain Azure cloud data pipelines (ADF, Azure SQL, Data Lake Storage) for insurance data migration, achieving 99%+ data accuracy across structured and unstructured sources
- Support on-prem to Azure cloud migration of Guidewire systems (ClaimCenter, PolicyCenter, BillingCenter), contributing to infrastructure reliability and deployment validation
- Collaborate on CI/CD-adjacent workflows: pipeline configuration, environment validation, and DevOps backlog items within an Agile team
- Write Python and SQL transformation scripts to validate and reconcile insurance data across cloud and on-prem systems

---

### Associate System Engineer — Database Administrator — Tata Consultancy Services
**Dec 2021 – Jan 2024 &nbsp;|&nbsp; Bengaluru, India**
`MSSQL` `MySQL` `Splunk` `Bash` `Kubernetes (exposure)` `ServiceNow`

- Administered MSSQL and MySQL production environments ensuring high availability, SLA compliance, performance tuning, and backup/restore integrity for enterprise clients
- Monitored database health, resource utilisation, and service account activity daily using Splunk; performed RCA for failures, resource contention, and service disruptions
- Managed RBAC-based access controls enforcing least-privilege; collaborated with DevOps teams on containerised deployments with Kubernetes namespace and pod management exposure
- Automated health checks, log rotation, and patching via Bash scripting; executed OS patching with CAB-aligned rollback planning and post-implementation verification

---

### Machine Learning Intern — Verzeo
**Jul 2020 – Sep 2020 &nbsp;|&nbsp; India**
`Python` `pandas` `scikit-learn`

- Built supervised ML pipelines — data cleaning, feature engineering, K-fold CV, model evaluation (F1, ROC-AUC, MAE/MSE) with stakeholder visualisations

---

## Education

| Degree | Institution | GPA | Year |
|---|---|---|---|
| MS, Information Technology & Management | Illinois Institute of Technology, Chicago | 3.7 / 4.0 | Jan 2024 – Dec 2025 |
| BE, Computer Science | M S Ramaiah Institute of Technology | 3.5 / 4.0 | Aug 2018 – Sep 2021 |

---

## Connect

- 📧 [shreelakshmidm18@gmail.com](mailto:shreelakshmidm18@gmail.com)
- 💼 [linkedin.com/in/shreelakshmidm](https://www.linkedin.com/in/shreelakshmidm)
- 🐙 [github.com/Shreelakshmi535](https://github.com/Shreelakshmi535)
