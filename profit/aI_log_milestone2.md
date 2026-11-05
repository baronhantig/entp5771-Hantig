# Milestone 2 — AI Supervision Log

## How I used AI

I used ChatGPT as a project assistant to interpret Professor Hatch's instructions, organize the six `profit/` deliverables, draft explanations, and calculate a profit model from my earlier demand and cost work. I reviewed the assumptions and asked for additional checks rather than treating its first numerical output as final. This log records the important decisions, mistakes, and corrections. I am responsible for reviewing these statements and the final files before submitting them.

## 1. Reconcile the inputs

**Prompt/task:** Compare my Week 6 cost and scale files with the final Milestone 1 demand curve and funnel, and draft `inputs.md` without changing the unit or period.

**AI output and my decision:** We kept one Bare Bones Ohsnap Wallet 2 over a 12-month period, a reachable fraternity population of `N = 124`, and the Week 6 variable-cost range of $15.43–$24.59 per wallet at a $60 price. I agreed to retain $500–$3,000 as **hypothetical** fixed-commitment scenarios, not actual Ohsnap expenses. We did not add Reddit post views to `N` because they are not unique, identifiable buyers. We also identified that the 39-person pooled willingness-to-pay sample may not represent the fraternity population.

**Check:** The $60 payment fee of $2.04 equals 2.9% of $60 plus $0.30. At other prices the model must recalculate that fee. We also kept a possible 300-unit inventory purchase separate from fixed cost to avoid counting manufacturing both per unit and again as a fixed expense.

## 2. Initial profit model — an error that required correction

**Prompt/task:** Apply the empirical willingness-to-pay staircase to `N = 124`, the low/high variable costs, and the $500/$3,000 fixed-commitment scenarios. Identify the best modeled price and profitable price widths.

**Initial AI output:** ChatGPT reported $49.99 as the best price for both cost scenarios and gave precise profitable intervals and sensitivity thresholds. It initially described those results as independently verified.

**Problem I challenged:** The published Milestone 1 curve showed 16 people willing to pay at least $45 but only 13 at least $50. Those counts alone did **not** establish that all 16 would pay $49.99. We revisited the assumption instead of accepting the exact-looking answer.

**Evidence supplied and correction:** I provided the original `responses(2).csv` with 42 submissions and 39 eligible numeric willingness-to-pay responses. The individual responses showed that three respondents gave **$45**, so they could not be counted at $49.99. We reran the model against each eligible respondent's actual maximum price on a one-cent grid from $0 to $100. The corrected peak is **$45** for the low-variable-cost scenario and **$55** for the high-variable-cost scenario—not $49.99 for both.

**Numerical checks:** The price-dependent contribution margin is `0.971p − 13.69` (low cost) or `0.971p − 22.85` (high cost), and modeled profit is `[124 × n(p)/39] × margin − f`. At $45, `n = 16`; the low-cost $500 scenario peaks at **+$1,026.41**. At $55, `n = 11`; the high-cost $500 scenario peaks at **+$568.64**. At $3,000 fixed commitment, both peak profits are negative (**−$1,473.59** and **−$1,931.36**). The $500 cases remain **robust** (64.47% and 48.37% profitable widths), while the $3,000 cases are **impossible**. I replaced the earlier profit-model results and any dependent figures.

**Lesson:** A table of selected price points is not sufficient to certify every one-cent threshold. I needed the respondent-level answers to check the staircase. The first AI assurance of verification was too strong.

## 3. Acquisition analysis — distinguishing effort from money

**Prompt/task:** Calculate the recruiting effort per usable response by channel, relate it to per-wallet margin, and explain whether margin can cover acquisition effort without inventing spending.

**Check and clarification:** The final funnel reports **124 fraternity approaches for 9 usable responses**, or **13.78 approaches per survey response**. Reddit recorded **311 post views and 30 responses inferred by subtraction**, or **10.37 views per inferred response**; views are not necessarily unique people and are not equivalent to direct approaches. We cannot turn those survey rates into a real cost per paying customer.

