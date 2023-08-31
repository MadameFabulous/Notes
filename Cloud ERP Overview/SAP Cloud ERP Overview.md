# SAP Cloud ERP
![[Cloud ERP Overview/SAP Cloud Banner.png]]
## SAP S/4HANA Cloud Deployment- Public (Multi-tenant server)
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
[SAP Best Practices Blog Post](https://help.sap.com/docs/SAP_Best_Practices)
## Two-Tier ERP Deployment
### Best practices for Two-Tier ERP
- Functionality Requirements by Subsidiary
- Interdependencies Documented
- Inter-company Transactions Defined Early
- Reporting Considerations and aggregation

![[Cloud ERP Overview/SAP Cloud Multi System Private Edition Master System with Public Subsidiaries.png]]

A single system of record is maintained that is responsible for the higher order functions of the ERP systems. This in turn frees up the Tier 2 ERP deployments for localization and specialized processes.

This also had additional benefits when the business engages in significant M&A Activity or planned divestiture 

![[Cloud ERP Overview/SAP Systems with External Vendors.png]]
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
![[Cloud ERP Overview/Business Processes and BTP.png]]

![[Cloud ERP Overview/BTP, Applications, and Process.png]]

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
![[Cloud ERP Overview/Sustainability Framework Pic.png]]
### Intelligent Enterprise Suite Qualities
As enterprises have become increasingly automated they increase the proportion of labor that is delegated to high value tasks
![[Cloud ERP Overview/Intelligent Enterprise Value Pipeline Breakdown.png]]
### "The Experience Economy"
![[Cloud ERP Overview/Experience Economy - X and O data with Intelligence.png]]
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
![[Cloud ERP Overview/Grow and Rise with SAP.png]]
#### SAP Grow with SAP S/4HANA Cloud, public edition
![[Cloud ERP Overview/Grow Public Edition.png]]
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
![[Cloud ERP Overview/BTP and Private On Prem.png]] 
Private Edition CPEA Credit Usage
- CPEA Credits for Private Edition customers can be used on SAP Build
- CPEA Credits can be used on other SAP Products like [Signavio]([SAP Signavio | The Only All-in-One Business Process Software](https://www.signavio.com/))
## SAP BTP Build
![[Cloud ERP Overview/SAP Build for Private Onprem.png]]
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
![[Cloud ERP Overview/Baseline Activation Service.png]]
Instanced deployments of SAP meant to help customers align on best practices. These environments can be configured and populated with sample data from existing systems. In turn these can be stood up as production environments. There is a central system that handles the predefined scope of the business.

> The **predefined scope** is a selection of **Finance-led ERP business processes**, which are already used by the majority of our customers. Finance-led ERP covers core processes in the Finance, Sales, and Procurement lines of business with **one company** and **one legal entity**.

As part of the Baseline Activation Service, SAP maintains a three-system deployment of the SAP instance.
### SAP Signavio
![[Cloud ERP Overview/Signavio.png]]
Included in the premium RISE with SAP package
Signavio is a set of prebuilt reports that draw upon the standard data structures of SAP. Over 300 KPI's included although I'm unclear whether the KPI's are preconfigured to draw from the right data sources or if it's meant to be a global benchmarking tool.
###### SAP Signavio Process Manager & Process Collaboration Hub
Collaborative platform for engaging with Signavio across the business.
### Digital Discovery Assessment
Part of the Sales process as a discernment step for right-sizing the solution
![[Cloud ERP Overview/Digital Discovery Assessment Process Overview.png]]
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
![[End-to-End Business Processes for the Intelligent Enterprise/Introduction/Activate Methodology (from Record to Report).png]]
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
![[Cloud ERP Overview/Cloud ALM Native vs Open.png]]
#### SAP ALM for Implementation
This is a preconfigured guided workspace tailored to the environment. It is based on the Activate methodology and pipes tasks, deliverables, and timelines to the analyst
![[Cloud ERP Overview/ALM for Implementation.png]]
#### SAP ALM for Operations
Steady-state tool focused on quality and execution. Similar feedback cycle to DMAIC but with Automation tacked onto the end.
![[Cloud ERP Overview/ALM Detect-diagnose-correcct-automate.png]]
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
## Configuration Options
### New Implementation
#### Public Cloud
SAP Central Business Configuration is the tool for managing a multi-system deployment. Handles provisioning for SAP Cloud edition as well as SaaS platforms(Ariba, Concur, SuccessFactors)
Consists of three Subject Areas
- Project Experience
  - Project management intake pipeline
- Scoping
  - Identifying the correct application of the SAP Best Practices guide to the project or the task
- Central Configuration
  - Serves as a staging ground for deployments
  - Build organizational structure and set up configurations before deployment to the subsystems
# SAP Best Practices
## New Implementation
### Configuration Pathways for Private Cloud
- Activate Methodology with Best Practices (and Enterprise Management Layer if delegated during the sales pipeline)
- Implementation Guide(IMG) with Activate Methodology with Best Practices for task management
- Only IMG is used - this will involve the SPRO txn
##### SAP Best Practices for Private Cloud
SAP Solution Builder is the tool for the deployment of SAP Best practices for Private Cloud customers 
Best Practice Scenarios are predefined process flows for the business that are deployed through the solution builder
Best practices are deployed to the development environment and then flow through to the test/quality system and production via "Transports"
##### Signavio for New Implementations
Signavio picks up where the Solution Builder left off and breaks out the selected deployment into tasks and deliverables while providing the Collaboration Hub as a space to work through the deployment.
##### Configuration Responsibilities
SAP Consultants are responsible for the questionnaire that is conducted as part of the sales pipeline
Client or Implementation Consultant is responsible for tasks and customization that is required for their deployment
### System Conversion for Legacy Systems
![[Cloud ERP Overview/Prepare-Realize phase of System Conversion.png]]
SAP Consultants handle configurations of technical items like Client 000 (Admin Client) that cannot be prepared by the client
#### Client Responsibilities
- SAP Readiness Check
- Custom Code Optimization
- Functional Testing
- Integration Testing 
### Activate Methodology Steps for Conversions
#### Prepare Phase Tools
##### Simplification Item Catalog
Simplification Items are the steps needed to be taken for a conversion for the business and IT
##### SAP Readiness Check
Only for SAP ERP 6.0 Customers. Automated tool for high level, rough-cut specifications and compatibility considerations.
##### Maintenance Planner
This is the first step in an SAP conversion.
Checks compatibility with SAP S/4HANA.
Creates the stack file that is used in the conversion which is a requirement for the Software Update Manager(SUM) tool
##### Simplification Item Check
These are the technical checks to  ensure that you can be converted. This is a mandatory step that is triggered by the System Update Manager(SUM) tool. Since SUM is required, this is required for all conversions.
##### Custom Code Migration
The Custom Code Migration Tool checks against a list of simplifications. This is not mandatory for the prepare phase
#### Realize Phase Tools
##### Software Update Manager(SUM)
The SUM manages the migration of mapped data and custom applications. For larger legacy systems the Silent Data Migration Infrastructure (SMDI)
### Fiori Launchpad Configuration for Private Cloud
![[Cloud ERP Overview/Fiori Launchpad Configuration.png]]
For all implementation paths Fiori Launchpad is configured separately from the applications that are managed. Public Edition comes with a preconfigured set of suggested applications. Private Edition customers will have a set of Fiori applications identified as part of the Readiness Check step of the deployment.
#### Deployment Options for Fiori Launchpad
Client 100 is deployed with the Fiori launchpad for New implementations by the SAP consultants. This serves as the template for the business and is configured by SAP Consultants as identified during the readiness check.
Customers or Implementation Partners are responsible for the non-technical activities like designing user profiles and application selection
## Integrations with S/4HANA Cloud Deployment
### Intelligent Enterprise Toolkit
The Intelligent Enterprise Toolkit has four pillars.
- Out-of-the-Box Integrations
  - Prepackaged end-to-end integrations
  - Cloud Integration Automation Services(CIAS)
- Open Integrations
  - Any third-party integration and custom extensions that leverage public APIs can be integrated into SAP Cloud
  - 160+ third-party applications currently integrated
- AI-Optimized Integrations
  - Integration Advisor is a crowd-based(customer data trained?) tool to drive ease of use for B2B and A2A integrations
  - Artificial intelligence and machine learning are used to simplify the development of integration scenarios.
  Content Advisor Architecture
  ![[Cloud ERP Overview/Cloud Platform Integration Diagram CPI Content Advisor.png]]
### [Integration Solution Advisor Methodology(ISA-M)]([Integration Solution Advisory Methodology (ISA-M): Define Integration Guidelines for Your Organization | SAP Blogs](https://blogs.sap.com/2019/02/24/integration-solution-advisory-methodology-isa-m-define-integration-guidelines-for-your-organization/))
![[Cloud ERP Overview/ISA-M Diagram.png]]

![[Cloud ERP Overview/ISA-M Components.png]]
### Components of ISA-M
- Integration Domains - Entry Points
  - On-premise-to-cloud
  - Cloud-to-cloud
- Integration Styles - Categories
  Defined by characteristics and use-case patterns that group these categories
  - Process
  - Data
  - User
  - IOT
- Integration Technology Mapping
  This is the timeline and breakout of skills and tools that already exists in the domains. It is a combination of domain location and integration style
## SAP Integration Suite
Useful Links for Integrations:
[Setup and Monitoring of Integration Scenarios](https://support.sap.com/en/alm/solution-manager/expert-portal/monitoring-of-integration-scenarios.html)
[SAP Integration Suite – Cloud Integration](https://support.sap.com/en/alm/solution-manager/expert-portal/public-cloud-operations/sap-cloud-platform-integration.html) 
![[Cloud ERP Overview/SAP Integration Suite.png]]

The **SAP Integration Suite** offers a modular set of integration services that help manage each pillar of the ecosystem.
- Process integrations (application to application)
- Master data integrations in coordination with the SAP One Domain Model
- API-driven integrations, including full API lifecycle management and omnichannel access
- Event-driven integrations to support sense-and respond scenarios based on business events
- Data integration and pipelines to support data use in other applications as well as the SAP Data Intelligence platform
- B2B integrations to integrate with suppliers, and governmental entities across the digital ecosystem
Key enablers of the Integration Suite are the SAP Data Services and Process Orchestration modules
![[Cloud ERP Overview/Data Services and Process Orchestration Modules.png]]
### SAP Cloud Connector Integration
Works via a reverse invoke proxy component
- Propogate identity security across systems to ensure consistency for users in multi deployment environments
- Database Connections for Analysts
### SAP API Management
API unification for all business users
### Integration and Exception Monitoring with Cloud ALM for Operations
Provides an interface for the monitoring of peer-to-peer interfaces as well as the orchestration platforms
Closes gap between business and IT during problem resolution process (technical issue vs. business issue) by:
- Alerting to notify responsible persons in business and IT about discovered integration related problems
- Search and track single messages based on exposed business context attributes e.g. order numbers
- Operation automation to trigger operation flows context sensitivity for automated correction of problems
### Integration Monitoring with SAP Solution Manager
![[Cloud ERP Overview/SAP Solution Manager.png]]
Similar to the Integration Monitor, the Solution Manager integrates the legacy SAP metric platforms (Interface Channel Monitoring, Connection Monitoring, and Interface Monitoring metrics from Business Process Monitoring).
This tool is for troubleshooting mission critical components 
### SAP Solution Manager Focused Run
This tools is meant for broad networks that need robust testing to troubleshoot and diagnose their issues. Not a lot of other information given outside of the graphic.
### Integration Monitoring in SAP Business Technology Platform
- **Monitor Message Processing:** View the number and status of processed messages within a specified time window.
- **Manage Integration Content:** View the number and status of integration content artifacts (e.g. integration flows).
- **Mange Security:** Manage certain tasks related to the setup of secure connections between your tenant and remote systems.
- **Manage Stores:** Manage temporary data stores on the tenant.
- **Access Logs:** Monitor audit logs (resulting from system changes) and analyze errors that occurred during inbound HTTP processing.
- **Manage Locks**: Display and manage lock entries that are created (in the in-progress repository) to avoid the same message being processed several times in parallel.
### Integration Monitoring in SAP Analytics Cloud
Using the dashboard, you can:
- Monitor the integration flows which has the highest processed messages.
- Analyze the status of processed messages.
- Get the count of the deployed artifacts.
### Integration Monitoring with SAP Fiori Apps
![[Cloud ERP Overview/Integration Monitoring Fiori.png]]
All-in-one platform for developers and interface development, mapping, etc.
Enables business users to reduce the time needed for error handling because they are able to monitor interfaces and troubleshoot issues without IT.
## Extending the SAP S/4HANA Cloud Deployment Options
### SAP S/4HANA Extensibility Concept
#### In-app Extensibility
##### Key User in-app extensibility
Key User extensibility is driven by the Fiori launchpad and the customization in the UI and configurations
##### Developer in-app extensibility
Enables developers to create custom ABAP code and partner extensions in an upgrade-stable, cloud-ready programming model.
![[Cloud ERP Overview/ABAP.png]]
##### Classic in-app extensibility
Custom code, modifying the SAP codebase. Can hinder or delay upgrade and merits more testing and consumes more IT resources to maintain
#### Side-by-Side Extensibility
This takes traditional Extensibility and manages it in SAP BTP. This decouples the extension from the code base.
### Transport Extensions for Public Cloud
#### Public edition
![[Cloud ERP Overview/Public edition deployment pipeline.png]]
Transport starts in the SAP Central Business Configuration. Once the Activation activities and configuration activities there will be a prompt for a customizing request. These are exported to the test system via the Fiori "Export Customizing Transports" application this starts the pipeline for the changes to the test system.
The Customizing Tenant of the development environment is the engine responsible for the transports but also defines workflows, teams, and responsibilities related to the maintenance of the extension.
The Development Tenant (Client 080) is where Workbench requests are logged and released from. These are a second input to the SAP Transport Organizer view This takes the extensibility and bundles it to client 100 where it can be carried to the test and production system
The "Import Collection App" bundles the developer extensibility, business configuration, and key user extensibility into a single package for the test system. This can then be carried forward to production once testing has been completed
#### Private edition
![[Cloud ERP Overview/Private Edition Development Pipeline.png]]
The Adaptation Transport Organizer(ATO) is responsible for the management of key user extensions. This is required to create packages and register extensions for transport.
The Fiori Configure Software Packages app is responsible for certain change management activities if required for the software package.
The Register Extensions for Transport app feels very similar. Unable to discern the difference a this point in my training.
## Migrating Data to the SAP S/4HANA Cloud Deployment Options
The Migration Cockpit is a tool to give you a platform for the three different migration solutions offered by SAP
Template-based Migration
Automatic Mapping
Fiori Migrate Your Data Application
**Recommended Migration Approaches**
Legacy system conversion + Staging Tables
Custom Migration Object  + Staging Tables
[Note on Custom Migration Objects Offered to Public Edition Customers](https://me.sap.com/notes/2999428)
Creating a new custom migration object with the modeler is only supported for private cloud.
### Data Migration in System Conversions
Database migration and custom code migration occur during the technical conversion process when an SAP ERP or SAP S/4HANA on premise system is converted to SAP S/4HANA Cloud, private edition.
## Testing Business Processes in the SAP S/4HANA Cloud Deployment Options
![[Cloud ERP Overview/Test Automation Tool.png]]
### Test Automation Tool in Public Cloud
300 pre-delivered test automates based on SAP Best Practices business processes, and supports customization.
Fiori's Three Testing Automation Tools
- Manage your Test Process
- Test Your Processes
- Analyze Automated Test Results
Phases of testing via the Automation Tool
1. Establish Scope
   Implementation Tests
   End User Acceptance Testing
   Regression Testing
2. Plan Tests
   Maintain the transactional data for process steps
   Assign a virtual test user to perform the work
   Scenario 1 - No extensions or Customizations
   - Use SAP Pre-Delivered Testing Plans
   Scenario 2 - Extension or Customized Process
   - Make a copy of the closest pre-delivered test process then tailor it to the extension or customization
   The Fiori Test Your Processes application
   - Create virtual test user
   - Create test plans
   - Create test plan variants for localizations
   - Provide consent/authorization to SAP for execute quality tests on the customers behalf after a major release upgrade. They'll use the established test plans that are built out and maintained by the customer to ensure that key functionality is in-tact on the other side of a system upgrade.
3. Perform Tests
- Test Your Processes - Execute Test Plans
- Analyze Automated Test Results
  - View results from the "Test Your Processes" app
  - View results from automated PUT(Provider Upgrade Testing?) after a major upgrade
  - Drill-down for details of plan execution
## Describing Security for the SAP S/4HANA Cloud Deployment Options
### Four Pillars of the SAP Cloud Secure Strategy
![[Cloud ERP Overview/Four Pillars of SAP Cloud Security.png]]
- Security Standards Management
	- Policy-Based Guidance
	- Compliance Support Through Integrated Management System
	- Data Protection Management System
	- General Rules and Scope Definitions
	- Problem Solving and Response to Disruptive Incidents
- Comprehensive Contracts
	- Order Forms
	- Personal Data Processing Agreement
	- Service Level Agreement
	- Terms and Conditions
- Independent Validation
	- Based on Globally Recognized Standardized
	- Audits
	- SOC (Security Operations Center) Reporting
	- ISO Certifications
	- Regularly Conducted Assessments
- Secure Architecture
	- Data Segregation
	- Intrusion Detection
	- Prevention and Monitoring
	- Service Continuity and Resiliency
	- Audit and Penetration Testing
### [SAP Trust Center](https://www.sap.com/about/trust-center.html) & My Trust Center
The Trust Center is the SAP network side of the security platform. The published metrics here are SAP, not customers.
####  SAP Trust Center
- Cloud Status
- Security
- Privacy
- Compliance
- Cloud Operations
- Data Center
- Agreements
#### My Trust Center
Only available to SAP Customers who have a valid SAP user ID.
- SAP Security Policies, Frameworks, and Technical and Organizational Measures (TOMs).
- Lists of SAP's sub-processors which provide data processing services on behalf of SAP to its customers
- Compliance evidence documents from SAP partners providing services to SAP (e.g. Hyperscaler infrastructure services).
- Useful links and documents about Security and Data Protection & Privacy for SAP Products, Cloud Services, Professional Services and Support.
## SAP Global Security Team
![[Cloud ERP Overview/SAP Global Security Team.png]]
#### Cyber Defense & Design
This team is responsible for the baseline security and firewall configuration recommendations for all operating systems for the SAP customer base. This team follows up on security concerns and suspicious activity reports by customers.
#### Security Risk & Compliance
Works with audit findings to align on best practices and regulatory requirements
#### Security Enablement Team
General security education for SAP customers
#### Communications team
Trains SAP employees on best practices and creates learning materials to support the SAP ecosystem
### Data Center Security
![[Cloud ERP Overview/Data Center Security.png]]
SAP's cloud is designed with redundancy in mind to ensure customer SLA's are met.
SAP Data Center Security Features
#### Physical Features
- Electricity is sourced from two separate grid sectors from the local utility creating redundant systems. There are also generators on-site prepared for sustained outage.
- Controlled Access
	- Segmented Access
	- Biometric Authorization for Sensitive Areas
- Inter Data Center traffic is encrypted
- SAP operates with a  3-2-1 back up process
#### Technical Security Features
- A Web dispatcher farm that hides the network topology from the outside world.
- Multiple Internet connections to minimize the impact of distributed denial-of-service (DDoS) attacks.
- Layered security measures that continuously monitors solution traffic for possible attacks.
- Multiple firewalls that divide the network into protected segments and shield the internal network from unauthorized Internet traffic.
- Third-party audits performed throughout the year to support early detection of any newly introduced security issues.
### Hybrid Security with Enterprise Security Services
![[Cloud ERP Overview/Hybrid Security with Enterprise Security Services.png]]
#### Components of Enterprise Security Services:
- **Cloud Identity Services** address identity and access management in the cloud. They can be used across the SAP cloud solution portfolio, and they include the Identity Authentication and Identity Provisioning services as a part of SAP Cloud Identity Services.
- **Secure Development Services** help support the development of secure applications on the Business Technology Platform. These services, such as SAP Cloud Application Programming Model and the Cloud Connector, enable developers to build secure enterprise business applications.
- **Risk and Compliance** are provided by solutions such as SAP Cloud Identity Access Governance to help security administrators manage risks and meet corporate compliance goals.
- **Insight** is delivered by SAP through its SAP Trust Center site to provide a transparent view into how SAP manages cloud applications for customers. With SAP Data Custodian, SAP customers can gain insight into the location and movements of data.

**Security partners** complete the picture by providing generic services such as static code and open source vulnerability scanners.

### Data Protection & Privacy
- Data Controller
	- Entity that determines the purposes, conditions, and means of the processing of personal data
- Data Processor
	- Entity which processes personal data on behalf of the controller
Regardless of deployment the responsibilities are the same for Data Controllers and Processors. Sub-processors of data are held to the same data standards as SAP is held to with its customers
#### Technical and Organizational Measures(TOMS)
TOMS are the measures designed by the Global Security Team
- Physical Access Control
- System Access Control
- Data Access Control
- Data Transmission Control
- Data Input Control
- Job Control
- Availability Control
- Data Separation Control
- Data Integrity Control
### SAP Data Protection Officer(DPO)
The DPO manages the Data Protection and Privacy(DPP). This is a cross functional team who consists of attorneys, auditors, and technical experts that report into the DPO.
### GDPR Compliance
Compliance is achieved through business processes so the standard for on-prem vs cloud deployments is consistent.
Communication outside of the EU achieves compliance [standard contractual clauses(SCC's)](https://commission.europa.eu/law/law-topic/data-protection/international-dimension-data-protection/standard-contractual-clauses-scc_en) SCC's are pre-approved data transmission standards from the European Commission
## Best Practices for Secure Operations
- Organization
	- Employee Awareness
	- Security Governance
	- Risk Management
- Process
	- Regulatory Process Compliance
	- Data Privacy & Protection
	- Audit & Fraud Management
- Application
	- User & Identity Management
	- Authentication & SSO
	- Roles & Authorization
	- Custom Code Security
- System
	- Security Hardening
	- Secure SAP Software
	- Security Monitoring and Forensics
- Environment
	- Network Security
	- Operating System & Database Security
	- Client Security
### SAP S/4HANA Cloud Starter System, public edition
![[Cloud ERP Overview/SAP Cloud Starter System Starter Public.png]]
#### 3 System Landscape(3SL)
- Development
- Quality
- Production
The [SAP Cloud Appliance Library](https://community.sap.com/topics/cloud-appliance-library)(CAL) is a library for private edition customers. Used in Trial, Scoping, or Sandbox deployments. These are available to both private and public edition customers. These deployments are designed to be run on a provider like Microsoft Azure, Google Cloud, or AWS in 2-3 hours.
##### SAP S/4HANA Fully Activated Appliance
An appliance is a compressed system image that can be rapidly extracted into a regular system instance while preserving everything that was configured for the appliance when it was developed. All standard supporting applications are also included.
- SAP Best Practices Processes
- Master Data Governance(MDG)
- Transportation Management(Development system package management)
- Portfolio Management
- Human Capital Management
- Analytics
- [Fully Activated Appliance Demos](https://blogs.sap.com/2019/04/23/sap-s4hana-fully-activated-appliance-demo-guides/)
##### Enterprise Management Layer(EML) for SAP S/4HANA
This is the successor technology to the *Model Company for Multinational Corporations* module. This tool is a tool for standardization and localization of deployments. SAP's Localization supports 43 local versions and 25 system languages.
There is a group ledger that is the leading ledger for the corporation. There are four additional subledgers that handle the translation to meet local currency reporting and governmental requirements.
#### SAP S/4HANA Cloud, private edition
Private edition has a similar flow to the public edition with the added option for sandbox spaces.
- Sandbox
	- **New Implementations:** Canned deployments out of the SAP CAL or based on the existing customers system and mapping. The sandbox systems are used by SAP consultants to conduct fit-to-standard workshops which are meant to get business SME's up to speed in their required activities and document any configuration or extension requirements. These are then tracked in SAP Cloud ALM for lifecycle monitoring.
	- **System Conversions:** Sandbox deployments are focused on reviewing a specific Workflow, Report, Interface, Conversion, Enhancement, and Forms (WRICEF).
- Development
	- **New Implementations:** fresh development system is deployed with SAP standard business process content, or as a blank system where customizing is done via the IMG (Implementation Guide).
	- **System Conversions:** the customer's existing development system is converted to SAP S/4HANA Cloud, private edition based on the migration approach validated with the sandbox
	There are two clients in the development environment. Items created or customized on the development client are available to the customization client as well as other development clients because when the changes are made to the development tenant they are tracked on a table that doesn't attribute them directly to one development object.
	- Development Tenant (Client 080)
	- Customizing Tenant (Client 100)
- Quality
	Changes are released from the development system to the quality system via the Transport Organizer SE09 Transaction
	There are no differences between the development-to-test pipeline regardless of deployment scenario.
- Production
	Changes are released from the quality system to the production system via the Transport Organizer SE09 Transaction
	- **New Implementations:** the configuration from the quality system is transported to the production system
	- **System Conversions:** the customer's existing production system is converted to SAP S/4HANA Cloud, private edition, based on the migration approach validated in the sandbox, development, and quality systems.
### Additional System Landscapes
- Partner Shared Demo Environment (PDE)
	Scripted-demo environment for SAP partners to model Intelligent Enterprise applications. Allows for Consultants to demo preconfigured modules to customers. Controlled access
- Partner Test, Demo, and Development (TDD)
	Sandbox demo space offered to SAP partners that uses the Central Business Configuration and Developer Extensibility like a private edition deployment
- SAP Learning Hub System 
	This is a training space for SAP customers with a Learning Hub Subscription. This system uses instanced deployments for student demos.
- Enablement Sandbox
	This is the free demo space for new SAP offerings. This sandbox is focused on new scope items from the latest release.
	Access is granted for a week to demo and learn the new functionality via the Learning Hub (only available with Learning Hub subscription).
## Discussing Support for the SAP S/4HANA Cloud Deployment Options
### SAP for Me
SAP Enterprise Support is the full-service support offering from SAP. This is entitled to the full support from SAP services.
**SAP for Me** is the Learning-Management-System that is included with the SAP id and access to the learning system. This is also the system is for support tickets and license provisioning from the CBC.
Included in SAP for Me there are a handful of preconfigured dashboards.
- **Customer Success**
    - Partners can manage their customers by analyzing their license portfolio, cloud consumption, upcoming renewals, and orders and contracts. Manage customer delivery such as cloud projects, certified consultants, and next generation cloud delivery migrations.
- **Finance & Legal**
    - Purchasers, controllers, and other related roles have multiple methods of reviewing their product portfolio from a financial perspective. Review your SAP orders, the licensed materials behind the orders, and the connection to the individual product. You can also view consumption metrics across all your cloud product licenses.
- **Partner Solutions**
    - Find enablement on how to build your own solutions, monitor the status of your developed solutions, and find your AIR key and links to register a new solution.
- **Partnership**
    - View your company and partnership details including Partner Tracks, contracts, sell & service authorizations, and grouping. In addition, you can find links to access key partner management apps and portals.
- **Products & Portfolio**
    - View your purchased SAP portfolio and its related products, find additional details in your product list like the number of related orders, systems, or licenses, and access links to additional information sources related to your product.
- **Sales & Marketing**
    - Partners can view their business plan, monitor your plan vs. actual revenue performance, view and manage end-to-end deal execution, and access sales apps.
- **Services & Support**
    - Review and submit maintenance and support cases across your company and find out information like planned upcoming maintenance events for your products.
- **Systems & Provisioning**
    - View a list of all cloud or on-premise systems related to a product, the current availability status of a system related to a product, and navigate directly to the Cloud Availability Center (CAC) for detailed status information for cloud systems.
- **Users & Contacts**
    - View a list of all SAP contacts that are available for a product or product portfolio, and view a list of contacts SAP is aware of in your company for a product or product order. You can also change the assignment of a contact in your company in relation to a product, and manage S-Users, P-Users, and SAP Universal ID (UID) users.
### Responsibilities for Governance in Hybrid Landscapes
![[Cloud ERP Overview/Responsibilities for Master Data Governance in a Hybrid Landscape.png]]
### Effective Governance in Hybrid Landscapes
![[Cloud ERP Overview/Master Data Governance in Hybrid Landscapes.png]]
SAP Recommendations:
- Customer Center of Excellence (CCOE): Collaboration space for the business and IT organization to share processes
- [SAP White Papers on Application Lifecycle Management](https://support.sap.com/en/alm/hybridALM.html)
## Defining Release Upgrades for the SAP S/4HANA Cloud Deployment Options
![[Cloud ERP Overview/SAP Release Nomenclature.png]]
SAP versioning is YYMM for major releases.
CFD's are delivered on a monthly cadence YYMM.X where 'X' is a revision of the CFD.
The _Activate New Features_ app is available in the Test system. This cannot be configured in the development system so any active development for CFD's must wait for the integration of the CFD into a major release so that they can be modified via the ABAP platform.
### SAP S/4HANA Cloud, public edition Release Strategy
SAP Cloud, public edition has two major releases a year. In addition to major releases there are also Continuous Feature Deliveries(CFDs) between releases for non-disruptive features that can be deployed with a low impact to the customer system.
CFD's are activated in the "Activate New Features" Fiori application. CFD's will be automatically activated as part of the next major release if a customer does not opt to use them during their pre-release phase. Feedback for CFD's is registered in the SAP Influence Portal
#### Release Assessment and Scope Dependency (RASD) Tool 2.0
RASD is a tool for SAP public edition customers to conduct change management activities in advance of a planned release. This tool is configured based on the customer's active products and will highlight new and deprecated functionality for the next major release.
### SAP S/4HANA Cloud, private edition Release Strategy
![[Cloud ERP Overview/SAP On Prem Release Strategy.png]]
SAP Cloud, private edition follows the same release path as the On Premise releases.
One annual release
Non-disruptive features are released in the form of Feature Pack Stacks (FPS).
Once there is a new major release, old releases will receive support in the form of Support Pack Stacks(SPS) until the end of the maintenance window after five years.
As part of the "RISE with SAP" program, customers are entitled to one upgrade per year. SAP will execute the upgrade on behalf of the customer to their cloud instances. Planning, preparaiton, testing, and other non-technical activities are delegated to the customer to coordinate

### New Feature Resources
[SAP On Premise Releases](https://help.sap.com/docs/SAP_S4HANA_ON-PREMISE)
[SAP Cloud, public edition Releases](https://help.sap.com/docs/SAP_S4HANA_CLOUD)
[SAP Road Map Explorer](https://roadmaps.sap.com/welcome#/)
