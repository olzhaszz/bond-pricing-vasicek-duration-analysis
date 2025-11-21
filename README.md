# Bond Pricing and Duration Analysis

This repository contains a small fixed-income valuation project focused on
zero-coupon bond pricing and interest rate risk measurement via duration.

## Description

The analysis covers three core tasks:

1. **Zero-coupon bond under flat yield curve**  
   - Compute the present value of a zero-coupon bond with 15 years to maturity.  
   - Assume a horizontal (flat) yield curve with a constant yield of 5%.  
   - Use the standard formula  
     \[
       P = \frac{F}{(1 + r)^t}
     \]
     where \(P\) is the price, \(F\) is face value, \(r\) is yield, and \(t\) is time to maturity.

2. **Zero-coupon bond under Vasicek model**  
   - Price the same 15-year zero-coupon bond using a **Vasicek short-rate model**.  
   - Parameters: initial short rate \(r_0 = 0.015\), mean reversion speed \(\alpha = 0.5\),
     long-run mean \(\beta = 0.025\), and volatility \(\sigma = 0.015\).  
   - Compare the Vasicek-implied price to the flat-yield price and interpret the
     impact of mean reversion and interest rate uncertainty on discounting.

3. **Macaulay and modified duration of a coupon bond**  
   - Consider a bond with:
     - Annual coupon rate: 4.5% (coupon paid once per year),
     - Maturity: 15 years,
     - Par value repaid at maturity,
     - Market interest rate (yield to maturity): 5%.  
   - Compute:
     - **Macaulay duration** as the weighted average time of cash flows,
     - **Modified duration** as an interest rate sensitivity measure.  
   - Interpret duration as the approximate percentage price change for
     a 1% (100 bps) change in yield.

## Files

A suggested structure:

- `notebooks/` – Jupyter notebook(s) with the full calculations and explanations  
  - e.g. `bond_pricing_and_duration.ipynb`
- `src/` – Python scripts implementing:
  - Zero-coupon bond pricing,
  - Vasicek model-based bond pricing,
  - Macaulay and modified duration calculations.
- `figures/` – (Optional) Plots or tables summarizing sensitivity and results.
- `README.md` – Project overview (this file).

Adapt the structure as needed for your implementation.

## Methods

The project applies standard fixed-income and term-structure tools:

- Time value of money and present value formulas,
- Continuous-time short-rate modeling via the **Vasicek model**,
- Duration as a first-order approximation of price sensitivity to interest rate changes.

All formulas and calculations are documented in the accompanying notebook/script.

Interpretation of Results

The final section of the analysis discusses:

The present value of a long-maturity zero-coupon bond under a flat 5% yield curve.

How the Vasicek term structure changes the price by incorporating
mean reversion and rate volatility.

The Macaulay and modified duration of the coupon bond, and how
these measures indicate the approximate percentage price change following a
1% increase or decrease in market interest rates.
