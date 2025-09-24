# 🎶 Automating Playlist Creation with Machine Learning

## 📌 Project Overview
Music platforms like Spotify rely on curated playlists to improve user engagement.  
Currently, manual playlist creation can’t keep up with demand at scale.  

This project explores whether **unsupervised machine learning** can help automate playlist generation by grouping songs with similar characteristics.  
The result is a **prototype** that demonstrates the potential of machine learning for playlist curation, while highlighting where human expertise is still needed.  

---

## 🎯 Business Goal
- **Challenge**: Manual playlisting is slow and resource-intensive.  
- **Objective**: Prototype an automated system that can generate playlists from song features.  
- **Outcome**: Machine learning can group songs into meaningful clusters, but a **hybrid human + AI approach** works best.  

---

## 📊 Data & Features
We used Spotify’s audio features dataset and selected **8 out of 13 key attributes**:  

- 🎵 Danceability  
- ⚡ Energy  
- 🗣️ Speechiness  
- 🎸 Acousticness  
- 🎹 Instrumentalness  
- 🎤 Liveness  
- 😊 Valence  
- ⏱️ Tempo  

Data preprocessing included experimenting with scaling techniques.  
✅ **RobustScaler** performed best, reducing the impact of outliers while preserving song relationships.  

---

## 🧠 Methodology
We applied and compared **unsupervised learning algorithms**:
- **KMeans** → Best balance of cluster cohesion & interpretability  
- **Agglomerative Clustering**  
- **DBSCAN**  

We tested different numbers of clusters (2–29) and found **~13 clusters** gave playlists that were both distinct and usable.  
To visualize results, we applied **PCA** for dimensionality reduction and 3D clustering plots.  

---

## 🎧 Results & Insights
- Clusters reflected **meaningful song groupings** (moods/genres).  
- Example: energetic/dance tracks grouped together vs. acoustic/low-energy songs.  
- Playlists showed **moderate cohesion**, with some overlap between clusters.  
- Features like **tempo, energy, and danceability** were most helpful.  
- Audio features **alone cannot capture deeper context** such as lyrics, culture, or listener mood.  

📌 **Recommendation**:  
Adopt a **hybrid approach** →  
- **80% automated** playlist creation via clustering  
- **20% curated** by human experts  

---

## 🛠️ Tools & Tech Stack
- **Python** (scikit-learn, pandas, numpy, matplotlib, seaborn)  
- **Jupyter Notebook**  
- **Spotify audio features dataset**  

---

## 📂 Repository Structure
├── data/spotify_songs.csv # Dataset ([data](https://github.com/victoria-vasilieva/spotify-playlist-clustering/blob/main/3_spotify_5000_songs.csv))

├── spofify_songs_clustering.ipynb # Main analysis & clustering [notebook](https://github.com/victoria-vasilieva/spotify-playlist-clustering/blob/main/spofify_songs_clustering.ipynb)

├── Automating Playlist Creation.pdf # Business [presentation slides](https://github.com/victoria-vasilieva/spotify-playlist-clustering/blob/main/Automating%20Playlist%20%20Creation.pdf)

├── requirements.txt # Dependencies

├── README.md # Project documentation

___

## 📂 Data
The dataset used comes from Spotify’s audio features.  
A data set is included [data](https://github.com/victoria-vasilieva/spotify-playlist-clustering/blob/main/3_spotify_5000_songs.csv) for reproducibility.  

---

## ⚡ Quick Start (for developers)
To run the notebook locally:

1. Clone this repository  
   ```bash
   git clone https://github.com/yourusername/spotify-playlist-clustering.git
   cd spotify-playlist-clustering
Install dependencies

bash
Copy code
pip install -r requirements.txt
Open the Jupyter notebook

bash
Copy code
jupyter notebook spofify_songs_clustering.ipynb


## 📈 Key Takeaways
Connects machine learning to a real-world business challenge (scalable playlist creation).

Hands-on with unsupervised ML (KMeans, Agglomerative, DBSCAN) and PCA visualization.

Strong in data preprocessing (feature selection, scaling).

Skilled at communicating results: both technical (notebook) and business-focused (slides).

## 👩‍💻 Team
Azumi
Victoria
Sahand

✨ This project shows how AI can assist creativity, but still benefits from the human touch.
