---
title: "GCP budgets do NOT prevent creditcard overspending"
date: 2019-07-12
categories: 
  - "vizz"
tags: 
  - "billing"
  - "budgets"
  - "caps"
  - "gcp"
---

GCP budgets do NOT prevent overspending

- https://cloud.google.com/billing/docs/how-to/budgets

_Setting a budget does not cap resource or API consumption. [Learn more.](https://cloud.google.com/billing/docs/how-to/budgets?_ga=2.260398349.-1014214080.1562958871)_

You need to create a cloud function to shut down your GCP resources or create caps on your API usage

- https://cloud.google.com/billing/docs/how-to/notify#cap\_disable\_billing\_to\_stop\_usage
- https://cloud.google.com/apis/docs/capping-api-usage
