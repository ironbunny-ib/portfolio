## Business Overview
#### Bhajans behave differently from typical YouTube content.
The business consists of a devotional genre YouTube channel. The channel name is "Radharaman Bhakti Ras". There are more than 150k subscribers and 1.5M monthly views. Devotional Genre is a low RPM (Revenue per Mille) category of channels. Here the channel depends on consistency, and size of video library where virality is a smaller factor. Other categories try to make each video viral, which is not found to happen in Devotional Genre.

## Data Objectives 
We wanted to find out
1. Which bhajans are repeatedly listened to?
2. Are our bhajans becoming long-term assets?
- And we changed the analysis from per video to per week so as to have a weekly control cadence


### 📊 1. WEEKLY SCORECARD — “Did we grow the library?”
#### KPIs
- Total views (this week)
- % from old videos (published >30 days ago)
- New uploads count
- Avg views per upload

### 📚 2. LIBRARY HEALTH — “Is the catalog working?”
#### Chart
- Total weekly views (stacked):
    - Old videos
    - New videos

### 🌿 3. EVERGREEN LEADERS — “Which bhajans are assets?”
##### 📐 Metric 1 — Weekly Contribution
weekly_views(video, week)

##### 📐 Metric 2 — Evergreen Score (simple + powerful)
Evergreen Score = Average weekly views (after day 30) / Peak weekly views (first 2 weeks)

##### 📐 Metric 3 — Longevity
Number of weeks with > X views

##### 📐 Metric 4 — Library Contribution %
(video weekly views) / (total weekly views)

#### 📐 Metric 5 — Decay Rate
Week-over-week % drop

### Analysis
##### 🌿 Evergreen
- stable weekly views
- low decay
- high longevity
##### 🔥 Spike
- high early views
- fast drop
##### 💤 Dormant
- low but consistent

### Decisions
- Which bhajans should we repeat style-wise? → look at evergreen leaders
- Are we building long-term value? → check % views from old videos
- Are new uploads strong enough? → check first 7-day performance


## Choice of Technology Stack
- I chose the Technology Stack such that it had a resemblance to real world production systems but was still simple enough to be run without much cloud costs. Due to this our entire project is running at no cost under free tier limits.
- I also wanted to view the dashboard on any device, so we chose streamlit cloud. A docker container was created to store our scripts and dbt code, which is set to run 4 times a day through Github Actions. Once data is loaded, we query it through Streamlit using SQL.
- A wider architecture was conceived, though the implementation contained 70% of the system imagined. Today's system can be migrated to a more robust implementation if stakeholders or users increase. 

