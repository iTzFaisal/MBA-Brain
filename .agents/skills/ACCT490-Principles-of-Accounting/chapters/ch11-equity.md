# Chapter 11: Reporting and Analyzing Equity

## Core Idea
Corporate equity records the owners' claims created by stock issues and retained by operations. The accounting task is to keep contributed capital, retained earnings, dividends, treasury stock, and preferred-stock rights distinct, then use per-share measures to interpret the claim and its market prospects.

## Frameworks Introduced
- **Corporate equity map**: Use it when reading or preparing the equity section. Separate paid-in capital (amounts received from stockholders) from retained earnings (cumulative income less losses and dividends), then show common/preferred stock, additional paid-in capital, retained earnings, accumulated other comprehensive income, and treasury stock as applicable. Market trades between investors do not change the issuer's equity.
- **Stock-issuance procedure**: Identify the asset received and the stock's par, no-par, or stated value. Debit cash or the noncash asset at the more clearly determinable market value; credit the stock account for par or stated value and credit paid-in capital in excess of that value for the remainder. For no-par stock without a stated value, credit the entire proceeds to the stock account. Organization costs are expensed when incurred.
- **Three-date cash-dividend procedure**: At declaration, debit Retained Earnings and credit Dividend Payable; at the record date, make no entry; at payment, debit Dividend Payable and credit Cash. A dividend is not a liability until declared. A deficit or legal restriction may prevent ordinary cash dividends; a permitted return of contributed capital is a liquidating dividend.
- **Stock-dividend versus stock-split rule**: A small stock dividend, 25% or less of outstanding shares, capitalizes retained earnings at the market value of the shares; a large stock dividend, over 25%, uses par or stated value. A stock split changes shares and par/stated value but requires no journal entry and does not change total equity.
- **Preferred-dividend allocation**: Calculate the contractual preferred dividend first. For cumulative stock, add prior declared-but-unpaid dividends in arrears before allocating anything to common; for noncumulative stock, skipped prior dividends are not recovered. A preference does not guarantee that a dividend will be declared.
- **Cost-method treasury-stock procedure**: Record a purchase of the corporation's own shares at cost as Treasury Stock, a contra-equity account. On reissue, credit Paid-In Capital, Treasury Stock for proceeds above cost; for proceeds below cost, debit that account to its available credit balance and then debit Retained Earnings for any remainder. Never report a gain or loss on the corporation's own shares.
- **Equity analysis**: Use `basic EPS = (net income - preferred dividends) / weighted-average common shares`; `PE = market price per share / EPS`; `dividend yield = annual cash dividend per share / market price`; and `book value per common share = equity applicable to common / common shares outstanding`. For preferred stock, allocate its call price or par plus cumulative arrears before assigning residual equity to common.

## Key Concepts
- **Corporation**: Separate legal entity whose stockholders generally have limited liability and transferable ownership.
- **Authorized stock**: Shares the charter permits the corporation to sell; authorization alone requires no entry.
- **Issued stock**: Authorized shares that have been sold; **outstanding stock** excludes shares held in treasury.
- **Par value stock**: Stock assigned a per-share value in the charter; it is not the market value.
- **Paid-in capital**: Cash and other assets received from stockholders for shares.
- **Retained earnings**: Cumulative net income and losses not distributed to owners.
- **Preferred stock**: Stock with priority over common stock, usually for dividends and liquidation claims.
- **Treasury stock**: A corporation's reacquired shares, reported as a deduction from equity.
- **Prior period adjustment**: Correction of a material prior-period error, reported through beginning retained earnings.
- **Statement of stockholders' equity**: Roll-forward of each major equity component from beginning to ending balances.

## Mental Models
- **Use the account's economic source rule**: Stock transactions belong in paid-in capital; operating performance belongs in retained earnings; neither should be mislabeled as revenue or expense.
- **Think in ownership-preserving percentages**: A dividend or split gives additional shares in the same ownership proportion; it changes the per-share claim, not the owner's percentage or total company value.
- **Use preference before residual**: Allocate cumulative preferred claims first, then give the remaining declared dividend or liquidation equity to common stockholders.
- **Treat treasury stock as a contra-equity balance, not an asset**: It removes cash and equity at cost, and later reissuance differences stay within equity.

## Anti-patterns
- **Recording a stock premium as revenue**: The excess over par is contributed capital, not an operating inflow.
- **Making an entry on a cash-dividend record date**: The declaration already creates the liability; the record date only identifies recipients.
- **Using market value to record a stock split**: A split changes share descriptions and par value but does not remeasure total equity.
- **Charging a treasury-stock reissue shortfall to a loss**: The corporation cannot gain or lose on its own stock; use paid-in capital and then retained earnings.
- **Treating cumulative dividends in arrears as a liability before declaration**: They are disclosed claims, not liabilities, until the board declares a dividend.

## Worked Example
Quest has 10,000 common shares outstanding, $10 par value, and declares a 10% stock dividend when market value is $15. New shares are `10,000 x 10% = 1,000`; because 10% is small, capitalize market value, `$15,000`:

```text
Dec. 31  Retained Earnings                         15,000
             Common Stock Dividend Distributable              10,000
             Paid-In Capital in Excess of Par Value           5,000

Jan. 20  Common Stock Dividend Distributable       10,000
             Common Stock, $10 Par Value                         10,000
```

The declaration transfers $15,000 from retained earnings to contributed capital; the distribution replaces the temporary distributable account. Total assets and total equity remain $143,000, while common shares and the equity assigned to common stock increase.

## Key Takeaways
1. Distinguish authorized, issued, and outstanding shares before calculating ownership or per-share amounts.
2. Record par/stated value and the excess in separate contributed-capital accounts; record no-par proceeds according to whether a stated value exists.
3. For cash dividends, journalize declaration and payment, not the record date.
4. Allocate cumulative preferred dividends in arrears before current preferred dividends and common dividends.
5. Use the 25% threshold to choose market-value versus par/stated-value accounting for stock dividends; do not journalize a stock split.
6. Reconcile retained earnings and all equity components in the statement of stockholders' equity before interpreting EPS, PE, yield, or book value.

## Connects To
- **Chapter 1**: Extends the accounting equation and the corporation's separate-entity assumption.
- **Chapter 3**: Uses closing entries, prior-period adjustments, and changes in estimates.
- **Chapter 10**: Compares equity financing with long-term debt and financial leverage.
- **Chapter 12**: Stock issuance, dividends, debt, and treasury-stock cash flows are financing activities.
- **Chapter 13**: Supplies EPS, profitability, market-prospect, and equity-ratio measures.
- **Appendix A**: Apple, Google, and Samsung statements illustrate equity roll-forwards and comprehensive income.
