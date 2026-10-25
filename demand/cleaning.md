# Milestone 1: Demand — Data Cleaning

## Source and initial audit

I reviewed the original Google Forms export, `Modular Wallet Demand Instrument (Responses)`, before calculating demand. The export contains 42 response rows (Excel rows 2–43). I counted blank cells separately for every column, without replacing missing values with zeros.

| Survey column | Blank cells |
| --- | ---: |
| Timestamp | 0 |
| Q1. Age 18 or older | 0 |
| Q2. Personally chooses wallet/card holder | 1 |
| Q3. Carries physical cards at least occasionally | 2 |
| Q4. Product appeal | 3 |
| Q5. What respondent likes | 3 |
| Q6. Dislikes or concerns | 3 |
| Q7. Suggested changes | 3 |
| Q8. Maximum willingness to pay | 3 |
| Q9. Current wallet type | 3 |
| Q10. Number of physical cards | 3 |
| Q11. Price paid for current wallet | 3 |
| Q12. Age range | 3 |
| Q13. Prior product familiarity | 4 |

## Eligibility and exclusions

The three screening requirements were: (1) age 18 or older, (2) personally chooses their wallet or card holder, and (3) carries physical cards at least occasionally. I excluded a response from the demand analysis if it failed a screener or did not complete the screeners and the willingness-to-pay question.

| Original Excel row | Screening / response issue | Treatment |
| --- | --- | --- |
| 2 | Answered Q1 "Yes" but left Q2, Q3, and Q8 blank; remaining substantive questions also blank | Exclude: incomplete screening and no price answer |
| 4 | Answered Q3 "No" and left Q8 blank; remaining substantive questions also blank | Exclude: does not meet card-carrying screener and no price answer |
| 5 | Answered Q2 "No" and left Q3 and Q8 blank; remaining substantive questions also blank | Exclude: does not meet wallet-choice screener and no price answer |

The original export has 42 response rows. After excluding these three rows, **39 eligible respondents** remain, all with recorded numeric willingness-to-pay answers. I retained the original raw responses unchanged; exclusions apply only to the analytical sample.

## Missing answers versus actual zeros

Q8 (maximum willingness to pay) contains **three blanks**, all in excluded rows 2, 4, and 5. These blanks are missing answers, **not $0 bids**, and were not converted to zero. Among the 39 retained respondents, **eight explicitly entered $0** for willingness to pay. I kept all eight as valid evidence that those respondents would pay nothing for the described wallet.

One retained respondent left Q13 (prior product familiarity) blank. This does not affect eligibility or the demand calculation because the respondent completed the screening questions and supplied a valid Q8 price. I will treat that Q13 value as missing in any analysis of product familiarity, rather than filling it in.

## Cleaned sample and analysis rules

- Raw response rows: **42**
- Excluded responses: **3** (original Excel rows 2, 4, and 5)
- Retained eligible responses: **39**
- Valid numeric Q8 prices among retained responses: **39**
- Actual $0 Q8 responses retained: **8**
- Blank Q8 cells in the retained sample: **0**

For the demand curve, I will use only the 39 eligible numeric Q8 responses. I will not substitute zero for a blank, and I will not remove genuine $0 answers. I will keep the raw export as the source of record and make calculations from the documented cleaned sample.

## Limitations

This cleaning establishes which survey responses are usable for the price-demand analysis; it does not establish that the sample represents all potential wallet buyers. Recruiting-channel coverage and any response biases should be discussed separately in the funnel and demand-curve interpretation.
