# Iran project conventions

## Currency, dates and price basis

- Preserve the original unit on extraction. Normalize through a documented factor before aggregating. On the ordinary rial/toman convention, 1 toman = 10 rials, 1 thousand rials = 100 tomans, and 1 million tomans = 10 million rials. Confirm any different convention used by the source. Round for display after calculation and state the display scale.
- Record the source's Solar Hijri date, quote validity and price-base date. Convert to a verified Gregorian calendar date where software requires it, or use consistent period indexes for periodic models. Keep the displayed Jalali label. Separate time of reporting, valuation and commissioning.
- Record the original currency for imports and other FX exposures, the conversion rate, rate type, source and date. Include timing and the relevant duties, taxes, logistics, finance and payment costs only as supported. Make FX and inflation sensitivities visible. Escalate relevant lines individually where evidence calls for it.

## Verifying finance and execution

- For financing, record lender, approved terms and evidence, requested/approved/drawn status, availability dates, equity requirements, collateral, fees, grace-period treatment, payment convention and repayment schedule. Confirm terms from a dated lender document or mark them pending. Model delayed or smaller draw when it is decision-relevant.
- Confirm applicable tax, permit, environmental, utility, tariff, FX and import requirements against relevant official or contractual sources for the project and report date. Record sources and effective dates. Avoid universal rates, regulatory assumptions or claims of acceptance by a bank based on a generic template. Ask for the lender's template if formal submission is in scope.
- Preserve distinctions such as list or negotiated price, ex-works or delivered, cash or credit terms, VAT-inclusive or exclusive, tax expense or recoverable VAT, and Iranian versus imported inputs. Flag unknowns that could shift timing, costs or financing.
