# Business Data Analysis on Yelp Dataset
## Project Overview

This project provides a comprehensive data analysis of the large-scale **Yelp Dataset**, aiming to uncover key trends and relationships between business attributes, user activity, and overall performance metrics (like star ratings and review counts).

The analysis was executed on the **Databricks Unified Analytics Platform** using **Apache Spark**, allowing for efficient processing and manipulation of the expansive dataset.

### Project Goals

* Identify the characteristics (categories, attributes, location) that correlate with highly-rated businesses.
* Analyze user behavior patterns, including the influence of "elite" status and review history on rating distribution.
* Visualize geographical and temporal trends within the Yelp ecosystem.

---

## Analysis Areas and Notebooks

The project is structured into two dedicated Notebooks, focusing on distinct aspects of the Yelp data:

### 1. `Business_Level_Analysis.ipynb`

This notebook focuses on the business entities and their characteristics.

* **Key Explorations:**
    * Distribution of star ratings across different business categories.
    * Correlation between specific business attributes (e.g., parking, reservations, price range) and average ratings.
    * Geographical density and performance mapping.
    * Analysis of review counts and their relationship to business tenure.

### 2. `User_Level_Analysis.ipynb`

This notebook focuses on the users and their contribution to the platform.

* **Key Explorations:**
    * Profiling of user types based on review count, friend count, and 'elite' status.
    * Investigating the sentiment and rating tendencies of experienced users versus new users.
    * Temporal analysis of user reviewing activity.
    * The influence of user votes (`useful`, `funny`, `cool`) on overall engagement.

---

## Data Source

The analysis utilizes the publicly available **Yelp Dataset**.

* **Dataset Components:** The project typically works with the main JSON files including `business.json`, `checkin.json`, `tip.json`, `user.json`, `review.json`.
---

## Technologies and Environment

This project is a Big Data analysis project and requires a distributed computing environment.

| Category | Tool / Library | Description |
| :--- | :--- | :--- |
| **Platform** | **Databricks** | Unified Analytics Platform for cloud-based development. |
| **Engine** | **Apache Spark (PySpark)** | Core engine for large-scale data processing and ETL. |
| **Language** | Python 3.x | Primary language for analysis. |
| **Libraries** | `pyspark.sql` | Used for distributed data manipulation (ETL). |
| **Libraries** | `pandas`, `numpy` | Used for localized computations and final data aggregation. |
| **Visualization** | `matplotlib`, `seaborn` | Used for generating comprehensive plots and charts. |

---

## Setup and Execution

To reproduce or run this analysis, the code must be executed in a Spark-enabled environment.

### 1. Databricks Workspace (Recommended)

1.  **Clone the Repository:** Import this repository (`https://github.com/anagha0704/Yelp_Data_Analysis.git`) directly into your Databricks Workspace.
2.  **Data Ingestion:** Ensure the Yelp Dataset JSON files are uploaded to DBFS or mounted from your chosen cloud storage. **Note:** You may need to update the file paths within the notebooks (e.g., `dbfs:/FileStore/...`) to match your workspace setup.
3.  **Cluster Configuration:** Attach the imported notebooks to a running Databricks cluster.
4.  **Run:** Execute the cells sequentially in both notebooks.

### 2. Local Execution (Alternative)

Running this project locally requires configuring a local Spark instance (e.g., using `findspark` or `conda` environment). For simple review and minor testing, you can run the notebooks, but data loading and heavy processing steps will likely fail if a full Spark environment is not properly set up.
