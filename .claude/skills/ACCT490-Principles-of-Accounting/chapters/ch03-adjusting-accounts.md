# Chapter 3: Adjusting Accounts for Financial Statements

## Core Idea
Periodic reporting makes timely information possible, but some revenues and expenses cross reporting dates. Accrual accounting uses adjusting entries to bring asset and liability balances to their proper amounts and to match revenue and expense recognition, without using the Cash account.

## Frameworks Introduced
- **Three-Step Process for Adjusting Accounts**: Use at every period-end. (1) Determine what the current account balance equals. (2) Determine what it should equal at the reporting date. (3) Record the entry that moves the current balance to the required balance.
- **Framework for Adjustments**: Classify the cash timing first, then choose the entry:

| Type | Cash timing and purpose | Adjusting entry |
|---|---|---|
| Prepaid (deferred) expense | Cash paid before the expense is used | Dr Expense; Cr Asset (or Accumulated Depreciation) |
| Unearned (deferred) revenue | Cash received before revenue is earned | Dr Liability; Cr Revenue |
| Accrued expense | Expense incurred before cash payment or recording | Dr Expense; Cr Liability |
| Accrued revenue | Revenue earned before cash receipt or billing | Dr Asset; Cr Revenue |

Each adjustment affects at least one income-statement account and one balance-sheet account, but never Cash.
- **Accounting Cycle**: Apply the 10 repeating steps: analyze transactions; journalize; post; prepare unadjusted trial balance; adjust; prepare adjusted trial balance; prepare statements; close; prepare post-closing trial balance; and optionally reverse selected adjustments in the next period.
- **Four-Step Closing Process**: Use after statements. (1) Close credit balances in revenue and gain accounts to Income Summary. (2) Close debit balances in expense and loss accounts to Income Summary. (3) Close Income Summary to Retained Earnings. (4) Close Dividends to Retained Earnings.
- **Classified Balance Sheet Structure**: Separate current and noncurrent assets and liabilities. Current means expected to be collected or owed within one year or the operating cycle, whichever is longer; noncurrent assets include long-term investments, plant assets, and intangible assets.
- **Decision Analysis Ratios**: Profit margin is `Net income / Net sales`; current ratio is `Current assets / Current liabilities`. Use benchmarks and investigate the composition of the balances, not just the quotient.

## Key Concepts
- **Accrual basis accounting**: Recognizes revenue when earned and expenses when incurred, rather than when cash changes hands.
- **Cash basis accounting**: Recognizes revenue on receipt and expense on payment; it is not consistent with GAAP or IFRS.
- **Prepaid expense**: An asset representing future benefits that becomes expense as time passes or the item is used.
- **Unearned revenue**: A liability representing the remaining obligation to deliver products or services.
- **Accrued expense**: An incurred, unpaid, and unrecorded cost such as salaries or interest.
- **Accrued revenue**: Revenue earned but unrecorded and not yet received in cash.
- **Depreciation**: Allocation of a plant asset's cost over its expected benefit period, not a measure of market-value decline.
- **Accumulated depreciation**: A contra account with a credit balance that is subtracted from asset cost.
- **Adjusted trial balance**: Ledger balances after adjustments, used to prepare statements.
- **Temporary/permanent accounts**: Income statement, Dividends, and Income Summary accounts reset; balance-sheet accounts carry forward.

## Mental Models
- **Use the current-to-should bridge**: Do not guess an adjustment from the account name; calculate the balance already recorded, the balance required, and the difference.
- **Think "recognition follows consumption or performance"**: Expire a prepaid asset as benefits are used and release a liability as services are delivered.
- **Use no-cash as a diagnostic**: If a proposed adjusting entry debits or credits Cash, it is probably a regular transaction rather than an adjustment.
- **Treat closing as reset plus carry-forward**: Temporary accounts measure the new period; Retained Earnings carries the cumulative result.

## Anti-patterns
- **Using cash timing to measure income**: Paying a 24-month insurance premium is not a one-period expense under accrual accounting.
- **Leaving prepaids and unearned revenue untouched**: Assets, liabilities, revenue, expense, and net income become misstated.
- **Recording depreciation directly against the asset cost**: A separate accumulated-depreciation contra account preserves both original cost and cumulative allocation.
- **Closing permanent accounts**: Assets, liabilities, Common Stock, and Retained Earnings must carry their balances into the next period.
- **Assuming a work sheet is the accounting record**: It is a planning tool; adjustments still must be journalized and posted.

## Worked Example
FastForward applies the three-step process at December 31. Its key adjustments are:

```text
Insurance:    Dr Insurance Expense                    100
                  Cr Prepaid Insurance                              100
Supplies:     Dr Supplies Expense                   1,050
                  Cr Supplies                                     1,050
Depreciation: Dr Depreciation Expense--Equipment      300
                  Cr Accumulated Depreciation--Equipment             300
Unearned:     Dr Unearned Consulting Revenue          250
                  Cr Consulting Revenue                            250
Accrued pay:  Dr Salaries Expense                     210
                  Cr Salaries Payable                              210
Accrued rev.: Dr Accounts Receivable                1,800
                  Cr Consulting Revenue                          1,800
```

The amounts come from one month of a $2,400/24-month policy (`$100`), a physical supplies count of $8,670 versus $9,720 recorded (`$1,050` used), straight-line depreciation `($26,000 - $8,000) / 60 months = $300`, five days of a $3,000/60-day service contract (`$250`), three unpaid days at $70 (`$210`), and 20 of 30 days of a $2,700 consulting contract (`$1,800`). After posting, revenues are $8,150, expenses $4,365, net income $3,785, and ending retained earnings $3,585 after a $200 dividend. The adjusted balance sheet totals $42,745 on both sides. Closing then resets revenues, expenses, and dividends; the post-closing trial balance contains only permanent accounts.

## Key Takeaways
1. Apply the three-step current/should/difference process rather than relying on memorized amounts.
2. Use accrual accounting to report the period's earned revenue and incurred costs.
3. Prepare the adjusted trial balance before statements, in the order income statement, retained earnings, and balance sheet.
4. Close only temporary accounts and verify that permanent debits equal permanent credits.
5. Classify current items using one year or the operating cycle, whichever is longer.

## Connects To
- **Chapter 1**: Implements the time-period, revenue-recognition, and expense-recognition principles.
- **Chapter 2**: Starts with the unadjusted ledger and trial balance produced by journalizing and posting.
- **Chapter 4**: Adds inventory shrinkage, sales-discount, and returns estimates to the adjustment process for merchandisers.
- **Financial analysis**: Adjustments change profit margin, current ratio, asset balances, and reported operating performance.
