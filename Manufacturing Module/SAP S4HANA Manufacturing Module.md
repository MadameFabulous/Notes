T-Codes
MM02 = Part
MD61 = Planned Independ Requirements Creation(PIR) - Forecast
MD04 = Stock Requirements List

Planning Strategy 10 - Made to Stock Production
Planning Strategy 20 - Made-to-Order Production
Planning Strategy 40 - Planning with Final Assembly
Planning Strategy 50 - Planning without Final 
Planning Strategy 60 - Planning with Planning Material
Planning Strategy 70 - Planning at Assembly Level
Strategy
Planning Strategy 82 - Assembly Processing

Modes
![[Manufacturing Module/Change Material.png]]

Mode 1 - Backward Consumption
The customer requirement consumes planned independent requirements that come before it
![[Manufacturing Module/Backwards Consumption.png]]
Mode 2 - Backward and Forward Consumption
Consumes past requirements before forward requirements
Mode 3 - Forward Consumption
The customer requirement consumes planned independent requirements that come after it
![[Manufacturing Module/Forward Consumption.png]]
Mode 4 - Backward and Forward Consumption
Consumes future requirements before past requirements
Mode 5 - Period Specific Consumption
Only planned independent requirements in the related period are consumed

Individual vs Collective
MRP S/4HANA

# MRP Types
## Deterministic Planning
Driven by forecasting and sales orders to calculate materials requirements gaps based on plan
Better suited for high-touch or A Stock type items
## Consumption-Based Planning
Uses past historical consumption to define replenishment behaviors
Better suited for B/C Stock types with historical data at steady state
- The demand for the material remains quite consistent.
- The replenishment of the requested inventory must be ensured to avoid stockouts.
- The replenishment lead time for procurement is known and remains constant.
- ROP is considered consumption based planning
![[Manufacturing Module/ROP Sawtooth.png]]

# MRP Process Steps
## BOM Explosion & Backward Scheduling
## BOM Explosion and Multilevel Backward Scheduling
Backwards scheduling date is based on the requirement date of the finished product which is driven by the sales order.
![[Manufacturing Module/BOM Explosion and Multilevel Backward Scheduling.png]]

## Second Step of the MRP Process – Net Requirements Calculation and Lot Sizing

Lot sizing, and rescheduling horizon considered and checked against safety stock and requirements 
![[Manufacturing Module/Safety Stock.png]]
## Third Step of the MRP Process – Procurement Types
![[Manufacturing Module/Procurement Types.png]]
Type E: In-house production
Type F: External Procurement
Type X: Both Procurement Types

## Fourth Step of the MRP Process – Scheduling
![[Manufacturing Module/MRP Scheduling.png]]

Determination of Basic Dates for Planned Orders
Milestone based ordering dictated by Master Material File
Opening Period - Order Placement Time
In-house Production time - Sum total of operations and internal lead times
Lead Time Scheduling and Capacity Planning
![[Manufacturing Module/Planned Order MRP.png]]

## MRP Live
![[Manufacturing Module/pMRP Settings.png]]

pMRP - Predictive MRP
![[Manufacturing Module/pMRP FLow.png]]

![[Manufacturing Module/MRP Planned.png]]

![[Manufacturing Module/Monitor Material Coverage.png]]


## Maintain PIR's
Select Material
![[Manufacturing Module/Maintain PIRs.png]]
Enter a Forecast per week for the material, save the record. Then turn the PIR to active "Version is Active" flag.
![[Manufacturing Module/Maintain PIR with Forecast.png]]
## Stock Requirements List
![[Manufacturing Module/Stock Requirement List.png]]
Queries based on material, shows availability of inventory. Pre MRP Run PIR's show without any planned orders. After MRP runs the materials are met with planned orders to cover the PIR's.
![[Manufacturing Module/Stock Requirements List.png]]
## Production Order Data Elements
![[Manufacturing Module/Production Order Data Elements.png]]

![[Manufacturing Module/Production Order Header.png]]

### Production Order Header - Operations
Work Center Number
Control Key - Used to control and identify gateway operations
Standard Values - Unit of Measure
Quantity/Dates
### Operation Line
#### Material Components
- Drives the sequencing of materials consumption
- Item Category - Business Qualitative Factors (e.g. Stock vs Non-Stock[one time purchase]).
#### Production Resources and Tools (PRT)
- PRT Number
- PRT Type - Grouping Field
- Qty/Date Requirements for Capacity
##### Trigger Points
Order Processing automation. Rework etc
##### Confirmations
Final recording of operations data 
# Production Order Life Cycle
![[Manufacturing Module/Production Order Lifecycle.png]]

## Release Production Order Process
![[Manufacturing Module/Release Production Order Process.png]]

Red in the "Coverage" field indicates the component production orders haven't been confirmed
![[Manufacturing Module/Coverage.png]]

Releasing the Production Order Header will release the component shop orders and confirm their quantities.
![[Manufacturing Module/Manage Production Orders Confirmed.png]]

## Pick Components for Production Orders
![[Manufacturing Module/Pick Components for Production Orders.png]]

Header Level Search
![[Manufacturing Module/Production Order Header Level.png]]

![[Manufacturing Module/Material Requirements.png]]

Pick List can be modified on the Picking screen to reflect any qty or location adjustments
![[Manufacturing Module/Pick materials.png]]
Once the qty and locations are correct the transaction is posted to the production order
## Production Order Relief
![[Manufacturing Module/Production Order Relief.png]]

## Manage Production Operations
![[Manufacturing Module/Manage Production Orders.png]]

This screen flows into "Enter Time Ticket for Production Order"
![[Manufacturing Module/Enter Time Ticket for Production Order.png]]
Filter Values are available to search for the operation to be claimed

## Post Goods Movement
![[Manufacturing Module/Post Goods Movement Txn.png]]

Select 'Goods Receipt' and filter to the Order Number
![[Manufacturing Module/Good Reciept.png]]

Posting the goods receipt will relieve the Production Order to inventory
![[Manufacturing Module/Posting receipt relieves to inventory.png]]
