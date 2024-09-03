# Medical Drug Recommendation System

## Overview

This project focuses on developing a recommendation system for medical drugs based on user reviews and other relevant factors. The system utilizes a combination of machine learning (ML), deep learning (DL), and transfer learning techniques, specifically employing Generative Pre-Trained Transformer (GPT) models. The main goal is to predict the sentiment of drug reviews and generate drug recommendations that can assist in improving pharmacotherapy and patient safety.

## Project Structure

The project is divided into several key sections:

1. **Data Preprocessing**
2. **Data Visualization**
3. **Machine Learning and Deep Learning Models**
4. **Transfer Learning using GPT**
5. **Final Drug Recommendations**

## 1. Data Preprocessing

### Dataset Overview

The dataset used in this project contains information about drugs, medical conditions, and user reviews. The key attributes include:

- **drugName**: Name of the drug.
- **condition**: Name of the medical condition.
- **review**: Patient's review text.
- **rating**: Numerical rating of the drug (1-10).
- **date**: Date of the review.
- **usefulCount**: Number of users who found the review helpful.

### Initial Data Reduction

Given the large size of the dataset, an initial reduction was performed to retain only those drugs that appeared at least 400 times in the dataset. Reviews were also classified into positive and negative sentiments based on the rating, with ratings above 5 considered positive.

### Text Preprocessing

The text reviews were preprocessed through several steps:

- **HTML Tag Removal**: Removed unwanted HTML tags from the reviews.
- **Lemmatization**: Converted words to their base forms.
- **Stop Word Removal**: Eliminated common stop words to focus on meaningful content.

This preprocessing ensured the data was clean and ready for analysis.

## 2. Data Visualization

Various visualizations were created to better understand the dataset:

- **Top 20 Drugs by Condition**: Showed the most common medical conditions and the drugs used to treat them.
- **Word Clouds**: Generated separate word clouds for positive and negative reviews to highlight the most frequently mentioned terms.
- **N-Gram Analysis**: Focused on 4-gram analysis to distinguish between positive and negative reviews.

These visualizations provided insights into the distribution and patterns within the data.

## 3. Machine Learning and Deep Learning Models

### Linear Regression

A linear regression model was applied to predict the sentiment of reviews based on the preprocessed text data. The predictions were stored in the `lr_pred` column.

### Deep Neural Network

A deep neural network was designed to capture more complex patterns in the text data. Despite some overfitting, the model provided valuable insights into sentiment prediction. The predictions were stored in the `deep_pred` column.

### Sentiment Analysis with Lexical Resources

A sentiment analysis was conducted using the Harvard General Inquirer, a lexical resource developed by Harvard University. This analysis identified positive and negative words in the reviews, with the results contributing to the overall sentiment score.

### Combining Predictions

The final recommendation formula combined the outputs of the linear regression, deep neural network, and sentiment analysis to generate a comprehensive drug recommendation.

## 4. Transfer Learning using GPT

### Model Selection

The project implemented transfer learning using the GPT-2 model. Given the size and complexity of the dataset, a reduced dataset (30% of the original) was used to facilitate this process.

### GPT-2 Fine-Tuning

The GPT-2 model was fine-tuned to better understand the sentiment and semantic content of the reviews. This involved tokenization, embedding adjustment, and model training to adapt the GPT-2 architecture for the specific task.

### Final Model Output

The fine-tuned GPT-2 model was combined with the previous models' outputs to enhance the accuracy and relevance of the drug recommendations.

## 5. Final Drug Recommendations

The final stage of the project involved generating the drug recommendations based on the integrated model outputs. The recommendations were designed to be both accurate and reflective of the sentiments expressed in user reviews.

## Conclusion

This project demonstrates the potential of artificial intelligence in improving medical drug recommendations. By combining traditional machine learning, deep learning, and cutting-edge transfer learning techniques, the system provides valuable insights into drug efficacy based on user experiences. While the model shows promising results, further research could focus on personalization and the inclusion of additional factors to enhance recommendation accuracy.

---

## Acknowledgments

The techniques and methodologies used are based on the latest advancements in machine learning and artificial intelligence.

## References

1. Y. Z. W. D. S. J. P. Qiang Yang, *Transfer Learning*, Springer, 2022.
2. Y. C. Jindong Wang, *Introduction to Transfer Learning - Algorithms and Practice*, Springer, 2022.
3. A. Mehra, *A Deep Dive into GPT Models: Evolution & Performance Comparison*, 2023.
4. Alec Radford, et al., *Language Models are Unsupervised Multitask Learners*, 2020.

--- 

This `README.md` provides a comprehensive overview of the project's objectives, methodologies, and outcomes. Adjustments can be made based on specific details or additional sections if necessary.
