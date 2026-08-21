# Chapter 5: Reporting and Analyzing Inventories

## Core Idea
Inventory accounting allocates the cost of goods available for sale between cost of goods sold (COGS) and ending inventory. The result depends on which goods belong in inventory, which costs are inventoriable, the inventory system, and the cost-flow assumption; the reported amount is then tested for lower of cost or market (LCM) and analyzed with turnover measures.

## Frameworks Introduced
- **Inventory inclusion and cost**: Include goods the company owns and holds for sale, regardless of location. Under FOB shipping point, the buyer includes goods when shipped; under FOB destination, the buyer includes them when received. The consignor retains consigned goods in inventory; the consignee never does. Exclude damaged or obsolete goods that cannot be sold; if they can be sold, carry them at a conservative estimate of net realizable value (selling price less cost of making the sale). Inventory cost is invoice cost net of discounts plus expenditures needed to bring goods to salable condition and location, such as freight-in, tariffs, insurance, storage, or aging costs.
- **Goods-available allocation**: Use the matching principle and the identity `Beginning inventory + net purchases = goods available for sale = ending inventory + COGS`. A periodic system updates Merchandise Inventory at period-end after a physical count; a perpetual system updates it continually as purchases and sales occur.
- **Four periodic cost-flow methods**: Use **specific identification** when each unit and sale can be traced to its invoice; it is practical for expensive or custom goods and is not a cost-flow assumption. **FIFO (first-in, first-out)** assigns earliest costs to COGS and leaves recent costs in ending inventory. **LIFO (last-in, first-out)** assigns recent costs to COGS and leaves oldest costs in inventory; physical flow need not follow the assumption. **Weighted average** assigns one average cost per unit: `cost of goods available / units available`, then multiplies that cost by units sold and units remaining. Under perpetual weighted average, recompute the average after each purchase and use it for the next sale.
- **Method-selection effects**: With rising purchase costs, FIFO generally produces the lowest COGS and highest gross profit/net income, LIFO the highest COGS and lowest gross profit/net income, and weighted average results between them; LIFO can provide a temporary tax advantage. FIFO approximates current cost on the balance sheet, LIFO better matches current costs with revenue, weighted average smooths cost changes, and specific identification matches unit cost to related revenue. A company discloses its method and applies the consistency concept; a justified change requires disclosure of its reason and income effect. IFRS does not permit LIFO.
- **Lower of cost or market**: Market is current replacement cost in the usual manner. Compare cost and market for each item, a category, or the whole inventory; individual-item application is the most conservative. If market is lower, write inventory down; do not write it up when market exceeds cost. The write-down is recorded as COGS in the chapter's illustration.
- **Inventory analysis**: Inventory turnover is `COGS / average inventory` and measures how many times inventory is sold. Days' sales in inventory is `ending inventory / (COGS / 365)` and estimates the days of sales available without new purchases. Interpret both against competitors and over time: high turnover is desirable only if inventory remains adequate to avoid backorders.

## Key Concepts
- **Merchandise inventory**: Goods owned and held for sale, including costs necessary to place them in salable condition and location.
- **Goods in transit**: Inventory whose inclusion follows the ownership transfer specified by FOB terms.
- **Consignor/consignee**: The owner shipping goods on consignment/the party selling them for the owner.
- **Net realizable value**: Expected selling price less the cost of making the sale.
- **Goods available for sale**: Beginning inventory plus net purchases available to be assigned to COGS or ending inventory.
- **Cost-flow assumption**: A rule assigning available unit costs to units sold and units remaining, independent of physical flow except for specific identification.
- **Cost of goods sold**: The inventory cost matched with sales in the current period.
- **Lower of cost or market**: Reporting inventory at the lower of recorded cost and replacement cost when market is lower.
- **Inventory error**: A misstatement of count or cost that distorts COGS, income, assets, and equity in the current and following period.
- **Inventory shrinkage**: The difference between recorded perpetual inventory and the physical count caused by theft, loss, damage, or error.

## Mental Models
- **Use ownership before arithmetic**: Before counting units, ask who owns them at the reporting date, where they are, and whether they are saleable. FOB terms and consignment status can change inventory before any cost calculation.
- **Use the cost identity to debug**: If `beginning inventory + purchases` does not equal `COGS + ending inventory`, the count, unit costs, or flow assignment is wrong. An understated ending inventory overstates current COGS and understates current income; the next period reverses the income effect because ending inventory becomes beginning inventory.
- **Choose the method for the reporting question**: Prefer FIFO when current-looking inventory and higher income are important during rising costs; LIFO when matching recent costs and temporary tax deferral matter; weighted average when smoothing volatility matters; specific identification when traceability is reliable.
- **Treat turnover as a balance, not a maximization goal**: Low turnover can signal excess or obsolete stock; very high turnover can signal stockouts. Pair the ratio with days' sales in inventory and evidence of customer demand.

## Anti-patterns
- **Assuming the cost acronym describes physical movement**: FIFO and LIFO describe the assumed flow of costs to COGS, not necessarily the warehouse sequence.
- **Capitalizing selling costs as inventory**: Advertising, sales salaries, store lighting, and similar selling-period costs do not bring the product to salable condition and location.
- **Writing inventory up to market**: A market increase is not recorded above original cost; LCM is a downward valuation rule in this chapter.
- **Treating a physical count as optional**: Perpetual records can differ from actual goods because of theft, damage, loss, and error; controls and a count are needed to correct shrinkage.
- **Changing methods for an undisclosed earnings effect**: Consistency and full disclosure exist so users can compare periods and understand income changes.

## Worked Example
Trekking has 55 bikes available in August: 10 at $91, 15 at $106, 20 at $115, and 10 at $119, for total cost of $5,990. It sells 43 and ends with 12. Under the periodic system:

```text
Method                 Ending inventory       COGS
Specific identification       $1,408          $4,582
FIFO                          $1,420          $4,570
LIFO                          $1,122          $4,868
Weighted average              $1,307          $4,683
```

Specific identification traces the actual sales: $2,000 on the first sale and $2,582 on the second. FIFO leaves 10 units at $119 and 2 at $115. LIFO leaves 10 units at $91 and 2 at $106. Weighted average is `$5,990 / 55 = $108.91` per unit; 12 units produce about $1,307 of ending inventory. With rising costs and $6,050 of sales, the method changes gross profit even though units and sales do not change.

## Key Takeaways
1. Establish ownership, saleability, units, and inventoriable costs before applying a costing method.
2. Reconcile goods available for sale to ending inventory plus COGS; investigate any difference.
3. State clearly whether the calculation is periodic or perpetual, especially for weighted average.
4. Interpret FIFO, LIFO, weighted average, and specific identification as different cost assignments with different income, tax, and balance-sheet effects.
5. Apply LCM when replacement cost is below recorded cost and record the required write-down.
6. Use turnover and days' sales in inventory together to assess both efficiency and stock availability.

## Connects To
- **Chapter 2**: Uses inventory records, subsidiary ledgers, source documents, and double-entry postings.
- **Chapter 3**: Applies adjusting entries, physical-count corrections, consistency, and the self-correcting pattern of inventory errors.
- **Chapter 4**: Supplies the COGS and ending-inventory amounts used in merchandising income statements and ratios.
- **Chapter 6**: Extends internal-control ideas to physical counts, restricted access, requisitions, and independent verification.
