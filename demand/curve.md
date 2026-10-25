# Milestone 1 — Empirical Demand Curve

## Survey measure and method

The survey asked each respondent: “What is the most you would pay, in U.S. dollars, for one bare bones modular wallet during the next 12 months?” This is a **maximum willingness-to-pay** question for one wallet, not a three-anchor quantity instrument.

I built an **empirical staircase demand curve** from the 39 eligible respondents with numeric answers. At each listed price, I count each respondent **once** if their stated maximum willingness to pay is greater than or equal to that price. I then add those individual indicators to obtain the sample count. I do not assume that one person's answer predicts another person's behavior.

No interpolation or fitted mathematical function was used. In particular, the three-anchor interpolation method does not apply because this survey did not ask for quantities at free, intermediate, and maximum prices. The empirical staircase is the estimate reported here; there is no fitted curve to report.

## Source-data audit and exclusions

The original response sheet contains **42 submitted rows**. Three are excluded from the willingness-to-pay analysis:

- **Spreadsheet row 2:** Age screener answered “Yes,” but the wallet-choice and physical-card screeners and price answer were blank.
- **Spreadsheet row 4:** Answered “No” to carrying physical cards at least occasionally and left the price answer blank.
- **Spreadsheet row 5:** Answered “No” to personally choosing a wallet/card holder and left the price answer blank.

That leaves **39 eligible respondents** with valid numeric maximum-price answers. The full per-column blank audit and exclusion rules are documented in `cleaning.md`. A missing product-familiarity answer among otherwise eligible respondents does not invalidate a numeric price response.

Three source-data checks that require no fitted model:

| Known quantity | Verified result |
|---|---:|
| Eligible numeric responses | 39 |
| Respondents who explicitly typed $0 | 8 |
| Highest stated maximum | $100 |

The **lowest** stated maximum was $0, and the **median** was $35. All eight typed $0 answers remain in the sample. Blank price cells were **not** converted to zero.

## Empirical demand staircase

Each count is the number of eligible respondents whose stated maximum is **at least** the listed price. The shares use 39 as the denominator.

| Price (USD) | Willing respondents | Share of 39 |
|---:|---:|---:|
| $0.00 | 39 | 100.0% |
| $10.00 | 31 | 79.5% |
| $15.00 | 31 | 79.5% |
| $19.99 | 28 | 71.8% |
| $20.00 | 27 | 69.2% |
| $22.00 | 25 | 64.1% |
| $25.00 | 24 | 61.5% |
| $30.00 | 22 | 56.4% |
| $35.00 | 20 | 51.3% |
| $40.00 | 18 | 46.2% |
| $45.00 | 16 | 41.0% |
| $50.00 | 13 | 33.3% |
| $55.00 | 11 | 28.2% |
| $60.00 | 8 | 20.5% |
| $70.00 | 6 | 15.4% |
| $80.00 | 4 | 10.3% |
| $90.00 | 2 | 5.1% |
| $100.00 | 2 | 5.1% |

**Important boundary detail:** All 39 respondents meet the threshold at exactly $0. At any *positive* price below $15, the count is 31 because eight respondents gave a maximum of $0. At any price **above $100**, the observed threshold count is zero. This is a staircase, so the count stays constant between successive stated maximum prices and changes only when a threshold is crossed.

## Pricing interpretation

At the proposed **$60** price, **8 of 39 respondents (20.5%)** reported a maximum willingness to pay of at least $60. I wanted to explore lower prices at which approximately **35%–45%** of eligible respondents would be willing to pay. The closest price among the reference prices examined was **$45**, with **16 of 39 (41.0%)**; at **$40**, **18 of 39 (46.2%)** met the threshold.

For an illustrative gross-revenue comparison, I multiplied each price by the number of respondents whose maximum met that price. This assumes that **every qualifying respondent buys exactly one wallet** at that price; it is **not** an observed sales figure or a real-market revenue forecast.

| Price | Qualifying respondents | Illustrative gross revenue |
|---:|---:|---:|
| $35 | 20 | $700 |
| $40 | 18 | $720 |
| $45 | 16 | $720 |
| $50 | 13 | $650 |
| $55 | 11 | $605 |
| $60 | 8 | $480 |

Both $40 and $45 yield **$720** in this illustrative comparison, versus **$480** at $60. That is **$240 more**, or **50% higher illustrative gross revenue**. The $45 price achieves the same illustrative gross revenue with two fewer units, which could matter for variable costs. However, **the survey does not establish the profit-maximizing price**: actual conversion, unit costs, fulfillment, fees, and the representativeness of the sample are unknown. The difference between 16 and 18 respondents is small, so both $40 and $45 are pricing hypotheses worth testing, not proven market outcomes.

## Sanity checks and limits

1. **Nonnegative and non-increasing:** Every empirical quantity is between 0 and 39, and the count never rises as the price increases.
2. **No implausible zero-price explosion:** At $0 the maximum sample count is 39, not an unlimited number of wallets. The unit is **one wallet per respondent during the next 12 months**, not wallets per month.
3. **High-price behavior:** Two respondents stated a maximum of $100, and none stated a maximum above it; the staircase therefore falls to zero at any price above $100.
4. **Match to the staircase:** No fitted line was overlaid or substituted. Every listed count comes from the individual price thresholds, rather than a smooth function that could sit above or below the observations.
5. **Known-value checks:** The table gives 39 at $0, 8 at $60, and 2 at $100, matching the underlying respondent-level counts. The eight $0 answers remain in the data.
6. **Evidence boundaries:** The minimum and maximum observed answers are **$0 and $100**. The proposed $60 price, and the alternative $40 and $45 prices, fall inside that range. The observed sample supports a threshold count over that range; it does **not** establish purchasing behavior for the wider market, quantities greater than one wallet per person, or demand in a different time period. A smooth model outside the observed range would require additional assumptions; none was fitted here.
7. **Survey limitations:** The respondents were recruited through convenience channels rather than a representative random sample. Stated willingness to pay may differ from actual purchases, and the question itself may influence responses. These limits cannot be fixed merely by choosing a different mathematical curve.

## Calculation and transcription verification

The original spreadsheet was reopened and the eligible responses were recalculated from the source data. For each reference price `p`, the count is:

`number of eligible respondents with Q8 maximum >= p`

Equivalent spreadsheet logic on the **39 eligible numeric Q8 cells** is `COUNTIF(valid_WTP_range, ">=" & p)`; this formula must not include ineligible or blank responses. The table was checked price by price against the recalculated counts, including $40 = 18, $45 = 16, $60 = 8, and $100 = 2. The raw responses were left unchanged.

**Conclusion:** The empirical evidence shows substantially fewer respondents willing to pay the proposed $60 price than $40 or $45. I would consider $40 and $45 as candidates for a real-world price test, while avoiding a final pricing or profit claim until purchasing and cost evidence is available.
