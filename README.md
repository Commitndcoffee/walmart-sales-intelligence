# **Strategic Sales Intelligence: Walmart Retail Performance Framework**

**Executive Summary**
This repository hosts a high-level retail analytics framework built on **SQL**. The project transitions raw transactional data into a suite of business intelligence tools designed to monitor branch performance, identify customer spending tiers, and detect operational anomalies. By implementing advanced database logic, the system provides a scalable solution for multi-branch retail optimization.

---

## **Technical Walkthrough**
**[Watch the Analytical Deep-Dive]** — [https://drive.google.com/file/d/1QisQX4ZImKkhRPju4UHOliqKd5vtLTvM/view?usp=sharing](https://drive.google.com/file/d/1QisQX4ZImKkhRPju4UHOliqKd5vtLTvM/view?usp=sharing)

---

## **Pillar I: Data Architecture & Infrastructure**

The first layer of the project focuses on building a reliable **MySQL** environment to handle multi-dimensional retail data.

* **Schema Design:** Transactions are mapped across branches (A, B, C) with integrated tracking for product lines, customer demographics, and payment methods.
* **Data Sculpting:** Raw date strings were programmatically converted into standardized SQL date formats to enable time-series analysis and month-over-month growth tracking.

---

[Data Schema and Table Preview]<img width="1439" height="671" alt="image" src="https://github.com/user-attachments/assets/94bfb45f-2a0d-4657-a427-51c971f184fb" />


---

## **Pillar II: Advanced Analytical Logic**

Beyond basic querying, this framework utilizes **Complex SQL Architectures** to extract non-obvious patterns in retail behavior.

* **Inferential Anomaly Detection:** Utilized **Common Table Expressions (CTEs)** and **Statistical Standard Deviation** to calculate **Z-Scores** for every transaction. This allows the system to flag "Anomalies"—sales that deviate significantly from the mean for specific product lines.
* **Temporal Logic:** Employed **Window Functions (`LAG`)** to track repeat purchase behavior. By calculating the `DATEDIFF` between consecutive visits, the system identifies the "Retention Rate" of specific customer IDs within 30-day windows.

---

[Advanced SQL Logic and Z-Score Results]<img width="773" height="554" alt="image" src="https://github.com/user-attachments/assets/21b82f28-a705-41bd-aa89-97007b01d3f0" />


---

## **Pillar III: Strategic Customer Segmentation**

A core feature of this intelligence stack is the **Automated Segmentation Engine**, which categorizes the customer base into actionable tiers based on financial contribution.

* **Tiered Spender Model:** Using `CASE` logic, customers are partitioned into **High**, **Medium**, and **Low** spenders. This enables targeted marketing—focusing high-reward loyalty programs on the "High" tier (Revenue > 22,000) while optimizing acquisition for the "Low" tier.
* **Performance Benchmarking:** Sales growth rates are calculated per branch to identify which locations are scaling and which require inventory intervention.

---

[Customer Segmentation Results]<img width="513" height="529" alt="image" src="https://github.com/user-attachments/assets/0bc9f046-12d1-4cd4-bb27-7d0e200e9211" />


---

## **Business Intelligence Matrix & Strategic Results**

The following matrix summarizes the core analytical outputs, correlating technical SQL methodology with direct business applications.

| Analysis Category | Technical Method | Key Business Finding |
| :--- | :--- | :--- |
| **Peak Demand** | `DAYNAME` & `SUM` Grouping | **Sunday** is the highest revenue-generating day, indicating a surge in weekend consumer activity. |
| **Customer Affinity** | `RANK()` Over `Customer type` | Members prioritize **Health & Beauty**, while Normal customers drive **Electronic Accessory** sales. |
| **Regional Payments** | `COUNT` & `DENSE_RANK()` | **E-wallet** usage is dominant in Naypyitaw, whereas Mandalay demonstrates a preference for **Cash**. |
| **Inventory Logic** | `SUM(cogs)` by Branch | **Branch C** leads in profit for **Food & Beverage**, signaling a geographic advantage for perishables. |

---

[Transactional Trends Table]<img width="506" height="493" alt="image" src="https://github.com/user-attachments/assets/1a693e6b-de77-465c-8c00-fec2fc1b19f4" />


*Caption: The query result above (Task 10) highlights transactional volume and average revenue per day, providing a blueprint for data-driven inventory cycles.*

---

## **Technical Repository Map**

* **`sql/`**: Contains the **`analytical_queries.sql`** script featuring Window Functions, CTEs, and Z-Score logic.
* **`data/`**: Standardized retail transaction records.
* **`documentation/`**: **`executive_insights.pdf`** detailing the full business case and visualized findings.
* **`requirements.txt`**: Environment specifications for MySQL 8.0.

---

## **Tooling & Technology**
* **Database:** MySQL 8.0
* **Advanced Logic:** CTEs, Window Functions (`RANK`, `LAG`), Z-Score Statistics.
* **Documentation:** MS Excel, Power Query.

---

**This framework demonstrates a dual-competency in database engineering and strategic business analysis, providing a blueprint for data-driven retail growth.**
