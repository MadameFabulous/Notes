T-Codes

MM02 = Part

MD61 = Planned Independ Requirements Creation(PIR) - Forecast

MD04 = Stock Requirements List

Planning Strategy 10 - Made to Stock Production

Planning Strategy 40 - Planning with Final Assembly

Planning Strategy 70 - Planning at Assembly Level

Planning Strategy 20 - Made-to-Order Production

Planning Strategy 50 - Planning without Final Strategy

Planning Strategy 60 - Planning with Planning Material

Planning Strategy 70  - MTO Strategy?

Planning Strategy 82 - Assembly Processing

Modes

![](C:\Users\wright\AppData\Roaming\marktext\images\2023-08-16-07-08-32-image.png)

Mode 1 - Backward Consumption

The customer requirement consumes planned independent requirements that come before it

![](C:\Users\wright\AppData\Roaming\marktext\images\2023-08-16-06-57-23-image.png)

Mode 2 - Backward and Forward Consumption

Consumes past requirements before forward requirements

Mode 3 - Forward Consumption

The customer requirement consumes planned independent requirements that come after it

![](C:\Users\wright\AppData\Roaming\marktext\images\2023-08-16-06-58-12-image.png)

Mode 4 - Backward and Forward Consumption

Consumes future requirements before past requirements

Mode 5 - Period Specific Consumption

Only planned independent requirements in the related period are consumed

Individual vs Collective

MRP S/4HANA

MRP Process Steps

1. BOM Explosion & Backward Scheduling

2. 

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

ROP is considered consumption based planning

![](https://learning.sap.com/service/media/topic/d80db90d-b3ad-4c97-bb31-ba49d260ce82/S42000_23_en-US_media/S42000_23_en-US_images/U3_L1_01.png)

## BOM Explosion and Multilevel Backward Scheduling

Backwards scheduling date is based on the requirement date of the finished product which is driven by the sales order.

![](https://learning.sap.com/service/media/topic/d80db90d-b3ad-4c97-bb31-ba49d260ce82/S42000_23_en-US_media/S42000_23_en-US_images/U3_L1_02.png)

## Second Step of the MRP Process – Net Requirements Calculation and Lot Sizing

Lot sizing, and rescheduling horizon considered and checked against safety stock and requirements 

![](https://learning.sap.com/service/media/topic/d80db90d-b3ad-4c97-bb31-ba49d260ce82/S42000_23_en-US_media/S42000_23_en-US_images/MRP_Basics_004.png)

## Third Step of the MRP Process – Procurement Types

![](C:\Users\wright\AppData\Roaming\marktext\images\2023-08-17-06-42-09-image.png)

Type E: In-house production

Type F: External Procurement

Type X: Both Procurement Types

## Fourth Step of the MRP Process – Scheduling

![](C:\Users\wright\AppData\Roaming\marktext\images\2023-08-17-06-52-45-image.png)

Determination of Basic Dates for Planned Orders

Milestone based ordering dictated by Master Material File

Opening Period - Order Placement Time

In-house Production time - Sum total of operations and internal lead times

Lead Time Scheduling and Capacity Planning

![](https://learning.sap.com/service/media/topic/d80db90d-b3ad-4c97-bb31-ba49d260ce82/S42000_23_en-US_media/S42000_23_en-US_images/U3_L2_01.png)

## MRP Live

![](C:\Users\wright\AppData\Roaming\marktext\images\2023-08-17-07-30-32-image.png)

pMRP - Predictive MRP

![](C:\Users\wright\AppData\Roaming\marktext\images\2023-08-17-07-42-32-image.png)

![](C:\Users\wright\AppData\Roaming\marktext\images\2023-08-21-05-40-47-image.png)

## ![](C:\Users\wright\AppData\Roaming\marktext\images\2023-08-21-05-48-13-image.png)

## Maintain PIR's

Select Material

![](C:\Users\wright\AppData\Roaming\marktext\images\2023-08-21-05-46-19-image.png)

Enter a Forecast per week for the material, save the record. Then turn the PIR to active "Version is Active" flag.

![](C:\Users\wright\AppData\Roaming\marktext\images\2023-08-21-05-47-34-image.png)

## Stock Requirements List

![](C:\Users\wright\AppData\Roaming\marktext\images\2023-08-21-05-50-21-image.png)

Queries based on material, shows availability of inventory. Pre MRP Run PIR's show without any planned orders. After MRP runs the materials are met with planned orders to cover the PIR's.

![](C:\Users\wright\AppData\Roaming\marktext\images\2023-08-21-05-53-27-image.png)

## Production Order Data Elements

![](https://learning.sap.com/service/media/topic/db840dee-a409-4f3c-b81f-304ce922509e/S42000_23_en-US_media/S42000_23_en-US_images/U5_L2_02_Prod_Ord_Struct.png)

![](C:\Users\wright\AppData\Roaming\marktext\images\2023-08-21-06-12-05-image.png)

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

![](C:\Users\wright\AppData\Roaming\marktext\images\2023-08-21-06-45-38-image.png)

## Release Production Order Process

![](C:\Users\wright\AppData\Roaming\marktext\images\2023-08-21-06-47-23-image.png)

Red in the "Coverage" field indicates the component production orders haven't been confirmed

![](C:\Users\wright\AppData\Roaming\marktext\images\2023-08-21-06-48-31-image.png)

Releasing the Production Order Header will release the component shop orders and confirm their quantities.

![](C:\Users\wright\AppData\Roaming\marktext\images\2023-08-21-06-52-45-image.png)

## Pick Components for Production Orders

![](C:\Users\wright\AppData\Roaming\marktext\images\2023-08-21-06-55-25-image.png)

Header Level Search

![](C:\Users\wright\AppData\Roaming\marktext\images\2023-08-21-06-57-37-image.png)



![](C:\Users\wright\AppData\Roaming\marktext\images\2023-08-21-06-58-10-image.png)

Pick List can be modified on the Picking screen to reflect any qty or location adjustments

![](C:\Users\wright\AppData\Roaming\marktext\images\2023-08-21-06-58-43-image.png)

Once the qty and locations are correct the transaction is posted to the production order

## Production Order Relief

![](C:\Users\wright\AppData\Roaming\marktext\images\2023-08-21-07-01-00-image.png)

## Manage Production Operations

![](C:\Users\wright\AppData\Roaming\marktext\images\2023-08-21-07-14-30-image.png)

This screen flows into "Enter Time Ticket for Production Order"

![](C:\Users\wright\AppData\Roaming\marktext\images\2023-08-21-07-15-23-image.png)

Filter Values are available to search for the operation to be claimed

## Post Goods Movement

![](C:\Users\wright\AppData\Roaming\marktext\images\2023-08-21-07-18-55-image.png)

Select 'Goods Receipt' and filter to the Order Number

![](C:\Users\wright\AppData\Roaming\marktext\images\2023-08-21-07-19-56-image.png)

Posting the goods receipt will relieve the Production Order to inventory

![](C:\Users\wright\AppData\Roaming\marktext\images\2023-08-21-07-20-24-image.png)
