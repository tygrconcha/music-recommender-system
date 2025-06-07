# Music Recommendation System

This is my individual project presentation on Machine Learning.

---

## Credits & Acknowledgments

- Initial inspiration and dataset from Andrada Olteanu’s Kaggle notebook “Work with Audio Data – Visualise, Classify, Recommend” (GTZAN dataset).  
- Project improvements made on top of the original work:  
  https://www.kaggle.com/code/andradaolteanu/work-w-audio-data-visualise-classify-recommend  
- Dataset source:  
  https://www.kaggle.com/datasets/andradaolteanu/gtzan-dataset-music-genre-classification

---

## Steps Overview

| Step                                             | Description                                                                                                                         |
| ------------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------- |
| **Explore Audio Data**                           | Audio file was loaded with `librosa`, trimmed of silence, and its array shape and sample rate were displayed.                      |
| **Understanding Audio**                          | Waveform (`y`) and sample rate (`sr`) were inspected to understand time-domain representation.                                      |
| **2D Representation: Sound Waves**               | Trimmed audio was plotted as a time-series waveform to visualize amplitude over time.                                               |
| **Fourier Transform**                            | Short-time Fourier transform (STFT) was applied to decompose the signal into frequency components.                                 |
| **Spectrogram**                                  | STFT magnitudes were converted to decibel scale and plotted on a log-frequency spectrogram.                                        |
| **Mel Spectrogram**                              | A mel-scaled spectrogram was generated to reflect human auditory perception of pitch.                                              |
| **Audio Features**                               | Zero-crossing rate, harmonic/percussive components, tempo (BPM), spectral centroid, spectral rolloff, MFCCs, and chroma were extracted. |
| **Exploratory Data Analysis**                    | `features_30_sec.csv` (1 000×60) was loaded; structure and summary statistics were reviewed.                                        |
| **Correlation Heatmap**                          | Correlations among the 30-sec feature means were computed and visualized with a heatmap.                                            |
| **Box Plot for Genres**                          | BPM distributions across the 10 genres were compared via box plots.                                                                 |
| **PCA**                                          | Features were normalized, PCA was performed, and the first two principal components were plotted by genre.                          |
| **Machine Learning Classification**              | `features_3_sec.csv` was loaded, labels encoded, 70/30 train/test split by song ID was applied, and data was scaled.                |
| **Model Evaluation Function**                    | A reusable function was defined to fit a model and report accuracy, precision, recall, and F1 on the test set.                      |
| **Model Benchmarking**                           | Five classifiers (KNN, Random Forest, SVM, Logistic Regression, XGBoost) were trained and tuned; before/after scores were compared. |
| **Feature Importance**                           | Permutation importance was computed on the best SVM pipeline to identify the top-5 influential features.                            |
| **Recommender System**                           | Cosine similarity was computed on 30-sec feature vectors to build a 1 000×1 000 similarity matrix and a `find_similar_songs()` function. |
| **Similarity Examples**                          | Top-5 song recommendations were demonstrated for sample tracks (e.g., “pop.00019.wav” and “metal.00002.wav”).                         |

---

## Purpose  
The goal of this project is to apply my knowledge and skills in Machine Learning. I chose the topic *Music Recommendation System* because I enjoy music and wanted to combine my interest in Data Science with something I’m passionate about, which is music.
