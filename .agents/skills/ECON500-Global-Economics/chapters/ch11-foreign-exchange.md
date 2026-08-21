# Chapter 11: Foreign Exchange

## Core Idea
The foreign exchange market converts claims denominated in one national currency into another and coordinates international trade, investment, and payments. Exchange rates are prices: their direction changes the domestic-currency cost of imports, the competitiveness of exports, and the value and risk of foreign-currency cash flows.

## Frameworks Introduced
- **Foreign Exchange Market**: The decentralized, global, nearly round-the-clock network in which banks, firms, governments, investors, and households trade currencies and currency-denominated claims.
  - When to use: Identify who supplies liquidity, where a transaction is executed, and whether the exposure is retail, wholesale, interbank, or speculative.
  - How: Trace the three levels: customers with commercial banks; domestic interbank dealing through brokers; and trading among banks, overseas branches, and correspondents. Banks quote a bid (buying price) and offer (selling price); the spread covers costs and provides a trading margin.
- **Types of Foreign Exchange Transactions**: Match settlement and risk to the timing of the obligation.
  - **Spot** settles conventionally two business days after agreement and leaves the rate exposed until the trade is made. **Forward** fixes a rate today for delivery later, eliminating uncertainty but also eliminating gains from a favorable move. **Swap** exchanges currencies now and reverses the exchange later at prearranged rates. **Futures** use standardized contracts, exchange trading, set delivery dates, and daily settlement. **Options** give the holder a right, not an obligation, to trade at a strike price; a call buys foreign currency, a put sells it, and the writer receives the premium.
- **Supply-and-Demand Model of Exchange Rate Determination**: In a flexible market, the equilibrium exchange rate is where demand and supply of foreign exchange intersect.
  - Demand for pounds, viewed from the United States, is derived from U.S. imports, foreign investment, debt repayment, and transfers; it corresponds to balance-of-payments debit items and slopes downward against the dollar price of the pound. Supply is derived from British demand for U.S. goods and assets; it corresponds to U.S. balance-of-payments credit items and slopes upward.
  - How: A rightward demand shift raises the foreign-currency price and depreciates the dollar. A leftward demand shift appreciates it. A rightward supply shift appreciates the dollar; a leftward supply shift depreciates it.
- **Exchange Arbitrage**: Simultaneously buy currency where it is cheap and sell it where it is expensive. Two-point arbitrage links two currencies and centers; three-point (triangular) arbitrage cycles through three currencies. Trading removes discrepancies, subject to transfer, interest, and transaction costs.
- **Interest Arbitrage**: Compare foreign and domestic investment returns after accounting for currency movement. Uncovered interest arbitrage accepts exchange risk; covered interest arbitrage buys foreign currency spot, invests abroad, and sells the expected foreign proceeds forward.

## Key Concepts
- **Exchange rate**: The price of one currency in units of another. If `E = domestic currency / foreign currency`, then `E` rising means the domestic currency depreciates; `E` falling means it appreciates. The reciprocal quote is `1/E`.
- **Cross exchange rate**: A non-dollar currency pair derived from each currency's dollar quote, e.g. `GBP/CHF = ($/GBP) / ($/CHF)`.
- **Bid-offer spread**: The difference between a dealer's buying and selling quotes; it widens for illiquid or volatile currencies and for small retail transactions.
- **Forward premium/discount**: A forward currency is at a premium when `F > S`, and at a discount when `F < S`. Annualized percentage: `((F - S) / S) * (12 / months forward)`.
- **Nominal, effective, and real exchange rates**: The effective (trade-weighted) rate averages bilateral rates by trading importance. The real rate adjusts the nominal rate for relative prices: `RER = E * (foreign price level / home price level)`. Real rates better measure international competitiveness.
- **Currency risk**: The uncertain domestic-currency value of future foreign-currency receipts, payments, or investment returns.
- **Hedging**: Covering an exposure to stabilize its domestic-currency value. An importer buys foreign currency forward; an exporter sells expected foreign receipts forward.
- **Interest-rate parity logic**: Higher foreign interest rates attract funds, but the foreign currency tends to trade at a forward discount; the discount offsets the extra interest return as arbitrage proceeds.
- **Stabilizing versus destabilizing speculation**: Stabilizing trades oppose a currency movement; destabilizing trades reinforce a fall or rise and can increase hedging costs and impede trade.

