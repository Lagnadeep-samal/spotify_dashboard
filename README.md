# 🎵 Spotify Music Analytics Dashboard — Power BI

An interactive Spotify music analytics dashboard built with **Microsoft Power BI** to explore songs, artists, popularity, album types, explicit content, rankings, and time-based trends.

## 📊 Dashboard Preview

![Spotify Power BI Dashboard](assets/spotify-dashboard.png)

## 🎯 Project Objective

The objective of this project is to transform Spotify music data into an interactive dashboard that helps analyze:

- Total and distinct songs
- Distinct artists
- Average song popularity
- Average song duration
- Album-type distribution
- Explicit vs non-explicit content
- Song/ranking trends
- Time-based popularity and song-count patterns

## 🛠️ Tools & Technologies

- **Microsoft Power BI Desktop**
- **DAX**
- **Power Query**
- **Data Visualization**
- **Data Modeling**

## 📁 Project Structure

```text
Spotify-PowerBI-Dashboard/
│
├── Spotify.pbix
├── README.md
├── .gitignore
│
├── assets/
│   └── spotify-dashboard.png
│
└── data/
    └── README.md
```

## 📌 Key KPIs

The dashboard contains measures for:

- Total Records
- Total Days
- Distinct Songs
- Distinct Artists
- Average Popularity
- Maximum Popularity
- Minimum Popularity
- Average Duration
- Explicit Songs
- Non-Explicit Songs
- Explicit Song %
- Album / Single / Compilation distribution
- Ranking-based metrics

## 📈 Main Visualizations

### Song and Artist Explorer
A searchable/list-style visual for exploring songs and their artists with album artwork.

### KPI Cards
High-level metrics provide a quick overview of the dataset.

### Songs by Artist
Used to compare song/popularity-related metrics across artists.

### Songs by Album Type
Shows the distribution of records across album types.

### Explicit vs Non-Explicit
Compares explicit and non-explicit songs.

### Songs by Year
Shows the distribution of songs across available years.

### Average Popularity by Month
Used to examine popularity patterns over time.

### Distinct Songs by Month
Shows how the number of distinct songs varies by month.

## 🧮 Example DAX Measures

```DAX
Total Records =
COUNTROWS('Top-50-world')
```

```DAX
Total Days =
DISTINCTCOUNT('Top-50-world'[date])
```

```DAX
Distinct Songs =
DISTINCTCOUNT('Top-50-world'[song])
```

```DAX
Distinct Artists =
DISTINCTCOUNT('Top-50-world'[artist])
```

```DAX
Average Popularity =
AVERAGE('Top-50-world'[popularity])
```

```DAX
Average Duration Minutes =
DIVIDE(
    AVERAGE('Top-50-world'[duration_ms]),
    60000
)
```

```DAX
Explicit Songs =
CALCULATE(
    COUNTROWS('Top-50-world'),
    'Top-50-world'[is_explicit] = TRUE()
)
```

```DAX
Explicit Song % =
DIVIDE(
    [Explicit Songs],
    [Total Records],
    0
)
```

## 🔄 Data Analysis Workflow

```text
Raw Spotify Data
       ↓
Power BI
       ↓
Data Preparation / Power Query
       ↓
Data Model
       ↓
DAX Measures
       ↓
Interactive Visualizations
       ↓
Dashboard
       ↓
Insights
```

## 🎓 What I Learned

- Importing and preparing data in Power BI
- Identifying categorical, numerical, and date fields
- Creating reusable DAX measures
- Using `COUNTROWS`, `DISTINCTCOUNT`, `AVERAGE`, `MIN`, `MAX`, `CALCULATE`, and `DIVIDE`
- Creating KPI cards
- Building charts and slicers
- Working with image URLs / album artwork
- Designing an interactive dashboard
- Converting raw data into analytical questions and insights

## 🔍 Analytical Insights

The dashboard can be used to investigate:

- Overall dataset size and artist coverage
- General popularity levels
- Explicit vs non-explicit content
- Album-type distribution
- Popularity patterns over time
- High-ranking/high-popularity songs and artists
- Changes in song counts across time

> Do not claim a specific finding in the README unless it is actually supported by the data. For example, instead of saying "Taylor Swift is the most popular artist," verify that result first.

## 🚀 How to Use

1. Install Power BI Desktop.
2. Clone or download this repository.
3. Open `Spotify.pbix`.
4. If Power BI asks for the local data source, update the source path.
5. Refresh the data.
6. Explore the dashboard and its filters.

## ⚠️ Dataset

Before uploading the raw CSV/data file to GitHub, verify that its license allows redistribution.

If redistribution is not allowed, keep the dataset out of the repository and put the original source/download instructions in `data/README.md`.

## 💼 Resume Description

**Spotify Music Analytics Dashboard | Power BI, DAX**

> Developed an interactive Spotify music analytics dashboard using Power BI and DAX to analyze song popularity, artists, album types, explicit content, rankings, and time-based trends. Created reusable measures and interactive visualizations to transform raw music data into meaningful analytical insights.





