![[Pasted image 20230830054216.png]]
Overview
![[Pasted image 20230830054641.png]]

![[Pasted image 20230830060604.png]]
# Enterprise Structure
International Financial Reporting Standards (IFRS 8) are the international accounting standards that govern how legal entities are structured.
Regional standards get layered in below this, like General Accepted Accounting Standards (GAAP)
IFRS 8 requires reporting breakouts by operational areas for the key financial figures.
![[Pasted image 20230830070932.png]]
## Client
Highest hierarchical structure within an SAP. Represents a corporate group and is made up of system that contains master records and tables.
## Operating Concern
- Enterprise structure defined by a Sales Market with a uniform structure
- Used in profitability analysis
## Controlling Area
- Enterprise structure defined by the entities it is configured to control
- Used in revenue and cost accounting
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