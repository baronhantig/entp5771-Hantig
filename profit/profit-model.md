# Milestone 2 — Profit Model and Reading

## Method and reconciled assumptions

I model one Bare Bones Ohsnap Wallet 2 per potential buyer over 12 months. My original survey contains 42 submissions, of which 39 meet the three screeners and have numeric willingness-to-pay responses. I used the **individual Q8 responses** in `responses(2).csv` to build the exact empirical staircase: `n(p)` is the number of eligible people with stated maximum willingness to pay **at least** price `p`. The observed price range is **$0–$100**, evaluated at one-cent increments. This is stated willingness to pay, **not actual sales**.

My reachable-population scenario is `N = 124`, the fraternity members I could identify and approach. I scale quantity as `q(p) = 124 × n(p) / 39`. Because the 39 eligible respondents include Reddit recruits, applying the pooled curve to the fraternity population is an **untested representativeness assumption**. Reddit views are not added to N.

Week 6 variable costs were $15.43–$24.59 **at a $60 sale price**, including a $2.04 payment-processing fee (2.9% plus $0.30). For other prices I recalculate processing:

- Low cost: `c_low(p) = 13.69 + 0.029p`.
- High cost: `c_high(p) = 22.85 + 0.029p`.
- Profit: `π(p) = [124 × n(p)/39] × [p − c(p)] − f`.

I retain Week 6's **hypothetical** incremental fixed-commitment endpoints, `$500` and `$3,000`; neither is verified Ohsnap spending. I do not add the comparable supplier's 300-unit inventory purchase to fixed cost while also including manufacturing in per-wallet cost. The inventory minimum remains a separate cash and unsold-stock exposure.

## Results verified from individual survey responses

| Variable cost | Fixed commitment | Price of highest modeled profit | Highest modeled profit | Positive-profit cent-price intervals | Positive width of $0–$100 range | Reading |
|---|---:|---:|---:|---|---:|---|
| Low | $500 | **$45.00** | **+$1,026.41** | $19.89–$19.99; $20.58–$80.00; $95.08–$100.00 | **64.47%** | **Robust** |
| High | $500 | **$55.00** | **+$568.64** | $31.64–$80.00 | **48.37%** | **Robust** |
| Low | $3,000 | $45.00 | **−$1,473.59** | None | 0% | **Impossible** |
| High | $3,000 | $55.00 | **−$1,931.36** | None | 0% | **Impossible** |

A price is profitable only if `π(p) > 0`. Width is the number of profitable cent-grid prices divided by 100 (approximately the width in dollars divided by the $100 observed range). It **adds disjoint profitable intervals**, rather than filling the gaps. Hatch's reading is impossible if no price is profitable, fragile if the profitable width is under 28%, and robust if it exceeds 28%. At $3,000, the listed peak is merely the **least negative** outcome.

## Hand checks and why the peaks changed

At **$45**, exactly **16 of 39** eligible respondents have maximum stated willingness to pay of at least $45. Low-cost margin is `0.971 × $45 − $13.69 = $30.005`. Modeled quantity is `124 × 16 / 39 = 50.8718`, yielding `50.8718 × $30.005 − $500 = **$1,026.41**`.

At **$55**, exactly **11 of 39** respondents qualify. High-cost margin is `0.971 × $55 − $22.85 = $30.555`. Modeled quantity is `124 × 11 / 39 = 34.9744`, yielding `34.9744 × $30.555 − $500 = **$568.64**`.

The earlier draft incorrectly claimed that **16 respondents** would pay **$49.99**. The original Q8 responses show **three respondents answered $45**, so only **13 respondents** would pay $49.99. That invalidated the earlier $49.99 optimum and several intervals. I recalculated every one-cent price directly from the raw answers. The low-cost model now peaks at $45 and the high-cost model at $55.

## Interpretation and limitations

At a hypothetical $500 fixed commitment, the profitable price range exceeds Hatch's 28% robust threshold under both variable-cost scenarios. At $3,000, neither scenario has any profitable price. **The business is not demonstrated to be profitable**: the fixed commitments are unverified, the demand curve comes from a small convenience sample, the pooled respondents may not represent the fraternity, and the model assumes stated willingness to pay becomes a purchase. Acquisition expenses have not yet been deducted. Just two respondents reported $100, making the isolated high-price profitable interval in the low-cost case especially uncertain. A 300-unit minimum order could also require cash before any of the modeled sales occur.

**My decision:** The profit scenarios justify testing actual costs and real buying behavior, not committing to broad production now.
