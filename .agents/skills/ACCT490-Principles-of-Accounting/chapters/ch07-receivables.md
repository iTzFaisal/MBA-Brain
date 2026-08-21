# Chapter 7: Reporting and Analyzing Receivables

## Core Idea
Receivables are claims that convert credit sales or lending into future cash. Good accounting keeps customer-level records, estimates uncollectibles so receivables are reported at net realizable value, recognizes note interest in the right periods, and distinguishes selling receivables from pledging them as loan collateral.

## Frameworks Introduced
- **Control-account and subsidiary-ledger procedure**: Record a credit sale by debiting Accounts Receivable and Sales, and maintain a separate account for each customer. The general-ledger Accounts Receivable control balance must equal the total of the customer accounts in the accounts receivable subsidiary ledger. Collections credit both the control account and the customer's account. Third-party credit card sales either debit Cash immediately or debit Accounts Receivable--Credit Card Company until payment; record the card fee as Credit Card Expense and record COGS separately under a perpetual system.
- **Direct write-off method**: When a specific account is determined uncollectible, debit Bad Debts Expense and credit that customer's Accounts Receivable. It is simple and requires no estimate, but it commonly fails the matching principle and temporarily overstates receivables and income. Use it only when bad debts are immaterial. A recovery requires two entries: reinstate the receivable, then record cash.
- **Allowance method**: Estimate the loss in the period of related credit sales with `Dr Bad Debts Expense / Cr Allowance for Doubtful Accounts`. The allowance is a contra asset, so `Accounts Receivable - Allowance` reports expected cash collections. Later write-offs debit the allowance and credit the customer's receivable; they do not create new expense or change net realizable receivables. A recovery first reverses the write-off, then records cash.
- **Three bad-debt estimation methods**: **Percent of sales** (income-statement method) computes `credit sales x uncollectible rate = Bad Debts Expense`; the existing allowance balance is ignored for the adjustment. **Percent of receivables** (balance-sheet method) computes `ending Accounts Receivable x rate = target allowance`; the entry brings the unadjusted allowance to that target. **Aging of receivables** classifies balances by days past due, applies a different uncollectible rate to each class, and totals the results as the target allowance; it is usually the most reliable because it examines specific accounts.
- **Notes receivable procedure**: A promissory note states principal, interest rate, maker, payee, and maturity. Record a note received at principal. Compute interest as `principal x annual rate x time fraction`; the chapter uses the 360-day banker's rule. At maturity, debit Cash and credit Notes Receivable and Interest Revenue. If dishonored, remove the note and charge the maker's Accounts Receivable for principal plus accrued interest. Accrue Interest Receivable and Interest Revenue at period-end for interest earned but not yet collected.
- **Disposal before maturity**: Sell receivables to a factor for cash less a factoring fee; ownership and bad-debt risk pass to the factor. Or pledge receivables as security for a loan; ownership and risk remain with the borrower, which records Notes Payable and discloses the pledged collateral.
- **Receivables analysis**: Accounts receivable turnover is `Net sales / average Accounts Receivable, net`, where average balance is `(beginning + ending) / 2`. A high turnover relative to competitors can support more liberal credit terms; a low turnover signals stricter credit and stronger collection efforts. Average collection days can be estimated as `365 / turnover`.

## Key Concepts
- **Accounts receivable**: Amounts due from customers for credit sales.
- **Accounts receivable subsidiary ledger**: Customer-by-customer record supporting the general-ledger control account.
- **Credit card expense**: Fee paid to a third-party card company for processing a sale.
- **Bad debts**: Amounts from credit sales that will not be collected.
- **Allowance for Doubtful Accounts**: Contra asset recording estimated uncollectibles.
- **Net realizable value**: Expected cash collection, or gross receivables less the allowance.
- **Direct write-off method**: Recognizes bad-debt expense only when a specific account is written off.
- **Aging of accounts receivable**: Estimation method based on days each receivable is past due.
- **Promissory note**: Written promise to pay a specified amount, usually with interest, on demand or at a definite date.
- **Maturity date**: Date when a note's principal and interest are due.

## Mental Models
- **Choose the estimation method by the question**: Use percent of sales to match bad-debt expense with current credit sales; use percent of receivables or aging to make the ending allowance and receivables balance realistic. Do not confuse an expense target with an allowance-balance target.
- **Separate estimate time from write-off time**: Estimate expected losses now, then remove specific accounts later against the allowance. A write-off is not a second bad-debt expense.
- **Treat a note as a timeline**: Identify the principal, annual rate, days or months, maturity date, and which reporting period earned each portion of interest before journalizing.
- **Distinguish sale from collateral**: Factoring provides earlier cash and transfers receivable ownership/risk for a fee; pledging provides a loan while the borrower retains the receivable and must disclose the security interest.

## Anti-patterns
- **Using direct write-off for material receivables**: It records expense after the related sale and can overstate current net receivables and income.
- **Debiting Bad Debts Expense for an allowance-method write-off**: The expense was recognized in the estimate; the write-off debits Allowance for Doubtful Accounts.
- **Using the unadjusted allowance balance with percent of sales**: The sales method sets current-period expense directly; balance-sheet methods target an ending allowance and then adjust for its existing debit or credit balance.
- **Leaving a dishonored note in Notes Receivable**: Transfer principal plus earned interest to the maker's Accounts Receivable so collection activity and credit history remain visible.
- **Treating a pledge like a sale**: Pledging does not transfer ownership or bad-debt risk; record the borrowing and disclose the collateral.

## Worked Example
TechCom has $300,000 of first-year credit sales and $20,000 of ending Accounts Receivable. Experience indicates $1,500 will be uncollectible. The allowance adjustment is:

```text
Dr Bad Debts Expense                         $1,500
    Cr Allowance for Doubtful Accounts                  $1,500
```

The balance sheet reports $20,000 gross receivables less $1,500 allowance, or $18,500 expected cash collections. If J. Kent's $520 account is later identified as uncollectible, record `Dr Allowance for Doubtful Accounts $520 / Cr Accounts Receivable--Kent $520`; net realizable value remains $18,500. If Kent later pays in full, first reinstate the receivable with the reverse entry, then debit Cash and credit Accounts Receivable for $520.

## Key Takeaways
1. Reconcile the subsidiary ledger to the Accounts Receivable control account and distinguish direct credit sales from card-company receivables.
2. Use the allowance method for material uncollectibles so expense matches credit sales and receivables show expected cash.
3. For balance-sheet methods, calculate the target allowance first and adjust from the unadjusted debit or credit balance.
4. Record note interest by time period, and move a dishonored note plus accrued interest back to the maker's receivable.
5. Sell receivables when paying a fee to transfer collection risk is worthwhile; pledge them when borrowing while retaining ownership is preferable.
6. Compare turnover and collection days with competitors and prior periods before changing credit policy.

## Connects To
- **Chapter 3**: Uses adjusting entries for accrued interest and estimated bad debts, plus the three-step adjustment process.
- **Chapter 4**: Extends credit-sale, sales-return, COGS, and perpetual-inventory entries.
- **Chapter 6**: Bank reconciliations may reveal NSF checks, note collections, and card-company deposits.
- **Chapter 9**: Receivables and notes are current assets whose collection and valuation affect liquidity analysis.
