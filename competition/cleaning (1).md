# Survey Cleaning — Wallet A vs. Wallet B

## Source, screening, and retained sample

The second wallet-comparison survey was distributed through one Reddit post. The exported Google Forms file contains **2 submitted responses**. Both respondents answered **Yes** to all three screeners: age 18 or older, personally chooses a wallet/card holder, and carries physical cards at least occasionally. **2 passed screening; 2 responses were retained; 0 were excluded.** The file does not identify people who opened or started the survey without submitting it.

All 2 respondents provided numeric, nonnegative whole-dollar maximum willingness-to-pay (WTP) answers and numeric, nonnegative integer quantities for all eight scenario questions. There are **0 missing WTP values** and **0 missing quantity answers**. The analysis uses anonymized respondent IDs R001 and R002; original survey answers were not altered.

## Four pricing scenarios

Each respondent answered quantities for both wallets under these four conditions:

| Condition | Price of A | Price of B |
| --- | --- | --- |
| 1 | $0 | $0 |
| 2 | Respondent's maximum WTP for A | $0 |
| 3 | $0 | Respondent's maximum WTP for B |
| 4 | Respondent's maximum WTP for A | Respondent's maximum WTP for B |

| Respondent | WTP A | WTP B | A quantities (C1,C2,C3,C4) | B quantities (C1,C2,C3,C4) |
| --- | ---: | ---: | --- | --- |
| R001 | $50 | $40 | 1, 1, 1, 0 | 1, 0, 1, 0 |
| R002 | $0 | $0 | 0, 0, 0, 0 | 0, 0, 0, 0 |

## Monotonicity rules and observed violations

A violation means a strict change in the wrong direction. For each rule, a respondent is counted as violating it if **either** relevant comparison violates the rule; the share is the number of violating respondents divided by all **2 retained respondents**.

| Rule | Required comparisons | Violating IDs | Share |
| --- | --- | --- | ---: |
| A own-price: raising A's price must not raise A quantity | A(C2) <= A(C1); A(C4) <= A(C3) | None | 0/2 = **0%** |
| B own-price: raising B's price must not raise B quantity | B(C3) <= B(C1); B(C4) <= B(C2) | None | 0/2 = **0%** |
| A cross-price: raising B's price must not lower A quantity | A(C3) >= A(C1); A(C4) >= A(C2) | R001 | 1/2 = **50%** |
| B cross-price: raising A's price must not lower B quantity | B(C2) >= B(C1); B(C4) >= B(C3) | R001 | 1/2 = **50%** |

For R001, A quantity decreases from **1 in C2 to 0 in C4** when B's price rises from $0 to $40 while A remains $50. Also, B quantity decreases from **1 in C1 to 0 in C2** when A's price rises from $0 to $50 while B remains free. These are cross-price violations under the assumption that the two wallets are substitutes. The own-price comparisons do not violate nonincreasing demand.

For R002, both maximum WTP values are $0, so all four conditions have the **same prices ($0, $0)**. Their quantities are consistently zero. R002 is included in the reported 2-person denominator, but their observations provide **no actual own-price or cross-price variation**. For transparency, restricting the denominator to respondents with a strictly positive relevant price change would yield **0/1 = 0% own-price violations** for each wallet and **1/1 = 100% cross-price violations** for each wallet. These conditional figures are supplementary, not replacements for the all-response shares above.

## Cleaning decisions and limitations

- **Retained both eligible respondents**, including R001's counterintuitive cross-price answers and R002's zero WTP. No quantities or WTP values were changed to enforce monotonicity.
- **Excluded no submitted records.** There are no missing quantity answers requiring imputation.
- Preserved the original qualitative comments, including unsolicited promotional text in R001's switching response, rather than treating that text as quantitative evidence.
- Used de-identified IDs instead of submission timestamps in the prepared `responses.csv`.
- The sample is extremely small (**n = 2**); only one respondent has positive WTP, and that respondent violates both cross-price rules. Any demand-system fit or inferred competitive advantage must be labeled exploratory and may be unidentified or unstable.

These checks describe the submitted data; they do not establish population-level demand or prove that either wallet is a substitute for the other.
