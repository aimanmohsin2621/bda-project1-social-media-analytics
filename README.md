# Big Data Analytics Project 1: Social-Media Engagement Analysis

**From 2,000 social-media records to a marketing decision**

Course: DS391 Big Data Analytics
Author: AIMAN (ID:F2023376387)

# Data source and provenance

- Dataset: [`mrudukp/social-media-sentiment-analysis`](https://github.com/mrudukp/social-media-sentiment-analysis) on GitHub
  (`social_media_sentiment_raw.csv`, 2,260 rows, 13 columns, five platforms).
- The original source of the data is not stated, and the repository has no license.
- It is not verified as data from Pakistani clothing brands, and the post texts are short templated sentences,
  so it may be synthetic. It is used here only to demonstrate the analytics workflow.
  **No conclusions are drawn about Pakistan or any real brand.**
- The data file is not re-uploaded here. The notebook downloads it from the source repository.

## What the notebook does

1. Loads the CSV and inspects it before making any assumptions (shape, types, missing values, duplicates).
2. Defines the data object (one row = one post) and writes a data dictionary.
3. Cleans the data: standardises platform/country spellings, converts follower counts, sets invalid negative likes
   to missing, and removes 60 duplicate posts (2,260 to 2,200 rows).
4. Runs exploratory analysis: summary statistics and charts (bar chart, box plot, histogram, scatter plot, stacked bar).
5. Runs a scaling experiment (about 2,000 to 2 million repeated rows) measuring file size, load/analysis time and memory.
   The repeated rows are an experiment, not new evidence.
6. Previews classification, clustering and regression with a train/test split and no target leakage.

## Findings (for this dataset only)

- TikTok posts have the highest median engagement per post and LinkedIn the lowest.
- Positive-tone posts have higher median engagement than neutral or negative ones.
- **Recommendation:** a brand could test shifting some content effort toward TikTok and positive-tone posts and compare results
  using one consistent metric.
- **Limitations:** no reach or impressions data, so this is engagement per post and not engagement rate or ROI.
  The data is unverified and possibly synthetic, and the differences are descriptive, not causal.

## How to run

1. Open `Project1_Social_Media_Analytics.ipynb` in [Google Colab](https://colab.research.google.com).
2. Click **Runtime > Run all**. If the automatic download fails, upload the CSV from the source repository when asked.

## Files

| File | Description |

| `Project1_Social_Media_Analytics.ipynb` | Full analysis notebook with outputs |

## Next step

Add genuine or clearly labelled sample paid-campaign data (spend, impressions, clicks, conversions) before moving to
Meta Ads and Google Ads analysis. Organic engagement data alone cannot calculate ROAS.
