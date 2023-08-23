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

## Grow - S/4HANA Cloud, public edition

SAP Grow offers a suite of products for midsized enterprises

- Solutions

- Adoption and Acceleration Services
  
  - SAP Activate Methodology
  
  - SAP Cloud ALM
  
  - SAP [Baseline Activation Service]([An Introduction to Baseline Activation Service for SAP S/4HANA Cloud | SAP Blogs](https://blogs.sap.com/2023/03/14/an-introduction-to-baseline-activation-service-for-sap-s-4hana-cloud/))

- Community Support

- Learning Management System



### CPEA Credits

Cloud Platform Enterprise Agreement(CPEA) credits are used to consume BTP services.

Credits have a baseline free value that is meant to allow customers to demo the BTP without commitment. Additional Credits can be purchased(Imagine that, they want your money!). Credits allow for demo usage of the BTP services without a firmed license.

CPEA Licensing is a commitment to buy the credits for the duration of the contract. There's an annual commitment contract for the BTP services

![](https://learning.sap.com/service/media/topic/cb2fcdc5-8e07-4ab0-8bf4-75a5139bd81a/S4CP01_27_en-US_media/S4CP01_27_en-US_images/U2_L2_1_PackageOverview_003.png) 

Private Edition CPEA Credit Usage

- CPEA Credits for Private Edition customers can be used on SAP Build

- CPEA Credits can be used on other SAP Products like [Signavio]([SAP Signavio | The Only All-in-One Business Process Software](https://www.signavio.com/))

## SAP BTP Build

![](https://learning.sap.com/service/media/topic/dedd2f9b-886a-4021-8809-65ffcc3c6c8d/S4CP01_27_en-US_media/S4CP01_27_en-US_images/U2_L2_2_BTP_002.png)

Low-code solution that allows for extension and automation of S/4HANA

### [SAP Build Apps]([SAP Build Apps | AppGyver | Visual Low-Code App Builder](https://www.sap.com/products/technology-platform/low-code-app-builder.html))

No-code solution with drag-and-drop development. Built out from SAP AppGyver and other SAP technologies.

### [Build Process Automation]([Business Process Automation Software | Low Code | SAP](https://www.sap.com/products/technology-platform/process-automation.html))

Workflow management platform that works with integrated RPA tools in S4/HANA. There's also some AI in here for good measure because it's 2023 after all.

### [SAP Build Work Zone | Digital Workplace Experience](https://www.sap.com/products/technology-platform/workzone.html)

Formerly SAP Launchpad service, Provides the tools for a traditional development environment.

### [SAP Mobile Start App]([SAP Mobile Start | SAP Community](https://community.sap.com/topics/mobile-experience/start))

Mobile platform targeted at iOS and Android devices. Integrates with SAP Task Center for SAP Workflow tasks. This replaces the Fiori Client for Mobile. 

### [SAP Baseline Activation Service]([An Introduction to Baseline Activation Service for SAP S/4HANA Cloud | SAP Blogs](https://blogs.sap.com/2023/03/14/an-introduction-to-baseline-activation-service-for-sap-s-4hana-cloud/))

![](https://learning.sap.com/service/media/topic/ae3a7b5e-b65b-4db6-af00-48ed4d831bd9/S4CP01_27_en-US_media/S4CP01_27_en-US_images/U2_L2_3_BaselineActivation_001.png)

Instanced deployments of SAP meant to help customers align on best practices. These environments can be configured and populated with sample data from existing systems. In turn these can be stood up as production environments. There is a central system that handles the predefined scope of the business.

> The **predefined scope** is a selection of **Finance-led ERP business processes**, which are already used by the majority of our customers. Finance-led ERP covers core processes in the Finance, Sales, and Procurement lines of business with **one company** and **one legal entity**.

As part of the Baseline Activation Service, SAP maintains a three-system deployment of the SAP instance.

### SAP Signavio

![](https://learning.sap.com/service/media/topic/bf076d44-f74f-484e-b2f7-d265ec48fc33/S4CP01_27_en-US_media/S4CP01_27_en-US_images/U2_L2_3_Signavio_001.png)

Included in the premium RISE with SAP package

Signavio is a set of prebuilt reports that draw upon the standard data structures of SAP. Over 300 KPI's included although I'm unclear whether the KPI's are preconfigured to draw from the right data sources or if it's meant to be a global benchmarking tool.

###### SAP Signavio Process Manager & Process Collaboration Hub

Collaborative platform for engaging with Signavio across the business.

### Digital Discovery Assessment

Part of the Sales process as a discernment step for right-sizing the solution

![](C:\Users\wright\AppData\Roaming\marktext\images\2023-08-23-06-41-52-image.png)

1. Supply Chain of Selling App
   Net New or Existing Customer
   Greenfield Deployment (Conversion automatically routes to Private Edition)
   Countries
   Industry
   Finance vs Operations led Processes
   Two-Tier Deployment

2. Create Customer Opportunity

3. Generates a recommendation based on the lead that routes them to either the public or private solution

4. Detailed Discovery (Required for Conversions)
   Known Integrations and Extensions
   Localizations and Legal Entities
   Percentage of Business Scenarios per BU/Functional Area
   Additional Goals
   Private customers also have the option of the Enterprise Management Layer which is preconfigured on best practices

5. Digital Discovery Assessment Report

## [ SAP Activate Implementation Methodology]([Roadmap Viewer (sap.com)](https://go.support.sap.com/roadmapviewer/))

![](https://learning.sap.com/service/media/topic/c935997d-572a-412d-872b-5eda72587e90/S4CP01_27_en-US_media/S4CP01_27_en-US_images/2102_U3_L3.1_0_ActivateOver_001.png)

The Activate methodology is SAP's framework for implementation success. This is a canned set of project phases, tasks, and deliverables that will serve as guard rails and goalposts for the implementation team inside the business.

The Roadmap Viewer is structured with the following elements

- **Phases**: stages of the project, including Discover, Prepare, Explore, Realize, Deploy, and Run. At the end of each phase, a quality gate exists to verify the completion of the deliverables.
- **Deliverables**: outcomes that are delivered during the course of the project. Several deliverables are included within a phase.
- **Task**: work to be performed. One or several tasks comprise a deliverable.
- **Workstream**: a collection of related deliverables that show time relationships within a project and among other streams. Streams can span phases and are not necessarily dependent on phase starts and end.
- **Accelerators**: provide assistance in the form of How-to guides, Best Practice recommendations, prescribed templates, and links to learning materials. Accelerators can be linked to Phases, Deliverables or Tasks.

### [SAP Best Practices]([SAP for Me](https://me.sap.com/processnavigator/))

The SAP Best Practice Explorer is configured based on the selected packages for the customer at the release date(Release to Customer Date RTC) of the solution.

Best Practice Explorer items include the following data 

- **Scope-item fact sheets**: A description of the business process including business benefits and key process steps covered.
- **Process flow:** A representation of the business process to show how the software works as standard.
- **Process flow (BPMN2):** A representation of the business process to show how the software works as standard, for displaying and editing in process modeling applications.
- **Test scripts**: A procedure for testing the activated system according to the defined business process.
- **Set-up Instructions:** A guide to the steps required to set up any integrations required for the business process to function correctly. The setup guide must be completed prior to the test script.

### SAP Application Lifecycle Management

Included for all SAP cloud offerings regardless of edition. Contingent on an Enterprise Support Agreement


![](C:\Users\wright\AppData\Roaming\marktext\images\2023-08-23-07-29-41-image.png)

#### SAP ALM for Implementation

This is a preconfigured guided workspace tailored to the environment. It is based on the Activate methodology and pipes tasks, deliverables, and timelines to the analyst

![](C:\Users\wright\AppData\Roaming\marktext\images\2023-08-23-07-33-16-image.png)

#### SAP ALM for Operations

Steady-state tool focused on quality and execution. Similar feedback cycle to DMAIC but with Automation tacked onto the end.

Put the process in a hole and forget about it :roll_eyes: 

![](C:\Users\wright\AppData\Roaming\marktext\images\2023-08-23-07-34-14-image.png)

## [SAP Solution Manager]([SAP Solution Manager](https://support.sap.com/en/alm/solution-manager.html))

Only for private edition customers. Includes SAP Focused Build and Focused Insights as part of the package.
Focused Build is tied to the SAP Solution Manager 7.2 application which has an end-of-life date of 2027 and an extended support window of 2030.

- **Focused Build** is an out-of-the-box, tool-supported methodology to manage requirements and software development for large, agile innovation projects.
- **Focused Insights** enables you to build and distribute powerful customer-specific dashboards in minutes using state-of-the-art user experience.

Tracks

- Implementation Tasks

- Decisions

- Open Requirements

- Fit-to-Standard workshops
