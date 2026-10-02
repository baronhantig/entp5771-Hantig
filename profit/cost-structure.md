# Cost Structure

For this analysis, I am modeling the decision to continue producing and selling the Bare Bones Wallet 2 beyond the Kickstarter campaign. One unit is one Bare Bones Wallet 2, and I am using its $60 MSRP as the current benchmark price. My decision period is 12 months, which matches the period used in my demand survey.

Ohsnap does not publish its supplier contracts or actual manufacturing costs, so some of the estimates below use comparable products and public pricing rather than Ohsnap's internal costs. I use ranges because the goal is to identify which costs could actually change the decision rather than pretend that I know exact costs that are not public.

## Part 1: Variable Cost

I started by walking through what would happen when one additional customer orders a $60 Bare Bones Wallet 2.

The order has to be processed, a wallet has to be manufactured and available for the order, the wallet has to be packaged and shipped to the customer, and there is some chance that the customer will return it or require a warranty replacement. Each of those events can create a cost because of that additional sale.

| Trigger | Low | High | Source / How I Estimated It |
| :-- | --: | --: | :-- |
| One wallet manufactured | $6.05 | $10.29 | Ohsnap does not publish its manufacturing cost. I used comparable aluminum wallets as benchmarks. Canterberry Gifts lists an aluminum RFID wallet at $6.05 each at 500 units and a slim aluminum wallet at $10.29 each at 200 units. These are comparison products, not Ohsnap's actual cost. |
| One wallet packaged for shipment | $0.16 | $2.86 | A small padded mailer can cost about $0.16 each in a 500-unit case, while a small cardboard mailer box is listed at $2.86 each in quantities up to 500. The actual cost depends on the packaging Ohsnap chooses. |
| One U.S. order shipped | $6.93 | $8.40 | USPS Ground Advantage commercial pricing for packages up to 15.999 oz currently ranges from $6.93 to $8.40 depending on shipping zone. The Kickstarter reward ships only within the United States. |
| One $60 online payment processed | $2.04 | $2.04 | Shopify Basic lists an online card rate of 2.9% + $0.30. At a $60 sale, the processing cost would be $2.04. This is a benchmark because Ohsnap's actual Shopify plan and negotiated rates are not public. |
| Expected return or warranty replacement | $0.25 | $1.00 | Ohsnap allows returns within 30 days, with the customer paying return shipping. Its current warranty policy also provides qualifying replacements and covers shipment of the replacement. The actual return/defect rate for Wallet 2 is not public, so I use a small expected-cost range rather than claiming a known rate. |
| **Estimated variable cost per wallet** | **$15.43** | **$24.59** | Sum of the estimates above. |

The manufacturing range is a decision as well as an estimate. Ohsnap can choose its supplier, order quantity, materials, manufacturing process, quality target, and amount of customization. Comparable pop-up wallet manufacturers show that quantity matters. One OEM manufacturer lists a minimum order of 300 units for standard mechanisms and says a completely new mechanism can require 500–1,000 units. Another aluminum pop-up wallet manufacturer lists a 300-unit MOQ for a standard configuration and 3,000 units for custom tooling.

Packaging is also a choice. A protective mailer is much cheaper than a custom presentation box. The company has to decide whether premium packaging adds enough customer value to justify the additional cost.

Shipping is partly a choice because the company can select carriers and service levels, although destination and package weight also affect the price. Ohsnap currently offers several U.S. shipping speeds, and its free economy shipping threshold is $79. A $60 Bare Bones wallet by itself is below that threshold.

Payment processing is triggered directly by a sale, but the rate depends on the commerce/payment platform. I used Shopify Basic as a public benchmark rather than assuming Ohsnap's private rate.

Returns and warranty replacements are also triggered by sales, but they are uncertain. Ohsnap's current return policy allows returns within 30 days, with customers paying return shipping. Its current warranty policy states that qualifying products can be replaced within one year and that Ohsnap pays the shipping cost for the replacement. Wallet 2's actual future return and defect rates are unknown.

## Which Ranges Matter?

### Clearly low enough to work at plausible prices

**Payment processing:** At approximately $2.04 on a $60 transaction, this cost is unlikely to determine whether the product can work. Even if the actual processing rate differs somewhat, the difference would be small relative to the $60 selling price.

### Clearly too high

At this point, I do not have a variable-cost line that is clearly too high by itself. Even the high-end total variable-cost estimate remains below the $60 benchmark price. That does not prove the product will be profitable because fixed commitments and actual demand still matter.

### Decisive ranges that deserve more research

**Manufacturing cost:** This is the most important unknown. Ohsnap's actual supplier cost is not public, and Wallet 2 has a custom fanning mechanism and interchangeable card core that may make it more expensive than the comparison wallets. A supplier quote would improve this estimate more than additional research on payment-processing fees.

**Packaging choice:** The range from a simple padded mailer to a more protective box is large enough to matter when multiplied across a production run. Ohsnap can also control this cost directly through its packaging decision.

**Returns and warranty replacements:** The expected cost per sale is not large in my current range, but the estimate is based on an assumed low failure/return rate because Wallet 2 has not yet produced public post-delivery return data. If the mechanism has a higher failure rate than expected, this cost could increase.

