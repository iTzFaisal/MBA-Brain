# Chapter 13: Lean Manufacturing and Activity Analysis

## Core Idea
A lean enterprise seeks high quality, low cost, fast response, and immediate availability by reducing waste, lead time, setup time, defects, unnecessary movement, and excess inventory. Activity analysis makes time, quality, and process costs visible; lean accounting supplies fast, understandable operational feedback.

## Frameworks Introduced
- **Lean/JIT principles**: Reduce inventory and setup time, use product cells, empower teams, pull production, pursue zero defects, and manage suppliers collaboratively.
- **Water-and-rocks model**: Lower inventory to expose process problems, then remove the problems rather than merely shifting the buffer.
- **Setup reduction and one-piece flow**: Shorten setup so small batches become economical and within-batch waiting falls.
- **Pull/kanban**: Let the downstream operation or customer signal the quantity and timing of upstream production.
- **Six Sigma DMAIC**: Define, measure, analyze, improve, and control defects.
- **Lean accounting/backflush**: Use combined cell accounts, fewer transactions, direct tracing, and nonfinancial measures when flow is rapid.
- **Cost of quality**: Classify prevention, appraisal, internal failure, and external failure costs.
- **Value-added/process activity analysis**: Map inputs, activities, time, cost, and outputs; remove activities that do not meet customer requirements.

## Key Concepts
- **Lead/throughput time**: Time from production start to completion.
- **Value-added time**: Time that transforms the product in a customer-required way.
- **Non-value-added time**: Waiting, movement, rework, or failure activity that should be reduced.
- **Value-added ratio**: Value-added time divided by total lead time.
- **Product cell**: Sequential work arranged around a product rather than a department.
- **Backflush accounting**: Simplified cost flow for lean cells.
- **Quality costs**: Prevention, appraisal, internal failure, and external failure.

## Mental Models
- Inventory is water; breakdowns, skill shortages, and quality problems are rocks hidden below it.
- A batch is a queue: every unit after the first waits for earlier units.
- Pull means the downstream signal controls upstream production.
- Prevention and appraisal can reduce much larger internal and external failure costs.
- Accounting should provide rapid feedback without becoming administrative waste.

## Anti-patterns
- Cutting inventory without fixing the exposed process problems.
- Pushing production from forecasts and creating excess inventory.
- Retaining large batches because setups are long.
- Using process-oriented layouts for sequential work when cells would reduce movement.
- Relying on rework and tolerating defects.
- Choosing suppliers only on quoted price.
- Gaming lead-time measures by prioritizing tagged items.
- Treating every movement as non-value-added without asking whether it completes the product.

## Worked Example
An automotive batch of 40 units has 24 minutes of processing, 25 minutes of movement, and within-batch waiting of `24 x (40 - 1) = 936` minutes.

- Total lead time = `24 + 25 + 936 = 985` minutes.
- Value-added ratio = `24 / 985 = 2.4%`.
- Setup reduction permits a batch of one, eliminating within-batch waiting. With movement unchanged, lead time becomes `49` minutes and the ratio rises to about `49.0%`.
- A product cell that also removes movement would reduce theoretical lead time to `24` minutes.

The example shows why setup reduction and product-oriented layout reinforce one another.

## Key Takeaways
1. Map processing, movement, waiting, inspection, rework, and failure separately.
2. Reduce setup before demanding smaller batches.
3. Use pull signals, cross-trained teams, reliable suppliers, and zero-defect practices together.
4. Track lead time, value-added ratio, setup time, scrap, stops, and failed inspections.
5. Shift resources from failure correction toward prevention when quality costs show failure dominance.

## Connects To
- **Ch 2-4**: Lean flow changes how product costs and activities are accumulated.
- **Ch 5**: Activity drivers and allocation choices expose support cost.
- **Ch 9**: Variance and quality measures help diagnose process problems.
- **Ch 14**: Nonfinancial lean measures become leading indicators in a scorecard.
