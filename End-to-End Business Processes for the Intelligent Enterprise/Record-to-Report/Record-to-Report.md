![[End-to-End Business Processes for the Intelligent Enterprise/Record-to-Report/FI and CO Flows - Video - identifying-the-areas-of-financial-and-management-accounting_.png]]
# Financial Accounting(FI)
Financial Accounting itself consists of different areas: The General Ledger (G/L) and various subledgers.
![[End-to-End Business Processes for the Intelligent Enterprise/Record-to-Report/FI - You are here diagram for BTP.png]]
# Managerial Accounting(CO)


# Record-to-Report Process
## Creditworthiness
- Manage Credit Limits
## Master Data & Financial Transactions
### Manage G/L Accounting
#### Basic Data for Chart of Accounts
General Tab
- G/L Account Number
- Account Description (Long Name)
- Translation Information (Account Name in Other Languages)
Account Company Code Data Tab
- Controlling Area
- Company Code
Company Code Assignment Tab
- Control Data Tab
	- Account Currency
	- "Only Balance in Local Currency"
- Create/Bank/Interest Tab
	Additional controls for the behavior of the account can be found here. An Example is the "Post Automatically Only" field which controls whether an account can be use for manual posting transactions
#### SAP G/L Accounts Default Configuration
	Default Account Grouping Headers for the YCOA (??? Chart of Accounts)
##### 1XXXXXXX
- Bank
- Petty Cash
- Fixed Asset Accounts
##### 2XXXXXXX
- Trade Payables
- Tax Accounts
- Accrued Net Payroll Accounts
##### 3XXXXXXX
- Share Capital Accounts
##### 4XXXXXXX
- Revenue
- Discount
- Deduction
##### 5XXXXXXX
- Material Consumption
- Inventory Change
##### 6XXXXXXX
- Travel Costs
- Payroll
- Operating Expense Accounts
##### 7XXXXXXX
- Interest
- Valuation Loss and Gain Accounts (Shareholder Equity)
- Tax Accounts
#### Checking G/L in SAP Fiori
##### Navigation
![[SAP Fiori Ledger.png]]
Manage Chart of Accounts
![[Manage Chart of Accounts.png]]
- Chart of Accounts shows the Master Data level. Identical for all companies
- Company Code View allows for site specific accounts
![[Chart of Accounts and Company Code View.png]]

#### Checking Global Hierarchies
##### Manage Global Hierarchies
![[Manage Global Hierarchies.png]]
##### Select Financial Statement Version
![[Manage Global Hierarchies - Select Financial Statement.png]]

##### View Financial Statement Version Elements
![[View Financial Statement Version Elements.png]]

#### Manage Accounts Payable
#### Manage Accounts Receivable
#### Manage Asset Accounting
#### Financial Close
## Money
- Manage Payments
- Manage Disputes
## Reporting

### General Journal Entry (Manual Journal Entry)
- Most Accounting Txns should automatically post to the correct accounts as a result of the account basic data configuration
- Occasional Manual Journal Entries are needed

#### Components of a Manual Journal Entry
- Document Header
	- Company Code
	- Total Balance
		Total Balance is displayed in the top right. Debit and Credits must be equal
	- Journal Entry Date: Day that document was issued (date of the original document or txn)
	- Posting Date: Day that document was registered in Financial Accounting
	- Journal Entry Type
		- KR - Vendor Invoice
		- ZP - Payment Posting
		- AA - Asset Posting
- Document Items
	- Account Number
		Filtered by the Company Code entered on the Document Header
	- Amount
	- Debit and Credit Assignments

#### Entering Manual Journal Entry SAP Fiori
##### Navigation
![[Post General Journal Entries.png]]
##### Post General Journal Entries
![[Post General Journal Entries - Populated txn.png]]
###### Key Data Elements
- Journal Entry Date
- Posting Date
- Total Balance (Top Right)
	- Displays the balance of the transaction. In order to be a legal transaction both sides of the transaction must be balanced and the total balance must net to zero
- Company Code
- G/L Account
- Debit and Credit Amounts
###### Simulation
	There is an option to simulate a transaction. This will show what the resulting transaction looks like and allows for double checking.
- Simulated Journal Entries have a different naming schema. Once the simulation is posted it will be assigned a journal entry in order of the ledger
![[Simulated Journal Entry.png]]
###### Finished Journal Entry
![[Finished General Journal Entry.png]]
