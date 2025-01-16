# DSBA 6156 Final Project: Classify Song Genres from Audio Data  
**Team Members**: Shivani Desai, Yaxin Zhao, Viviana Montenegro Cortez, Robert Bintu  


## 📌 **Project Overview**  
This project explores music genre classification using machine learning techniques to classify songs as either **Hip-Hop** or **Rock** based on their audio features. By automating genre classification, we eliminate manual errors and reduce processing time, enabling faster categorization for music streaming services and personalized recommendations.


## 🎯 **Objective**  
- Analyze audio features such as `acousticness`, `danceability`, `tempo`, and more to predict song genres.  
- Apply machine learning models to understand and improve classification accuracy.  
- Balance the dataset to reduce bias towards the majority class (Rock).  
- Evaluate performance using metrics like accuracy and F1-score.  


## 📂 **Dataset**  
- **Source**: Datacamp, Echo Nest Dataset.  
- **Tracks**: 4,802 songs after preprocessing.  
- **Features**: 8 continuous audio features and a target variable (`genre_top`).  
- **Classes**:  
  - **Rock**: 3,892 tracks (majority class).  
  - **Hip-Hop**: 910 tracks (minority class).  


## 🛠️ **Methodology**  
### 1. **Data Preparation**  
- Cleaned and merged datasets to create `echo_tracks`.  
- Features scaled using **StandardScaler** to normalize values.  
- Applied **Principal Component Analysis (PCA)** to reduce dimensions while retaining variance.  
- Balanced the dataset by downsampling the majority class (Rock).  

### 2. **Machine Learning Models**  
Implemented the following models for classification:  
- **Logistic Regression**  
- **Decision Tree**  
- **Random Forest**  
- **Support Vector Classifier (SVC)**  
- **K-Nearest Neighbors (KNN)**  

### 3. **Evaluation**  
- Assessed models on both imbalanced and balanced datasets.  
- Tuned hyperparameters using **GridSearchCV** for optimal performance.  
- Used **cross-validation** to validate generalization performance.  


## 📈 **Key Results**  
### **Model Performance on Imbalanced Data**  
| Model               | Accuracy  | F1 (Hip-Hop) | F1 (Rock) |
|---------------------|-----------|--------------|-----------|
| Decision Tree       | 87.76%    | 0.66         | 0.93      |
| Logistic Regression | 87.84%    | 0.62         | 0.93      |
| Random Forest       | 90.51%    | 0.71         | 0.94      |
| SVC                 | 88.18%    | 0.62         | 0.93      |
| KNN                 | 90.42%    | 0.71         | 0.94      |

### **Model Performance on Balanced Data**  
| Model               | Accuracy  | F1 (Hip-Hop) | F1 (Rock) |
|---------------------|-----------|--------------|-----------|
| Decision Tree       | 81%       | 0.81         | 0.81      |
| Logistic Regression | 82%       | 0.82         | 0.82      |
| Random Forest       | 85%       | 0.84         | 0.85      |
| SVC                 | 86%       | 0.86         | 0.86      |
| KNN                 | 85%       | 0.85         | 0.86      |

### **Cross-Validation Results**  
| Model               | CV Score  |
|---------------------|-----------|
| Decision Tree       | 75.5%     |
| Logistic Regression | 79.1%     |
| Random Forest       | 80.5%     |
| SVC                 | 81.6%     |
| KNN                 | 81.5%     |


## 💡 **Insights**  
1. **Random Forest** consistently performed well across imbalanced and balanced datasets, achieving the highest accuracy (90.51% on imbalanced data).  
2. Balancing the dataset significantly improved the performance for the minority class (Hip-Hop).  
3. SVC and KNN demonstrated robust generalization, as reflected in their high cross-validation scores.  


## 🔮 **Future Work**  
- **Feature Enhancement**: Explore additional audio features for better genre differentiation.  
- **Deep Learning Models**: Utilize CNNs on spectrograms for improved accuracy.  
- **Generalization Testing**: Evaluate models on entirely new datasets to assess robustness.  
- **User Feedback Integration**: Refine models based on user insights to enhance practical applicability.  

## 🤝 **Team Contributions**  
- **Shivani Desai**: Dataset preparation, PCA, Decision Tree model, Results & Analysis.  
- **Yaxin Zhao**: Logistic Regression, SVC models, Conclusion & Future Work.  
- **Viviana Montenegro Cortez**: Random Forest model, Data Acquisition & Methodology.  
- **Robert Bintu**: KNN model, Introduction & Project Overview.  

## 📚 **References**  
1. Datacamp (https://app.datacamp.com/learn/projects/449)  
