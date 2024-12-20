# Clustering Analysis on Wine Quality Dataset

This project demonstrates a comprehensive clustering analysis using the Wine Quality dataset from the UCI Machine Learning Repository. The primary goal is to evaluate the impact of various clustering algorithms and preprocessing methods on clustering performance, providing insights into how these techniques influence unsupervised learning outcomes.
The project applies multiple clustering algorithms (K-Means, Hierarchical Clustering, and Mean Shift) in conjunction with different preprocessing methods to assess their performance. Evaluation metrics include Silhouette Score, Calinski-Harabasz Index, and Davies-Bouldin Index. Visualizations and metric comparisons further illustrate the effectiveness of each approach.

## Dataset
The Wine Quality dataset comprises various physicochemical properties of wine samples, such as alcohol content, pH levels, and acidity. These features are used for unsupervised clustering analysis without considering the quality score column.

### Dataset Features:
- **Fixed Acidity**
- **Volatile Acidity**
- **Citric Acid**
- **Residual Sugar**
- **Chlorides**
- **Free Sulfur Dioxide**
- **Total Sulfur Dioxide**
- **Density**
- **pH**
- **Sulphates**
- **Alcohol**

### Sample Data:
```csv
fixed acidity;volatile acidity;citric acid;residual sugar;chlorides;free sulfur dioxide;total sulfur dioxide;density;pH;sulphates;alcohol;quality
7.4;0.7;0;1.9;0.076;11;34;0.9978;3.51;0.56;9.4;5
7.8;0.88;0;2.6;0.098;25;67;0.9968;3.2;0.68;9.8;5
7.8;0.76;0.04;2.3;0.092;15;54;0.997;3.26;0.65;9.8;5
```

## Methodology

### Preprocessing Methods:
1. **Normalization**: Scales data to a range [0, 1].
2. **Transformation**: Applies logarithmic or other transformations to features.
3. **PCA**: Reduces dimensionality while preserving variance.
4. **Combination Preprocessing**: Includes methods like Transform + Normalize (T+N) and Transform + Normalize + PCA (T+N+PCA).

### Clustering Algorithms:
1. **K-Means Clustering**: Evaluated with cluster sizes of 3, 4, and 5.
2. **Hierarchical Clustering**: Applied with various linkage criteria.
3. **Mean Shift Clustering**: Explored with bandwidth adjustments.

### Evaluation Metrics:
- **Silhouette Score**: Measures cohesion and separation of clusters.
- **Calinski-Harabasz Index**: Evaluates cluster dispersion.
- **Davies-Bouldin Index**: Assesses cluster compactness and separation.

## Results

### 1️⃣ Performance Metrics Summary:
| Algorithm      | Preprocessing | Clusters | Silhouette Score | Calinski-Harabasz | Davies-Bouldin |
|----------------|---------------|----------|------------------|-------------------|----------------|
| K-Means        | PCA           | 3        | 0.56             | 1425.87           | 0.56          |
| Hierarchical   | PCA           | 4        | 0.48             | 1123.34           | 0.68          |
| Mean Shift     | None          | N/A      | N/A              | N/A               | N/A           |

### 2️⃣ Observations:
- **K-Means with PCA** showed the highest Calinski-Harabasz scores, indicating well-separated clusters.
- **Normalization** improved Davies-Bouldin Index for most algorithms, signifying better cluster compactness.
- **Hierarchical Clustering** performed consistently well with minimal preprocessing.

### 3️⃣ Visualizations:
- **Cluster Performance Comparison**: Bar plots illustrating metric differences.
- **Silhouette Scores by Configuration**: Visual representation of cluster cohesion.

## How to Run

### Clone the Repository:
```bash
git clone https://github.com/sidharthd7/Clustering.git
```

### Install Dependencies:
```bash
pip install -r requirements.txt
```


## License
This project is distributed under the MIT License. Feel free to use, modify, and distribute it as needed.

