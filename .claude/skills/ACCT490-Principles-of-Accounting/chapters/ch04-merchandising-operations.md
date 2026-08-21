# Chapter 4: Reporting and Analyzing Merchandising Operations

## Core Idea
A merchandiser buys products and resells them. Its distinctive accounting problem is tracking merchandise inventory as it moves from purchase, to goods available for sale, to cost of goods sold or ending inventory. Under a perpetual system, every sale records both its revenue side and its cost side.

## Frameworks Introduced
- **Merchandiser Income Model**: Use to explain earnings beyond a service company's revenue-minus-expenses model:

```text
Net sales - Cost of goods sold = Gross profit (gross margin)
Gross profit - Other operating expenses +/- Nonoperating items = Net income
```

- **Merchandising Cost Flow**: Use to reconcile inventory and cost of sales:

```text
Beginning inventory + Net purchases = Merchandise available for sale
Merchandise available for sale = Ending inventory + Cost of goods sold
```

Net purchases include invoice cost less purchase discounts and returns/allowances plus transportation-in.
- **Perpetual versus Periodic Inventory Systems**: Use a perpetual system when management needs current units, inventory cost, and sales information; update Merchandise Inventory and Cost of Goods Sold with each transaction. A periodic system leaves inventory unchanged during the period, accumulates purchases in temporary accounts, and computes cost of goods sold after a physical count.
- **Gross Method for Cash Discounts**: Record the full invoice amount. Under terms such as `2/10, n/30`, pay 2% less within 10 days or the full amount within 30 days. A buyer taking the discount credits Merchandise Inventory for the discount; a seller debits Sales Discounts. The net method, described in the appendix, initially records the discounted amount.
- **FOB Ownership Transfer**: Under FOB shipping point, ownership transfers when goods leave the seller; the buyer owns goods in transit and records transportation-in in inventory. Under FOB destination, ownership transfers on arrival; the seller bears freight and records Delivery Expense.
- **Two-Sided Perpetual Sale**: Record the customer asset and Sales, then record Cost of Goods Sold and reduce Merchandise Inventory. This applies the expense-recognition principle at the moment of sale.
- **Merchandising Closing and Adjustments**: Adjust recorded inventory to the physical count for shrinkage; estimate future sales discounts and returns/allowances when required; close Sales, contra-revenue accounts, Cost of Goods Sold, other expenses, Income Summary, and Dividends.
- **Financial Statement Formats**: A multiple-step statement shows net sales, gross profit, operating income, and nonoperating items. A single-step statement groups revenues and expenses and computes one net-income subtotal; both produce the same net income.
- **Decision Analysis**: Acid-test ratio is `(Cash and equivalents + Short-term investments + Current receivables) / Current liabilities`; gross margin ratio is `(Net sales - Cost of goods sold) / Net sales`.

## Key Concepts
- **Merchandise inventory**: Current asset containing products owned and intended for resale, including necessary purchase and inbound freight costs.
- **Net sales**: Sales reduced by Sales Discounts and Sales Returns and Allowances.
- **Cost of goods sold (COGS)**: Cost assigned to merchandise sold during the period.
- **Gross profit/gross margin**: Net sales less COGS.
- **Purchase return**: Merchandise sent back to the seller at the buyer's recorded cost.
- **Purchase allowance**: Reduction in purchase cost for defective goods retained by the buyer.
- **Sales Discounts**: Contra-revenue account for discounts taken by customers.
- **Sales Refund Payable**: Current liability for expected future refunds.
- **Inventory Returns Estimated**: Current asset for the cost of merchandise expected to be returned.
- **Shrinkage**: Inventory loss from theft, deterioration, or error; recorded when physical count is below the perpetual balance.

## Mental Models
- **Use the two-entry sale test**: Ask both "what did the customer give us?" and "what inventory cost left us?" If the cost-side entry is missing, gross profit and inventory are wrong.
- **Treat freight by ownership**: The party that owns goods in transit bears the cost and risk; incoming freight becomes inventory, outgoing freight becomes Delivery Expense.
- **Use liquidity quality, not just quantity**: A strong current ratio can conceal weak quick assets when inventory dominates; compare it with the acid-test ratio and collection timing.
- **Read gross margin as a buffer**: Each sales dollar's gross margin must cover operating costs and still leave profit; compare the ratio with prior periods and industry benchmarks.

## Anti-patterns
- **Recording a merchandise sale as only revenue**: Omitting COGS overstates inventory and gross profit.
- **Treating trade discounts as journalized transactions**: Record the invoice amount net of the trade discount; trade discounts are not separate entries.
- **Charging buyer freight to Delivery Expense**: FOB shipping-point inbound freight is part of inventory cost; Delivery Expense is for seller-paid outbound freight.
- **Applying the discount to returned goods**: The discount applies only to the remaining invoice balance after returns or allowances.
- **Ignoring shrinkage or expected returns**: Perpetual records and reported net sales require period-end estimates and physical verification.

## Worked Example
Need-to-Know 4-2 sells 50 units at $150 each; cost is $100 per unit; terms are `2/10, n/30`.

```text
June 1   Dr Accounts Receivable                 7,500
             Cr Sales                                       7,500
         Dr Cost of Goods Sold                   5,000
             Cr Merchandise Inventory                         5,000

June 7   Dr Sales Returns and Allowances           300
             Cr Accounts Receivable                            300
         Dr Merchandise Inventory                  200
             Cr Cost of Goods Sold                              200

June 11  Dr Cash                                  7,056
         Dr Sales Discounts                         144
             Cr Accounts Receivable                          7,200

June 14  Dr Sales Returns and Allowances            50
             Cr Cash                                             50
```

The two returned units are restored at cost because they are not defective. The June 11 discount is `($7,500 - $300) x 2% = $144`; cash is $7,056. Final net sales are `$7,500 - $300 - $50 - $144 = $7,006`; COGS is `$5,000 - $200 = $4,800`; gross profit is `$2,206` before other expenses.

## Key Takeaways
1. Separate net sales, COGS, and gross profit before evaluating a merchandiser's operating expenses.
2. Under perpetual accounting, record inventory cost at purchase and COGS at every sale.
3. Read credit terms and FOB terms before selecting the payment, discount, or freight entry.
4. Reconcile perpetual inventory to a physical count and record shrinkage.
5. Use both the current ratio and acid-test ratio, then use gross margin to assess profitability capacity.

## Connects To
- **Chapter 1**: Extends the revenue-recognition, expense-recognition, operating-cycle, and financial-statement models.
- **Chapter 2**: Uses source documents, chart of accounts, double-entry journalizing, posting, and trial balances.
- **Chapter 3**: Applies adjusting, closing, and classified-balance-sheet procedures to inventory and sales estimates.
- **Inventory costing**: Later chapters assign costs to ending inventory and COGS under specific identification, FIFO, LIFO, and weighted average.
