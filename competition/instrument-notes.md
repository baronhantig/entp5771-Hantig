# Competition instrument — self-test and design notes

ENTP 5771 | Wallet A: Bare Bones Ohsnap Wallet 2 | Wallet B: Secrid Cardprotector

## Survey setup

I created the survey in Google Forms. It follows the seven required content sections: screening, context, product descriptions, appeal, valuation, switching, and respondent characteristics. Google Forms displays nine pages because the three eligibility questions need separate pages for answer-based routing. Wallet A and Wallet B are identified by letters rather than brand names in the respondent-facing descriptions.

## Self-test record (November 4, 2026)

- **Underage:** Tested answering “No” to being at least 18. The form directed the respondent to submit without showing the substantive survey.
- **Wallet choice:** Tested answering “No” to personally choosing a wallet after passing the age screen. The form directed the respondent to submit.
- **Physical cards:** Tested answering “No” to carrying physical cards after passing the first two screens. The form directed the respondent to submit.
- **Qualified path:** Walked through the full nine-page respondent path. The survey displayed the two appeal ratings, two WTP entries, eight quantity scenarios, switching response, and final characteristics questions. The Submit button was active using the public respondent link in a private browser window.
- **Zero WTP:** Entered $0 for both wallets; the form accepted both entries and allowed continuation. In this case, some nominal pricing conditions coincide, but all eight questions remain in the instrument.
- **Maximum WTP:** Entered $1,000 for both wallets; the form accepted both entries and allowed continuation.
- **Outside access:** Opened the public respondent link in a private browser window. The published form was set to accept responses from anyone with the link.

These were navigation and validation checks. No completed test submission was reported, so successful storage of a submitted record was **not** verified in these tests.

## Design checks and limitations

**Neutrality and recognition.** Both wallets are presented without brand names or prices before appeal ratings. The same image treatment should apply to both; the working choice is no images. Secrid could be recognizable from its mechanism or construction even without its name, potentially affecting appeal or WTP. The two descriptions are not perfectly symmetrical: Wallet B specifies aluminum and up to six cards, while Wallet A is less specific. I need to verify the product specifications and balance the detail without inventing features before launch.

**Appeal before price.** Both 1–10 appeal questions and optional likes/dislikes prompts appear before any WTP or price scenarios. Both appeal scales have the same endpoints.

**Own-price and cross-price variation.** Each respondent gives a WTP for A and B. Each wallet then has four quantity questions: (1) A free/B free, (2) A at own WTP/B free, (3) A free/B at own WTP, and (4) A at own WTP/B at own WTP. The conditions are repeated for B in the same order. These are hypothetical quantities per 12 months; zero is allowed.

**Google Forms price-reference limitation.** Google Forms does not automatically insert each person's earlier numerical WTP into later question text. The form tells respondents to remember their “Wallet A maximum price” and “Wallet B maximum price,” and each quantity scenario refers to those amounts. This preserves the intended four conditions but adds memory/interpretation risk. The form should be tested with a fresh reader for clarity, and this implementation should be disclosed to Professor Hatch if he expects the actual dollar amounts to be displayed dynamically.

**Numerical validation.** The $0 and $1,000 endpoints were tested successfully. The instructions request whole-dollar WTP, but whether decimals are rejected was **not** tested. Invalid letters and negative WTP entries were also **not** verified. Test these and align the instructions and validation before recruiting.

**Fresh sample.** Respondents from the first survey must not be recruited again. The form itself does not independently establish whether someone completed the first survey; recruitment procedures must address this separately.

## Final items before launch

- Verify Wallet A and Wallet B factual descriptions and remove any internal image reminder if still present.
- Check the exact live form against `competition/instrument.md`; the Markdown file must reflect the instrument actually fielded.
- Test decimal, negative, and nonnumeric WTP entries; test quantity-entry validation.
- Confirm a completed test submission appears in the Responses tab, then delete that test response before recruitment.
- Set up channel attribution and start tracking real approached, started, passed-screen, and finished counts, recording unavailable metrics as unavailable rather than estimating them.

The survey was accessible and accepting responses during testing, but this does not establish that actual recruitment or data collection had begun.
