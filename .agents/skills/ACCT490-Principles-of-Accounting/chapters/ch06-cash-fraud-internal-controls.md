# Chapter 6: Reporting and Analyzing Cash, Fraud, and Internal Controls

## Core Idea
Cash is the most liquid asset and the easiest to hide, move, or steal. Internal control combines assigned responsibility, independent records, separation of duties, technology, and review to protect cash and produce reliable accounting; bank reconciliations then explain the remaining differences between the bank's record and the company's Cash account.

## Frameworks Introduced
- **Internal control system**: Policies and procedures should protect assets, ensure reliable accounting, promote efficient operations, and urge adherence to company policies. For public companies, the Sarbanes-Oxley Act (SOX) requires management documentation and certification and auditor evaluation; Section 404 focuses on controls affecting financial reporting. COSO organizes control into the control environment, control activities, risk assessment, monitoring, and information and communication.
- **Seven principles of internal control**: (1) establish responsibilities; (2) maintain adequate records; (3) insure assets and bond key employees; (4) separate recordkeeping from custody of assets; (5) divide responsibility for related transactions; (6) apply technological controls; and (7) perform regular and independent reviews. Assign one accountable person, preserve prenumbered or electronic evidence, divide purchasing/receiving/payment, restrict access, and have an independent person review results.
- **Fraud triangle and control limits**: Opportunity comes from control deficiencies, pressure from financial or personal stress, and rationalization from justifying the act. Human error, management override, collusion, and the cost-benefit principle limit every control system; controls lower risk but do not guarantee prevention.
- **Cash control guidelines**: Keep cash handling separate from cash recordkeeping, deposit receipts promptly (preferably daily), and make disbursements by check or electronic funds transfer. Cash equivalents are short-term investments readily convertible to a known cash amount and purchased within about three months of maturity so market value is not sensitive to interest changes.
- **Receipt procedures**: For over-the-counter sales, enter each sale in a customer-visible register, issue a receipt, preserve the locked-in record, and compare the clerk's cash count with register data through a cashier and an independent supervisor. For mail receipts, two employees open the mail and prepare a triplicate list; copies go with the money, to accounting, and to the mail clerks. The cashier deposits, the recordkeeper posts, and another person reconciles the bank.
- **Voucher and petty-cash procedures**: A voucher system verifies, approves, and records obligations before checks are issued. A purchase requisition, purchase order, receiving report, invoice, and approval trail divide requesting, purchasing, receiving, accounting, and cashier duties. Petty cash is an imprest fund for small business payments: signed prenumbered receipts plus remaining cash must equal the fund, and reimbursement restores the fund while recording expenses.
- **Bank reconciliation**: Reconcile the bank statement and book Cash balances using nine steps: identify the bank balance; add deposits in transit and bank errors understating it; deduct outstanding checks and bank errors overstating it; compute adjusted bank balance; identify book balance; add unrecorded collections, interest, and book-understatement errors; deduct NSF items, bank charges, and book-overstatement errors; compute adjusted book balance; and verify that both adjusted balances agree. Only book-side unrecorded items require journal entries.
- **Days' sales uncollected**: Use `Accounts receivable / Net sales x 365` to estimate how long current receivables take to convert to cash. Compare the result with prior periods and industry peers rather than treating one number as universally good.

## Key Concepts
- **Liquidity**: Ability to pay near-term obligations.
- **Cash equivalent**: A short-term, highly liquid investment meeting the known-amount and near-maturity criteria.
- **Internal control system**: Policies and procedures used to protect assets and make operations and accounting reliable.
- **Separation of duties**: Dividing custody, authorization, recordkeeping, and review so one person cannot both steal and conceal.
- **Fraud triangle**: Opportunity, pressure, and rationalization that together explain fraud risk.
- **SOX Section 404**: Requirement to document and assess internal controls affecting public-company financial reporting.
- **Voucher system**: Documentation and approval process controlling obligations and cash disbursements.
- **Imprest petty-cash system**: A fixed fund replenished for documented payments.
- **NSF check**: A deposited check returned because the maker's bank account lacks sufficient funds.
- **Bank reconciliation**: A report explaining and correcting differences between bank and book cash balances.

## Mental Models
- **Create two independent trails**: For every cash flow, require an operational record and an independent bank or review record. A person who handles cash should not control the record that proves what happened.
- **Classify by the first recorder**: Timing items already recorded by one party stay on the reconciliation with no entry; an item first recorded by the bank, such as a fee, interest, collection, or NSF check, belongs on the book side and needs an entry.
- **Remove opportunity before blaming character**: Use the fraud triangle to ask which access, pressure, or justification is present, then add segregation, review, documentation, or support rather than relying on trust alone.
- **Use technology as evidence, not as segregation**: Registers, access logs, passwords, encryption, and locked files reduce errors and preserve evidence, but a programmer should not operate the system or control cash disbursements.

## Anti-patterns
- **Letting one employee receive cash, post it, and reconcile it**: The employee can conceal a shortage; the owner or an independent reviewer must compensate when staffing is small.
- **Recording timing differences as adjustments**: Deposits in transit and outstanding checks are already in the books; journalizing them duplicates the transaction.
- **Using petty cash for ordinary payments**: It weakens the check-based audit trail and defeats the fund's purpose as an exception for small expenses.
- **Assuming automation removes fraud risk**: Bad data, erroneous software, collusion, management override, and lost separation of duties remain possible.
- **Treating a reconciliation as proof that controls worked**: It detects many errors and frauds after the fact; it does not replace authorization, custody, documentation, and independent review.

## Worked Example
VideoBuster's October 31 bank balance is $2,050 and its book balance is $1,404.58. The bank-side adjustments are a $145 deposit in transit and outstanding checks of $150 and $200:

```text
Adjusted bank = $2,050 + $145 - $150 - $200 = $1,845
Adjusted book = $1,404.58 + ($500 - $15 note collection)
                + $8.42 interest - $23 check charge - ($20 NSF + $10 fee)
              = $1,845
```

The book entries record only the unrecorded items: Dr Cash $485, Dr Collection Expense $15, Cr Notes Receivable $500; Dr Cash $8.42, Cr Interest Revenue $8.42; Dr Miscellaneous Expense $23, Cr Cash $23; and Dr Accounts Receivable $30, Cr Cash $30 for the NSF check and fee. The deposit in transit and outstanding checks receive no entry.

## Key Takeaways
1. Separate custody, authorization, recordkeeping, and review whenever cash or cash equivalents are involved.
2. Deposit receipts promptly and use checks or EFTs for disbursements to create independent evidence.
3. Use vouchers, receiving evidence, approvals, and divided responsibilities before releasing payment.
4. Reconcile bank and book balances systematically; post only book-side reconciling items.
5. Treat human error, collusion, override, and cost as design constraints, not reasons to abandon controls.
6. Monitor days' sales uncollected to connect receivables policy with cash availability.

## Connects To
- **Chapter 2**: Relies on source documents, journals, ledgers, and subsidiary records as control evidence.
- **Chapter 3**: Bank-reconciliation entries and petty-cash adjustments are period-end accounting procedures.
- **Chapter 5**: Applies independent counts, restricted access, and records to inventory control.
- **Chapter 7**: Uses NSF checks, note collections, receivables, and collection speed in cash management.
