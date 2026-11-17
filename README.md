# BiteRush Colombo: Are We Growing the Right Way?

An interactive business intelligence dashboard for **BiteRush Colombo**, a fictional food delivery company created for teaching. It answers the five questions in the CEO's memo using four years of order data (2022 to 2025).

**Live dashboard:** https://YOUR-USERNAME.github.io/biterush-dashboard/

## The business question

The CEO asked: *growth is great, but are we growing the right way?* The dashboard gives a clear answer to each of his five board questions and ends with three recommendations for 2026.

## Dashboard pages

| Page | Question it answers |
|---|---|
| Overview | How have orders, earnings, late deliveries, cancellations and ratings changed? (year filter) |
| Free Delivery | Was the 2024 Free Delivery Summer a success? |
| Rain | How much does rain cost us? |
| Busy hours | When are we busiest, and when are we late? |
| Cancellations | Why are orders cancelled, and when did it get out of hand? |
| Who earns | Which restaurants, cuisines and zones make us money? Are we hitting targets? |
| Actions | Three recommendations for 2026 and the data problems that were fixed |

## Key findings

- **Free Delivery Summer (Jul to Sep 2024):** orders rose about 62%, but earnings per order fell about 69%, late deliveries rose from under 50% to over 70%, and ratings dropped. Marketing and Finance are both right.
- **Rain:** on heavy-rain days we get about 18% more orders, but deliveries are about 14 minutes slower, about 89% are late (24% on dry days), cancellations are 12.7% (5.7% on dry days) and the rating falls from 4.24 to 3.52.
- **Hidden story, July 2022:** 27% of orders were cancelled (normal is about 6%). 104 of the 119 cancellations were "No rider available" in a very wet month.
- **Targets:** orders reached 96% of target in 2022 and 98% in 2023, then 116% in 2024 and 106% in 2025.

## Recommendations

1. Do not run free delivery for everyone again. Use small, targeted offers.
2. Schedule more riders at the busiest hours and on rainy days, with a rain bonus.
3. Build a rider reserve before the wet months.

## How earnings are calculated

Earnings per delivered order = restaurant commission on food value + delivery fee − rider payout − discount.

## Data cleaning

- Removed 60 duplicate order IDs (45,341 rows became 45,281 orders).
- Fixed mixed date formats and merged spelling variants in status, payment method and cuisine.
- Treated impossible values as errors: delivery times of −58 and 999 minutes, and order values such as 1 and 810,900 LKR.
- Replaced −999 rainfall placeholders with the median.
- Data Dictionary mistakes found: weather conditions are Dry, Light Rain and Heavy Rain (not Sunny, Rainy, Stormy); commission is stored as 0.18 (not 18); ratings go from 1 to 5 (not 1 to 10); there is no Refunded status.

## Built with

- HTML, CSS and JavaScript
- [Chart.js](https://www.chartjs.org/) for the charts
- Python (pandas) for cleaning and summarising the data

## Run it locally

Download `index.html` and open it in any modern web browser. The dashboard needs an internet connection to load Chart.js and the font.

## Data

Source: BiteRush Colombo data pack (orders, restaurants, customers, riders, daily weather and monthly targets). The company and data are fictional and made for teaching.
