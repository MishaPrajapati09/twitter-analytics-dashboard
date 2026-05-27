# twitter-analytics-dashboard
Interactive Power BI dashboard for Twitter analytics using DAX formulas, engagement analysis, and dynamic visualizations.
The dataset was collected online in CSV format, imported into Power BI, transformed using Power Query, and used to create interactive analytical dashboards.

## Features
- Top 10 Tweets by Engagement
- Engagement Rate Comparison
- Media Interaction Analysis
- Monthly Engagement Rate Trend
- Tweet Interaction Breakdown
- Dynamic DAX Filters
- Interactive Month Slicer

## Tools & Technologies
- Power BI
- DAX
- Power Query
- CSV Dataset

## Data Preparation
- Imported Twitter dataset from an online CSV source
- Cleaned and transformed data using Power Query
- Created calculated columns and measures using DAX
- Built interactive visualizations and KPI cards


## Important DAX Formulas

### Tweet Time Filter
```DAX
TweetTimeFilter =
IF(SocialMedia[Hour] >= 9 && SocialMedia[Hour] <= 17,1,0)
```

### Remove Tweets Containing D
```DAX
NoDTweet =
IF(CONTAINSSTRING(SocialMedia[Tweet],"D"),0,1)
```

### Even Impression Filter
```DAX
EvenImpression =
IF(MOD(SocialMedia[impressions],2)=0,1,0)
```

### Word Count
```DAX
WordCount =
LEN(SocialMedia[Tweet])
-
LEN(SUBSTITUTE(SocialMedia[Tweet]," ",""))
+1
```


## Files Included
- Power BI Dashboard (.pbix)
- Dataset (.csv/.xlsx)
- Dashboard Screenshot
- README Documentation
