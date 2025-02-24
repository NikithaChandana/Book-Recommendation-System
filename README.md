# Banned Book Recommender System

## **Project Overview**
### **Team Members:**
- Prathyusha - prathyusha1231
- Nikitha Chandana - NikithaChandana
- Prakruti Pruthvi Kumar - ppruthvi22

### **Introduction**
The **Banned Book Recommender System** aims to address the issue of book censorship, which restricts access to information and discourages independent thinking. By recommending banned books based on user preferences for regular literature, we promote intellectual freedom and encourage diverse perspectives. Our stakeholders include students, parents, librarians, and readers who seek access to challenged literary works.

---

## **Literature Review**
Book censorship deprives individuals of diverse viewpoints and limits intellectual growth. The project leverages prior research on recommendation systems and text analysis techniques to develop an effective recommendation model. We use methods proven in collaborative filtering and content-based filtering to align recommendations with user preferences.

---

## **Data and Methods**
### **Datasets Used**
1. **Amazon Book Review Dataset** - Contains user ratings, book metadata, and reviews (3M+ entries, UCSD 2023).
2. **Amazon Book Metadata** - Includes book titles, descriptions, authors, and categories (200K+ entries, UCSD 2023).
3. **Banned Book Dataset** - Collected from **PEN America** and **Open Library API** (2K+ banned books between 2021-2023).

### **Data Preprocessing**
- Removed duplicate rows and handled missing values.
- Standardized text fields by converting to lowercase and removing inconsistencies.
- Merged Amazon and Banned Book datasets using **Book Title** for richer metadata.

### **Data Visualization**
- **Rating Distribution Chart** - Displays frequency of ratings.
- **Top Authors Chart** - Identifies authors with the most books.
- **Genre Distribution Pie Chart** - Analyzes book categories.
- **Most Reviewed Books Chart** - Highlights top-rated books.

### **Text Processing & Embedding Methods**
- **Sentence-BERT (SBERT)** - Generates semantic embeddings for book descriptions.
- **DistilBERT** - Converts book text to vector representations.
- **T5 Tokenizer** - Used for encoding textual data.

### **Dimensionality Reduction Techniques**
- **UMAP** - Captures complex global and local structures for better visualization.
- **PCA & t-SNE** - Used for alternate dimensionality reductions.

### **Clustering Algorithms Used**
- **K-Means** - Partitions books into meaningful clusters.
- **DBSCAN** - Identifies books with similar user engagement.
- **Agglomerative Clustering** - Hierarchical clustering method.

---

## **Recommendation System**
### **Final Model Workflow**
1. **Dimensionality Reduction** - Used **UMAP in 3D** to refine book clusters.
2. **Book Clustering** - Applied **K-Means** for better grouping.
3. **User Similarity Analysis** - Used **Singular Value Decomposition (SVD)** to infer user preferences.
4. **Personalized Recommendations** - Matched users to books in similar clusters.

### **Results & Performance Metrics**
- **Silhouette Score:**
  - Amazon Dataset: **0.6949**
  - Banned Book Dataset: **0.7663** (Higher score indicates well-defined clusters.)
- **Recommendation Accuracy:**
  - Root Mean Squared Error (RMSE): **0.8219** (Evaluated using 5-fold cross-validation.)
- **Example Recommendations:**
  - **Regular Books:** *How to Stop Worrying and Start Living*, *The Faeries Oracle*, *Outwitting Writer’s Block*.
  - **Banned Books:** *Were I Not a Girl: The Inspiring and True Story of Dr. James Barry*, *Girl Talk: The Ultimate Body Puberty Book for Girls*, *What to Do When I’m Gone: A Mother’s Wisdom to Her Daughter*.

---

## **Discussion**
While the system successfully recommends banned books based on user preferences, limitations exist due to the **small size of the banned book dataset**, restricting variety in recommendations.

### **Future Improvements:**
1. **Expand Dataset** - Gather additional banned books for broader representation.
2. **Enhance Metadata** - Incorporate user reviews and book popularity metrics.
3. **Develop User Interface** - Build an interactive platform for real-time recommendations and feedback.

---

## **Conclusion**
Our recommender system supports intellectual freedom by providing access to banned literature, encouraging critical thinking and diverse perspectives. With future enhancements, the system will better serve its stakeholders, enabling more comprehensive and personalized book recommendations.

---

