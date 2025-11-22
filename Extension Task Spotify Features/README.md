# Spotify Music Features Analysis: Genre Characteristics Dashboard 🎧🎶

This repository contains the dataset and the analytical dashboard used to explore and compare the audio features of music across various genres 🎵, leveraging Spotify's track characteristics. 🔬

---

## 💾 Data Source 📁

The primary data source is the extracted CSV file containing details for over 40,000 unique tracks:

* **File:** `Extension_Task_SpotifyFeatures.xlsx - in.csv` 🧾
* **Original Source:** Spotify API (features derived from audio analysis of tracks). ✨

---

## 📋 Data Dictionary: Track Features 🎼

The following table explains the core columns (features) used in the analysis, which are often scaled between **0.0 (low/none)** 📉 and **1.0 (high/maximum)** 📈 unless otherwise noted.

| Column Name | Type | Description | Scale / Notes |
| :--- | :--- | :--- | :--- |
| **genre** | Categorical | The primary genre classification for the track. 📂 | (e.g., Pop, Rap, Rock, Movie) |
| **artist_name** | Text | The name of the main artist for the track. 🎤 | |
| **track_name** | Text | The title of the song. 🏷️ | |
| **popularity** | Numeric | A measure of how popular the track is, calculated by Spotify. ⭐ | **0 to 100** (where 100 is most popular) |
| **acousticness** | Numeric | Confidence measure that the track is **acoustic**. 🎸 | **0.0 to 1.0** |
| **danceability** | Numeric | How suitable a track is for **dancing** based on tempo, rhythm stability, and beat strength. 🕺 | **0.0 to 1.0** |
| **duration_ms** | Numeric | The duration of the track in **milliseconds**. ⏳ | (e.g., 200,000 ms = 3 min 20 sec) |
| **energy** | Numeric | A measure of intensity and activity (perceptual measure of high/fast/loud tracks). 🔥 | **0.0 to 1.0** |
| **instrumentalness** | Numeric | Predicts whether a track contains **no vocals** (excluding ad-libs/speech). 🎹 | Values closer to 1.0 are more likely to be instrumental. |
| **key** | Categorical | The estimated key of the track. 🎼 | (e.g., C, C#, D, etc.) |
| **liveness** | Numeric | Detects the presence of an audience in the recording. 🧑‍🤝‍🧑 | Values above 0.8 suggest a high probability of a **live performance**. |
| **loudness** | Numeric | The overall **loudness** of a track in decibels (dB). 🔊 | Typically ranges from **-60 to 0 dB**. |
| **speechiness** | Numeric | Detects the presence of **spoken words**. 🗣️ | Values above 0.66 suggest spoken word; below 0.33 suggests music. |
| **tempo** | Numeric | The overall estimated **tempo** of a track in beats per minute (BPM). ⏱️ | |
| **valence** | Numeric | A measure describing the musical **positivity** conveyed by a track. 😊 | High valence means positive (happy, cheerful); low valence means negative (sad, gloomy). 😞 |

---

## 📊 Visualization Overview: Spotify Feature by Genre Dashboard (`SpotifyFeaturebyGenre.twbx`) 🖼️

The Tableau or Power BI dashboard is designed to facilitate a comparative analysis of audio features across different music genres. 🎤

### Key Sheets/Charts:

1.  **Popularity Top 10 Genre** ⭐🥇
    * **Description:** Visually maps the relative market share of popularity across the top 10 most popular genres. Larger rectangles indicate genres with a higher average popularity score.
    * **Tree Map:** Average **Popularity** (Size), **Genre** (Color/Label)

<img width="1360" height="607" alt="image" src="https://github.com/user-attachments/assets/1ac0440a-f6af-4348-abd7-e60b222b6f42" />

2.  **Popularity Top 10 Instrumentalness** 🎹🏆
    * **Description:** Identifies the top 10 genres based on their instrumental focus. The size clearly indicates which genres are typically the most instrumental, while the color provides secondary context on their overall popularity.
    * **Packed Bubbles:** Average **Instrumentalness** (Bubble Size), Average **Popularity** (Color), **Genre** (Label)

   <img width="1239" height="609" alt="image" src="https://github.com/user-attachments/assets/8528231c-c8ad-47cc-899a-60fc61812f34" />

3.  **Energy Vs Loudness** 🔥🔊
    * **Description:** Directly compares the average intensity (**Energy**) with the average volume (**Loudness**) across genres. This helps confirm the general correlation between these two features and highlights any genres that are unusually energetic for their loudness (or vice-versa).
    * **Bar Chart (Clustered):** Average **Energy** and Average **Loudness** side-by-side for each Genre. 📊

   <img width="1239" height="608" alt="image" src="https://github.com/user-attachments/assets/f499238b-062a-431d-8134-652e7d41adc4" />

4.  **Danceability Top 10 Genre** 🕺⏱️
    * **Description:** Used to explore the relationship between how **danceable** tracks are and their tempo **(BPM**), focusing only on the 10 genres with the highest average danceability. Each point represents an individual track, revealing clusters and outliers.
    * **Scatter Chart:** **Danceability** (Y-axis), **Tempo** (X-axis), **Genre** (Color) ⚫

<img width="1237" height="606" alt="image" src="https://github.com/user-attachments/assets/362a11d1-9014-441a-9cdb-363435f17433" />

---

