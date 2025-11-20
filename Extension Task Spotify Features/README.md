# Spotify Music Features Analysis: Genre Characteristics Dashboard

This repository contains the dataset and the analytical dashboard used to explore and compare the audio features of music across various genres, leveraging Spotify's track characteristics.

---

## 💾 Data Source

The primary data source is the extracted CSV file containing details for over 40,000 unique tracks:

* **File:** `Extension_Task_SpotifyFeatures.xlsx - in.csv`
* **Original Source:** Spotify API (features derived from audio analysis of tracks).

---

## 📋 Data Dictionary: Track Features

The following table explains the core columns (features) used in the analysis, which are often scaled between **0.0 (low/none)** and **1.0 (high/maximum)** unless otherwise noted.

| Column Name | Type | Description | Scale / Notes |
| :--- | :--- | :--- | :--- |
| **genre** | Categorical | The primary genre classification for the track. | (e.g., Pop, Rap, Rock, Movie) |
| **artist_name** | Text | The name of the main artist for the track. | |
| **track_name** | Text | The title of the song. | |
| **popularity** | Numeric | A measure of how popular the track is, calculated by Spotify. | **0 to 100** (where 100 is most popular) |
| **acousticness** | Numeric | Confidence measure that the track is **acoustic**. | **0.0 to 1.0** |
| **danceability** | Numeric | How suitable a track is for **dancing** based on tempo, rhythm stability, and beat strength. | **0.0 to 1.0** |
| **duration_ms** | Numeric | The duration of the track in **milliseconds**. | (e.g., 200,000 ms = 3 min 20 sec) |
| **energy** | Numeric | A measure of intensity and activity (perceptual measure of high/fast/loud tracks). | **0.0 to 1.0** |
| **instrumentalness** | Numeric | Predicts whether a track contains **no vocals** (excluding ad-libs/speech). | Values closer to 1.0 are more likely to be instrumental. |
| **key** | Categorical | The estimated key of the track. | (e.g., C, C#, D, etc.) |
| **liveness** | Numeric | Detects the presence of an audience in the recording. | Values above 0.8 suggest a high probability of a **live performance**. |
| **loudness** | Numeric | The overall **loudness** of a track in decibels (dB). | Typically ranges from **-60 to 0 dB**. |
| **speechiness** | Numeric | Detects the presence of **spoken words**. | Values above 0.66 suggest spoken word; below 0.33 suggests music. |
| **tempo** | Numeric | The overall estimated **tempo** of a track in beats per minute (BPM). | |
| **valence** | Numeric | A measure describing the musical **positivity** conveyed by a track. | High valence means positive (happy, cheerful); low valence means negative (sad, gloomy). |

---

## 📊 Visualization Overview: Spotify Feature by Genre Dashboard (`SpotifyFeaturebyGenre.twbx`)

The Tableau or Power BI dashboard is designed to facilitate a comparative analysis of audio features across different music genres.

### Key Sheets/Charts:

1.  **Genre Feature Comparison (Radar/Spider Chart)**
    * **Description:** A chart where each axis represents a key audio feature (**Energy, Danceability, Valence, Acousticness, etc.**). Each genre is represented by a separate line or shaded area, allowing for an immediate visual comparison of their average characteristics.     * **Purpose:** To quickly determine the **sonic signature** of each genre (e.g., see if "Classical" is high on acousticness and low on energy, while "Techno" is the opposite).

<img width="1361" height="685" alt="image" src="https://github.com/user-attachments/assets/762c2e96-f186-4892-a5be-93ddc03c744e" />

2.  **Popularity by Genre (Ranked Bar Chart)**
    * **Description:** A horizontal bar chart ranking all genres based on the **average 'popularity'** score of the tracks within them.
    * **Purpose:** Identifies which genres contain the most highly-rated or successful tracks on the platform.

<img width="1360" height="607" alt="image" src="https://github.com/user-attachments/assets/1ac0440a-f6af-4348-abd7-e60b222b6f42" />




3.  **Tempo & Duration Distribution (Box Plot or Histogram)**
    * **Description:** Charts showing the distribution (median, quartiles, range) of **Tempo (BPM)** and **Duration (ms)** for selected genres.
    * **Purpose:** Reveals the typical speed and length of songs within a genre and highlights outliers (e.g., a "Classical" box plot might show a wider range of durations than "Pop").

   <img width="1239" height="609" alt="image" src="https://github.com/user-attachments/assets/8528231c-c8ad-47cc-899a-60fc61812f34" />

4.  **Loudness vs. Energy Scatter Plot**
    * **Description:** A scatter plot with **Loudness** on one axis and **Energy** on the other. Genres are color-coded, showing the correlation between these two variables.
    * **Purpose:** To confirm the expected relationship that higher energy tracks are generally louder, and to see if any genres deviate significantly from this trend.

<img width="1239" height="608" alt="image" src="https://github.com/user-attachments/assets/f499238b-062a-431d-8134-652e7d41adc4" />


5.  **Data Grid / Detail Table**
    * **Description:** A filtered table showing the top tracks (by popularity) for the currently selected genre, including their individual feature scores.
    * **Purpose:** Allows users to drill down and examine specific tracks that represent the genre's aggregated characteristics.

<img width="1237" height="606" alt="image" src="https://github.com/user-attachments/assets/362a11d1-9014-441a-9cdb-363435f17433" />

