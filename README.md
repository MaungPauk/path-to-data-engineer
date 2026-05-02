<p align="center">
  <img width="100%" src="/image/path-to-de.png" alt="Path to Data Engineering: Notes from the Field">
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
- [🐧 Environment Setup](./02_Environment_Setup/linux_for_de.md) - How I built my Linux/Windows lab.
- [ SQL for Data Engineer](./03_SQL_de/README_SQL.md) - Why SQL is essential for Data Engineering
- [🐍 Python for Data Engineer](./04_python_de) - Python for ETL process
- [Git & Github](./05_Git-Github/git_and_github.md) - Version Control
- [Containerization](./06_Containerization/docker_notes.md) - Git & Github
- [🚀 Zoomcamp Progress](./07_Zoomcamp_Labs/) - Weekly lab notes and homework.
- [🛠️ Project Portfolio](./08_Projects/) - End-to-end data applications.

---

<h2 align="center">
    <strong>Phase 1: From Data Analyst to Data Engineer Journey</strong>
</h2>


## **Foundational Skills & Certifications**

I built my foundational data literacy and analytical thinking through two Google Professional Certificates on Coursera:
### Google Data Analytics Professional Certificate
**_Focus_**: Data lifecycle, integrity, and exploratory analysis.
- **Key Skills** : Data Cleaning (SQL/Spreadsheets), Exploratory Data Analysis (EDA), Data Visualization (Tableau), and R Programming.
- **Methodology** : Applied the Ask, Prepare, Process, Analyze, Share, and Act framework to real-world case studies.
- **Learned from here**: [Google Data Analytics Professional Certificate - Coursera](https://www.coursera.org/professional-certificates/google-data-analytics)
- **📌 Notes from** : [Google Data Analytics Professional Certificate](./00_foundations/google_da.md)

### Google Business Intelligence Professional Certificate
**_Focus_**: Moving from analysis to infrastructure and automation. Data warehousing, business intelligence, and data storytelling.
* **Key Skills** : ETL (Extract, Transform, Load) processes, BigQuery for large-scale data warehousing, and Data Modeling (Star/Snowflake schemas).
* **Methodology** : Applied the Ask, Prepare, Process, Analyze, Share, and Act framework to real-world case studies.
* **Learned from here**: [Google Business Intelligence Certificate Course - Coursera](https://www.coursera.org/professional-certificates/google-business-intelligence)
* **📌 Notes from** : - [Google Business Intelligence Certificate Course](./00_foundations/google_bi.md)

---

## Why the Shift? From Analytics to Engineering 

Through my **Google Data Analytics and Business Intelligence** certifications, I learned how to turn raw data into insights. However, I noticed a recurring challenge: Insights are only as good as the pipelines that deliver them.

## 🛠️ Technical Foundation: The DE Toolkit

Before transitioning into advanced orchestration, I solidified these core competencies through the **Google Data Analytics** and **Business Intelligence Professional Certificates** and independent lab work.

  ### 🖥️ Systems & Environment
  - **Linux for Windows Users (WSL2**): Mastered the transition from GUI to Command Line (CLI). Proficient in Bash navigation, file system permissions, and managing local development environments.
    * Learning Note -> [**Linux for Data Engineering**](./02_Environment_Setup/linux_for_de.md)
  - **Operating Systems**: Comfortable managing workflows across both Windows and Linux to ensure production-ready script execution.
  - **IDE**: There are many IDE for code editing tools such as Virtual Studio Code (VS Code), Jetbrain, Sublinetxt, Cursor, Antigravity, etc.
    * Learning Note -> [**VS Code and Extensions Setup**](./02_Environment_Setup/vscode_extensions.md)

  ### 🐍 Data Programming & Querying
  - **Structured Query Language (SQL)**: Proficient in relational database design, complex joins, and data transformation within **PostgreSQL** and **BigQuery**.
  - **Python for Automation**: Utilizing Python for more than just analysis—focusing on script modularity, API data extraction, and automating repetitive ETL tasks.

  ### ☁️ Cloud & Architecture
  - **Google Cloud Platform (GCP)**: Foundational experience with Cloud Storage, BigQuery for data warehousing, and utilizing Google Cloud Shell for remote script execution.
  - **Pipeline Architecture**: Understanding the core flow of data from **Source → Stage → Warehouse**, with a focus on data integrity and schema design (Star/Snowflake).

---


<h2 align="center">
    <strong>Phase 2: Learning for Data Engineering</strong>
</h2>


## 📚 Data Engineering Foundations & Theories

Before writing a single line of code, I invested time into understanding the architectural principles of Data Engineering. I believe that a strong grasp of the "Why" and "How" is what separates a Coder from an Engineer.

Coding is the *tool*; Concepts and Theories are the *blueprint*. A theoretical framework allows me to avoid
coding errors, ensure scalability, and align code with business goals. If I don't understand the concepts, the
system I built is hard to maintain or misaligned with the business reality.

> *"Being a good data engineer has very little to do with 'how good you write code.' It is about using your experience to make good decisions regarding architecture and data models."*  — **Daniel Beach**, *Introduction to Data Engineering*

### **📌 Notes**
I have taken notes about: [**Data Engineering Core Concepts and Theories**](./01_Theory_and_Concepts/de_core_concepts_and_theories.md)

---

## Learning Skills
As analysis of essential skills for data engineering, the following skills is needed to master:
1.  Linux & Bash
2.  SQL and Database
3.  Python
4.  Version Control (Git & Github)
5.  Containerzations (Docker)
6.  Data Warehousing
7.  Pipelines (ETL, ELT)
8.  GCP, AWS, Azure
9.  Orchestration & Transformation (Airflow, dbt, Terraform, Pyspark, Kafka) 

---

## SQL for Data Engineering

At the core of Data Engineering lies [**SQL**](./03_SQL_de/README_SQL.md). While it is often seen as the standard for querying, it is not merely a syntax tool; it is the universal lingua franca for managing, analyzing, and storing relational data
across a cloud or distributed environment.

SQL is the backbone of Data Engineering. It handles data extraction, querying, and optimization across the modern
stack. Without it, pipelines fail, models drift, and performance degrades. It is the cornerstone of scalable data
architectures and ensures long-term maintainability.

Ultimately, the mission of SQL is to bridge the gap between the Data Engineer's raw data and business value,
ensuring the engineering process is transparent, reproducible, and aligned with data quality goals.

### **📌 Notes**

Here is my notes about: [**Why SQL is essential for Data Engineering**](./03_SQL_de/README_SQL.md)

---


## Python Programming for Data Engineering

Python stands as a cornerstone in data engineering due to its unparalleled versatility, robust ecosystem, and seamless integration with diverse tools and technologies. 
Here are 5 essential points of Python usage:
- Python streamlines data processing, analysis, and automation with robust tools.
- It enhances scalability, enabling efficient handling of large datasets.
- Versatile libraries integrate seamlessly with databases and APIs.
- Essential for machine learning, supporting model development and deployment.
- Offers flexibility, adapting to diverse data engineering challenges effectively.

### **📌 Notes**
Here is my notes about: [**Python for Data Engineering**](./04_python_de/python_essentials_for_data_engineering.md)

---

## Version Control (Git & Github)
Git and GitHub are foundational to data engineering, providing robust version control, collaboration tools, and change management essential for handling complex workflows. They facilitate branching for feature development, enabling teams to isolate updates, share progress, and resolve conflicts swiftly. Centralized repositories ensure secure storage and accessibility, while backups safeguard against data loss. This infrastructure supports scalable teamwork, maintaining clarity and reproducibility. Transparent history tracking enhances accountability, streamlines communication, and adapts to evolving needs. Their role in ensuring reliability, scalability, and precision underpins successful data projects, making them indispensable for modern engineering practices. The synergy between version control, collaboration, and integrity forms the backbone of efficient, adaptive data management, ensuring precision and trust in dynamic environments.

What Git can help me:
* Git manages version control for code tracking.
* GitHub hosts repositories for collaboration.
* Supports branching and merging efficiently.
* Offers security and access management.
* Facilitates project coordination and deployment.

### **📌 Notes**
Here is my notes about: [**Git and Github**](./05_Git-Github/git_and_github.md)

---


<h2 align="center">
    <strong>Phase 3: Applied Engineering (The DataTalks.Club Zoomcamp)</strong>
</h2>

Having solidified my theoretical foundations, I am currently transitioning to the **Applied** phase of my journey. I am enrolled in the [DataTalks.Club Data Engineering Zoomcamp](https://datatalks.club/blog/data-engineering-zoomcamp.html), a project-based course focused on the **Modern Data Stack**.

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

### **📌 Notes**
Here is all of my notes from: [**DataTalk Zoomcamp**](./07_Zoomcamp_Labs/datatalk_zoomcamp_notes.md)

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