I asked what the AI's hypothetical **$2 per fraternity approach** meant. It explained that `124 × $2 / 9 = $27.56` would be a **hypothetical cost per completed survey response**, not an observed expense or customer-acquisition cost. We revised `acquisition.md` to emphasize the measured effort and label the illustration clearly. We also clarified that $49.99 is only a comparison price in that discussion, **not** the corrected profit-maximizing price. No paid-customer conversion, actual recruiting hours, or real acquisition spending was measured.

## 4. Sensitivity — recalculating thresholds and stress-testing demand

**Prompt/task:** Change fixed commitments, reachable population, additional per-wallet costs/acquisition effort, and demand one at a time. Find thresholds where the reading changes, rather than just saying which input matters most.

**Correction:** Because the first profit model had used the wrong staircase, its sensitivity thresholds also needed to be recalculated. Using the original respondent-level data and a one-cent price grid, the $500 fixed-cost model loses **robust** status at approximately **$1,046.25** in fixed commitment under low variable costs and **$763.32** under high variable costs. At approximately **$1,526.41** and **$1,068.64**, respectively, no profitable price remains. These are modeled thresholds, not verified Ohsnap bills.

**Additional test:** We removed the two $100 willingness-to-pay answers from modeled demand while retaining the 39-person denominator. The $500 scenarios still classified as robust, with widths of **48.86%** (low cost) and **33.46%** (high cost). This is a stress test, not a claim that the two respondents were invalid.

**Carrying belief and decision:** In the high-cost, $500 baseline, a reduction of modeled purchasing to about **65.5%** of the original level eliminates the robust reading. The assumption that stated willingness to pay will become actual buying is therefore a major untested belief. Fixed commitments are also critical because our $500–$3,000 scenario range spans robust and impossible outcomes. I chose to recommend testing real purchasing and obtaining written cost quotes rather than treating the favorable scenario as a green light.

## 5. Return to my Week 3 decision question

**Prompt/task:** Compare the milestone results with my *actual* Week 3 decision and stopping rule instead of reconstructing them from memory.

**Evidence check:** I supplied the original Week 3 `project/decision.md` PDF. My precommitted question was whether **at least 30%** of qualified people unfamiliar with Ohsnap would purchase at **$60**, with a stopping rule of **at least 50** qualified responses. The final survey had **8 of 39 (20.5%)** at $60 and did not reach the planned sample size.

**Decision:** I would **not** commit to broader production based on this evidence. The corrected profit model suggests that a $45–$55 price experiment may be worth testing, but a favorable hypothetical profit scenario is not evidence of actual purchases or verified costs. The next actionable question is whether qualified people will make real purchase commitments at a clearly stated test price, at an acquisition effort and verified cost structure that leave positive margin.

## 6. Final cross-file consistency checks and remaining limits

I checked that `inputs.md`, `profit-model.md`, `acquisition.md`, `sensitivity.md`, and `next-question.md` consistently use one wallet, a 12-month period, `N = 124`, 39 eligible survey responses, the price-adjusted processing fee, and hypothetical fixed commitments. The corrected model's peak prices are **$45 low cost / $55 high cost**; any mention of **$49.99** elsewhere is an illustrative comparison price only. The Week 3 outcome remains **8/39 at $60**, below 30% and short of the planned 50 responses.

**Limits I cannot resolve from this dataset:** Actual Ohsnap manufacturing/tooling/fixed costs; representativeness of the pooled sample; actual paid-customer conversion; acquisition spending or hours; and whether a 300-unit inventory commitment could be financed and sold through. These are reasons to test and seek quotes, not numbers to invent.

**My final call:** Do not make the broader production commitment yet. Verify supplier and fulfillment costs and run a limited, tracked real-purchase test before reconsidering.
