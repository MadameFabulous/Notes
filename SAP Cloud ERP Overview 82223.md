# SAP Cloud ERP

![](https://learning.sap.com/service/media/topic/a49a28ad-926f-4fe4-a9cf-6a9dd74da031/S4CP01_27_en-US_media/S4CP01_27_en-US_images/U1_L1_02_S4H_Characterist_001.png)

## SAP S/4HANA Cloud Deployment

- Public (Multi-tenant server)
  
  - Lowest cost, scaleable
  
  - Hinges on reliability

- Private (Private management of server e.g. SAP Datacenter)
  
  - Secure as you make it
  
  - Costly to scale
  
  - Most applicable in sensitive industries

- Hybrid
  
  - Blended use of private datacenters and on-prem
  
  - More scalable than on-prem only
  
  - Security can vary depending on cloud provider still

## Services

- SaaS - Software as a Service
  
  - Software that is scalable (no need for new licenses etc. all inclusive)
  
  - Thin clients and web browsers lower hardware implementation costs across the business
  
  - Upgrades are handled by the vendor
  
  - SAP Offerings
    
    - SAP SuccessFactors (Human Capital Management)
    
    - SAP Fieldglass (Vendor Management System)
    
    - SAP Ariba (B2B Hub)
    
    - SAP Concur (T&E)

- PaaS - Platform as a Service
  
  - A la carte development environment maintained by the vendor
  
  - Services are optional and can be selected for a fee
  
  - SAP Business Technology Platform is the SAP offering

- IaaS - Infrastructure as a Service
  
  - Vendor maintains the computing resources and provisions them to customers who are free to deploy and manage it
  
  - Maintains control over the development environment while outsourcing hardware costs and maintenance
  
  - SAP HANA Enterprise Cloud (HEC) is the SAP product for this vertical
    
    - Integrates with other Cloud Providers
    
    - Bring-your-own-license: Existing SAP customers can bring their existing deployments into the cloud

## SAP S/4HANA Architecture

-  User Interface

- ERP Software

- Analytical Layer

- Database
  
  - In-memory computing engine favors memory on the user's machine for resources
  
  - Column-oriented database (vs row-oriented)

- Core Data Services
  
  - Domain-specific language collection that prepares views
  
  - CDS views are intended to consumed (e.g. by a UI, analytics platform, or other systems)

## SAP Fiori Launchpad

- Cross-platform (Mobile and Desktop)

- User Personalization of their assigned applications

- Role-specific configurations

[SAP Best Practices | SAP Help Portal](https://help.sap.com/docs/SAP_Best_Practices)

## Two-Tier ERP Deployment

### Best practices for Two-Tier ERP

- Functionality Requirements by Subsidiary

- Interdependencies Documented

- Inter-company Transactions Defined Early

- Reporting Considerations and aggregation

![](https://learning.sap.com/service/media/topic/fe99ef3b-60f7-49e4-a782-595ab9aa5dff/S4CP01_27_en-US_media/S4CP01_27_en-US_images/2Tier%20Intro.png)

A single system of record is maintained that is responsible for the higher order functions of the ERP systems. This in turn frees up the Tier 2 ERP deployments for localization and specialized processes.

This also had additional benefits when the business engages in significant M&A Activity or planned divestiture 

![](https://learning.sap.com/service/media/topic/fe99ef3b-60f7-49e4-a782-595ab9aa5dff/S4CP01_27_en-US_media/S4CP01_27_en-US_images/2Tier%20Scenarios.png)

### Headquarter and Subsidiary

- HQ runs a highly customized instance that is tailored to accept the data from the subsidiaries

- Subsidiaries all run SAP Public Cloud and have standardized data architecture

- Customization is pushed to the aggregating ERP system

### Central Services/Shared Services

- Financial System is a separate legal entity

- Similar to HQ and Subsidiary but the business units/sites have autonomy to run whatever system they choose

### Supply Chain Ecosystem

- HQ runs a highly customized instance that is tailored to accept the data from a single cloud instance

- Cloud system is offered to vendors and partners, can be tailored to hyper-automated tasks at low risk to the continuity of the business

## Intelligent Sustainable Enterprise

![](https://learning.sap.com/service/media/topic/c18a0483-3403-497b-85d5-f47264188a09/S4CP01_27_en-US_media/S4CP01_27_en-US_images/Modular%20Portfolio.png)

![](C:\Users\wright\AppData\Roaming\marktext\images\2023-08-22-06-51-35-image.png)



- Lead to Cash - Revenue and CX for Order to Cash

- Design to Operate - Engineering to Manufacturing

- Source to Pay - Spending process management

- Recruit to Retire - Workforce management

### Qualities

- Seamless UX

- Consistent Security & Identity Management (SSO)

- End-to-End Process Blueprints

- Aligned Domain Models
  
  - Standardizes data models
  
  - Synchronizes Master Data across systems (SAP Master Data Integration Service)

- Embedded Intelligence & Analytics

- Coordinated Lifecycle Management

- One Inbox & Workflow Management

### Sustainability Framework

![](https://learning.sap.com/service/media/topic/ce07dbda-de89-4d8b-92e4-8c2c0fb27da9/S4CP01_27_en-US_media/S4CP01_27_en-US_images/U1_L2_iERP_002.png)

### Intelligent Enterprise Suite Qualities

![](https://learning.sap.com/service/media/topic/ce07dbda-de89-4d8b-92e4-8c2c0fb27da9/S4CP01_27_en-US_media/S4CP01_27_en-US_images/suite%20qualities.png)

As enterprises have become increasingly automated they increase the proportion of labor that is delegated to high value tasks

![](https://learning.sap.com/service/media/topic/ce07dbda-de89-4d8b-92e4-8c2c0fb27da9/S4CP01_27_en-US_media/S4CP01_27_en-US_images/U1_L2_iERP_005.png)

### "The Experience Economy"

![](https://learning.sap.com/service/media/topic/ce07dbda-de89-4d8b-92e4-8c2c0fb27da9/S4CP01_27_en-US_media/S4CP01_27_en-US_images/U1_L2_iERP_004.png)

#### X Data

- SAP Qualtrics Experience Management is the SAP product

- Qualitative Research into your services

- Goal of being predictive/proactive

#### O Data

- Classical ERP Systems

- Focus on being intelligence ready

#### Intelligence Data

- Serves to bridge O and X data by offering analytical insights into Customer Experience Events in the context of Operations data

- Marries up the data collection with data usage

#### Intelligent Technologies

- Artificial Intelligence
  
  - SAP Conversational AI allows for the business to maintain tailored chatbots for their users

- Machine Learning

- Robotic Process Automation

- Internet of Things

## SAP GROW & SAP RISE

![](https://learning.sap.com/service/media/topic/c18a0483-3403-497b-85d5-f47264188a09/S4CP01_27_en-US_media/S4CP01_27_en-US_images/Cloud%20ERP%20Product%20Family.png)

#### SAP Grow with SAP S/4HANA Cloud, public edition

![](https://learning.sap.com/service/media/topic/cb2fcdc5-8e07-4ab0-8bf4-75a5139bd81a/S4CP01_27_en-US_media/S4CP01_27_en-US_images/U2_L2_1_PackageOverview_001.png)

Base Customers have access to the basic tools for process automation and reporting

More tailored tools and the ability to customize your deployment is limited to premium users of SAP Cloud, public

Although access to BTP tools is limited, customers get credits proportional to their Annual Contract Value(ACV)
