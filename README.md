# Stance Detection on Twitter: MBG Public Opinion Analysis
This project analyzes public opinion on the Makan Bergizi Gratis (MBG) program using Twitter data.
Instead of only performing sentiment analysis, this project focuses on stance detection: identifying whether a tweet supports, opposes, or remains neutral toward the MBG program.

## Project Objectives
The main objectives of this project are:
1. To transform raw Twitter crawling output into structured and analysis-ready data.
2. To perform text preprocessing and duplicate removal based on content similarity.
3. To classify public opinions into three stance categories: Pro, Kontra, and Netral.
4. To visualize stance distribution for better storytelling and decision support.

## Dataset
The dataset is obtained from Twitter crawling with keyword/hashtag related to MBG.
The raw data initially comes in semi-structured text format and contains: Date, Tweet ID, Text, Language, Retweet, Count, Reply Count, Like Count, Quote Count.
This data is then converted into a structured DataFrame and cleaned before modeling.

## Workflow
1. Data Parsing: Convert raw crawling output text into a structured table format.

2. Text Cleaning: Convert to lowercase, Remove URLs, mentions, hashtags, symbols, Remove stopwords / conjunction words, Normalize whitespace.

3. Duplicate Removal: Remove duplicated tweets based on cleaned text to ensure content uniqueness.

4. Sentiment Analysis: Apply Indonesian RoBERTa Sentiment Classifier to classify: Positive, Negative, Neutral

5. Stance Mapping: Sentiment labels are mapped into stance classes: Positive → Pro, Negative → Kontra, Neutral → Netral

6. Visualization: An interactive bar chart is used to display: Number of tweets per stance, Percentage of each stance.---

## Tools and Technologies

Python

Pandas

Regex

HuggingFace Transformers

Indonesian RoBERTa Sentiment Model

Plotly (for interactive visualization)

## Key Findings

The majority of tweets regarding MBG fall into the Netral category, indicating that public discussions are mostly informative rather than emotionally polarized.
Supportive (Pro) and opposing (Kontra) opinions exist but do not dominate the dataset.

This suggests that the MBG discourse is still in an early phase of opinion formation, leaving room for stronger policy communication and public engagement.

## Output

The final processed file includes:

Tweet ID

Cleaned Text

Stance (Pro / Kontra / Netral)

Confidence Score


Saved as:

tweets_mbg_stance.csv

## Author: Cindy Pramudita

This project was developed as part of a Natural Language Processing practice on political and public policy discourse analysis using social media data.
