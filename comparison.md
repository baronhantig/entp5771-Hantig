# Milestone I: Demand — Comparison with the Kickstarter Campaign

## Estimated profit-maximizing price

My `curve.md` counts how many of 39 eligible respondents said their maximum willingness to pay was at least each price. To compare prices on an estimated contribution basis, I used `(price − estimated variable cost per wallet) × qualifying respondents`. My earlier `cost-structure.md` estimated variable cost at $15.43–$24.59 per wallet, using public comparables rather than Ohsnap's actual internal costs. That cost range includes a payment-processing benchmark calculated for a $60 transaction; holding it constant across prices is a simplifying assumption, not an exact price-specific cost calculation. Fixed costs are not included.

| Price | Respondents willing to pay | Estimated contribution at $15.43/unit | Estimated contribution at $24.59/unit |
| ---: | ---: | ---: | ---: |
| $35 | 20 | $391.40 | $208.20 |
| $40 | 18 | $442.26 | $277.38 |
| $45 | 16 | **$473.12** | $326.56 |
| $50 | 13 | $449.41 | $330.33 |
| $55 | 11 | $435.27 | **$334.51** |
| $60 | 8 | $356.56 | $283.28 |

Among these evaluated prices, **$45 maximizes estimated contribution in the low-cost scenario**, while **$55 maximizes it in the high-cost scenario**. Neither is a proven real-market profit maximum: these are selected reference prices rather than every individual willingness-to-pay threshold, the unit costs are uncertain, and stated willingness to pay does not guarantee a purchase. The comparison shows that the preferred price depends on cost assumptions.

## Kickstarter price and observed backing

The Ohsnap Wallet 2 Kickstarter offered the **Bare Bones** reward at **$45**, advertised against a **$60 MSRP**. The saved September 4, 2026 campaign rewards snapshot also shows other configurations at **$52, $56, $63, and $67**. These tiers offered different components and bundles, so they are not five prices for an identical product and cannot be turned into a demand curve. The completed campaign reports **5,532 backers and $465,897 pledged** (Kickstarter campaign page). A backer count is not necessarily the number of Bare Bones wallets sold: people could choose other rewards, pledge without a reward, or purchase add-ons.

The $45 Bare Bones Kickstarter tier matches the **low-cost scenario's** preferred price among the prices tested in my sample. My high-cost scenario favors $55, close to—but not equivalent to—the $56 tiers, which included different configurations. At $45, **16 of my 39 eligible respondents (41.0%)** stated they would pay at least that amount for one bare-bones wallet during the next 12 months. That is a sample threshold count, **not 16 confirmed buyers**.

## Reachable quantity and why the numbers differ

My earlier access analysis identified **124 fraternity members** as a directly reachable population; Reddit's post views do not establish a similarly identifiable population of prospective buyers. If I *illustratively* applied the pooled survey's 16/39 willingness-to-pay share at $45 to those 124 people, the result would be approximately **51 potentially willing people** (`124 × 16/39 ≈ 51`). This is **not a reliable forecast**: the 39 responses combine fraternity and Reddit respondents, the channels were not separately tagged, and survey volunteers may differ from nonrespondents. The only directly observed quantity in my sample is 16 respondents stating willingness at $45, not actual purchases or 51 verified reachable buyers.

The campaign's **5,532 backers** are therefore not evidence that my curve is wrong, nor does my smaller estimate predict Kickstarter's national sales. My survey used a relatively neutral product description and recruited through two convenience channels; Ohsnap used a promotional campaign, discounts, imagery, and an established brand to attract a much larger, self-selected audience already interested enough to consider pledging. Most importantly, a survey answer describes what someone says they might pay, while Kickstarter backers committed money to a particular reward. The campaign is stronger evidence of actual purchasing interest, but its different bundles, capacity limits, add-ons, and changing availability prevent its reward tiers and backer count from serving as an empirical demand curve for one bare-bones wallet.

## Sources and calculation trail

- `demand/curve.md` — 39 eligible numeric willingness-to-pay responses and price threshold counts.
- `cost-structure.md` — estimated variable cost of $15.43–$24.59 per wallet; not Ohsnap's actual supplier cost.
- `scale.md` — 124-person directly reachable fraternity population, with limitations on extrapolation.
- Saved Kickstarter rewards PDF, *Ohsnap Wallet 2 - Couldn't Carry Less — Rewards*, captured September 4, 2026 (reward prices $45, $52, $56, $63, $67): https://www.kickstarter.com/projects/ohsnapofficial/ohsnap-wallet-2-couldnt-carry-less/rewards
- Completed Kickstarter campaign totals (5,532 backers; $465,897 pledged): https://www.kickstarter.com/projects/ohsnapofficial/ohsnap-wallet-2-couldnt-carry-less/

## 6. Explain My Own Data

What surprised me most about my demand curve was that only 8 out of 39 respondents (20.5%) were willing to pay the $60 retail price for the Bare Bones Wallet 2. At $45, that number doubled to 16 respondents. I think the biggest reason is that many of the people I surveyed were college students on a budget who probably would not prioritize spending $60 on a new wallet. Most people also already own a wallet that works, so replacing it is not an urgent purchase. For someone to spend that much money, the new wallet would need to offer enough convenience or improvement over their current wallet to make switching worthwhile. I think this explanation is plausible because my survey reached mostly college-aged consumers rather than people specifically shopping for premium wallets. However, I cannot prove these were their reasons because the survey measured willingness to pay rather than asking why respondents chose their prices.
