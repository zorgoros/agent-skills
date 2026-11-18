# Industrial project financial model

## Build and reconcile the schedules

Use one calendar, price basis, unit and currency convention. Choose period granularity that exposes construction, working-capital and repayment gaps (often monthly through commissioning and early operations). Record time zero, cash timing, valuation date, horizon and terminal assumptions. Use one assumptions register with source, date, status and range for material inputs. Identify outputs that depend on each missing input.

| Schedule | Required links and checks |
|---|---|
| Construction and capital spending | Quantity × unit cost, milestones, contingency basis, commissioning and replacements, taxes/duties and recovery timing where applicable. Tie capital spending to funding by period. |
| Production and revenue | Capacity, uptime, yield, ramp, inventory movements and constrained sales. Volume sold × realized unit price, by product/customer group where needed. Reflect collection terms and discounts. |
| Operating costs and profit | Separate fixed and variable costs and their drivers. Include materials, utilities, labor, maintenance, selling and freight. Show depreciation, financing cost and tax when supported. Reconcile unit cost to the disclosed volume and cost basis. |
| Working capital | Model inventory, receivables, payables and other material operating balances using the matching flows and timing. Increase in net working capital uses cash. Count initial funding, subsequent changes and release once each. Base release on recoverability. |
| Financing and liquidity | Date equity and debt draws, fees, grace terms, capitalized interest, principal and cash interest. Reconcile beginning debt + draws + capitalized interest − principal = closing debt. Reconcile beginning to ending cash each period. Show uncovered shortfalls, peak funding gap and its date. |
| Terminal items | Include salvage, associated taxes, recoverable working capital and closure costs only where supported or as clear assumptions. Avoid counting ongoing cash flows and terminal proceeds twice. |

Use evidenced tax treatment or label and explain the scenario assumption. State whether figures include VAT and how timing affects cash. Use a consistent real or nominal valuation basis, and match each discount rate to its flow perspective, currency, period and price basis. Convert effective annual rates to the chosen period when needed. Model nominal contract debt service on its actual schedule, then translate to the chosen reporting basis if required.

## Keep cash-flow perspectives distinct

- **Project cash flow:** cash generated and invested by the project before debt draws, interest, principal, equity contributions and distributions. Apply taxes consistently with the unlevered perspective when calculating after-tax project returns. State treatment of financing-related tax shields where relevant.
- **Equity cash flow:** investor outflows are contributions. Investor inflows are actual or explicitly modeled distributions and residual proceeds after debt and reserves. Specify distribution policy, retention, additional equity requirements and ownership shares where relevant. If using cash available to equity as a proxy, label it and explain its assumptions.
- **Lender:** calculate DSCR where relevant as cash flow available for debt service divided by scheduled service over the same period. Define numerator and denominator from the term sheet or disclose the convention used, including fees or reserve treatment if applicable. A zero-service period is not applicable. Report the minimum and its date, and compare it with a verified covenant only if available.
- **Economic appraisal:** where requested, assess incremental resource costs and benefits versus a without-project case, relevant external effects, and distribution of impacts. Explain valuation basis and transfers. Keep unpriced effects qualitative and avoid treating financial sales, employment counts or financial IRR as a welfare measure.

## Calculate decision metrics

- For periodic flows use `CF0 + NPV(period_rate, CF1:CFn)` when time-zero cash occurs now. For irregular dates use dated discounting or XNPV with the intended valuation date included as the first date. Explain the timing convention.
- Use IRR for equally spaced flows and XIRR for dated flows. Label period and annualization. Check both signs and confirm NPV at the proposed rate is near zero. With multiple sign changes, test for competing roots over a stated range, explain solver limits, and prioritize NPV at the decision rate if IRR is absent or ambiguous.
- Define simple versus discounted payback and which cash-flow series applies. Use the cumulative crossing and disclose any within-period interpolation. Show if investment is not recovered within the horizon or a later outflow reverses the crossing.
- For a single product with constant contribution, operating breakeven volume is relevant fixed costs divided by unit net price minus variable unit cost. If contribution is nonpositive there is no positive finite breakeven under those assumptions. For multiple products state mix or solve on the actual model. Distinguish accounting breakeven from liquidity or debt-service thresholds.

## Test uncertainty and validate the workbook

Use one-at-a-time sensitivity to identify drivers: price, volume, input/utility cost, investment, ramp, delays, exchange rates or financing as relevant. For a supported model build base, upside and downside scenarios with documented ranges and a coherent combined downside. Change assumptions at their source and propagate effects across all linked schedules. Report effects on profit, cash shortfall, returns and debt service as applicable. Identify switching values for a decision threshold where meaningful. Separate stress cases from forecasts.

For requested Excel, create editable inputs with source cells or an assumptions tab. Link calculations and outputs to inputs, keep dates as real dates, and separate scenario overrides from the baseline. A check tab should show material reconciliations. Recalculate using an available engine, check for formula errors, and independently spot-check at least a key cash-flow/return calculation when material. Modify a driver and verify downstream changes if delivering a scenario workbook. If no engine is available, distinguish formula inspection from recalculation. Do not present a populated financial metric based on blanks treated as zero by spreadsheet functions.

References: [Microsoft Excel NPV and IRR timing](https://support.microsoft.com/en-us/excel/go-with-the-cash-flow-calculate-npv-and-irr-in-excel), [World Bank project finance and DSCR](https://ppp.worldbank.org/financing/issues-in-project-financed-transactions), [World Bank financial and economic analysis](https://documents1.worldbank.org/curated/en/104901591342572602/pdf/Measuring-Jobs-linked-Externalities-in-Private-Investment-Projects-A-Fragility-Conflict-and-Violence-Perspective.pdf).
