# Real-Time Data Streaming and Processing with Azure Functions & Fabric Real-Time Intelligence Framework

This project demonstrates a real-time streaming architecture using **Azure Functions**, **Event Hubs**, **Fabric Real-Time Intelligence Framework**, and **Power BI**. The system fetches data from an external website via an API, processes the data in real time, and presents valuable insights using Power BI. Additionally, an **alert mechanism** is set up to notify users of critical events via email using **Data Activator**.

## Architecture Overview

### Components Involved

1. **API Integration**:
   - Fetches data from an external website via a RESTful API.

2. **Azure Functions**:
   - Serverless compute service used to fetch and process data from the API and push it to **Azure Event Hubs**.

3. **Azure Event Hubs**:
   - A high-throughput data streaming platform that ingests and buffers real-time data for further processing.

4. **Fabric Real-Time Intelligence Framework**:
   - Processes event streams from Event Hubs and loads them into **Azure Event House (Kusto DB)** for further analysis.

5. **Kusto DB (Event House)**:
   - A highly scalable, distributed data store used for storing time-series data.

6. **Power BI**:
   - Provides real-time data visualization and insights by connecting to Kusto DB.

7. **Data Activator**:
   - A service that triggers custom alerts based on specific conditions in the incoming data, sending email notifications when certain events occur.

8. **Azure Key Vault**:
   - Securely manages and stores sensitive data such as API keys and connection strings.

---

## Project Workflow

1. **Data Fetching**:
   - **Azure Functions** are scheduled to periodically fetch data from an external API.

2. **Data Pushing to Event Hubs**:
   - Once the data is fetched, it is processed within **Azure Functions** and pushed into **Azure Event Hubs**.

3. **Data Processing in Fabric Real-Time Intelligence Framework**:
   - **Fabric Real-Time Intelligence Framework** processes the event streams from Event Hubs, performing any necessary transformations or computations.

4. **Storing Data in Kusto DB**:
   - Processed event data is stored in **Kusto DB (Event House)**, which serves as the long-term data store.

5. **Real-Time Insights with Power BI**:
   - **Power BI** is connected to **Kusto DB** to provide real-time data visualization and insights.

6. **Alerting with Data Activator**:
   - Custom alerts are configured using **Data Activator**, triggering email notifications based on predefined conditions in the data.

---

## Security Management

### Key Vault Integration

- **Azure Key Vault** is used for securely managing sensitive information like API keys, Event Hub connection strings, and other credentials.
  
- **Managed Identity** for **Azure Functions** is enabled, ensuring that the function can securely authenticate and access **Key Vault** without storing sensitive data in the codebase.

---

## Cost Management: Databricks vs Azure Functions

**Cost Decision**:
- **Azure Functions** is ideal for this project due to its serverless nature, scalability, and cost-effectiveness for real-time data streaming workloads.
- **Azure Databricks** is more suitable for large-scale, complex data processing but may incur higher costs.

---

## Cost Management Strategy

- Use **Azure Functions** for data fetching and processing, as it is cost-effective and scalable for real-time streaming workloads.
- **Azure Event Hubs** will manage the ingestion and buffering of data streams.
- **Kusto DB (Event House)** will serve as the data store optimized for time-series data.
- **Power BI** will provide real-time insights and dashboards.
- For security, **Azure Key Vault** will handle all sensitive credentials.

---

## Technologies Used

- **Azure Functions**
- **Azure Event Hubs**
- **Fabric Real-Time Intelligence Framework**
- **Kusto DB (Event House)**
- **Power BI**
- **Data Activator**
- **Azure Key Vault**
- **API Integration (RESTful)**
  
---

## Conclusion

This project provides a scalable, secure, and cost-efficient solution for real-time data streaming and processing. By leveraging Azure services such as **Azure Functions**, **Event Hubs**, and **Kusto DB**, along with real-time insights through **Power BI**, organizations can make data-driven decisions quickly. The integrated alerting mechanism using **Data Activator** ensures critical events are immediately flagged, keeping stakeholders informed.

---


# System Architecture

![image](https://github.com/user-attachments/assets/5e4ffaab-926a-433d-91cc-fa4b19dbefc3)

---





