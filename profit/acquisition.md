# Milestone 2 — Acquisition: What a Customer Costs

## Funnel evidence and effort per usable response

My Milestone 1 survey used two recruiting channels: my University of Utah fraternity and a Reddit r/SampleSize post. The fraternity produced **9 usable completed responses from 124 approaches**, or **124 / 9 = 13.78 approaches per usable response**. Reddit produced **30 usable responses attributed by elimination from 311 post views**, or **311 / 30 = 10.37 post views per attributed usable response**. Together these are **39 usable responses from 435 recorded approaches/views**, or **11.15 mixed exposures per usable response**, but the combined figure is not a clean person-to-person conversion rate.

These numbers describe **survey recruiting, not customer acquisition**. The Google Form did not record the respondent's channel; I identified nine fraternity completions and attributed the remaining 30 to Reddit. Reddit post views can repeat and do not represent unique identifiable people. I also did not record hours spent recruiting, advertising expenditures, or actual purchases. I cannot honestly convert these results into an observed dollar cost per customer.

## Margin available to cover acquisition

My corrected profit model peaks at **$45** in the low-cost scenario and **$55** in the high-cost scenario. For a common **illustrative comparison price of $49.99** (not a verified optimum), the price-adjusted variable-cost assumptions are:

- Low: `c_low(49.99) = 13.69 + 0.029 × 49.99 = $15.13971`; margin `p − c = $34.85029` (about **$34.85**).
- High: `c_high(49.99) = 22.85 + 0.029 × 49.99 = $24.29971`; margin `p − c = $25.69029` (about **$25.69**).

My survey asks about **one wallet per respondent during 12 months**. Under that one-wallet assumption, **one actual buyer would have to buy one wallet** to cover an acquisition cost at or below the contribution margin. If acquisition costs exceeded $25.69–$34.85 per buyer, one wallet would not cover them, even before accounting for fixed commitments. I cannot assume repeat purchases to rescue the calculation.

For a hypothetical acquisition cost per paying buyer `A`, the wallets required to recover it are `ceil(A / margin per wallet)`. For example, at $49.99 and `A = $27.56`, one wallet covers the low-cost margin ($34.85), while **two wallets** would be required at the high-cost margin ($25.69). My 12-month model assumes **one wallet per buyer**, so the two-wallet outcome would **not** be viable under that assumption. This $27.56 is hypothetical, not observed.

## What if reaching people required payment?

No documented money changed hands for these approaches, and I did not measure recruiting hours. Rather than invent a wage, booth fee, or ad spend, I can calculate **break-even ceilings**. If every usable survey response became one paying customer (an optimistic, unverified assumption), the most I could spend **per approach/view** before exhausting the margin would be:

| Channel | Recorded approaches/views per usable response | Ceiling per approach/view at $34.85 margin | Ceiling at $25.69 margin |
|---|---:|---:|---:|
| Fraternity | 13.78 | $2.53 | $1.86 |
| Reddit (views, not unique people) | 10.37 | $3.36 | $2.48 |

These are **conditional thresholds, not actual acquisition costs or recommended advertising bids**. **Illustration only:** Suppose each fraternity approach hypothetically cost $2. The 124 approaches would then cost $248, or **$248 / 9 = $27.56 per usable completed survey response**. I did not report paying this amount, and **$27.56 is not an observed customer-acquisition cost**. Only under the additional, unverified assumption that every survey respondent bought one wallet would $27.56 also be the cost per buyer. In that optimistic case, it would be below the low-cost contribution margin ($34.85) but above the high-cost margin ($25.69). The measured result is **13.78 approaches per usable survey response**, not a dollar cost per customer.

Any conversion rate below 100% from survey respondent to paying customer would increase the number of approaches needed per buyer, assuming the same recruiting pattern. If only half of usable respondents bought, the approaches/views per buyer would double, and the allowable spend per approach/view would halve. I have not measured that conversion rate, so I cannot present a dollar customer-acquisition cost as a fact.

## Does the margin survive reaching the buyer?

**I cannot establish that it does.** The modeled margin at the illustrative $49.99 price is positive before acquisition, but I have measured only the effort to obtain free survey responses, not paid orders or hours/dollars spent. The fraternity is directly accessible, but it took nearly 14 approaches per usable response; Reddit's roughly 10 views per inferred response cannot be treated as a repeatable customer-recruitment process. Acquiring a paying customer could require more effort than obtaining a survey response. Any real acquisition expense would also reduce the positive-profit regions in `profit-model.md`, which currently exclude that expense.

My next useful measurement would be a **small, permission-based real purchase or preorder test** with separate tracked recruiting links for each channel, recording unique approaches, time or money spent, and completed purchases. That would let me estimate actual acquisition cost per paying customer and test whether the contribution margin survives it. Until then, acquisition is a consequential uncertainty, not a demonstrated advantage.

## Checks and limitations

- Hand-check: `124 / 9 = 13.78` and `311 / 30 = 10.37`; neither denominator is a verified count of paying customers.
- At $49.99, the variable payment fee is recalculated as `0.029 × 49.99 + 0.30`, not held at the $60-price fee.
- The per-approach ceilings assume one wallet per buyer and a **100% conversion of usable responses into buyers**, solely to show an optimistic upper bound.
- Survey recruiting and customer acquisition are different stages; these figures must not be described as observed acquisition costs.
