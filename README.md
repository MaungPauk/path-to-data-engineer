<p align="center">
  <img width="100%" src="/image.path-to-de.png" alt="Path to Data Engineering: Notes from the Field">
</p>

<h1 align="center">
    <strong>Path to Data Engineering: Notes from the Field</strong>
</h1>
<h3 align="center">
    <i>____by Maung Pauk</i>
</h3>

<p align="center">
Documenting a transition to Data Engineering: From core SQL & Python foundations to production-grade pipelines. Currently deep-diving into the DataTalksClub Zoomcamp—sharing lab notes, environment setups, and the road ahead. Built for beginners, by a beginner.
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/maungpauk/">
    <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn">
  </a>
</p>


## 🗺️ Navigation
- [📚 Theory & Concepts](./01_Theory_and_Concepts/de_core_concepts_and_theories.md) - The "Why" before the "How."
- [🐧 Environment Setup](./02_Environment_Setup/wsl2_docker_config.md) - How I built my Linux/Windows lab.
- [🚀 Zoomcamp Progress](./03_Zoomcamp_Labs/) - Weekly lab notes and homework.
- [🛠️ Project Portfolio](./04_Projects/) - End-to-end data applications.

---

# 🚀 Phase 1: From Data Analyst to Data Engineer Journey

## 🏗️ Foundational Skills & Certifications

