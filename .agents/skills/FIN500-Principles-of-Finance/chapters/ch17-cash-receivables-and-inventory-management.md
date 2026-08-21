# Chapter 17: Cash, Receivables, and Inventory Management

## Core Idea
Current-asset management creates value by holding the minimum liquid resources that keep operations reliable, collecting receivables without destroying profitable sales, and holding enough inventory to uncouple operations without paying for unnecessary stock. The central decisions are timing, risk, and the opportunity cost of cash tied up in operating assets.

## Frameworks Introduced
- **Cash-management risk-return framework**
  - When to use: When setting cash and near-cash balances.
  - How: Separate the transactions motive (ordinary payments), precautionary motive (uncertain needs), and speculative motive (anticipated bargains). Meet the two objectives: keep enough cash for disbursements and minimize idle cash that earns little or no return. Use marketable securities for part of the precautionary buffer when liquidity permits.
- **Float-reduction framework**
  - When to use: When customer payments arrive but cannot yet be used.
  - How: Map collection float into mail float, processing float, and availability float. Accelerate receipts through faster internal processing, lockbox arrangements, and concentration banking; slow and control disbursements without violating obligations. The before-tax annual value of a one-day reduction is `daily receipts * investment yield`.
- **Marketable-securities selection**
  - When to use: When investing temporary excess cash.
  - How: Evaluate financial risk, interest-rate risk, liquidity, taxability, and yield. Prefer short maturities when cash may be needed, because longer maturities have greater price sensitivity. Compare after-tax yields; the taxable equivalent of a tax-exempt yield `r*` is `r = r* / (1 - T)`.
- **Credit-policy framework**
  - When to use: When deciding which customers receive credit and how aggressively to collect.
  - How: Recognize that credit-sales percentage and sales level are largely nondecision variables; manage terms of sale, customer quality, and collection effort. Use `a/b, net c` terms, credit scoring, aging, collection ratios, and escalating dunning efforts. Weigh added sales against investigation, default, and collection costs.
- **Altman Z-score**
  - When to use: As a screening signal for a business customer's near-term bankruptcy risk.
  - How: `Z = 3.3(EBIT/TA) + 1.0(Sales/TA) + 0.06(MVE/BVD) + 1.4(RE/TA) + 1.2(WC/TA)`. A score below 2.7 was associated in the chapter with firms tending to fail within a year; use it as a model signal, not a guarantee.
- **Inventory buffer and EOQ framework**
  - When to use: When deciding how much to order and when to reorder.
  - How: Separate raw materials, work-in-process, and finished goods by the operation each buffer uncouples. Minimize `total inventory cost = carrying cost + ordering cost`, with `total carrying cost = (Q/2)C`, `total ordering cost = (S/Q)O`, and `EOQ Q* = sqrt(2SO/C)`. Reorder at `delivery-time stock + safety stock`; average inventory becomes `Q/2 + safety stock`.

## Key Concepts
- **Cash**: Currency, coins, and demand deposits.
- **Marketable securities**: Low-risk investments quickly convertible to cash.
- **Float**: Time between a customer's payment and the firm's ability to use the funds.
- **Insolvency**: Inability to meet interest or principal obligations when due.
- **Terms of sale**: Discount, discount period, and total credit period offered to customers.
- **Credit scoring**: Numerical evaluation of applicants against a predetermined standard.
- **Raw-materials inventory**: Purchased inputs awaiting production.
- **Work-in-process inventory**: Partially finished goods awaiting further work.
- **Finished-goods inventory**: Completed goods awaiting sale.
- **Safety stock**: Inventory held for unexpectedly high usage during delivery time.

## Mental Models
- **Cash is a special inventory**: It uncouples payment from collection, but idle cash has an opportunity cost.
- **Every buffer buys reliability**: Receivables and inventory reduce operating friction, but the firm pays carrying, default, storage, and capital costs for that protection.
- **Credit policy is an incremental decision**: Grant credit only when the expected contribution from additional sales exceeds investigation, collection, default, and tied-up-capital costs.
- **EOQ balances two opposing curves**: Larger orders reduce ordering frequency but increase carrying cost; smaller orders do the reverse.

## Anti-patterns
- **Keep excess cash without measuring its yield**: Liquidity protects against insolvency, but idle balances reduce profitability.
- **Reduce collection time at any cost**: Collection expense and lost customer goodwill can exceed the value of faster cash.
- **Judge credit policy only by zero bad debts**: Refusing good customers can destroy profitable sales; evaluate the complete incremental economics.
- **Treat EOQ as a universal answer**: Variable demand, quantity discounts, changing carrying or ordering costs, delayed delivery, and joint orders require modifications or safety stock.
- **Invest cash in long-maturity securities for a small yield pickup**: A rate increase can cause a large price loss exactly when liquidity is needed.

## Worked Example
An inventory item has annual demand `S = 5,000` units, ordering cost `O = $200` per order, and carrying cost `C = $2` per unit per year.

`Q* = sqrt((2 * 5,000 * $200) / $2) = 1,000 units`

Ordering 1,000 units each time balances the annual carrying and ordering costs under the EOQ assumptions. If demand or delivery is uncertain, add safety stock and reorder when inventory reaches delivery-time stock plus safety stock; do not use the basic EOQ alone.

## Key Takeaways
1. Cash management is a balance between avoiding insolvency and minimizing low-return idle balances.
2. Measure mail, processing, and availability float separately; a one-day release has value equal to daily receipts times the investable yield.
3. Compare marketable securities on risk, interest-rate sensitivity, liquidity, taxability, and yield, not yield alone.
4. Control receivables through terms, customer selection, credit scoring, aging, and disciplined collection effort.
5. Use EOQ for order size and delivery-time stock plus safety stock for reorder timing; test the model's assumptions.

## Connects To
- **Chapter 14**: Cash budgets depend on collection lags, payment timing, and inventory purchases.
- **Chapter 15**: DSO, DSI, and DPO aggregate these asset and liability policies into the cash conversion cycle.
- **Chapter 16**: Foreign-currency cash, receivables, inventory, and marketable securities add exchange-rate risk.
- **Appendix A**: Present-value, yield, and cash-flow calculations support security and investment decisions.
