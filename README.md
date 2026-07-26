# Funnel Analysis

## Project Overview

This project analyzes user behavior through a signup and checkout funnel. The analysis uses event-level data containing the user ID, funnel step, and timestamp.

The main goal is to find how many unique users reached each stage, calculate conversion rates between stages, identify the biggest drop-off, and understand the time taken between different stages.

## Funnel Stages

The funnel was analyzed in the following order:

1. Visited Site
2. Signup Started
3. Details Filled
4. Email Verified
5. Purchase Completed

## Key Results

| Stage              | Unique Users | Conversion Rate |
| ------------------ | -----------: | --------------: |
| Visited Site       |          200 |               — |
| Signup Started     |          150 |          75.00% |
| Details Filled     |           96 |          64.00% |
| Email Verified     |           52 |          54.17% |
| Purchase Completed |           44 |          84.62% |

## Biggest Drop-off

The biggest drop-off was found between **Signup Started and Details Filled**.

* Users lost: **54**
* Conversion rate: **64.00%**
* Drop-off rate: **36.00%**

This stage appears to be the main point where users leave the funnel.

## Time-to-Convert

The average time between the first two transitions was:

* Visited Site → Signup Started: approximately **15 minutes 50 seconds**
* Signup Started → Details Filled: approximately **17 minutes 5 seconds**

The later transitions could not be calculated because there were no matching users with valid timestamps for both consecutive stages.

## Segment Comparison

Users were divided into two simple segments based on the last digit of their user ID:

* Even ID
* Odd ID

Both segments had the same conversion rates at every funnel stage. Therefore, there was no meaningful difference between the two segments in this dataset.

## Recommendation

The biggest user drop-off happens while moving from Signup Started to Details Filled. I would recommend simplifying the details form by removing unnecessary fields and using autofill and inline validation. This could make the process easier for users and help reduce abandonment at this stage.

## Files

* `funnel_analysis.ipynb` - Jupyter/Google Colab notebook containing the analysis and visualizations.
* `funnel_events_sample.csv` - Dataset used for the funnel analysis.

