# News Labeling Project Summary

## 1. Introduction
The project aims to address the challenges of identifying misinformation and fake news through machine learning. By distinguishing between real articles and mass-produced fake news, the goal is to develop a model capable of accurately categorizing articles as true or fake. Full article available under docs.

## 2. Problem Formulation and Dataset
### 2.1 Other Contributions
Previous attempts to tackle fake news have often relied on word frequency analysis. This project seeks alternative methods to analyze features without computationally intensive processes.

### 2.2 Idea for Implementation
The dataset comprises true articles from Reuters.com and fake articles labeled by Politifact. Only textual and linguistic features are considered, excluding subject and date columns. The approach involves word frequency analysis on titles and feature extraction from the text, utilizing techniques such as stemming and Part-of-Speech (PoS) tagging.

## 3. Data Preprocessing and Feature Extraction
### Feature Extraction from the Title
- Tokenization, removal of stop words, and stemming to create a Bag of Words (BoW).
- Transformation of BoW into a frequency dictionary and creation of a matrix representing word occurrences.

### Feature Extraction from the Text
- Extraction of additional features: average word length, average sentence length, and PoS tag ratios.
- PoS tagging used to identify patterns in language usage.
- Result of Feature Extraction: Combining title and text features creates a comprehensive set of features for analysis.

## 4. Methods
Two models are employed:
1. **Logistic Regression:**
   - Selected for its ability to assign weight to different variables.
   - Utilizes L1 loss function for feature selection.
   - Data split into 80/20 for training and validation.
   
2. **Random Forest Classifier (RFC):**
   - Good at finding complex relationships between features.
   - Parameters tuned to prevent overfitting using cross-validation with a randomized search algorithm.

## 5. Results
Logistic Regression outperforms RFC, achieving 94% accuracy on validation data. Feature importance analysis indicates the effectiveness of L1 regularization. The final logistic regression model demonstrates robust performance.

## 6. Conclusions
The project successfully establishes relationships between linguistic data and the truth value of articles. However, the model's limitations include homogeneity of datasets, English language restriction, and potential bias. The model's application needs refinement, incorporating contextual features for real-world adaptability.

## 7. Recommendations for Improvement
- Consider diverse datasets for broader validation.
- Enhance the model to accommodate non-English news and varied sources.
- Integrate context-specific features for practical applications, such as social media post truth-value prediction.

*Note: The detailed project report includes specific methodologies, code references, and visualizations.*
