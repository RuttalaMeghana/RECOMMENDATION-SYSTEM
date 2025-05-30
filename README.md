# RECOMMENDATION-SYSTEM

*COMPANY*: CODTECH IT SOLUTIONS

*NAME*: RUTTALA MEGHANA

*INTERN ID*: CT06DF1095

*DOMAIN*: MACHINE LEARNING

*MENTOR*: NEELA SANTOSH

*DESCRIPTION*:

Tools Used:-
The implementation leverages a suite of Python libraries tailored for data processing, machine learning, and visualization:

Surprise (Scikit-Surprise): A specialized Python library for building and evaluating recommender systems, Surprise is used to implement the SVD algorithm for collaborative filtering. It provides the SVD class for matrix factorization, Dataset and Reader for loading and formatting data, and utilities like train_test_split and cross_validate for splitting data and computing evaluation metrics (RMSE, MAE). Surprise also includes the MovieLens 100k dataset, simplifying data access.
Pandas: Facilitates data exploration and manipulation by converting raw ratings into a DataFrame and loading movie titles from the MovieLens dataset for interpretable recommendations. It handles data filtering and merging operations efficiently.
NumPy: Supports numerical computations, such as calculating mean metrics from cross-validation results and handling item IDs for recommendation generation.
Matplotlib: Used to create a scatter plot of predicted versus actual ratings, saved as predicted_vs_actual.png, providing a visual assessment of model performance.
Scikit-learn: While not directly used for modeling, its train_test_split and metrics like mean_squared_error and mean_absolute_error are referenced for compatibility with other datasets or custom implementations.
These libraries are standard in data science and recommendation system workflows and are easily installed via Anaconda, which ensures compatibility and simplifies dependency management.

Platform Used:-
The task is implemented in a Jupyter Notebook running within Anaconda Navigator, a user-friendly graphical interface for managing Python environments and packages. Anaconda Navigator is ideal for data science tasks, offering seamless integration with Jupyter Notebook, a web-based environment that combines code, visualizations, and explanatory text. The notebook is executed in a custom Python environment (e.g., recsys_env) configured with Surprise, Pandas, NumPy, Matplotlib, and Scikit-learn. Anaconda Navigator simplifies the installation of the scikit-surprise library, which may require the conda-forge channel for compatibility. The notebook saves outputs as a PNG file (predicted_vs_actual.png) and a text file (recommendation_metrics.txt), facilitating sharing and analysis. Jupyter’s interactive, cell-based structure supports iterative development, making it perfect for prototyping and evaluating recommendation systems.

Task Implementation:-
The Jupyter Notebook executes the following steps:

Data Loading: The MovieLens 100k dataset is loaded using Surprise’s Dataset.load_builtin('ml-100k'), providing user-item-rating triplets. A Pandas DataFrame is created for exploration, and movie titles are loaded from the MovieLens website for interpretable recommendations.
Data Splitting: The dataset is split into 80% training and 20% test sets using surprise_train_test_split with a random seed for reproducibility.
Model Training: An SVD model is initialized with 100 latent factors and 20 epochs, then trained on the training set to learn user and item embeddings.
Evaluation: Predictions are made on the test set, and performance is evaluated using RMSE and MAE. Five-fold cross-validation provides robust estimates of these metrics.
Recommendation Generation: A function (get_top_n_recommendations) predicts ratings for unrated items for a given user (e.g., user ID '1') and returns the top 10 recommendations with movie titles and predicted ratings.
Visualization: A scatter plot visualizes predicted versus actual ratings, with a reference line for perfect predictions, saved as predicted_vs_actual.png.
Output Storage: Metrics (RMSE, MAE, cross-validation results) and top-10 recommendations are printed on notebook.

Applicability of the Task:-
Recommendation systems using collaborative filtering and matrix factorization have wide-ranging applications across industries:

E-commerce: Platforms like Amazon use recommendation systems to suggest products based on user purchase or browsing history, enhancing user experience and increasing sales.
Streaming Services: Companies like Netflix and Spotify leverage collaborative filtering to recommend movies, TV shows, or music, improving user engagement and retention.
Social Media: Platforms like X or YouTube recommend posts, videos, or accounts based on user interactions, driving content discovery.
Online Learning: Educational platforms recommend courses or resources tailored to user interests or learning history, personalizing education.
Advertising: Recommendation systems suggest targeted ads based on user preferences, optimizing marketing campaigns.
Healthcare: Personalized treatment or wellness recommendations can be made based on patient interaction data, improving care delivery. The visualizations and metrics (e.g., RMSE, MAE, top-N recommendations) provide interpretable insights, enabling businesses to assess model performance and refine user experiences.
