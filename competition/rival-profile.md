# Rival Profile: Ohsnap Wallet 2 vs. Secrid Cardprotector

## Rival and current information

My product is the Bare Bones Ohsnap Wallet 2 (firm *i*), and my closest purchasable rival is the Secrid Cardprotector (firm *j*). In my Week 7 rival research, I found a Secrid retail price of about **$49**, compared with an Ohsnap MSRP of about **$60**. I estimated Secrid's unit cost at **$10–$20**, not from Secrid's own records but from an indirect distributor-cost comparison. I cannot responsibly narrow that range without better manufacturing or wholesale information. Neither retail price is the same as unit cost.

The demand model has two sides:

- `q_i = a_i - b_i*p_i + d_i*p_j` (Ohsnap)
- `q_j = a_j - b_j*p_j + d_j*p_i` (Secrid)

Here, `d_i` describes customers Ohsnap gains when Secrid raises its price, while `d_j` describes customers Secrid gains when Ohsnap raises its price. They do not have to be equal.

## Eight-parameter inventory

| Parameter | Meaning | Status | Basis / what is still needed |
|---|---|---|---|
| `a_i` | Ohsnap's baseline demand / appeal | Coming from survey (estimate) | My demand research can help estimate Ohsnap's demand, though survey responses may not represent the whole market. |
| `b_i` | How Ohsnap demand changes with its own price | Coming from survey (estimate) | Price and purchase-intent responses can inform this, with assumptions needed to scale responses to actual sales. |
| `d_i` | How Ohsnap demand changes when Secrid changes price | Coming from survey (estimate, if the questions support it) | The competition survey can provide evidence about switching toward Ohsnap; the final coefficient may still require modeling assumptions. |
| `c_i` | Ohsnap unit cost | Assumed until verified | I need a defensible production or supplier cost for the specific wallet; the $60 MSRP is a selling price, not a cost. |
| `a_j` | Secrid's baseline demand / appeal | Assumed | My survey of potential Ohsnap customers does not measure Secrid's full market demand; use a clearly labeled scenario until rival-market evidence is available. |
| `b_j` | How Secrid demand changes with its own price | Assumed | No direct Secrid sales or price-response data; a scenario or outside evidence is needed. |
| `d_j` | How Secrid demand changes when Ohsnap changes price | Assumed for now | This is the reverse switching direction. My survey may give clues, but it does not automatically identify a reliable market-wide coefficient. |
| `c_j` | Secrid unit cost | In hand (estimated range) | Week 7 `competition/rival.md`: **$10–$20 per unit**, an indirect estimate, not a published Secrid manufacturing cost. |

**Additional known input:** Secrid's observed price is approximately **$49** from Week 7 research. Price is useful for checking the model, but it is **not** one of the eight demand/cost parameters above.

**Fixed commitment:** Secrid's `f_j` is unknown. I will not invent a figure. It affects whether Secrid earns a profit, but it does **not** change the equilibrium prices in this model because it is a fixed cost.

## Prediction before the competition survey closes

**Prediction: `d_i < d_j`. Confidence: moderate (about 60%).**

I think Ohsnap may have a harder time attracting Secrid customers than Secrid has attracting Ohsnap customers when prices change. A Secrid owner may already be used to its card-ejection mechanism, compact design, and established brand, so switching to Ohsnap requires paying more at current listed prices and changing a familiar routine. For an Ohsnap customer, Secrid's lower listed price and similar slim, quick-access purpose could make switching easier. That said, Ohsnap's distinct features and the attachment some users have to its design could make its customers more loyal than I expect.

I would change my prediction if the competition survey shows that Secrid users are consistently more willing to move to Ohsnap after a price increase than Ohsnap users are to move to Secrid after the same comparable change. I would also reconsider if respondents value Ohsnap's unique features enough to overcome the price difference. The survey closes **November 22**, so this is a prediction, not a finding.

## Sources and limits

- Week 7 rival research: `competition/rival.md` (Secrid price, cost estimate, and switching-cost discussion). This earlier file should remain unchanged.
- Professor Hatch, *How Differentiation Preserves Margin*: https://ea.nilehatch.com/differentiated-competition.html
- Current assignment: *Rival profile, and best responses*, due November 15, 2026.

The numbers in Professor Hatch's three classroom cases are **supplied examples**, not measured parameters for the wallet market. I will not treat those values as real estimates for Ohsnap or Secrid.
