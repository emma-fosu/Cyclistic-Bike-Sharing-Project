# Cyclistic Bike-Sharing (Google Data Analytics Project)

_This is the capstone project of the Google Professional Data Analytics Certificate in R programming language._

---

## Table of Contents

- [Problem Statement](#-problem-statement)
- [Solution Approach](#-solution-approach)
- [Results](#-results)
- [Recommendations](#-recommendations)
- [Dataset](#-dataset)
- [Methodology](#️-methodology)
- [Tools & Technologies](#️-tools--technologies)
- [Project Structure](#-project-structure)
- [How to Run or Setup the Project](#-how-to-run-or-setup-the-project)
- [Challenges & Learnings](#-challenges--learnings)
- [Future Improvements](#-future-improvements)
- [Conclusion](#-conclusion)
- [Contact](#-contact)

---

## 📝 Problem Statement

Cyclistic is a bike-share program in Chicago with over 5,000 bicycles, including reclining bikes, hard tricycles, and cargo, which operates with over 600 docking stations.

The marketing director wants to maximze its annual membership as he believes this is key to long-term success.  
Therefore, this anaylsis is to inform them on the riding behaviour of both members and casuals to plan on designing new products, and guide promoting targeted marketing strategies to convert casual riders.  

This analysis explores trip duration, ride frequency, peak usage times, and common routes over the last 12 months throughout the year (2022).

---

## 💡 Solution Approach

Briefly describe how you solved the problem at a high level:

- Your general workflow (analysis, visualization, insights).
- Avoid technical jargon here — think “executive summary.”

---

## 📈 Results

Highlight the main findings:

- Insight 1
- Insight 2
- Insight 3

_Add supporting charts/visuals if possible._

---

## 🔑 Recommendations

Provide actionable takeaways based on your analysis:

- Recommendation 1
- Recommendation 2
- Recommendation 3

---

## 📂 Dataset

The dataset has been made available by Motivate International Inc. under this [license](https://www.divvybikes.com/data-license-agreement).

- **Source:** [Kaggle](https://www.kaggle.com/datasets/emmanfosu/cyclistic-dataset-2024)
- **Description:** The data source is partitioned into twelve zip folders. Each zip folder contains a `.csv` file for a particular month in 2024.  
  The zip folder and `.csv` file are named: `YYYYMM-divvy-tripdata` and `YYYMM-divvy-tripdata.csv` respectively.
- **Schema:**
  - ride_id: The unique ride identifier
  - rideable_type: The bike types.
  - started_at: The start time of the ride.
  - ended_at: The end time of the ride.
  - start_station_name: The start station name of the ride.
  - start_station_id: The unique start station identifier.
  - end_station_name: The end station name of the ride.
  - end_station_id: The unique end station identifier.
  - start_lat: The starting ride latitude.
  - start_lng: The starting ride longitude.
  - end_lat: The ending ride latitude.
  - end_lng: The ending ride longitude.
  - member_casual: member or casual subscriber.

---

## 🛠️ Methodology

1. Data cleaning & preparation
   - Joined all 12 separate `.csv` files into one and stored it in a single variable.
   - Removed any duplicate in fields(`ride_id`) that must be unique.
   - Removed any trip that took less than one minute.
   - Removed trips without ending station name and id, ending station and id, and latitude and longitude.  
     Such trips had a median trip duration of 24.5 hours (Techincal error or stolen bike).
   - Removed trips beyond California geographical boundary (`lat > 41`, `lat < 43`, `lng > -90`, and `lng < 86`).
   - Filled all empty station names and id with `unknown`.
   - Added new fields (`duration`, `month`, `day`, `hour`).
2. Exploratory Data Analysis (EDA)  
   The following questions were verified or answered during this phase:
   - What is the average ride duration for members compared to casual riders?
   - Which days of the week have the highest ridership for members and casual users?
   - How does seasonal variation affect members and casual riders?
   - What are the peak usage hours for members and casual riders?
   - Are casual riders using the service during peak commuting hours, suggesting a pattern similar to member riders?
   - What bike types do members and casual riders prefer the most?
   - What are the most popular starting and ending stations for members and casual riders?
   - What is the average distance traveled per trip for members and casual riders?

---

## ⚙️ Tools & Technologies

- Languages: R
- Libraries: tidyverse, vroom, mapview.
- Platforms: R Studio.

---

## 📁 Project Structure
Cyclistic-bike-sharing-project/
├── .gitignore # Git ignore file
├── datadivvy-tripdata-2024/ # Raw data
├── Cyclistic-Bike-Sharing-Project.Rproj # RStudio Project file
├── index.html # Jupyter notebook export
├── main.nb.html # Reusable Python scripts
├── main.Rmd # Charts and plots
└── README.md # Project documentation

## How to Run or Setup the Project

To set up the project:

1.  Download the zip file or clone the repository.
2.  Download the cyclistic dataset available on [Kaggle](https://www.kaggle.com/datasets/emmanfosu/cyclistic-dataset-2024).
3.  Unzip both the dataset and the downloaded zip repository. If you cloned the repository, you don't need to unzip.
4.  Moved the dataset folder to the root directory of the repository.
5.  Open the `Cyclistic-Bike-Sharing-Project.Rproj` with RStudio and run the markdown.

If you don't have RStudio, you can also view the [markdown](https://emma-fosu.github.io/Cyclistic-Bike-Sharing-Project/).

## Challenges & Learnings

- This is my first R project so learning the language and new libraries syntax was challenging.  
  Afterall, my favourite part was to map the location using `mapview`.

## 🔮 Future Improvements

- Initially, I planned to use Excel to analyze this project, but because of the large dataset it crashed frequently.
  With the introduction of Power Query and Power Pivot in Excel, this large dataset can be analyzed undisruptly. I have planned to master these tools for my next project.

## 🏁 Conclusion

With this analysis on member and casual riding patterns, it is obvious that casual riders are leisure-driven and members are commuter-oriented.  
Starting a promotion like a discount on weekdays for member subscribers will hopefully convert casuals.

## 📬 Contact

👤 Emmanuel Fosu

LinkedIn: [Your LinkedIn]

Email: [emmanuel.fosuduffour@gmail.com](mailto:emmanuel.fosuduffour@gmail.com)

Portfolio/Website: [Your Website]