## Mental Models
- **The balance-of-payments mirror**: Treat foreign-exchange demand as the currency counterpart of debit transactions and supply as the counterpart of credit transactions. Use it to predict which trade or capital-flow change shifts each schedule.
- **Exposure-direction test**: A future payable becomes more expensive when the foreign currency appreciates, so buy it forward. A future receivable loses home-currency value when the foreign currency depreciates, so sell it forward.
- **Insurance versus obligation**: A forward contract is binding insurance with no upside; an option is paid insurance with a choice. Use a forward for certainty at a known rate; use an option when protection matters but favorable exchange-rate moves should remain available.
- **Return decomposition**: Foreign investment return equals the foreign interest differential plus currency appreciation, or minus currency depreciation. Covered investment replaces the uncertain currency term with the forward premium/discount.

## Anti-patterns
- **Reversing a quotation**: Do not infer appreciation without checking whether the quote is domestic currency per foreign currency or its reciprocal.
- **Treating a forward premium as a forecast**: The spot-forward relation is primarily shaped by interest-rate differentials and market mechanics; it is not automatically a prediction of the future spot rate.
- **Calling speculation arbitrage**: Arbitrage is simultaneous, near-riskless price equalization; speculation deliberately carries exchange risk for an expected future gain.
- **Over-hedging or leaving predictable exposure unmanaged by reflex**: Hedging stabilizes cash flow but costs money and sacrifices favorable moves. Choose coverage based on exposure size, predictability, margins, volatility, and the firm's ability to absorb losses.
- **Using leverage as a risk-control method**: A small margin can control a very large currency position; a small adverse movement can therefore create losses far beyond the expected gain.

## Worked Example
A U.S. investor compares three-month Treasury bills yielding 6% annualized in New York with 10% annualized in London. The pound costs `$2` spot. The London advantage is `4%` per year, or `1%` for three months. If the investor leaves the position uncovered and the pound falls to `$1.99`, the currency loss is `0.5%`, leaving only `0.5%` extra return; if it falls to `$1.98`, the interest advantage is erased. If the investor buys pounds spot and simultaneously sells the expected proceeds forward at `$1.99`, the 0.5% forward discount is the cover cost. Net covered advantage is `1.0% - 0.5% = 0.5%`. Competition then pushes the spot pound up and the forward pound down until the discount offsets the interest differential, eliminating the arbitrage opportunity.

## Key Takeaways
1. Exchange rates are prices; always state the quotation convention before interpreting appreciation or depreciation.
2. Flexible-market equilibrium links currency supply and demand to balance-of-payments credits and debits.
3. Spot provides immediacy, forwards provide certainty, swaps provide temporary currency access, futures standardize trading, and options cap downside while preserving choice.
4. Real, trade-weighted exchange rates are more informative about competitiveness than a single nominal bilateral rate.
5. Arbitrage aligns prices across markets; interest arbitrage aligns returns after exchange-rate cover.
6. Hedging manages exposure, not prediction. Speculation assumes risk and can either stabilize or destabilize markets.

## Connects To
- **Balance of payments**: Its credit and debit entries generate the supply and demand schedules for foreign exchange.
- **International trade and investment**: Real exchange rates affect competitiveness, import prices, export revenues, output, employment, and inflation.
- **Interest-rate parity**: Covered arbitrage explains why interest differentials and forward premiums/discounts tend to offset.
- **Chapter 15**: Destabilizing speculation and its broader monetary consequences are developed further there.
