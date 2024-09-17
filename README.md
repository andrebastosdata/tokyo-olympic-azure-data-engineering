# Tokyo Olympic Azure Data Engineering

## This project involves building a data pipeline that extracts raw data, applies transformations, and makes it available for visualization.

**Architecture Diagram:**

![image](https://github.com/user-attachments/assets/90580c53-6c01-4457-80c7-9772bae3cd0e)

**Data Flow Overview**
The data pipeline was designed using multiple Azure services to streamline data extraction, transformation, and visualization. Below is a brief description of each step and tool used in the project.

**1. Data Source**
The initial data is sourced from an on-premise SQL Server database.
The raw data contains historical information related to the Tokyo Olympics, including events, athletes, and results.

**2. Azure Data Factory**
Purpose: Data Factory serves as the orchestration engine for the pipeline.
Functionality: It extracts the raw data from the SQL Server, transferring it into the cloud.
Process:
A pipeline was created to retrieve the data and store it in Azure Data Lake Gen2 as raw data. This pipeline includes trigger-based workflows for continuous data synchronization.

**3. Azure Data Lake Gen2 (Raw Data Store)**
Purpose: Azure Data Lake Gen2 is used to store the raw data extracted by Data Factory.
Functionality: It acts as a highly scalable storage solution to hold both structured and unstructured data in the cloud for further processing.
Process: Raw data is written to the Data Lake in its original format, maintaining the integrity of the source data.

**4. Azure Databricks**
Purpose: Databricks is responsible for the transformation of the raw data.
Functionality: This is where data cleaning, filtering, and formatting happen.
Process:
Data from Azure Data Lake Gen2 is loaded into Databricks. Here, various transformations such as normalization, aggregation, and joining tables are performed.
The transformed data is then written back to the Data Lake in a structured format.

**5. Azure Data Lake Gen2 (Transformed Data Store)**
Purpose: The transformed data is stored back into the Data Lake for further analysis.
Functionality: The data here is now in a ready-to-use format and can be queried and analyzed efficiently.
Process: Structured data is now available for subsequent analytics processes in Azure Synapse Analytics.

**6. Azure Synapse Analytics**
Purpose: Synapse Analytics acts as the data warehouse for the project.
Functionality: It enables powerful querying and analytics over the transformed data.
Process: Data from the Azure Data Lake is loaded into Synapse for further analysis. SQL-based queries and other advanced analytical functions are used to generate insights.

**7. Data Visualization (Power BI, Looker Studio, Tableau)**
Purpose: The final step in the pipeline is data visualization, where insights are presented to stakeholders.
Functionality:
Power BI, Looker Studio, and Tableau are integrated with the Azure Synapse Analytics database for real-time reporting and visualization.
Dashboards are created to allow users to explore various statistics and insights related to the Tokyo Olympics.
Conclusion
This project demonstrates the full pipeline for data engineering, utilizing cloud-based tools for ETL (Extract, Transform, Load), data warehousing, and visualization. The final dashboard provides a comprehensive view of the Tokyo Olympics data, enabling data-driven insights and decision-making.
