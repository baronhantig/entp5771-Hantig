# Demand system — Wallet A (Ohsnap Wallet 2) and Wallet B (Secrid Cardprotector)

## Data and units

This analysis uses the **two screened-in, retained survey respondents** (`responses.csv`). Quantities are wallets a respondent says they would purchase **per 12 months**; prices and maximum willingness to pay (WTP) are **USD per wallet**. No observations were deleted. These are hypothetical stated quantities, not actual purchases.

- R001: WTP A = $50, WTP B = $40; A quantities `(q00,qA0,q0B,qAB) = (1,1,1,0)`; B quantities `(1,0,1,0)`.
- R002: WTP A = $0, WTP B = $0; all quantities zero. R002 is retained, but supplies no positive-price variation.
- Both respondents passed the three screeners. **n = 2** usable records for descriptive reporting; only **one** has positive WTP for either product.

## Common observed-WTP grid; interpolate first, then sum

The **distinct respondent-named prices** are **A: $0, $50** and **B: $0, $40**. The common grid is the four combinations of those values. For each respondent, the four answers define a bilinear interpolation surface within their WTP rectangle. For a respondent with positive WTP values, let `x = min(pA / WTP_A, 1)` and `y = min(pB / WTP_B, 1)`; inside the rectangle:

`q(pA,pB) = (1-x)(1-y) q00 + x(1-y) qA0 + (1-x)y q0B + xy qAB`.

**Caps:** For demand for A, set quantity to zero when `pA > WTP_A`; for demand for B, set quantity to zero when `pB > WTP_B`. Clamp the *rival's* price to its WTP before interpolation, so further rival-price increases have no additional effect. At a WTP of $0, use the respondent's recorded zero quantity at price $0; quantities above their own zero WTP remain zero. No division by zero is performed. At the four observed grid corners, interpolation reproduces R001's four answers exactly, while R002 contributes zero. Sum the respondent surfaces at **each common grid point**, then fit to these four totals; **do not pool the raw respondent-specific price points into a regression**.

| A price | B price | Total A quantity/year | Total B quantity/year |
|---:|---:|---:|---:|
| $0 | $0 | 1 | 1 |
| $50 | $0 | 1 | 0 |
| $0 | $40 | 1 | 1 |
| $50 | $40 | 0 | 0 |

## Functional forms and sign checks

**Form 1: additive linear system**, least-squares fit to the four aggregated grid cells:

- `q_A = 1.25 - 0.010 p_A - 0.0125 p_B`
- `q_B = 1.00 - 0.000 p_B - 0.0200 p_A`

These are *descriptive fitted coefficients*, not a credible competitive-substitutes demand model. A's own-price coefficient is positive in the required `b` convention (`b_A=0.010`), but **B's `b_B=0`**. Both estimated cross-price terms are **negative** (`d_A=-0.0125`, `d_B=-0.0200`), contrary to the expected substitution signs. The additive model cannot reproduce the four A quantities exactly because they contain a price interaction.

**Form 2: bilinear/interacting surface**, which fits the four grid cells exactly:

- `q_A = 1 - (p_A p_B / 2000)` within the observed WTP rectangle
- `q_B = 1 - (p_A / 50)` within the observed WTP rectangle

Apply the respondent-specific own-WTP and rival-price caps described above outside the observed rectangle. This second form is not the six-parameter additive system: the interaction term captures R001's inconsistent response, rather than a valid substitution effect.

