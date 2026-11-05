# Milestone 2 — Sensitivity: What Could Change My Profit Decision?

## Starting point

I recomputed the empirical demand staircase using the **39 eligible individual Q8 amounts** in `responses(2).csv`, rather than interpolating between the published Milestone 1 price points. I model one wallet over 12 months, `N = 124`, and `π(p) = [N × n(p)/39] × [0.971p − b − d] − f`, where `b = $13.69` (low cost) or `$22.85` (high cost), `d` is any additional cost per wallet, and `f` is a hypothetical fixed commitment. Prices are evaluated at $0.01 increments across the observed $0–$100 range. I vary **one input at a time**. A robust reading requires **more than 28%** profitable price width; fragile has positive profit but less than 28%; impossible has no profitable price. The precise 28% equality case is not material to the reported rounded thresholds.

At `f = $500`, the verified profitable widths are **64.47%** (low cost) and **48.37%** (high cost): both **robust**. At `f = $3,000`, both are **impossible**. These are conditional models, not Ohsnap financial results or observed sales.

## One-at-a-time thresholds

| Input varied; other inputs held at baseline | Low-cost scenario | High-cost scenario | Meaning |
|---|---|---|---|
| **Fixed commitment `f`**, N=124, no added acquisition expense | Robust ends at approximately **$1,046.25**; no profitable price at **$1,526.41** or higher | Robust ends at approximately **$763.32**; no profitable price at **$1,068.64** or higher | Between these boundaries, the model is fragile. Thresholds are cent-grid approximations. |
| **Reachable population `N`**, f=$500 | First profitable at **41** whole potential buyers; first robust at **60** | First profitable at **59**; first robust at **82** | Assumes the pooled stated-WTP proportions still apply to a different population size. |
| **Extra per-wallet cost `d`**, N=124, f=$500 | Robust ends after about **+$19.55** per wallet; impossible after about **+$28.07** | Robust ends after about **+$10.39**; impossible after about **+$18.91** | Extra costs are **in addition** to the existing variable-cost estimates. |
| **Proportional demand factor**, N=124, f=$500 | Robust needs roughly **47.8%** of modeled demand; any profit needs **more than 32.8%** | Robust needs roughly **65.5%**; any profit needs **more than 46.8%** | This tests a uniform drop in real buying versus stated WTP, not a measured conversion rate. |

At the $3,000 fixed-commitment endpoint, the reachable population would have to increase from 124 to **at least 244** (low cost) or **349** (high cost) for *any* profitable price, and to **356** or **488**, respectively, for a robust reading. I have no evidence that these larger populations are reachable.

## Acquisition-effort threshold

My measured fraternity survey funnel required `124/9 = 13.78` approaches per usable **survey response**, not per paying buyer. For a deliberately optimistic illustration, suppose every usable response became one wallet buyer and each approach cost `a` dollars. This adds `d = (124/9) × a` to each sold wallet. The high-cost model loses robust status at approximately **$0.75 per approach** and becomes impossible at approximately **$1.37 per approach**. The low-cost model loses robust status at approximately **$1.42** and becomes impossible at approximately **$2.04** per approach. A hypothetical `$2` per fraternity approach would imply `$27.56` per usable response; at that assumption, the low-cost case retains a narrow profitable range but is no longer robust, and the high-cost case is impossible.

**None of these are observed acquisition expenses.** I have no measured advertising spend, recruiting hours, or actual paid conversion. If only half of survey respondents bought, approaches per buyer would double and the allowable price per approach would be halved. Reddit's 311 post views are not unique people and should not be priced as direct approaches.

## Changing the *shape* of the demand curve

Uniform demand scaling is not enough: a few high willingness-to-pay answers can change the staircase's shape. As a stress test, I removed the **two $100 answers** from modeled purchasing demand while retaining the original **39-person denominator** (a conservative scenario in which those two do not buy at any price). At `N = 124`, `f = $500`:

| Scenario | Low cost | High cost |
|---|---:|---:|
| Revised peak price | $45 | $45 |
| Revised peak profit | **+$835.61** | **+$427.87** |
| Positive-profit width | **48.86%** | **33.46%** |
| Reading | **Robust** | **Robust** |

Thus the $500 reading survives this **specific** stress test, but both widths shrink and the high-cost case approaches the 28% threshold. This is a modeled exclusion, not a claim that the two respondents were invalid.

## Which belief carries the decision?

For a **single comparable baseline**, I use the **high-variable-cost, $500 fixed-commitment case**, which is robust with a 48.37% positive-profit width. Holding everything else constant, the model loses robust status if fixed commitment rises by about **$263.32 (52.7%)**, or if reachable/converted demand falls to roughly **65.5% of baseline (a 34.5% decrease)**. An added per-wallet cost of about **$10.39** is approximately **40.5% of the $25.69 margin at $49.99** (a comparison price, not the optimum). These percentage comparisons have different denominators and are **not a claim of universal risk ranking**.

**The smallest proportional change among these three scenarios is a roughly 34.5% reduction in actual buying versus stated willingness to pay.** That is my primary *carrying belief*: that enough people who state a price will actually buy. I have not tested purchase conversion. Fixed costs are a separate immediate exposure: the hypothetical $500–$3,000 range itself crosses the robust, fragile, and impossible boundaries, so I also need supplier quotes before any commitment.

## What can be tested, designed, deferred, or treated as fixed?

| Input | Type | Action |
|---|---|---|
| Actual fixed setup/tooling and commitments | **Testable**, partly **designable** | Request itemized written supplier quotes; distinguish setup fees from per-unit manufacturing and avoid double-counting inventory. |
| Manufacturing, shipping, packaging, returns and payment costs | **Testable**, partly **designable** | Obtain vendor and fulfillment estimates at the intended selling price. |
| Reachable qualified buyers and paid conversion | **Testable** | Use channel-specific tracked offers; measure unique people reached and real purchases or permitted preorders. |
| Acquisition effort and money | **Testable**, partly **designable** | Log approaches, time, spending, and actual purchases by channel. |
| Original survey responses and observed $0–$100 range | **Fixed historical evidence** | Preserve the original answers; label any new data separately. |
| Full production and inventory commitment | **Deferrable** | Wait for cost quotes and a small real-purchase test before committing cash. |

If a material assumption cannot be tested or controlled, I would state the exposure explicitly and limit the size of any commitment. I would not use the favorable $500 scenario to justify a 300-unit inventory purchase without evidence that those units can sell.

## My conclusion and verification

The model is **robust at a hypothetical $500 commitment and impossible at $3,000**, under both variable-cost assumptions. The strongest immediate next experiment is a **real-purchase conversion test**, alongside itemized cost quotes. I verified the price staircase against individual survey values, reran the one-cent profit grid, varied inputs one at a time, and checked the high-price-respondent stress test. The earlier $49.99 peak and related sensitivity thresholds were based on an incorrect assumption about three $45 respondents and have been replaced.
