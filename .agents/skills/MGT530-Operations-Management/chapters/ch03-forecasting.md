# Chapter 3: Forecasting

## Core Idea

A forecast estimates a future value, usually demand, to match supply with capacity, inventory, workforce, purchasing, and schedules. It is decision support, not certainty. Forecasts assume the past causal system continues, but randomness and unforeseen events guarantee error. Accuracy falls as the horizon lengthens; aggregating items often improves it because errors can cancel. A good forecast is timely, accurate with stated error, reliable, meaningful, written, understandable, and cost-effective.

## Frameworks Introduced

- **Six-step forecasting process:** (1) determine the purpose and use, (2) establish the time horizon, (3) obtain, clean, and analyze appropriate data, (4) select a forecasting technique, (5) make the forecast, and (6) monitor forecast errors and revise the method, assumptions, or data when performance is unsatisfactory.
- **Three approach families:** judgmental forecasts use subjective inputs; time-series forecasts project historical patterns; associative models use explanatory or predictor variables. A practical forecast can combine them.
- **Qualitative techniques:** **Executive Opinions**, **Salesforce Opinions**, **Consumer Surveys**, and the **Delphi method** (anonymous, iterative questionnaires reaching consensus). Manager/staff and outside expert opinion help when data are absent, obsolete, or too slow to collect, especially for new products and long-range or technology forecasts.
- **Method-selection lens:** balance cost, accuracy, responsiveness, data/software, preparation time, personnel skill, and horizon. Moving averages and exponential smoothing are mainly short-range; trend models extend farther; qualitative methods suit long-range or data-poor situations; causal regression needs substantial data.

## Key Concepts

### Time-Series Structure and Methods

A **time series** is a time-ordered sequence at regular intervals. Plot it to identify **trend**, **seasonality**, **cycles** (wavelike movement longer than one year), **irregular variation**, and residual **random variation**. Forecast demand, not unit sales, when stockouts mean sales understate what customers wanted.

- **Naive forecast:** for a stable series, `F_(t+1) = A_t`; for seasonality, use the actual from the comparable prior season; with trend, use the last value plus or minus the latest change. It is inexpensive and transparent, but usually less accurate.
- **Moving Average:** `F_t = MA_n = (sum from i=1 to n of A_(t-i))/n`. Add the newest actual and drop the oldest. A small `n` is responsive but noisy; a large `n` is stable but lags changes and weights every included value equally.
- **Weighted moving average (weighted average):** `F_t = w_(t-n)A_(t-n) + ... + w_(t-1)A_(t-1)`, with weights summing to 1, normally giving larger weights to recent observations.
- **Exponential smoothing:** `F_t = F_(t-1) + alpha(A_(t-1) - F_(t-1))`, where `0 < alpha < 1`. Larger alpha responds faster; smaller alpha smooths more. It suits data around an average or showing step/gradual changes. Start several periods back using an average, subjective estimate, or first actual as the forecast for period 2.
- **Focus Forecasting:** apply several methods to recent data after removing irregular variation, then use the method with the best recent accuracy. **Diffusion Models** forecast new-product adoption using market potential, media attention, and word of mouth.
- **Linear trend equation:** `F_t = a + bt`, where `t = 0` identifies the intercept, `b` is the slope, `b = [n(sum ty) - (sum t)(sum y)]/[n(sum t^2) - (sum t)^2]`, and `a = [sum y - b(sum t)]/n = y-bar - b(t-bar)`.
- **Trend-Adjusted Exponential Smoothing:** use when a linear trend exists, because simple smoothing lags it. `TAF_(t+1) = S_t + T_t`; `S_t = TAF_t + alpha(A_t - TAF_t)`; `T_t = T_(t-1) + beta(TAF_t - TAF_(t-1) - T_(t-1))`. Select `alpha`, `beta`, a starting forecast, and an initial trend estimate.

### Seasonality and Association

The **additive model** is `Demand = Trend + Seasonality`; the more widely used **multiplicative model** is `Demand = Trend x Seasonality`. A **seasonal relative** or index expresses the seasonal percentage of average/trend. Deseasonalize by `actual / seasonal relative`; forecast by multiplying trend by the applicable relative. Compute relatives with a **centered moving average** (actual/centered average, averaged by season, then standardized so relatives sum to the number of seasons) or the **Simple Average (SA) method** (season average/overall average; no standardization). SA suits a stationary mean and is less suitable with strong trend. With an even seasonal length, center MA4 or MA12 with a second MA2.

