# E-Commerce Funnel Analysis – Methodology and Growth Insights

## Dataset
Kaggle: **Ecommerce Events History in Cosmetics Shop**
- `2020-Jan.csv`
- `2020-Feb.csv`

The two files are concatenated into one event-level DataFrame.

## Methodology
1. Load both monthly CSV files with pandas and parse `event_time`.
2. Inspect `event_type` distribution for view, cart, and purchase.
3. Build a user-level funnel using unique users:
   - View: viewed at least one product.
   - Cart: added at least one product to cart.
   - Purchase: completed at least one purchase.
4. Calculate:
   - View→Cart = cart users / view users
   - Cart→Purchase = purchase users / cart users
   - View→Purchase = purchase users / view users
5. Select the top 8 categories by view-user count and calculate their funnel metrics.
6. Calculate January and February funnel metrics independently and quantify the change in percentage points.
7. Rank the top 10 brands by purchase-event count and calculate their view-to-purchase rate.
8. Detect purchase-price outliers using the IQR rule.
9. Bonus: calculate time from first view to first purchase and identify high-view/low-conversion products.

## Visualizations
- Funnel bar chart
- Category conversion bar chart
- January vs February conversion comparison
- Top 10 brands horizontal bar chart

## Growth interpretation
The final five insights are generated from the calculated data. The supplied task notes contain benchmark figures such as 10.2% view→cart, 71.4% cart→purchase, 7.3% overall conversion, +0.8pp February improvement, and 12.1% for accessories. These should be treated as checks; the notebook calculates the actual values directly from the CSV files and should report those values if they differ.
