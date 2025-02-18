# 🎵 Music Popularity Analysis 🎵 
**Understanding the Factors Behind Hit Songs**  

![Music Analysis](https://upload.wikimedia.org/wikipedia/commons/thumb/6/6a/Music_Equalizer_Animation.gif/800px-Music_Equalizer_Animation.gif)  

## 📌 Project Overview  
This project explores what makes a song popular using **data science and machine learning techniques**. By analyzing a dataset of over **50,000 songs** from Spotify, I examine the impact of **various audio features** on song popularity.  

---

## 🚀 Features & Findings  

### 🎼 **Feature Distributions**  
- **Histograms** show the distribution of 10 selected song features.  
- **Danceability and tempo** follow a normal distribution, while others vary.

### 📏 **Song Length vs Popularity**  
- **Scatter plots & correlation coefficients** reveal a **weak negative correlation** (~ -0.08 Pearson, ~0.07 Spearman).  
- **Conclusion**: Song length does not strongly impact popularity.

### 🔥 **Explicit Songs & Popularity**  
- **Mann Whitney U test** shows **explicit songs are significantly more popular** than non-explicit ones (**p < 0.05**).  

### 🎹 **Major vs Minor Key**  
- **Mann Whitney U test** indicates **no significant difference** in popularity between major and minor key songs.

### 🔊 **Energy vs Loudness**  
- **Strong correlation (~-0.78 Pearson, ~0.73 Spearman)**: Songs with higher energy tend to be louder.

### 📊 **Predicting Popularity with Regression**  
- **A simple linear regression model** was built for each of the 10 features to predict popularity, after normalizing data.
- **Instrumentalness** was the best individual predictor of popularity, but still had low predictive power (**R² ≈ 0.03, RMSE ≈ 20.45**).  
- **A multiple linear regression model** slightly improved prediction based on the 10 features but remained weak (**R² ≈ 0.07, RMSE ≈ 20.06**).  

### 🏆 **Principal Component Analysis (PCA)**  
- **A correlation matrix** was used for initial visualization, followed by a **scree plot** to extract three components using the **Kaiser criterion**.
- **Three meaningful components extracted**: **Intensity, Expressiveness, Quietness**  and visualized with **loading plots** to show how each feature contributes to each component.
- **57.27% of variance explained** by these components.

### 🎯 **Song Key Prediction with Logistic Regression**
- **A logistic regression model** was built to predict a song's key from valence, with **61.30% accuracy**.
- **Confusion matrix** and plotting the model showcased low predictive power.

### 🎯 **Genre Prediction with Random Forest**  
- Achieved **~32% accuracy** using a **Random Forest Classifier** with **k-fold cross-validation**.
- Feature importance plot reveals **which attributes matter most** for predicting genre.  

---

## 🛠️ Installation & Setup  

### **1️⃣ Clone the Repository**  
```bash
git clone https://github.com/yourusername/music-popularity-analysis.git
cd music-popularity-analysis
```

### **2️⃣ Install Dependencies**  
Ensure you have **Python 3.8+** and install the required packages:  
```bash
pip install -r requirements.txt
```

### **3️⃣ Run the Analysis**  
Execute the main script to perform data analysis and generate visualizations: 
```bash
python CapstoneAnviCode.py
```

## 📊 Data & Methods

### Dataset
- **Source:** Spotify dataset (`spotify52kData.csv`)
- **49,221 songs** after cleaning (removal of duplicates, missing values)
- **Key attributes:** Duration, Danceability, Energy, Loudness, Speechiness, Acousticness, Instrumentalness, Liveness, Valence, Tempo, Popularity, Explicitness, Genre, Key

### Machine Learning Models Used
- **Linear & Multiple Regression** for predicting song popularity.
- **Logistic Regression** for predicting major/minor key.
- **Random Forest Classifier** for genre classification.
- **Principal Component Analysis (PCA)** for feature reduction.
- **K-Means Clustering** for song grouping.

---

## 📌 Results & Takeaways

- **No strong predictor of song popularity exists** among the selected features.
- **Explicit songs tend to be more popular** than non-explicit ones.
- **Energy and loudness are strongly correlated** (~0.78).
- **Machine learning models struggle to predict popularity and genre accurately**, indicating that **external factors (ex. marketing, social trends, social media) may play a bigger role**.
- **PCA reveals three dominant components** influencing music characteristics.

---

## 📖 Future Improvements

🔹 Incorporate **social media engagement data**.  
🔹 Use **deep learning models (LSTMs, transformers)** for sequence-based analysis.  
🔹 Expand dataset with **real-time streaming data from Spotify API**.  

---

## 👩‍💻 Author

📝 **Anvi Parikh**  

📧 Email: anviparikh@nyu.edu  
📌 LinkedIn: [linkedin.com/in/anvi-parikh](https://linkedin.com/in/anvi-parikh)  
📂 GitHub: [github.com/anvi-parikh](https://github.com/anvi-parikh)  

---







