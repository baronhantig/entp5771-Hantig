# Milestone I — AI Supervision Log

## Purpose and tools

I used ChatGPT to help organize my survey analysis, check calculations, and draft Markdown files for the `demand/` folder. I treated its outputs as suggestions to verify, not as evidence. The Google Forms export, my recruitment records, the campaign rewards documentation, and my earlier cost-structure work were the sources of evidence.

## What I asked, what came back, and what I did

| Task / request | AI output | My supervision and decision |
| --- | --- | --- |
| Clean the survey responses and build the demand curve | A proposed screening and willingness-to-pay analysis | I checked the analysis against the original 42 submitted form rows. Three rows did not meet or complete the required screeners and lacked usable willingness-to-pay answers. I retained 39 eligible numeric answers. |
| Handle blanks and zero-dollar answers | Guidance on distinguishing missing responses from actual $0 answers | I checked the underlying entries rather than automatically treating blanks as zero. Eight eligible respondents explicitly entered $0; they stayed in the demand curve. Three excluded rows with missing price answers were not turned into invented $0 buyers. |
| Estimate demand at different prices | An empirical staircase using each respondent's maximum willingness to pay | I checked known counts before relying on the rest: 39 eligible respondents at $0, 18 at $40, 16 at $45, 8 at $60, and 2 at $100. The method counts each eligible respondent once when their stated maximum is at least the tested price. No fitted line or interpolation was used. |
| Interpret the pricing results | An illustrative revenue comparison and discussion of $40, $45, and $60 | I kept revenue separate from profit. The $40 and $45 options each produced $720 in illustrative sample revenue, but that alone did not establish a profit-maximizing price. For the campaign comparison, I used the earlier estimated variable-cost range of $15.43–$24.59 per wallet and identified the sensitivity of the estimated contribution-maximizing price to those assumptions. |
| Report recruitment by channel | A funnel table and suggested conversion calculations | I checked what the recruitment tools actually recorded. The fraternity had 124 approaches and 9 known usable responses; Reddit had 311 post views, and the remaining 30 usable responses were attributed to Reddit by elimination. I did not invent channel-specific form starts or screener passes, since both channels shared the same form link. |
| Compare the survey to Kickstarter | A comparison of sample pricing with campaign reward tiers and backers | I used campaign documentation for tier descriptions and prices rather than treating tiers as points on a demand curve. I kept the 39-person convenience sample separate from actual campaign backers and noted that a survey answer is not a purchase. |
| Explain a feature of my own data | A suggested paragraph about the small number willing to pay $60 | I chose the feature myself: only 8 of 39 respondents would pay $60. I supplied my own interpretation that many respondents were budget-conscious college students and already owned functional wallets, so the convenience of switching would have to justify the price. I also noted that the survey did not directly ask respondents why they chose their amounts. |

## Checks and dead ends

**Blank versus zero was an important potential error.** If I had converted every missing price answer to $0, the curve would have included non-buyers who never actually gave a price. I went back to the source rows, excluded three unusable submissions with documented reasons, and kept the eight genuine $0 answers. That decision affects the shape of the curve, especially at low prices.

**Revenue was not the same as profit.** The initial demand-curve comparison showed a revenue tie between $40 and $45. I did not call either one a proven profit-maximizing price. I used a separate variable-cost sensitivity check for the campaign comparison; it still cannot establish Ohsnap's actual profit because the company's true costs and real conversion rates are unknown.

**The recruitment funnel could not be fully reconstructed.** Google Forms showed submitted responses, not everyone who started and abandoned the form. The shared link also prevented reliable channel-specific screener counts. Rather than fill missing cells with estimates, I reported those stages as unmeasurable and identified Reddit's 30 responses as an inference, not direct source tracking.

**A smooth fitted curve was not appropriate for this instrument.** My question asked for one maximum price per respondent, not quantities at several price anchors. I used the observed threshold-count staircase instead of inventing intermediate quantities or choosing a fitted equation just to produce a smoother graph.

## What I learned about supervising AI

The most useful check was to test AI-assisted calculations against counts I could verify directly in the response sheet before trusting the full table. I can explain the method: for each price, count the eligible respondents whose stated maximum willingness to pay is at least that price. I also learned to challenge labels such as “started,” “profit,” and “buyer,” because those words imply measurements my survey did not necessarily collect. ChatGPT helped with calculation, organization, and wording, but I remained responsible for the screening decisions, interpretation, and limitations.

## Sources checked

- Original Google Forms survey export (`responses.csv`)
- `demand/cleaning.md`
- `demand/curve.md`
- `demand/funnel.md`
- `demand/comparison.md`
- Earlier wallet cost-structure analysis
- Ohsnap Wallet 2 Kickstarter campaign rewards documentation

*This is a summary of the documented AI-assisted workflow, not a verbatim transcript of prompts. Review the descriptions against the actual chat history before submitting.*
