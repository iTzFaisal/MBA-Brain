# Appendix D: Reporting and Analyzing Partnerships

## Core Idea
Partnership accounting turns a legal and economic agreement among co-owners into separate capital and withdrawals accounts, an explicit income/loss allocation, and a controlled process for admission, withdrawal, and liquidation. Appendix D is marked as available through Connect/print in the front matter, and the included pages provide the procedures summarized here.

## Frameworks Introduced
- **Business-form choice**: Compare partnership, limited partnership, LLP, LLC, S corporation, and corporation using liability, taxation, management/agency, continuity, ownership transfer, capital needs, and distribution goals. A general partnership has mutual agency, unlimited liability, limited life, pass-through taxation, and jointly owned property; limited partners trade management rights for limited liability, while LLP/LLC rules depend on law and agreement.
- **Formation procedure**: Record each partner's contributed assets at agreed market value, record liabilities assumed, and credit that partner's Capital account for net investment. Maintain a separate capital and withdrawals account for every partner.
- **Income/loss allocation ladder**: Follow the partnership agreement. If no agreement exists, share income and loss equally; if only income is specified, use that ratio for losses. Otherwise use a stated ratio, beginning-capital ratio, or salary allowances plus interest allowances plus an agreed remainder ratio. Salary and interest allowances allocate income; they are not partnership expenses. Close Income Summary to partner capital accounts, then close withdrawals to the respective capital accounts.
- **Partner-admission procedure**: A purchase of an interest from an existing partner is a personal transaction; debit the seller's Capital and credit the buyer's Capital, with no partnership cash or total-equity change. An investment into the partnership increases assets and total equity. Compare the new partner's target equity percentage with the investment to allocate a bonus to old partners or the new partner under the income/loss-sharing ratio.
- **Withdrawal/death procedure**: For a withdrawal paid by partnership assets, debit the departing partner's capital and credit cash/assets. A payment below recorded equity gives a bonus to remaining partners; a payment above it gives a bonus to the withdrawing partner. Death dissolves the partnership; close the books, update current income and asset/liability values, and settle the deceased partner's estate under the contract.
- **Three-step liquidation**: (1) Sell noncash assets and allocate the resulting gain/loss using the income-and-loss-sharing ratio; (2) pay partnership liabilities; (3) distribute remaining cash according to final capital balances. A partner with a debit capital balance must cover the deficiency if able; if not, credit-balance partners absorb it using the income/loss-sharing ratio.
- **Partner-performance analysis**: Compute `partner return on equity = partner net income / average partner equity` separately for each partner. A negative average equity makes the ratio not meaningful; total partnership return can conceal very different individual returns.

## Key Concepts
- **Partnership**: Unincorporated association of two or more co-owners pursuing profit.
- **Partnership agreement**: Contract specifying contributions, duties, allocation, admission, withdrawal, disputes, and death provisions.
- **Mutual agency**: Each partner can bind the partnership within the ordinary scope of its business.
- **Unlimited liability**: Partners' personal assets may be used to satisfy partnership debts.
- **Partner capital account**: Separate equity record of a partner's investment, allocations, and withdrawals.
- **Withdrawals account**: Temporary record of cash or property taken by a partner.
- **Salary/interest allowance**: Allocation device, not an expense paid before partnership income is allocated.
- **Bonus**: Difference between a partner's investment/payment and the capital credited under the agreement.
- **Statement of partners' equity**: Roll-forward of each partner's beginning capital, investment, allocation, withdrawal, and ending balance.
- **Capital deficiency**: Debit balance remaining in a partner's capital account during liquidation.

## Mental Models
- **Use the agreement as the source of truth**: Capital percentage, income percentage, salary allowances, interest allowances, and loss sharing may differ; never infer one from another.
- **Separate personal from partnership transactions**: Cash paid by a new partner to an old partner changes capital ownership but not partnership assets; cash invested in the partnership changes both assets and total equity.
- **Allocate before distributing**: First recognize income/loss and liquidation gains/losses, then settle creditors, then distribute residual cash.
- **Think of capital as the settlement claim**: Income/loss uses the sharing ratio, but final liquidation cash uses the updated capital balances.

## Anti-patterns
- **Recording partner salary allowances as expenses**: Partners are owners; allowances divide net income or loss and do not reduce partnership income.
- **Assuming equal sharing despite an agreement**: The agreement controls; absent an agreement, equal sharing is the default.
- **Recording a buyer's payment to an old partner as partnership revenue or cash**: A purchase of interest is personal and only reallocates capital accounts.
- **Distributing cash before paying creditors**: Liquidation pays liabilities before partners receive residual cash.
- **Using capital balances to allocate liquidation gains/losses**: Those gains/losses follow the income-and-loss-sharing ratio; capital balances determine the final distribution.
- **Ignoring a capital deficiency**: A debit capital account requires payment by the deficient partner when possible or absorption by the remaining partners.

## Worked Example
BOARDS begins with Zayn's $30,000 net investment and Perez's $10,000 cash investment. Its agreement gives salary allowances of $36,000 to Zayn and $24,000 to Perez, interest allowances of 10% on beginning capital, and an equal split of the remainder. With $70,000 net income:

```text
Salary allowances:             $36,000 + $24,000 = $60,000
Interest allowances:           10% x $30,000 + 10% x $10,000 = $4,000
Remainder:                     $70,000 - $64,000 = $6,000; $3,000 each
Zayn allocation:               $36,000 + $3,000 + $3,000 = $42,000
Perez allocation:              $24,000 + $1,000 + $3,000 = $28,000
After withdrawals of $20,000 and $12,000:
Zayn capital = $30,000 + $42,000 - $20,000 = $52,000
Perez capital = $10,000 + $28,000 - $12,000 = $26,000
```

The statement of partners' equity reports the investment, allocation, withdrawals, and ending balances separately; the allowances never appear as operating expenses.

## Key Takeaways
1. Record each contribution at agreed market value, assume liabilities separately, and maintain one capital and withdrawals account per partner.
2. Apply the income/loss agreement in sequence; allowances and remainder allocations must total partnership income or loss.
3. Distinguish a personal purchase of an interest from a new investment into the partnership before journalizing admission.
4. Account for withdrawal bonuses and death settlements under the contract and the partners' sharing ratio.
5. Liquidate by selling noncash assets, allocating gains/losses, paying liabilities, and distributing residual cash by final capital balances.
6. Use partner-specific return on equity to evaluate each owner's result rather than relying only on total partnership return.

## Connects To
- **Chapter 1**: Compares proprietorship, partnership, and corporate forms and extends the accounting equation.
- **Chapter 11**: Contrasts partnership capital and withdrawals with corporate stock, dividends, and retained earnings.
- **Chapter 13**: Applies return-on-equity and financial-statement analysis to partner performance.
- **Appendix C**: Uses the same ownership/influence distinction when accounting for equity-method investments and control.
- **Legal/tax context**: Partnership agreements and state law govern liability, admission, withdrawal, and estate settlements; accounting entries must follow the governing agreement.
