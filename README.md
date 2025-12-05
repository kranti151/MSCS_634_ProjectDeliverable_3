# MSCS_634_ProjectDeliverable_3

# Deliverable 3: Customer Experience Analysis for AI-Driven Optimization

This project analyzes `customer_experience_data.csv` using machine learning to predict customer retention, segment customers, and discover behavioral patterns.

## Key Insights

### Classification (Customer Retention Prediction)
*   **Models**: Decision Tree and Random Forest (tuned with `GridSearchCV`).
*   **Performance**: Both models achieved perfect accuracy and F1-scores (1.0) on the test set, indicating a highly separable dataset, likely due to its synthetic nature. This suggests strong predictive capability for customer retention but requires real-world validation.
*   **Impact**: Enables proactive retention strategies and targeted interventions based on predicted churn risk.

### Clustering (Customer Segmentation)
*   **Model**: K-Means clustering identified 3 distinct customer segments.
*   **Visualization**: Principal Component Analysis (PCA) reduced data to 2 dimensions for clear visualization of clusters.
*   **Impact**: Provides a basis for personalized marketing, tailored product development, and customized customer service.

### Pattern Mining (Association Rules)
*   **Algorithm**: Apriori algorithm was used after binarizing 'Products_Purchased', 'Products_Viewed', and 'Num_Interactions'.
*   **Findings**: Discovered strong association rules (e.g., `Products_Viewed` => `Products_Purchased`) with high support, confidence, and lift (often 1.0), suggesting a tightly coupled customer journey. This strong correlation is likely an artifact of the synthetic data.
*   **Impact**: Informs cross-selling, bundle promotions, and website layout optimization to enhance customer purchasing behaviors.

## Challenges and Solutions

*   **Perfect Performance on Synthetic Data**: The exceptionally high metrics (1.0) highlight the need for rigorous validation on diverse, real-world datasets to ensure model robustness and generalizability.
*   **Cluster Interpretability**: Further profiling of K-Means clusters by examining original feature values is essential to derive actionable business insights.
*   **Binarization for Apriori**: Careful consideration of binarization thresholds is crucial to avoid losing granular information and accurately reflect real-world patterns.
