# mini-shazam
Our project draws inspiration from the famous app Shazam and aims to recreate its core functionality using the GTZAN dataset and various machine learning algorithms. Through our project, we seek to explore the fundamental aspects of audio signal processing, feature extraction, and classification techniques to study, classify, and even recommend music based on audio inputs. Our goal is to develop a user-friendly interface that allows users to upload audio files and get accurate and fast results for identifying songs and discovering new music.
## Exploratory Data Analysis

To help users explore the data, we created a Gradio interface that displays various graphs related to the audio signal. To use the interface, follow these steps:

1. Clone the repository and install the data.
2. Open the EDA notebook using google colab.
3. Run all the cells and click on the gradio link
4. Upload an audio file in WAV format.
5. Select the type of graph you want to display from the dropdown menu.
6. The interface will display the selected graph and related statistics.

Here's what the interface looks like in action:

![Gradio Interface](EDA.gif)

## Data preparation

Before delving into the analysis and modeling, our data preparation pipeline ensures the GTZAN dataset is primed for effective utilization. This involves steps such as data cleaning, audio file parsing, and feature extraction. Detailed instructions can be found in the data_preparation section of the homemade_shazam notebook.

## Model Benchmarking

Our quest for optimal song classification led us to a thorough evaluation of various machine learning models. Below, we outline the models employed in our benchmarking process and their respective strengths:

### Models 

1. **Naive Bayes (GaussianNB)**: This probabilistic model assumes independence between features. Despite its simplicity, it often performs surprisingly well for text and categorical data.

2. **Stochastic Gradient Descent (SGDClassifier)**: This linear classifier utilizes stochastic gradient descent to find the best-fitting hyperplane. It's suitable for large datasets and is particularly effective for linear models in text classification.

3. **K-Nearest Neighbors (KNN)**: KNN classifies data points based on the majority class among their k-nearest neighbors. It's intuitive and versatile, making it effective for non-linear data.

4. **Decision Trees**: Decision trees divide data into subsets based on the value of specific input features. They're interpretable and capable of capturing non-linear relationships.

5. **Random Forest**: This ensemble model aggregates multiple decision trees to enhance accuracy and control overfitting. It's robust and suitable for complex datasets.

6. **Support Vector Machine (SVM)**: SVMs aim to find a hyperplane that maximizes the margin between classes. They're effective in high-dimensional spaces and can handle both linear and non-linear data.

7. **Logistic Regression**: Despite its name, logistic regression is a linear model used for binary and multiclass classification. It estimates the probability of belonging to a certain class.

8. **XG Boost (Extreme Gradient Boosting)**: XG Boost is an ensemble model that combines multiple weak learners to create a strong classifier. It excels in handling complex relationships and imbalanced datasets.

9. **Cross Gradient Boosting (XGBRFClassifier)**: This variation of XG Boost focuses on random forests, integrating the gradient boosting technique. It's capable of handling multiclass classification tasks.

### Evaluation and Insights

After fitting each model to our training data and predicting on the test set, we visualized the confusion matrix for each model. The confusion matrix provides insights into the distribution of true positive, true negative, false positive, and false negative predictions. This visualization aids in understanding the model's performance across different music genres.

The accuracy score, indicating the proportion of correctly classified instances, was also calculated for each model. This metric offers a quick overview of how well the model performs overall.

The combination of confusion matrices and accuracy scores enabled us to identify the models that excel in classifying various music genres. These insights guide our decision-making in selecting the most suitable model for our song classification endeavor.

As we refine our models and continue to harmonize our project's accuracy and efficiency, we invite you to explore the fascinating world of audio analysis and machine learning with us. Your engagement, feedback, and contributions are integral to the evolution of mini-shazam.
