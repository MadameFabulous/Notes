![[End-to-End Business Processes for the Intelligent Enterprise/Introduction/Business Process Map.png]]

![[End-to-End Business Processes for the Intelligent Enterprise/Introduction/Business Process Alignment by LOB Process and Department.png]]

![[End-to-End Business Processes for the Intelligent Enterprise/Introduction/BTP Overview.png]]
# Enterprise Structure
International Financial Reporting Standards (IFRS 8) are the international accounting standards that govern how legal entities are structured.
Regional standards get layered in below this, like General Accepted Accounting Standards (GAAP)
IFRS 8 requires reporting breakouts by operational areas for the key financial figures.
![[End-to-End Business Processes for the Intelligent Enterprise/Introduction/Enterprise Structures Diagram.png]]
## Client
Highest hierarchical structure within an SAP. Represents a corporate group and is made up of system that contains master records and tables.
## Operating Concern
- Enterprise structure defined by a Sales Market with a uniform structure
- Used in profitability analysis
## Controlling Area
- Self-Contained
- Enterprise structure defined by the entities it is configured to control
- Used in revenue and cost accounting (CO - Managerial Accounting/Cost Accounting)
- Can contain multiple company codes (many-to-one)
- Costs and Revenues can only be allocated within a Controlling Area, not into another controlling area
## Valuation Level
Used in the valuation of material and inventory accounts. This can be configured two ways
- Plant Levels: Required if you plan on operating a standard cost environment
- Company Code level
### Company Code
- Enterprise structure that is used in the mapping of organizational units
- Used for grouping organizational units for external financial reporting
- Company codes cannot be mapped outside of their controlling area, company to controlling area is a one-to-one relationship
- Plants are mapped to a company code, this is a many-to-one relationship
### Segment
- Optional Enterprise structure
- Not directly attributed to another organizational object
- Determined on a transactional basis during the posting process
- Breaks out reporting further in accordance with GAAP/IFRS
### Sales Organization
- Subdivides the organization based on sales requirements
- Groups the revenue and activities for the sale of goods and services within the organization
- One-to-one relationship with a Company Code
### Purchasing Organization
- Grouping entity for purchasing activities
	- Central Purchasing Organization
	- Cross-Plant Purchasing Organization
	- Plant-Specific Purchasing Organization
- Consolidates purchasing activities and spend
#### Plant
- Logistical Unit for operations
- Subdivides accounting based on the areas of operation
- One-to-one relationship to company code
- Since plants correlate to the physical location of the inventory of goods they cannot be mapped across multiple company codes because this would potentially violate reporting guidance
#### Personnel Area
- Subdivision of company code for organizing labor
- Can represent different physical sites or reporting areas
#### Distribution Channels
- Characterize the way that goods are delivered or provided
- Used to break out business lines (e.g. new product sales from service and maintenance contracts)
- Can be assigned to a sales organization. This is a many-to-one relationship where one sales organization can have multiple distribution channels 
#### Division
- Divisions are use to group materials and services to provide sales analytics
- Divisions are mapped to sales organizations in a many-to-many relationship
##### Warehouse Number
- Defined by a physical location
- Groups 'Storage Types' and 'Storage Sections' that group storage locations
- Warehouses can group storage locations from multiple plants
##### Storage Locations
- Subdivision of Plant where inventory is physically kept
- Storage locations can be mapped to multiple plants. The combination of plant-storage location is what makes a unique location in the system
	- This means that locations can use standard nomenclature across all sites and cross reference the storage locations across plants. (e.g. Site1-Picking would be represented by linking the picking loc to another plant)
- One storage location is **required** per plant
##### Shipping Point
- Location that controls the shipment of the inventory
- Many-to-one relationship with plants, this is meant to represent cross-site shipping or staging of sales orders
## SAP Warehousing Definitions 
- "Chaotic Warehousing" - inventory and availability is a cross-site activity facilitated by a WMS
- "Fixed Warehousing" - Fixed locations, cross planning not used. Facilitated by traditional Inventory Management
## Sales Area
The combination of sales organization, distribution channel, and division make up a unique "sales area". This ensures that distribution channels can be mapped by activities.
## Master Data and Enterprise Structure
![[End-to-End Business Processes for the Intelligent Enterprise/Introduction/Master Data Integration - Data Flows Video Clip.png]]
### SAP Master Data Definition
- Have all the essential information required to map processes in a system (Defined Process)
- Remain unchanged over a long period
- Are maintained with a reference to the enterprise structure
### SAP Master Data Examples
- Product master data (material master)
- Customer or vendor master data
- G/L accounts
- Cost center
- Employee master data
### SAP Transactional Data Definition
- Records single process steps in the SAP system
- Short-lived nature
- Documents will always be attributed to an enterprise structure
### SAP Transactional Data and Document Examples
- Create sales order
- Post vendor invoice
- Create production order

Standard data elements, broken out by site off of the master data record.
![[End-to-End Business Processes for the Intelligent Enterprise/Introduction/Master Data Record and Enterprise Structures Video.png]]
# SAP Activate Methodology with Best Practices 
## SAP Activate Roadmap Viewer
![[End-to-End Business Processes for the Intelligent Enterprise/Introduction/Activate Methodology (from Record to Report).png]]
	SAP Activate is the implementation framework for all kind of SAP projects. It simplifies and accelerates new implementation, system conversion or landscape transformation of SAP Solutions.
	SAP Best Practices are part of SAP Activate
[Activate Roadmap Viewer](https://go.support.sap.com/roadmapviewer/)
## SAP Best Practices
SAP Best Practices are a set of defined data that helps structure the business processes. When used correctly the SAP Best Practice module ensures alignment on system data. Best Practices are updated with each release of SAP
## Scope Items
Scope Items are a bundle of details that represent what the process is meant to do when it is fully configured.
### Scope Item Content
- #### Scope item fact sheets:
    A description of the business process including business benefits and key process steps covered.
- #### Process flow:
    A representation of the business process to show how the software works as standard.
- #### Process flow (BPMN2):
    A representation of the business process to show how the software works as standard, for displaying and editing in process modeling applications (for example SAP Signavio).
- #### Test scripts:
    A procedure for testing the activated system according to the defined business process.
- #### Set-up Instructions:
    A guide to the steps required to set up any integrations required for the business process to function correctly. The setup guide must be completed prior to the test script.
### Scope Item Examples
Two Examples of Scope Items Attributed by Process Owner for the "Record-to-Report" processes