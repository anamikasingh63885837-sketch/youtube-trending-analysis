# YouTube Trending Videos Analysis (India)

Exploratory analysis of what characterises videos on YouTube's trending list in India.

## Data
Trending YouTube Video Statistics — Kaggle  
https://www.kaggle.com/datasets/datasnaek/youtube-new  
Files used: `INvideos.csv`, `IN_category_id.json` (Nov 2017 – Jun 2018)  
37,352 rows → 16,307 unique videos after removing repeat trending appearances.

## Questions
1. Which categories appear on trending most often?
2. Which categories have the most engaged audiences?
3. Does publish timing relate to trending?
4. Do title features relate to views?
5. How quickly do videos reach trending?

## Key findings
- Entertainment leads by volume (7,558 videos) but has one of the lowest median engagement rates (0.66%).
- Science & Technology (8.90%) and Education (6.35%) have the highest engagement despite far lower trending volume.
- Median time from publish to trending is 1 day.
- Title length, tag count and capitalisation showed near-zero correlation with views (-0.08 to 0.09).

## Data quality note
An initial load returned only 4,833 rows. Since the source file is 58 MB, this implied ~12 KB per row, which is implausible. Investigation showed an incomplete file upload, and that `on_bad_lines='skip'` was discarding rows without raising an error. Loading from Google Drive recovered all 37,352 rows.

## Limitations
The dataset contains only videos that reached trending. Videos that never trended are absent, so no factor here can be shown to *cause* trending.

## Tools
Python, pandas, matplotlib, seaborn
