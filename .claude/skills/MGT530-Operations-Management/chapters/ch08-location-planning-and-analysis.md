# Chapter 8: Location Planning and Analysis

## Core Idea

Location is a strategic operations decision because it commits resources for a long time and shapes capacity, flexibility, cost, revenue, customer access, supply-chain responsiveness, and competitive advantage. A good decision is not necessarily the single mathematically "best" site; it is a defensible choice among acceptable alternatives after considering the organization's strategy, risks, and system-wide effects. Manufacturing choices usually emphasize cost and supply; service and retail choices usually emphasize revenue, access, and the customer.

## Frameworks Introduced

- **Decision hierarchy:** Screen countries first, then regions, communities, and finally specific sites. The factors become more concrete as the search narrows.
- **Location options:** Expand an existing facility; add a location while retaining current facilities; close and relocate; or do nothing. The last option is valid when analysis does not show enough benefit to justify change.
- **Formal procedure:** (1) establish evaluation criteria, (2) identify relevant factors, (3) develop country, regional, community, and site alternatives, and (4) evaluate alternatives and select one.
- **Economic comparison:** Locational cost-profit-volume analysis, transportation modeling, break-even comparisons, and load-distance analysis quantify cost or movement implications.
- **Multi-factor comparison:** Factor rating combines weighted qualitative and quantitative judgments.
- **Geographic positioning:** The center-of-gravity method estimates a distribution or service point that minimizes distance-weighted movement.

## Key Concepts

Location belongs in supply-chain configuration: the number and placement of suppliers, plants, warehouses, and distribution centers affect cost, revenue, and response time. Centralized distribution can provide scale economies and control, but may increase transportation distance; decentralized facilities improve local responsiveness but may sacrifice scale.

Global locations are enabled by trade agreements and communication technology. Potential benefits include new markets, better local service, lower labor/material/transportation/tax costs, favorable regulation, incentives, and new ideas. These benefits must be netted against long-distance transport, weak infrastructure or skills, security, import restrictions, lower productivity, ethical concerns, and criticism of labor or environmental practices. Risks include intellectual-property loss, political or economic instability, terrorism, changing laws, corruption, cultural mismatch, and quality failures. Low wages do not guarantee low unit cost: productivity, inventory, delay, exchange-rate, and supply-chain agility effects may reverse the apparent advantage.

Country factors include government policy, foreign ownership and local-content rules, currency and imports, labor capability and cost, resources, finance and taxes, technology, market potential, safety, and cultural/customer preferences. Regional factors commonly include raw materials, markets, transportation, and labor. Raw-material proximity may be required by necessity, perishability, or bulk-reduction economics. Market proximity matters for perishability, distribution expense, customer contact, and competitive positioning. Labor analysis should include availability, skills, wages, productivity, work attitudes, turnover, absenteeism, and union conditions, not wages alone.

Community factors include quality of life, utilities, schools, housing, medical/fire/police services, local attitudes, taxes, environmental rules, and government incentives such as grants, loans, training, or abatements. Site factors include land cost and development, soil and drainage, zoning, utilities and sewer capacity, expansion room, parking, truck roads or rail access, and airport or train connections. Industrial parks reduce development and zoning effort but can restrict activities, building design, or future expansion. Ethical analysis also covers honest promises, taxpayer exposure to incentives, and hidden payments or favors.

Manufacturing networks trade specialization against flexibility. Product-focused plants gain scale and lower operating cost; market-area plants reduce shipping and improve local response; process plants specialize components but require central coordination and add shipping; general-purpose plants respond flexibly but may be less productive. GIS supports these decisions by combining maps with demographics, traffic, competitors, utilities, crime, transportation, and sales data.

For cost-volume analysis, use `TC = FC + vQ`, where `FC` is fixed cost, `v` variable cost per unit, and `Q` output. Profit is `Q(R - v) - FC`. A break-even volume between two alternatives is found by equating their total-cost lines. The method assumes one product, a reliable output estimate, constant fixed cost, and linear variable cost over the relevant range. Transportation cost can be added to variable cost or analyzed separately with a transportation-model linear program when multiple origins and destinations exist.

**Load-distance** is a screening measure for comparing feasible sites: `LD = sum(load_i * distance_i)`. Use shipment quantities or trip counts as loads and compare the resulting weighted distances; lower load-distance generally indicates less movement, subject to actual routes, rates, and capacity constraints. The center-of-gravity method uses coordinates and shipment weights: `xbar = sum(x_i Q_i) / sum(Q_i)` and `ybar = sum(y_i Q_i) / sum(Q_i)`. It is an initial geometric recommendation, not a final site decision.

Service and retail decisions are usually revenue-focused. Evaluate demographics, population and drawing area, income and education, competition, traffic volume and patterns, customer convenience, access, parking, safety, and public transportation. Clustering near complementary or competing businesses can increase traffic and convenience; an isolated or unique business may have its own drawing power. Multi-outlet systems must avoid cannibalization, protect market share, and assess the effect of a competitor or new outlet on the entire portfolio. Online retailers increasingly place warehouses near markets for rapid delivery.

## Mental Models

- **Strategy determines the weight:** A low-cost strategy favors labor, materials, energy, transportation, and taxes; a market-share or convenience strategy favors traffic, visibility, access, and many outlets.
- **Follow the flow:** Locate near the scarce, costly, perishable, bulky, or time-sensitive input or customer, then test whether transport, inventory, and risk erase the benefit.
- **Screen, then score:** Use the country-to-site hierarchy to reduce the search set, quantitative models to expose economic ranges, and factor rating to include nonfinancial realities.
- **System beats site:** Judge an outlet or plant by its effect on the whole network, not by its standalone rent or wage rate.

## Anti-patterns

- Choosing low wages, cheap land, or tax incentives without testing productivity, infrastructure, transport, inventory, currency, and regulatory risk.
- Treating a center-of-gravity point or the highest factor score as an automatically buildable site.
- Ignoring expansion capacity, zoning, utilities, parking, safety, community resistance, or employee relocation realities.
- Adding nearby outlets without modeling cannibalization and total-system sales.
- Assuming global coordination, culture, quality, and intellectual-property controls will work as they did at home.

## Worked Example

Four plant alternatives have annual fixed/variable costs: A ($250,000, $11), B ($100,000, $30), C ($150,000, $20), and D ($200,000, $35). Equating B and C gives a break-even of 5,000 units; equating C and A gives 11,111 units. Thus B is the lowest-cost choice below 5,000, C from 5,000 to 11,111, and A above 11,111; D is never superior. At 8,000 units, choose C on cost. Management should still test transportation, labor, quality, capacity, risk, and service effects. A factor-rating example shows why: an alternative scoring 82.7 versus 70.6 wins the weighted comparison, but only if it clears any minimum threshold. For a distribution point, unequal destination quantities require weighted coordinates; the chapter example produces approximately `(3.05, 3.7)`, which then must be checked against roads, zoning, and actual freight costs.

## Key Takeaways

1. Location decisions are strategic, long-term, and supply-chain-wide.
2. Separate country, region, community, and site screening; match factors to the facility type.
3. Combine cost-volume, break-even, transportation/load-distance, factor rating, GIS, and center-of-gravity evidence rather than relying on one metric.
4. Make trade-offs explicit: scale versus responsiveness, low wages versus productivity and risk, specialization versus flexibility, and clustering versus competition.

## Connects To

This chapter connects to capacity and process strategy, supply-chain network design, transportation and inventory decisions, just-in-time supplier proximity, service-system design, retail market analysis, sustainability and ethics, and data-supported planning through GIS.
