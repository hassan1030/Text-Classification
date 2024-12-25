# Sentiment Analysis: Comparing Deep Learning and Traditional NLP Models

## Project Scope
This project explores sentiment analysis on a Twitter dataset using two approaches:
1. A **deep learning model** (AWD_LSTM fine-tuned with ULMFiT).
2. A **traditional NLP model** (Naive Bayes classifier with CountVectorizer).

The objective is to compare model performance, development complexity, and identify practical recommendations for deploying sentiment analysis models in real-world business contexts.

## Dataset
- **Source**: Twitter dataset (sentiment labeled as positive or negative).
- **Size**: A sample of 1,000 rows for efficient processing.
- **Key Variables**:
  - `Text`: The tweet content.
  - `Target`: Sentiment label (`positive` or `negative`).

## Analysis
### Workflow:
1. **Data Cleaning and Preparation**:
   - Filtered necessary columns and handled missing values.
   - Mapped `Target` values to `positive` and `negative` for clarity.
2. **Data Splitting**:
   - 80% training set (800 rows), 20% validation set (200 rows).
3. **Deep Learning Model (AWD_LSTM + ULMFiT)**:
   - Fine-tuned a pre-trained AWD_LSTM language model for binary classification.
   - Accuracy: **79.4%** on the validation set.
4. **Traditional NLP Model (Naive Bayes)**:
   - Trained using `CountVectorizer` with stop words for feature extraction.
   - Accuracy: **76%** on the validation set.

### Results:
- The deep learning model outperformed the Naive Bayes model by 3.4% in accuracy.
- While the deep learning model required more development effort, it demonstrated better performance in capturing nuanced text patterns.

## Business Applications
This sentiment analysis can be applied to:
1. Analyzing customer feedback for products or services.
2. Monitoring brand reputation in real-time.
3. Assessing public opinion toward marketing campaigns.

## Recommendations
### When to Choose Deep Learning:
- Use when **higher accuracy** is crucial.
- Suitable for complex tasks requiring nuanced understanding of text.

### When to Choose Traditional NLP:
- Use when **speed and simplicity** are essential.
- Best for resource-constrained environments or simpler tasks.

## Future Considerations
1. **Data Scaling**:
   - Expanding the dataset size could improve model generalization.
2. **Hyperparameter Tuning**:
   - Further tuning of learning rates, dropout rates, and number of layers may enhance deep learning model performance.
3. **Productization**:
   - For practical use, integrate the model into a real-time feedback system for customer sentiment analysis.

## How to Use
1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/text-classification.git
