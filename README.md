
# Distributed Database for Healthcare Industry

## Project Overview

This project involves the design and implementation of a distributed database system that integrates pharmaceutical company, healthcare providers, and regulatory authorities. The system is built on two Google Cloud Platform (GCP) instances, each hosting distinct sets of data relevant to the zone where the instance is located, for example infomation related to drugs and its subsidiary are in US instance zone as they will be accessed frequently in there as the customers are american citizens. Moreover, data related to manufacturing and raw materials is in INDIA instance zone, as the manufacturers are based in India. The distributed architecture ensures secure, efficient, and scalable data management across multiple organizations.

## Architecture

The system architecture is divided into two main GCP instances, each serving specific functions:

-   **GCP Instance 1 (India)**: Hosts data related to pharmaceutical companies, research and development (R&D), raw material suppliers, manufacturing departments, and funding sources.
-   **GCP Instance 2 (USA)**: Manages data related to drugs, wholesale distributors, pharmacies, hospitals, patients, doctors, clinical trials, federal regulators, and test results.

These instances are connected through a Global Data Center (GDC), which serves as the central hub for data integration and retrieval. The GDC interacts with an application layer, allowing users to run SQL queries to access and manipulate data across both GCP instances.

Below is the architecture diagram:
![Distributed Database Architecture](./Architecture_Diagram.jpg)


### Visual Representation

Below is the visual representation of the system architecture:

## Components

### GCP Instance 1

-   **Pharma Company**
-   **R&D Department**
-   **Researchers**
-   **Funding**
-   **Raw Material Supplier**
-   **Manufacturing Department**

### GCP Instance 2

-   **Drug**
-   **Wholesale Distributor**
-   **Pharmacy**
-   **Invoice**
-   **Prescription**
-   **Hospital**
-   **Patient**
-   **Doctor**
-   **Patient Kin**
-   **Inventory**
-   **Notice of Compliance**
-   **Federal Regulator**
-   **New Drug Application**
-   **Clinical Phases**
-   **Test Subjects**
-   **Results**

### Global Data Center (GDC)

The GDC acts as the central repository that integrates data from both GCP instances. It processes SQL queries from the application layer and provides the necessary data to the user.

### Application Layer

The application layer is the user interface that allows users to interact with the distributed database system. Users can execute SQL queries to retrieve and manipulate data from both GCP instances through the GDC.

## Technologies Used

-   **Google Cloud Platform (GCP)**: Cloud infrastructure for hosting the distributed database instances.
-   **SQL**: Query language for data retrieval and manipulation.
-   **Distributed Database Design**: The system is designed using distributed database principles, ensuring data is stored across multiple locations to enhance availability, fault tolerance, and performance.
