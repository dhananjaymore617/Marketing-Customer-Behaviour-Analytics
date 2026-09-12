# DAX Measures

The following measures are implemented in the Power BI model. The definitions below are documented exactly as provided from the current report.

## Conversion & Journey Measures

### Conversion_Rate

```DAX
Conversion_Rate = 
VAR Total_Visitors = CALCULATE(COUNT(fact_customer_journey[Action]), fact_customer_journey[Action] = "View")
VAR Total_Purchase = CALCULATE(COUNT(fact_customer_journey[Action]), fact_customer_journey[Action] = "Purchase")
RETURN 
IF(Total_Visitors = 0, 0, DIVIDE(Total_Purchase, Total_Visitors))
```

Calculates purchase actions as a proportion of view actions and returns 0 when there are no visitors.

### Total_Visitors

```DAX
Total_Visitors = CALCULATE(COUNT(fact_customer_journey[Action]), fact_customer_journey[Action] = "View")
```

Counts customer-journey actions where the action is `View`.

### Total_Purchase

```DAX
Total_Purchase = CALCULATE(COUNT(fact_customer_journey[Action]), fact_customer_journey[Action] = "Purchase")
```

Counts customer-journey actions where the action is `Purchase`.

### Number of Customer Journeys

```DAX
Number of Customer Journeys = DISTINCTCOUNT(fact_customer_journey[JourneyID])
```

Counts distinct customer journey records.

## Engagement Measures

### Total_Views

```DAX
Total_Views = SUM(fact_engagement_data[Views])
```

Calculates total views from the engagement fact table.

### Total_Clicks

```DAX
Total_Clicks = SUM(fact_engagement_data[Clicks])
```

Calculates total clicks from the engagement fact table.

### Total_Likes

```DAX
Total_Likes = SUM(fact_engagement_data[Likes])
```

Calculates total likes from the engagement fact table.

### Number of Campaigns

```DAX
Number of Campaigns = DISTINCTCOUNT(fact_engagement_data[CampaignID])
```

Counts distinct campaigns represented in the engagement data.

## Customer Review Measures

### Rating_Average

```DAX
Rating_Average = AVERAGE(fact_customer_reviews_with_sentiment[Rating])
```

Calculates the average rating from the sentiment-enriched customer review table.

### Number of Customer Review

```DAX
Number of Customer Review = DISTINCTCOUNT(fact_customer_reviews[CustomerID])
```

Counts distinct customers represented in the customer review table.

### Number of Customer Review with Sentiment

```DAX
Number of Customer Review with Sentiment = DISTINCTCOUNT(fact_customer_reviews_with_sentiment[CustomerID])
```

Counts distinct customers represented in the sentiment-enriched review table.

## Measure Inventory

| Measure | Purpose |
|---|---|
| `Conversion_Rate` | Purchase actions ÷ view actions |
| `Number of Campaigns` | Distinct campaign count |
| `Number of Customer Review` | Distinct customer count in reviews |
| `Number of Customer Journeys` | Distinct journey count |
| `Number of Customer Review with Sentiment` | Distinct customer count in sentiment-enriched reviews |
| `Rating_Average` | Average review rating |
| `Total_Clicks` | Total engagement clicks |
| `Total_Likes` | Total engagement likes |
| `Total_Purchase` | Purchase-action count |
| `Total_Views` | Total engagement views |
| `Total_Visitors` | View-action count |

## Note

This file documents the DAX measures supplied for the current Power BI report. It does not add measures that were not provided.