**Associative Forecasting Techniques** identify predictor variables. **Simple Linear Regression** fits the least-squares line `y_c = a + bx`, minimizing squared vertical deviations. `b = [n(sum xy) - (sum x)(sum y)]/[n(sum x^2) - (sum x)^2]`; `a = [sum y - b(sum x)]/n = y-bar - b(x-bar)`. **Correlation** is `r = [n(sum xy) - (sum x)(sum y)] / sqrt({n(sum x^2) - (sum x)^2}{n(sum y^2) - (sum y)^2})`; `r^2` is the proportion of `y` variation explained by `x`. A leading indicator needs a logical relationship, enough lead time, and fairly high correlation. Regression assumes random variation around the line, normally distributed deviations, and predictions within observed `x`; plot first. **Nonlinear and Multiple Regression Analysis** handle other forms.

### Error and Control

Forecast error is `e_t = A_t - F_t`; positive means the forecast was too low, negative means it was too high. The main summaries are:

- `MAD = sum|e_t| / n` (linear, easy to interpret).
- `MSE = sum(e_t^2) / (n - 1)` (Stevenson's chapter convention; larger errors receive more weight).
- `MAPE = [sum(|e_t| / A_t) x 100] / n` (relative error; useful across products or scales).

For a **control chart**, use `s = sqrt(MSE)`, `UCL = 0 + z sqrt(MSE)`, and `LCL = 0 - z sqrt(MSE)`, typically `z = 2` or `3`. Assume random errors normally distributed around zero: about 95.5% lie within +/-2s and 99.7% within +/-3s. A forecast is in control only when every error is within limits and no trend, cycle, bias, or other pattern appears. A **tracking signal** is `TS_t = (cumulative error through t) / MAD_t`; limits of +/-4 or +/-5 are common. Update MAD as `SMAD_t = MAD_(t-1) + alpha(|A_t - F_t| - MAD_(t-1))`. An out-of-limit signal indicates bias and corrective action. Control charts are generally superior because cumulative errors can cancel in a tracking signal.

## Mental Models

- **Stability versus responsiveness:** smoothing suppresses random noise but delays real change; choose the lag you can afford.
- **Forecasting is a feedback loop:** forecast, observe actual demand, measure error, diagnose patterns, and revise.
- **Flexibility buys accuracy:** shorter response lead times permit shorter horizons, which are usually more accurate.

## Anti-patterns

- Treating model output as truth while ignoring weather, competitors, prices, shortages, or other causal changes.
- Using sales as demand despite stockouts, or averaging data that clearly contain trend or seasonality.
- Giving sales staff quota incentives without accounting for deliberately low estimates, or treating one executive's opinion as consensus.
- Extrapolating regression beyond observed values, skipping the plot and assumptions, or mistaking correlation for a causal explanation.
- Declaring a forecast sound because a tracking signal is inside its limits; inspect control-chart patterns even when individual errors are within limits.
- Selecting the most accurate method without weighing cost, responsiveness, and error cost.

## Worked Example

Complaints over five periods are `60, 65, 55, 58, 64`; the plot indicates variation around an average. For period 6: **Naive** = `64`; **MA3** = `(55 + 58 + 64)/3 = 59`; **weighted average** with weights `.20, .30, .50` from oldest to newest = `.20(55) + .30(58) + .50(64) = 60.4`. With **exponential smoothing**, `alpha = .40` and starting `F_2 = 60`, successive forecasts are `F_3 = 62`, `F_4 = 59.2`, `F_5 = 58.72`, and `F_6 = 60.83`. The methods differ because weighting and smoothing trade stability against responsiveness.

## Key Takeaways

Forecasts make capacity and supply-demand decisions possible but are never perfect. Match the method to the data pattern and horizon, state expected accuracy, and monitor actual errors. Use MAD, MSE, and MAPE for comparison; use tracking signals for cumulative bias and control charts for individual errors plus patterns. Revise assumptions when errors stop looking random.

## Connects To

Forecasts connect directly to capacity planning, inventory and workforce levels, purchasing, production scheduling, outsourcing, budgeting, yield management, and supply-chain collaboration. Sharing demand and inventory data, shortening lead times, and building operational flexibility reduce dependence on long, inaccurate horizons. Control-chart logic also connects forecasting to quality-control monitoring.
