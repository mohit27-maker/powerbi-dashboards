# Spotify Power BI Dashboard

## 📌 Project Overview

This Power BI dashboard provides an interactive and visual analysis of Spotify music data. It focuses on **song popularity**, **explicit content trends**, **artist performance**, and **time-based insights** (year and month). The dashboard is designed to help users quickly understand music trends and listener preferences using clean KPIs and intuitive visuals.

This project is ideal for:

* Data Analyst portfolios
* Power BI practice projects
* Music & streaming data analysis use cases

---

## 📊 Dataset Description

The dataset contains Spotify song-level information with the following key attributes:

* **Song Name**
* **Artist Name**
* **Release Date / Year**
* **Popularity Score**
* **Explicit Flag (Yes/No)**
* **Album Type** (Single, Album, Compilation)
* **Song Duration**

> Dataset Scope: *Top Spotify tracks across multiple years*

---

## 🎯 Key Objectives

* Analyze overall song popularity
* Compare explicit vs non-explicit songs
* Track popularity trends over time
* Identify top-performing artists
* Understand album type performance

---

## 📌 Dashboard KPIs

The top-level KPIs give a quick snapshot of the dataset:

| KPI                       | Description                                 |
| ------------------------- | ------------------------------------------- |
| **Explicit Songs Ratio**  | Proportion of explicit songs in the dataset |
| **Artist Count**          | Total number of unique artists              |
| **Average Song Duration** | Mean duration of songs (minutes)            |
| **Average Popularity**    | Overall average popularity score            |

---

## 📈 Visuals & Insights

### 1️⃣ Song & Artist List (Left Panel)

* Displays song names along with artist names
* Includes filters for easy selection
* Helps drill down into specific songs or artists

**Insight Example:**

> Identify songs driving high popularity or analyze artist-wise contributions.

---

### 2️⃣ Explicit vs Non-Explicit Songs

**Visuals Used:** Donut Charts

* Explicit vs Non-Explicit song distribution
* Explicit songs by album type

**Insights:**

* Non-explicit songs dominate the dataset
* Singles have a higher share of explicit content compared to albums

---

### 3️⃣ Songs by Year

**Visual Used:** Donut Chart

* Compares song counts across release years

**Insights:**

* Recent years show a higher number of popular releases
* Indicates increasing music production and streaming consumption

---

### 4️⃣ Average Popularity by Album Type

**Visual Used:** Donut Chart

* Album vs Single vs Compilation popularity

**Insights:**

* Singles tend to have the highest average popularity
* Compilations perform moderately

---

### 5️⃣ Average Popularity by Month

**Visual Used:** Line Chart

* Monthly popularity trend across the year
* Toggle between **Month** and **Quarter** view

**Insights:**

* Popularity peaks in early and late months
* Slight dip during mid-year period

---

### 6️⃣ Explicit Songs by Month

**Visual Used:** Column Chart

* Monthly distribution of explicit songs

**Insights:**

* Explicit content peaks during certain months
* Seasonal trend observed in explicit releases

---

### 7️⃣ Average Popularity by Artist

**Visual Used:** Horizontal Bar Charts

* Top artists by average popularity
* Artists ranked based on performance

**Insights:**

* A small group of artists consistently dominate popularity
* Useful for identifying high-impact artists

---

## 🛠 Tools & Technologies Used

* **Power BI Desktop** – Data modeling & visualization
* **DAX** – Measures and KPIs
* **Microsoft Excel / CSV** – Data source

---

## 📂 Data Model Overview

* Single fact table containing song-level data
* Measures created using DAX for:

  * Average Popularity
  * Explicit Song Ratio
  * Artist Count
  * Duration Metrics

---

## 🔍 Filters & Interactivity

* Song and Artist slicers
* Album type filters
* Year and Month toggles

> All visuals are cross-filtered for seamless interaction.

---

## 📌 Business Use Cases

* Music trend analysis
* Content moderation insights (explicit content)
* Artist performance evaluation
* Streaming strategy optimization

---

## 🚀 Future Enhancements

* Add genre-based analysis
* Include audio features (danceability, energy, tempo)
* Implement Top-N dynamic artist filters
* Add geographical insights

---

## 👤 Author

**Mohit Sengar**
Aspiring Data Analyst | Power BI | SQL | Python

---

## 📎 Notes

This dashboard is built for learning and portfolio purposes. All insights are derived from the provided dataset and may vary with updated data.

---

✅ *Feel free to customize this README based on your dataset or portfolio requirements.*
