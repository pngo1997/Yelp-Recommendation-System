# 📌 Yelp Business Recommendation System  

## 📜 Overview  
This project builds an **item-based collaborative filtering recommendation system** for businesses using the **Yelp dataset**. The system integrates **table lookups, embeddings, and collaborative filtering** to provide accurate business recommendations based on user queries.  

## 🎯 Problem Explanation  
Users often search for **recommended businesses** based on specific categories, attributes, and locations. This project aims to:  
- **Retrieve business recommendations** using structured queries.  
- **Enhance recommendation accuracy** with **text embeddings and collaborative filtering**.  
- **Visualize recommendations** using an interactive **geo-mapping system**.  

📌 **Note**: Users dataset is very large. Please contact me if you want to use it.

📌 **Dataset**: Yelp Business Dataset (including business attributes, reviews, users, and ratings).  

## ⚙️ Installation & Dependencies  
### **Requirements**  
- **Python 3.x**  
- **Libraries Used**:  
  - `pandas` – Data processing  
  - `numpy` – Numerical computations  
  - `spaCy` – Text processing  
  - `scikit-learn` – ML models, cosine similarity  
  - `folium` – Geospatial visualization  
  - `geopy` – Location services  

## 🔍 Project Structure
### 1️⃣ Business Recommendation by Table Lookup
📌 **Objective**: Retrieve businesses based on predefined query formats.

✅ **Methodology**:
- Analyzed key attributes (categories, city, attributes) to determine recommendation factors.
- Transformed category text into a structured format (Coffee & Tea → Coffee, Tea).
- Implemented:
  - getRec(query): Retrieves businesses based on structured queries.
  - geoRec(query, numRec): Generates interactive maps for recommendations.
- Applied query filtering logic:
  - Best = Businesses with **ratings > 4.0.**
  - **Category-based** and **location-based** filtering.
  - Integrated **geospatial mapping** using folium and geopy.
 
## 2️⃣ Recommender System using Embeddings
📌 **Objective**: Predict business ratings using word embeddings and improve recommendation accuracy.

✅ **Methodology**:
- **Text preprocessing** using spaCy (stop word removal, tokenization).
- **Generated word embeddings** using GloVe (50D vectors).
- **Computed business recommendations** based on dot product similarity.
- Applied a **binning strategy** to improve rating predictions.
- **Reduced RMSE from high variance to 1.89** after optimizations.

## 3️⃣ Item-Based Collaborative Recommendation using Embeddings
📌 **Objective**: Recommend businesses based on category similarity and embeddings.

✅ **Methodology**:
- **Refined business categories** for better retrieval (Coffee & Tea → [Coffee, Tea]).
- Implemented:
  - filteredData(query): Extracts businesses matching query attributes.
  - computeRecommendation(query): Computes recommendations using cosine similarity.
- **Query parsing logic**:
  - Extracts **city name, business name, and categories** from user input.
  - Filters businesses based on **category similarity** (must match at least 3 categories).
- Integrated geo-mapping for visualization.

## 📊 Results & Findings
✅ Successful integration of table lookups, embeddings, and collaborative filtering.

✅ Improved categorization enhances recommendation accuracy. 

✅ Binning techniques significantly refined rating predictions. 

✅ Challenges in query sensitivity were mitigated through text preprocessing. 
