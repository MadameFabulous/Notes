Pick Up here Tomorrow
![[Pasted image 20230906075440.png]]




![[FI and CO Flows - Video - identifying-the-areas-of-financial-and-management-accounting_.png]]
# Accounting Definitions
![[FI vs CO Expenses and Income.png]]
## Financial Accounting(FI)
Financial Accounting itself consists of different areas: The General Ledger (G/L) and various subledgers. The goal of FI is to manage expenses and income.
![[FI - You are here diagram for BTP.png]]
## Managerial Accounting(CO)
Short for Controlling. Specifically accounting for the costs and revenues.

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
#### Account Type
![[Account Type By Domain.png]]
##### Cash Account
G/L Accounts Range 10000000-39999999
- Balance Sheet Reporting for FI
- Manage all bank accounts via a single reconciliation
##### Balance Sheet Account
G/L Accounts Range 10000000-39999999
- Only used in reporting for the Balance Sheet
- Not relevant to CO
##### Non Operating Expense or Income
G/L Accounts Range 40000000-79999999
- Income Statement Account used by FI that reports revenues from activities that are not part of the main purpose of the company.
- Defined by a lack of cost or revenue elements (Non-Recurring Activities usually)
##### Primary Costs or Revenue
G/L Accounts Range 40000000-79999999
- Income Statement Account used by FI that tracts the primary operating costs
- Primary Costs will automatically generates the corresponding cost or revenue postings
##### Secondary Costs
G/L Accounts Range 90000000-99999999
- Result from value flows within the organization such as internal activity cost allocations, overhead allocations, and settlement transactions.
- Only used for CO
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
## Money
- Manage Payments
- Manage Disputes
#### G/L Account Master Data
##### GL Account

##### Cost Element Categories
- Maintained on the G/L Account Master Data>Controlling Data Tab
- Flag for whether this account is used in CO
- Dictated by the Account Type from the G/L Account Master Data>General Tab
- How it can be used and the balances can be transferred
![[Cost Element Categories.png]]
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

## Managing Accounts Payable

### Business Partner
The Business Partner is the SAP term for vendor or client. These are maintained as master data on the client which is shared all users of the SAP ecosystem.

Company Code views of the Business Partners allow for specific configurations for localities like VAT's, payment methos, and banks.

### 