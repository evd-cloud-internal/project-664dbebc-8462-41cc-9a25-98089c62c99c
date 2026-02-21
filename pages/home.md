---
name: Home
assetId: 499661bd-9d0f-4f1d-a856-a3c4c9817877
type: page
---

# Sales Overview

{% big_value
  data="demo_daily_orders"
  value="sum(total_sales)"
  fmt="usd1m"
  title="Total Sales"
  sparkline={
    type="area"
    x="date"
    date_grain="month"
  }
/%}

{% line_chart
  data="demo_daily_orders"
  x="date"
  y="sum(total_sales)"
  series="category"
  y_fmt="usd"
  date_grain="month"
  title="Monthly Sales by Category"
  subtitle="Revenue trends across product categories"
/%}

{% bar_chart
  data="demo_daily_orders"
  x="category"
  y="sum(total_sales)"
  y_fmt="usd"
  order="sum(total_sales) desc"
  title="Total Sales by Category"
  subtitle="All-time revenue by product category"
/%}
