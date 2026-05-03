<h1 align="center">
    <strong>Core Concepts and Theories of Data Engineering</strong>
</h1>
<h3 align="center">
    <i>____by Maung Pauk</i>
</h3>


My theoretical foundation is built upon industry-standard resources, most notably:
1. [Introduction to Data Engineering](http://leanpub.com/dataengineeringwithpython) (Daniel Beach)
2. [Fundamentals of Data Engineering](http://oreilly.com/) (Joe Reis & Matt Housley)

---

## Core Concepts & Theories of Data Engineering

This note summarizes the foundational principles derived from *Fundamentals of Data Engineering* (Reis & Housley) and *Introduction to Data Engineering* (Beach). Understanding these theories is the first step toward building professional-grade data systems.

---

### 1. The Data Engineering Lifecycle
The "Lifecycle" is the most important framework in the field. It moves the focus away from specific tools and onto the evolution of data.


* **Generation:** Data is created in source systems (APIs, IoT, Logs, Transactions).
* **Storage:** Choosing the right "home" for data based on access patterns (Hot vs. Cold storage).
* **Ingestion:** Moving data from the source to the storage layer (Batch or Streaming).
* **Transformation:** Cleaning and structuring data to make it useful.
* **Serving:** Delivering data to end-users (Analysts, Data Scientists, or ML models).

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
# 📘 Course Outline

- **Module 1: Foundations and Building Blocks**
  - Chapter 1: Data Engineering Described
  - Chapter 2: The Data Engineering Lifecycle
  - Chapter 3: Data Architecture
  - Chapter 4: Choosing Technologies
- **Module 2: The Data Engineering Lifecycle in Depth**
  - Chapter 5: Data Generation in Source Systems
  - Chapter 6: Storage
  - Chapter 7: Ingestion
  - Chapter 8: Transformation and Data Modeling
  - Chapter 9: Serving Data for Analytics and ML
- **Module 3: Advanced Topics and Undercurrents**
  - Chapter 10: Security, Privacy, and Data Management
  - Chapter 11: The Future of Data Engineering
  - Appendix: Networking, Serialization, and Compression

---

# 🧠 Chapter Summaries

## Module 1: Foundations and Building Blocks

### Chapter 1: Data Engineering Described
- **Definition:** Data engineering is the development and maintenance of systems that turn raw data into high-quality information for downstream use.
- **Historical Evolution:** Roots in 1980s data warehousing (Inmon/Kimball), moving through the "Big Data" era (Hadoop/MapReduce), to modern cloud-first practices.
- **Core Goal:** To facilitate data movement and enable consumption for analysts and data scientists.
- **The Lifecycle Idea:** Focuses on the stages data travels through: Generation, Storage, Ingestion, Transformation, and Serving.
- **Distinction:** Unlike data science, it focuses on the foundations and infrastructure rather than just the analysis.

### Chapter 2: The Data Engineering Lifecycle
- **Stages:** The lifecycle includes Generation (source), Storage (persistence), Ingestion (movement), Transformation (logic), and Serving (output).
- **Undercurrents:** Critical concepts that apply to every stage: Security, Data Management, DataOps, Data Architecture, Orchestration, and Software Engineering.
- **Theory of Pipelines:** Essential traits include being Repeatable, Resilient, and Scalable.
- **Containerization:** Tools like Docker are highlighted as basics for creating consistent environments.

### Chapter 3: Data Architecture
- **Scope:** Data architecture is a subset of enterprise architecture.
- **Core Focus:** Establishing patterns for how data is organized and managed across the lifecycle.
- **Architecture First:** The text emphasizes designing architecture before picking specific tools.
- **Cost and Value:** Understanding the trade-offs between different architectural patterns and their impact on the business.

### Chapter 4: Choosing Technologies
- **The "Undercurrent" Influence:** Decisions should be driven by the data engineering undercurrents (security, cost, etc.).
- **Build vs. Buy:** Evaluating whether to build custom solutions or use managed services (SaaS/PaaS).
- **Team Skillset:** Technology choices must align with the current team's capabilities and long-term maintenance needs.
- **Future-Proofing:** Avoiding vendor lock-in where possible and choosing modular components.

## Module 2: The Data Engineering Lifecycle in Depth

### Chapter 5: Data Generation in Source Systems
- **The Starting Point:** Understanding how and where data is created, including its "quirks."
- **Types of Systems:** Operational systems like databases (PostgreSQL), IoT devices, and application logs.
- **Timestamps:** Critical to track Event Time (creation), Ingestion Time, and Process Time.
- **Data Quality at Source:** Best practice is to fix issues in the software producing the data whenever possible.

### Chapter 6: Storage
- **SQL vs. NoSQL:** Choosing between relational databases and non-relational files or document stores.
- **Row vs. Columnar:** Transactional systems use row storage; analytical systems prefer columnar storage (like Parquet) for speed.
- **Access Patterns:** Storage choice must be dictated by how the data will be read (e.g., full scans vs. specific lookups).
- **Compression:** Essential for reducing costs and improving performance in data lakes.

### Chapter 7: Ingestion
- **Batch vs. Stream:** Batch is traditional (interval-based); streaming is real-time.
- **Push vs. Pull:** Data is either written to a target (push) or retrieved from a source (pull).
- **CDC:** Change Data Capture allows ingesting only the changes from a source database.
- **Reliability:** Ingestion systems must be durable to ensure no data is lost during transit.

### Chapter 8: Transformation and Data Modeling
- **The "Core" Process:** Transformations sit at the heart of pipelines, turning messy data into useful info.
- **Modeling Techniques:** Includes the Star Schema (Facts and Dimensions) and Normalization.
- **Tools:** Use of SQL, dbt, and Looker for managing complex data flows.
- **Joins:** Integer keys are generally faster for joins than long string hashes.

### Chapter 9: Serving Data for Analytics and ML
- **End Users:** Data is served to analysts, data scientists, and external applications.
- **Serving Layers:** Data warehouses for BI, feature stores for ML, and APIs for application consumption.
- **Latency Requirements:** Understanding whether the user needs data in sub-seconds or daily reports.

## Module 3: Advanced Topics and Undercurrents

### Chapter 10: Security, Privacy, and Data Management
- **Principle of Least Privilege:** Users and systems should only have access to the data they absolutely need.
- **Data Governance:** Ensuring data is discoverable, high-quality, and compliant with regulations.
- **Encryption:** Managing data-at-rest and data-in-transit security.

### Chapter 11: The Future of Data Engineering
- **Trend Toward Automation:** Moving away from manual pipeline builds to automated, metadata-driven architectures.
- **The "Full-Stack" Engineer:** Increasing overlap between data engineering, DevOps, and software engineering.

---

# 🔑 Key Concepts

- **Data Engineering Lifecycle:** The end-to-end process of data generation, storage, ingestion, transformation, and serving.
- **Undercurrents:** Foundation skills like Security, DataOps, and Orchestration that support the lifecycle.
- **ETL (Extract, Transform, Load):** The process of moving data from source systems to a data warehouse.
- **CDC (Change Data Capture):** A technique for tracking and ingesting changes made to a database.
- **Star Schema:** A data modeling pattern featuring a central "Fact" table surrounded by "Dimension" tables.
- **Parquet:** A columnar storage file format optimized for big data and analytics.
- **Orchestration:** The automated coordination and management of complex workflows.
- **SQL (Structured Query Language):** The primary language used for interacting with relational databases.
- **Data Lake:** A storage repository that holds a vast amount of raw data in its native format.
- **Data Warehouse:** A system used for reporting and data analysis, containing integrated data.
- **PostgreSQL:** An open-source relational database often used as a source or storage layer.
- **Docker/Containerization:** Creating consistent, portable environments for code to run.

---

**[↑ Up](/README.md)** | **[← Previous](/README.md)** | **[Next →](./02-linux_setup_for_de.md)**