# -ChatGPT-Analysis-Video-Presentation
Python analysis of ChatGPT reviews using TextBlob sentiment, rating comparisons, keyword themes, and monthly visualizations in Google Colab. Explores user satisfaction, common praise, and concerns.
# ChatGPT Reviews Analysis

<p align="center">
  <strong>Explore what users appreciate, what concerns they report, and how feedback changes over time.</strong>
</p>

<p align="center">
  <a href="https://colab.research.google.com/drive/1G24HLmDR5zRm0e3wU6t2eCO9W35YoOjV?usp=sharing#scrollTo=OBpcu9mThan6">
    <img src="https://img.shields.io/badge/Open%20in-Google%20Colab-F9AB00?logo=googlecolab&logoColor=white" alt="Open in Google Colab">
  </a>
  <img src="https://img.shields.io/badge/Python-Data%20Analysis-3776AB?logo=python&logoColor=white" alt="Python data analysis">
  <img src="https://img.shields.io/badge/NLP-TextBlob-5A5A5A" alt="TextBlob NLP">
</p>

## Contents

- [Project overview](#project-overview)
- [Questions explored](#questions-explored)
- [Dataset](#dataset)
- [Analysis workflow](#analysis-workflow)
- [Visualizations](#visualizations)
- [Run the notebook](#run-the-notebook)
- [Interpretation notes](#interpretation-notes)
- [Video demo outline](#video-demo-outline)

## Project overview

This Google Colab notebook analyzes ChatGPT customer reviews with Python. It combines written feedback, star ratings, and review dates to summarize satisfaction, estimate text sentiment, identify recurring themes, and explore changes in feedback over time.

The example themes in the project brief, such as learning support, coding help, answer quality, technical issues, and subscription cost, are treated as topics to investigate rather than assumed conclusions.

## Questions explored

- Are review texts mostly positive, neutral, or negative?
- How opinion based does the wording appear?
- Do star ratings and text sentiment tell a similar story?
- Which words and phrases recur in positive and critical reviews?
- How does review volume and sentiment vary by month?

## Dataset

The notebook uses a review CSV with these fields:

| Field | Description |
|---|---|
| `Review Id` | Identifier for a review |
| `Review` | Customer's written feedback |
| `Ratings` | Star rating |
| `Review Date` | Date and time the review was submitted |

The notebook's data-loading cell uses the CSV source already included in the notebook: [chatgpt_reviews.csv](https://statso.io/wp-content/uploads/2024/08/chatgpt_reviews.csv). If you use a local copy instead, upload it to Colab and update the loading cell.

## Analysis workflow

1. **Inspect and prepare data** - review the columns and missing values, standardize column names, convert ratings to numbers, and parse review dates.
2. **Score sentiment** - use TextBlob to calculate polarity and subjectivity for nonempty reviews.
3. **Classify text** - label polarity above `0.1` as positive, below `-0.1` as negative, and values between those cutoffs as neutral.
4. **Compare with ratings** - summarize rating distributions and compare ratings with sentiment categories.
5. **Explore themes** - extract frequent words and phrases from positive and negative reviews; use keyword lists to check themes such as performance, features, user experience, accuracy, and subscription.
6. **Study neutral feedback** - use simple keyword rules to explore questions, feature requests, and positive or negative leaning language.
7. **Track review dates** - chart review volume and sentiment counts by month.

## Visualizations

The notebook creates charts for:

- Star rating distribution
- Sentiment distribution
- Subjectivity score distribution
- Ratings within each sentiment group
- Frequent positive and negative terms or phrases
- Keyword based issue categories
- Neutral review categories
- Monthly review volume and sentiment counts

## Run the notebook

1. Open [ChatGPT_Reviews_Analysis.ipynb in Google Colab](https://colab.research.google.com/drive/1tXhYcgFSHpm8Uaa_JThFAyDmZJK3Dr3y & https://colab.research.google.com/drive/18EaBAgBiX7PDr51yPZBskeCMWN1sp3WU#scrollTo=i1e3ykBfd7bA)
2. Run the notebook cells from top to bottom.
3. Review the tables and charts, then use the findings in the project demo.

## Interpretation notes

TextBlob provides a first-pass estimate of sentiment; it may misread sarcasm, slang, mixed language, and context. The theme categories are based on keywords and can include false matches. Frequent terms are useful clues, but they do not prove why a user gave a particular rating. Read example reviews before making recommendations, and avoid generalizing this sample to all ChatGPT users.

## Video demo outline

1. Introduce the problem and project question.
2. Describe the dataset and cleaning decisions.
3. Explain polarity, subjectivity, and sentiment categories.
4. Walk through the rating, keyword, and date charts.
5. Share the main findings and practical recommendations.