Shipping matters to total variable cost, but its current published range is relatively narrow. I would therefore spend additional research effort on manufacturing and product reliability before trying to make the shipping estimate more precise.

## Variable-Cost Floor

My estimated variable cost is approximately **$15.43–$24.59 per wallet**. This means the variable cost sets a floor under any viable price. Selling below approximately **$24.59** would be especially risky under the high-cost case because each additional sale could fail to cover the costs triggered by that sale. At the current $60 benchmark price, the estimated contribution per wallet before fixed commitments is approximately **$35.41–$44.57**.

## Part 2: Fixed Commitments

The fixed-cost question is different from the variable-cost question. For this project, I define a fixed commitment as something I would have to commit to before knowing how many customers will actually buy during the next 12 months.

The biggest commitment I can identify from public information is the initial production run. Comparable manufacturers of aluminum pop-up wallets commonly require minimum production quantities. One manufacturer lists a 300-unit MOQ for a standard pop-up wallet, while another reports 300 units for a standard mechanism and 500–1,000 units when a new mechanism is required.

Ohsnap's actual supplier and MOQ for Wallet 2 are not public, so I cannot claim that Ohsnap is required to order exactly 300 units. I use 300 units as a low-end planning scenario based on comparable suppliers.

| Commitment | Low | High | When I Am Committed | Reversible? |
| :-- | --: | --: | :-- | :-- |
| Initial 300-unit production run | $1,815 | $3,087 | When the production order is placed with the manufacturer, before knowing how many post-Kickstarter retail customers will buy | No. Once production begins, the company is committed to the inventory even if it does not sell. |
| New custom tooling specifically required for post-Kickstarter production | $0 | Unknown | Only if the manufacturer requires new tooling before the next production run | No once tooling work begins, but public information does not establish that a new tooling commitment is necessary. |
| Existing Ohsnap website/e-commerce platform | $0 incremental | $0 incremental | Already operating before the Wallet 2 post-Kickstarter decision | Not treated as a new commitment for this decision |

The initial production commitment is **one-off for the first post-Kickstarter production run**, although another production commitment would occur if inventory had to be reordered later in the 12-month period.

I do not count Ohsnap's existing website, existing employees, or previously completed product-development work as new fixed commitments unless continuing Wallet 2 actually requires additional spending. Those resources already exist and are not created by one additional post-Kickstarter Wallet 2 sale.

I also do not assume a new tooling cost. Wallet 2 is already designed and the Kickstarter campaign has already committed to fulfilling wallets for backers. Any tooling that has already been purchased for Kickstarter production would be a sunk cost for the later retail decision. Without evidence that another tooling commitment is required, assigning an invented tooling number would make the model less accurate.

### Avoiding Double Counting

The minimum production run creates an important modeling issue. Manufacturing is economically a per-unit cost, but ordering 300 wallets means the company may have to commit to paying for all 300 before it knows how many post-Kickstarter customers will buy.

For the variable-cost analysis above, I include manufacturing because each wallet ultimately has to be produced and the manufacturing cost helps determine the minimum viable long-run price.

For a break-even calculation that treats the initial 300-wallet purchase as the fixed commitment, I would not also subtract that same manufacturing cost again from every one of those first 300 sales. Doing both would count the same manufacturing expense twice. In the scale analysis, I therefore state explicitly which treatment I use when calculating required sales.

## Sources

- Ohsnap Wallet 2 Kickstarter campaign — Bare Bones reward: $60 MSRP, $45 Kickstarter price, U.S.-only shipping, estimated February 2027 delivery. https://www.kickstarter.com/projects/ohsnapofficial/ohsnap-wallet-2-couldnt-carry-less/rewards
- Canterberry Gifts — RFID Blocking Aluminum Alloy Wallet: $6.05 each at 500 units. https://www.canterberrygifts.com/rfid-blocking-aluminum-alloy-wallet/
- Canterberry Gifts — Aluminum Slim Metal Wallet with Money Clip: $10.29 each at 200 units. https://www.canterberrygifts.com/aluminum-slim-metal-wallet-with-money-clip/
- Packaging Supply Depot — #000 Premium Poly Bubble Mailer: approximately $0.16 each when purchased by the 500-unit case. https://www.packagingsupplydepot.com/polybubblemailer-000-4x7.25.aspx
- ODBOX — Small Mailer Box: $2.86 each for quantities of 25–500. https://odbox.com/product/small-product-white/
- USPS Notice 123 — current commercial USPS Ground Advantage pricing. https://pe.usps.com/text/dmm300/Notice123.htm
- Shopify — Basic online card-processing benchmark. https://www.shopify.com/pricing
- Ohsnap — Shipping and Returns policy. https://support.ohsnap.com/hc/en-us/articles/32376653520404-Shipping-and-Returns
- Ohsnap — Product Warranty. https://ohsnap.com/pages/2025-ohsnap-warranty
- TOPWALLET — Aluminum Automatic Pop-Up RFID Wallet: comparable MOQ information. https://topedcwallet.com/products/aluminum-pop-up-rfid-wallet/
- GSTAR — Pop-Up Wallet OEM Manufacturing: comparable MOQ information. https://www.gstartec.com/pop-up-wallet-oem-manufacturer-mechanism-design-production.html