I built my foundational data literacy and analytical thinking through two Google Professional Certificates on Coursera:
### 🎓 Google Data Analytics Professional Certificate
**_Focus_**: Data lifecycle, integrity, and exploratory analysis.
- **Key Skills** : Data Cleaning (SQL/Spreadsheets), Exploratory Data Analysis (EDA), Data Visualization (Tableau), and R Programming.
- **Methodology** : Applied the Ask, Prepare, Process, Analyze, Share, and Act framework to real-world case studies.
- **Learned from here**: [Google Data Analytics Professional Certificate - Coursera](https://www.coursera.org/professional-certificates/google-data-analytics)
- **Notes from** : [Google Data Analytics Professional Certificate](./00_foundations/google_da.md)

### 🎓 Google Business Intelligence Professional Certificate
**_Focus_**: Moving from analysis to infrastructure and automation. Data warehousing, business intelligence, and data storytelling.
- **Key Skills** : ETL (Extract, Transform, Load) processes, BigQuery for large-scale data warehousing, and Data Modeling (Star/Snowflake schemas).
- **Methodology** : Applied the Ask, Prepare, Process, Analyze, Share, and Act framework to real-world case studies.
- **Learned from here**: [Google Business Intelligence Certificate Course - Coursera](https://www.coursera.org/professional-certificates/google-business-intelligence)
- **Notes from** : - **Notes from** : [Google Business Intelligence Certificate Course](./00_foundations/google_bi.md)
---

## 🛠️ Why the Shift? From Analytics to Engineering 

Through my **Google Data Analytics and Business Intelligence** certifications, I learned how to turn raw data into insights. However, I noticed a recurring challenge: Insights are only as good as the pipelines that deliver them.

---

## 🛠️ Technical Foundation: The DE Toolkit

Before transitioning into advanced orchestration, I solidified these core competencies through the **Google Data Analytics** and **Business Intelligence Professional Certificates** and independent lab work.

### 🖥️ Systems & Environment
- **Linux for Windows Users (WSL2**): Mastered the transition from GUI to Command Line (CLI). Proficient in Bash navigation, file system permissions, and managing local development environments.
- **Operating Systems**: Comfortable managing workflows across both Windows and Linux to ensure production-ready script execution.

### 🐍 Data Programming & Querying
- **Structured Query Language (SQL)**: Proficient in relational database design, complex joins, and data transformation within **PostgreSQL** and **BigQuery**.
- **Python for Automation**: Utilizing Python for more than just analysis—focusing on script modularity, API data extraction, and automating repetitive ETL tasks.

### ☁️ Cloud & Architecture
- **Google Cloud Platform (GCP)**: Foundational experience with Cloud Storage, BigQuery for data warehousing, and utilizing Google Cloud Shell for remote script execution.
- **Pipeline Architecture**: Understanding the core flow of data from **Source → Stage → Warehouse**, with a focus on data integrity and schema design (Star/Snowflake).
---

## 📚 Engineering Foundations & Theories

Before writing a single line of code, I invested time into understanding the architectural principles of Data Engineering. I believe that a strong grasp of the "Why" and "How" is what separates a Coder from an Engineer.

My theoretical foundation is built upon industry-standard resources, most notably:
1. [Introduction to Data Engineering](http://leanpub.com/dataengineeringwithpython) (Daniel Beach)
2. [Fundamentals of Data Engineering](http://oreilly.com/) (Joe Reis & Matt Housley)

### Core Concepts & Theories of Data Engineering

This note summarizes the foundational principles derived from *Fundamentals of Data Engineering* (Reis & Housley) and *Introduction to Data Engineering* (Beach). Understanding these theories is the first step toward building professional-grade data systems.

---

### 1. The Data Engineering Lifecycle
The "Lifecycle" is the most important framework in the field. It moves the focus away from specific tools and onto the evolution of data.

---

### 2. The "Undercurrents"
These are the constant responsibilities that a Data Engineer must manage across every stage of the lifecycle:

* **Security & Privacy:** Protecting data at rest and in transit.
* **Data Management:** Ensuring data quality, governance, and master data management.
* **DataOps:** Applying DevOps to data (Automation, Testing, and CI/CD).
* **Data Architecture:** Designing the overall blueprint of the data system.
* **Orchestration:** Coordinating the timing and dependencies of pipeline tasks.

---

### 3. Storage & Processing Theories

#### OLTP vs. OLAP
* **OLTP (Online Transactional Processing):** Designed for many small, fast transactions (e.g., a banking app). Usually row-based.
* **OLAP (Online Analytical Processing):** Designed for complex queries and large aggregations (e.g., a yearly sales report). Usually columnar.

#### Row-based vs. Columnar Storage
* **Row-based:** Better for looking up specific individual records.
* **Columnar (e.g., Parquet, Avro):** Better for analytical queries. It allows for high compression and "fine-grained seeking," meaning the system only reads the columns it needs.

---

### 4. Data Modeling Concepts
Data modeling is the "half art, half science" stage that can make or break a project.

* **The Grain:** The level of detail represented by a single row in a table.
* **Fact Tables:** Quantitative data (measures/numbers) about business events.
* **Dimension Tables:** Descriptive context (who, what, where) for the facts.
* **Schemas:** * **Star Schema:** A central fact table connected to multiple dimension tables.
    * **Snowflake Schema:** An extension of the Star schema where dimensions are further normalized.

---

### 5. Engineering Principles for Pipelines
A professional pipeline is more than just code; it must be:

1.  **Idempotent:** Running the process multiple times should produce the same result as running it once. This is critical for recovering from errors.
2.  **Repeatable:** The code should work exactly the same in any environment (Local, Dev, or Production).
3.  **Resilient:** The system should handle failures (like a missing file or a network timeout) without crashing.
4.  **Scalable:** The architecture should handle 1GB of data as efficiently as it handles 1TB.

---

> *"Being a good data engineer has very little to do with 'how good you write code.' It is about using your experience to make good decisions regarding architecture and data models."* > — **Daniel Beach**, *Introduction to Data Engineering*

---
# 🚀 Phase 3: SQL for Data Engineering

At the core of Data Engineering lies **SQL**. While it is often seen as the standard for querying, it is not
merely a syntax tool; it is the universal lingua franca for managing, analyzing, and storing relational data
across a cloud or distributed environment.

## 🎯 The Mission
The goal of this "Field Lab" is to move away from local scripts and build a fully automated, production-grade data pipeline in the cloud.
---
# 🚀 Phase 4: Python Programming for Data Engineering

Having solidified my theoretical foundations, I am currently transitioning to the **Applied** phase of my journey. I am enrolled in the [DataTalks.Club Data Engineering Zoomcamp](https://datatalks.club/blog/data-engineering-zoomcamp.html), a project-based course focused on the **Modern Data Stack**.

## 🎯 The Mission
The goal of this "Field Lab" is to move away from local scripts and build a fully automated, production-grade data pipeline in the cloud.
---

# 🚀 Phase 5: Applied Engineering (The DataTalks.Club Zoomcamp)

Having solidified my theoretical foundations, I am currently transitioning to the **Applied** phase of my journey. I am enrolled in the [DataTalks.Club Data Engineering Zoomcamp](https://datatalks.club/blog/data-engineering-zoomcamp.html), a project-based course focused on the **Modern Data Stack**.

## 🎯 The Mission
The goal of this "Field Lab" is to move away from local scripts and build a fully automated, production-grade data pipeline in the cloud.

---

## 🛠️ The Production Stack
In this phase, I am getting hands-on experience with the following industry-standard tools:

### 1. Infrastructure & Containerization
* **Docker & Docker-Compose:** Creating reproducible environments so that "it works on my machine" means it works everywhere.
* **Terraform:** Managing Infrastructure as Code (IaC) to automatically provision Google Cloud Platform (GCP) resources.

### 2. Workflow Orchestration
* **Kestra / Mage / Airflow:** Managing the "Data Traffic Control." Learning to schedule, monitor, and troubleshoot complex DAGs (Directed Acyclic Graphs).

### 3. Data Warehousing & Transformation
* **BigQuery:** Utilizing a serverless data warehouse to store and query massive datasets efficiently using partitioning and clustering.
* **dbt (data build tool):** Applying software engineering best practices (version control, testing, documentation) to SQL transformations.

### 4. Processing at Scale
* **Apache Spark:** Processing large-scale data using distributed computing (Batch processing).
* **Apache Kafka:** Handling real-time data streams for low-latency systems.

---

## 📂 My "Notes from the Field" Strategy
To ensure these skills stick, I am documenting specific "Field Notes" for each module:

* **Lab Setup:** Configuring WSL2 and Docker to communicate with Google Cloud.
* **Troubleshooting:** A log of "Red Errors" and how I fixed them (e.g., Python library conflicts or Terraform permission issues).
* **The Capstone:** I am building a final end-to-end project that integrates all these tools into a single automated pipeline.

---

## 📈 Progression Tracker
| Week | Topic | Status |
| :--- | :--- | :--- |
| 1 | Containerization & Infrastructure (Docker, Terraform) | 🟡 Inprogress |
| 2 | Workflow Orchestration (Kestra) | 📅 Upcoming |
| 3 | Data Warehousing (BigQuery) | 📅 Upcoming |
| 4 | Analytics Engineering (dbt) | 📅 Upcoming |
| 5 | Batch Processing (Spark) | 📅 Upcoming |
| 6 | Streaming (Kafka) | 📅 Upcoming |

---
*Follow my journey as I build my way toward becoming a Data Engineer.*

---

### **📚 Resources**
- [Course Videos](https://www.youtube.com/playlist?list=PL3MmuxUbc_hJed7dXYoJw8DoCuVHhGEQb)
- [Course Homework](https://github.com/DataTalksClub/data-engineering-zoomcamp/tree/main/cohorts/2026)

---

### **📌 Notes**
- **Week 1:** I struggled with setting up Docker and Terraform on WSL2. I had to troubleshoot permission issues and ensure Docker was properly

### My Directory Structure

├── 00_Foundations/           # Google Certs, Basic SQL, Python, & Linux
│   ├── google_analytics.md
│   ├── linux_for_de.md
│   └── basic_sql_labs/
├── 01_Theory_and_Concepts/    # Notes from the two books you read
│   ├── de_lifecycle.md
│   └── storage_theories.md
├── 02_Environment_Setup/      # The "Field Notes" on your hardware/WSL
│   ├── wsl2_docker_config.md
│   └── vs_code_extensions.md
├── 03_Zoomcamp_Labs/          # Weekly progress from DataTalksClub
│   ├── week_1_docker_terraform/
│   ├── week_2_orchestration/
│   └── homework_solutions/
├── 04_Projects/               # Independent projects (like TRON Predictor)
│   └── tron_analysis/
├── images/                    # Screenshots of your dashboards/terminal
├── .gitignore
└── README.md                  # The "Dashboard" of your journey