---
title: Social Volume AI
author: Ilya
date: 2024-01-26
description: The amount of messages/documents that relate to given assert found by NLP model
---

## Definition

Social Volume is build on top of the [Social Data](/metrics/details/social-data).

The **Social Volume AI** metric has the same idea as the **Social Volume**. But for finding relation of text to the given asset we use NLP (Named Entity Recognition and Named Entity Linking) models. And the same as in **Unique Social Volume** we take into account only unique text documents for each interval, i.e. completely duplicated messages will be excluded from the calculations.

---

## Access

[Restricted Access](/metrics/details/access#restricted-access).

---

## Measuring Unit

Amount of distinct related to the given asset documents extracted by NLP model.

---

## Data Type

[Timeseries Data](/metrics/details/data-type#timeseries-data)

---

## Frequency

[Five-Minute Intervals](/metrics/details/frequency#five-minute-frequency)
[One-Hour Intervals](/metrics/details/frequency#hourly-frequency)

---

## Latency

[Social Data Latency](/metrics/details/latency#social-data-latency)

---

## Available Assets

Available for [these assets](<https://api.santiment.net/graphiql?variables=&query=%7B%0A%20%20getMetric(metric:%20%22social_volume_ai_total%22)%20%7B%0A%20%20%20%20metadata%20%7B%0A%20%20%20%20%20%20availableSlugs%0A%20%20%20%20%7D%0A%20%20%7D%0A%7D%0A>)

> Note: `social_volume_ai_total` metric is available for the same set of assets.

---

## Sanbase

Social Volume AI for an asset can be seen on a a [project's page](https://app.santiment.net/charts).

## SanAPI

Available under the `social_volume_ai_total` name.

### Social Volume AI for an asset

```graphql-explorer
{
  getMetric(metric: "social_volume_ai_total") {
    timeseriesDataJson(
      selector: { slug: "santiment" }
      from: "2020-01-01T00:00:00Z"
      to: "2020-01-07T00:00:00Z"
      interval: "1d"
    )
  }
}
```

## Full list of metrics

The full list of Social Volume metrics is:

<Details>
<Summary>Open Change Metrics List</Summary>

- social_volume_ai_total

</Details>