**Illustrative equilibrium-price spread under the survey's price caps (not a credible market forecast):** The fitted additive form has `b_B = 0`, so it cannot generate a conventional unconstrained interior best response for B. If we *also impose the survey's stated own-WTP cap* (demand zero above B's $40 maximum), B's profit-maximizing price in the positive-demand region is the $40 boundary, using Secrid's estimated unit cost of $10–$20. With Ohsnap's estimated cost range of $15.43–$24.59, A's additive-form best response is `(75 + c_A)/2`, or **$45.22–$49.80**. In the bilinear form, B again chooses the $40 boundary; A's best response is `(50 + c_A)/2`, or **$32.72–$37.30**. Thus, across these two forms and Ohsnap's assumed cost range, the *mechanical* implied prices are **A: $32.72–$49.80; B: $40**. At those A prices, B's modeled quantity remains positive, and neither firm's price exceeds its own WTP cap. The spread is large for A (**$12.50 at any fixed cost**) and is dominated by a single respondent's inconsistent responses. It is **not a reliable equilibrium estimate**: the additive form has a zero B own-price slope and negative substitution effects, while the bilinear form has no valid positive substitution term. The boundary price of $40 reflects the respondent's WTP, not an observed market optimum. Without the caps, the additive form does not give a finite conventional B best response.

## Six parameters, in words

The course system is `q_A = a_A - b_A p_A + d_A p_B` and `q_B = a_B - b_B p_B + d_B p_A`.

The additive **sample-level descriptive** coefficients, before any population scaling, mean:

1. **a_A = 1.25:** the fitted intercept predicts 1.25 A wallets per year at both prices zero (the *observed* grid-cell quantity is 1; the intercept differs because the additive fit is imperfect).
2. **a_B = 1.00:** the fitted intercept predicts 1 B wallet per year at both prices zero.
3. **b_A = 0.010:** in this fitted form, each $1 increase in A's price lowers fitted A demand by 0.010 wallets/year, holding B's price fixed.
4. **b_B = 0.000:** the fitted B own-price effect is zero, which is not credible evidence that B buyers ignore price.
5. **d_A = -0.0125:** the fitted model predicts A loses 0.0125 wallets/year when B's price rises $1. This has the wrong sign for substitutes and **must not be interpreted as measured switching toward A**.
6. **d_B = -0.0200:** the fitted model predicts B loses 0.0200 wallets/year when A's price rises $1. This also has the wrong sign and **must not be interpreted as measured switching toward B**.

The negative cross-price coefficients match the data-quality finding in `cleaning.md`: **1/2 (50%)** of all respondents violated each cross-price rule; **1/1 (100%)** of respondents with a positive rival-price change did. These `d` terms are **unusable as substitution estimates**. Both own-price comparisons passed, but B's own-price slope is not identified as a positive response in the additive fit. The qualitative response from R002 explicitly says the product descriptions needed pictures, a possible reason the scenarios were difficult to evaluate.

## Week 11 switching prediction versus the results

In my Week 11 `rival-profile.md`, I predicted **`d_i < d_j`** with **moderate confidence (about 60%)**. I expected Secrid to gain more customers when Ohsnap raised its price than Ohsnap would gain when Secrid raised its price. My reasoning was that Secrid's approximately $49 price, established brand, and familiar card-ejection mechanism might make it easier for Ohsnap buyers to switch to Secrid; moving from Secrid to the approximately $60 Ohsnap wallet could require paying more and changing a familiar routine. The fitted coefficients instead give **`d_i = -0.0125` and `d_j = -0.0200`**, so **`d_i > d_j` numerically**, contrary to my prediction. But both signs are negative, meaning the survey did **not** measure credible switching in either direction. I therefore cannot conclude that my switching-cost prediction was disproved: I may have overestimated Secrid's price and familiarity advantages, or respondents may not have understood the rival-price scenarios or viewed the wallets as close substitutes. The data do not let me distinguish an error about Ohsnap customers from one about Secrid customers. A clearer survey with more responses would be needed to test that distinction.

## Reachable-population rescaling — earlier Scale assignment

Baron's earlier **Scale** analysis defined a defensible directly reachable fraternity population of **N = 124**. That earlier survey used **n = 6** usable fraternity responses and therefore a multiplier of **124 / 6 ≈ 20.7**. The **current second survey** instead has **n = 2** screened-in usable responses, recruited through a single Reddit post. For this assignment the multiplier is therefore **N / n = 124 / 2 = 62**. The Reddit post's 68 views are not treated as the reachable population.

Following Hatch's **explicit classroom scaling convention**, multiply only the fitted additive intercepts by 62 and leave all four slopes unchanged:

| Coefficient | Sample fitted value | Course-prescribed scaled value |
|---|---:|---:|
| `a_A` | 1.25 | **77.50** |
| `a_B` | 1.00 | **62.00** |
| `b_A` | 0.010 | **0.010** |
| `b_B` | 0.000 | **0.000** |
| `d_A` | -0.0125 | **-0.0125** |
| `d_B` | -0.0200 | **-0.0200** |

The resulting classroom-scaled descriptive equations are `q_A = 77.5 - 0.010 p_A - 0.0125 p_B` and `q_B = 62 - 0.000 p_B - 0.0200 p_A`. **These are not reliable forecasts or valid competitive-equilibrium inputs.** The intercepts arise from a poor, tiny-sample additive fit, the cross-price slopes have the wrong signs, and the survey participants were recruited on Reddit rather than sampled from the fraternity population being extrapolated to. The multiplier assumes those two Reddit respondents behave like the 124 fraternity members, which is unverified and particularly implausible here. This classroom convention also differs from conventional aggregate-demand scaling, which would ordinarily scale slopes as well as intercepts; the calculation here follows the assignment's explicit rule rather than asserting a generally valid statistical method.

## What can be concluded

The respondent-specific grid and two model forms were constructed without inventing prices or responses. But there are only two respondents, one has no price variation, and the only respondent with positive WTP gave counterintuitive substitution responses. The estimated cross-price effects cannot support a **credible** equilibrium comparison, a direction-of-switching claim, or a measured competitive advantage. The mechanical, capped-equilibrium spread above is reported solely to meet the form-comparison requirement. A larger, clearer survey with visual product descriptions and common, comprehensible price conditions is needed before treating the six parameters as decision-grade evidence.
