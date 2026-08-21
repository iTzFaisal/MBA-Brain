# Chapter 16: International Business Finance

## Core Idea
International finance applies the same cash-flow and valuation discipline as domestic finance, but cash flows are denominated in currencies whose values can change and are exposed to political restrictions. Read currency quotes in the correct direction, use parity relationships as no-arbitrage benchmarks, and evaluate a direct foreign investment using the cash flows the parent can actually repatriate in the parent currency.

## Frameworks Introduced
- **Foreign-exchange quote and conversion framework**
  - When to use: When pricing an international payment, investment, or currency exposure.
  - How: A direct quote is home currency per one unit of foreign currency (`$/FC`); an indirect quote is foreign currency per one unit of home currency (`FC/$`). Convert by taking the reciprocal, then multiply by the foreign amount when using a direct quote. Distinguish the bank's asked (selling) rate from its bid (buying) rate; the difference is the bid-asked spread.
- **Spot, forward, cross-rate, and arbitrage framework**
  - When to use: When settlement is immediate, future, or between two non-home currencies.
  - How: Use the spot rate for immediate delivery and a forward exchange contract for a rate fixed today with future delivery. Derive a cross rate by multiplying compatible rates and invert it for the reverse quote. If two markets quote inconsistent rates, buy where the currency is cheaper and sell where it is dearer; arbitrage should quickly remove the discrepancy.
- **Forward-spot differential**
  - When to use: When describing a forward currency premium or discount on an annualized basis.
  - How: `F - S` is a premium when `F > S` and a discount when `F < S`. Annualize it as `((F - S) / S) * (12 / n) * 100`, where `n` is the contract's months. A forward rate is a locked price, not a guaranteed forecast of the future spot rate.
- **Interest rate parity (IRP)**
  - When to use: When relating spot and forward rates to comparable risk-free interest rates.
  - How: `((1 + domestic rate) / (1 + foreign rate)) = F / S`, or equivalently `1 + domestic rate = (F/S) * (1 + foreign rate)`. Under IRP, investing at home or converting at spot, investing abroad, and converting back at the forward rate produces the same return apart from transaction costs.
- **Purchasing-power parity (PPP) and law of one price**
  - When to use: When estimating a long-run currency relationship from comparable goods and inflation.
  - How: `spot exchange rate ($/FC) = home price / foreign price`. The law of one price says identical tradable goods should have the same price after currency conversion. Higher expected inflation tends to reduce a currency's value; nontraded goods, taxes, labor, rent, and trade barriers weaken the relationship.
- **International Fisher effect**
  - When to use: When comparing nominal interest rates across countries and asking whether a high stated yield represents a real opportunity.
  - How: `nominal interest = expected inflation + real interest + (expected inflation * real interest)`. Over the long run, similar real rates imply that differences in nominal rates mainly reflect differences in expected inflation; do not choose a foreign deposit by nominal rate alone.
- **Direct foreign investment (DFI) cash-flow screen**
  - When to use: When evaluating a foreign factory, subsidiary, or other physical investment.
  - How: Forecast subsidiary cash flows, taxes, restrictions, and the timing of dividends, royalties, and management fees that can be repatriated. Convert repatriated cash to the parent's currency and discount it using a rate stated in that same currency. Add political and exchange-rate risk to ordinary business and financial risk.

## Key Concepts
- **Direct foreign investment (DFI)**: A company from one country making a physical investment in another.
- **Multinational corporation (MNC)**: A corporation with holdings or operations in more than one country.
- **Foreign exchange (FX) market**: The over-the-counter market where currencies are traded.
- **Spot/forward exchange rate**: A rate for immediate delivery versus a rate agreed today for future delivery.
- **Cross rate**: An exchange rate between two foreign currencies, neither being the domestic currency.
- **Arbitrage**: Buying and selling across markets to eliminate a riskless exchange-rate differential.
- **Interest rate parity (IRP)**: The relation tying forward/spot ratios to national interest-rate differences.
- **Purchasing-power parity (PPP)**: The long-run condition that exchange rates equalize purchasing power.
- **International Fisher effect**: The expectation that similar real rates leave nominal-rate differences to reflect expected inflation differences.
- **Repatriation of profits**: Bringing foreign profits back to the firm's home country.

## Mental Models
- **Unit analysis prevents quote errors**: Write the currency units beside every rate; reciprocal conversion should leave the desired currency.
- **Parity is a no-arbitrage benchmark**: IRP and PPP describe relationships that competitive trading should push toward, not promises that hold exactly after costs and barriers.
- **Risk follows the contract currency**: The party receiving or paying an uncertain foreign-currency amount bears the direct exchange-rate exposure; a third currency can expose both parties.
- **Parent cash flow is the decision variable**: A profitable subsidiary is not automatically a valuable DFI if profits are blocked, taxed, delayed, or weakened on conversion.

## Anti-patterns
- **Read a direct quote as an indirect quote**: Multiplying when the units require division can reverse the economic result.
- **Treat the forward rate as the future spot rate**: A forward contract locks a transaction price; it does not reveal certainty about the future market rate.
- **Chase the highest foreign nominal interest rate**: A high rate may only compensate for high expected inflation and currency depreciation.
- **Value a DFI on local accounting profit**: Discount the repatriated, parent-currency cash flow at the appropriate same-currency rate.
- **Ignore political controls**: Expropriation, blocked funds, tax changes, price or wage controls, and local-ownership requirements can change cash flows.

## Worked Example
The six-month U.S. risk-free rate is 2%; the spot rate is `$0.010798/yen`; and the six-month forward rate is `$0.010803/yen`. IRP implies:

`1.02 = (0.010803 / 0.010798) * (1 + Japan rate)`

so the Japanese six-month risk-free rate is `1.9528%`. Starting with `$100`, convert at spot to `9,260.97 yen`; invest at 1.9528% to obtain `9,441.82 yen`; convert at the forward rate and receive `$102.00`. That equals the U.S. investment return, illustrating IRP.

## Key Takeaways
1. Always label the currency units and invert a quote only when the desired units require it.
2. Use forward contracts to manage known future currency payments or receipts, and include the bid-asked spread in real decisions.
3. Use IRP, PPP, and the international Fisher effect as linked benchmarks for rates, prices, inflation, and currencies.
4. Exchange-rate risk affects trade contracts, portfolio returns, subsidiary assets, and repatriated profit streams.
5. DFI analysis must model repatriation timing, taxes, blocked funds, political controls, and currency conversion in addition to ordinary project risk.

## Connects To
- **Chapter 14**: Forecasting and cash budgets provide the operating cash flows whose currency exposure must be managed.
- **Chapter 15**: International short-term credit retains the same maturity, liquidity, and effective-cost logic, with FX risk added.
- **Chapter 17**: Foreign cash, receivables, inventory, and investment balances can change value when exchange rates move.
- **Capital budgeting**: DFI decisions use the same NPV discipline, but cash-flow currency and repatriation timing must match the discount rate.
