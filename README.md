# Customer feedback analysis for amazon logistics services

As a regular Amazon user, I know how crucial their logistics services are to customer experience. This project focuses on analyzing customer feedback to understand how people feel about these services—whether it's positive, negative, or neutral. By building a sentiment analysis model, I aim to pinpoint strengths and areas for improvement, helping Amazon enhance its delivery experience.

**Dataset Overview**

I used a dataset from Kaggle containing customer reviews from various regions where Amazon operates. To keep the analysis focused, I filtered it to North American countries, giving me a familiar perspective on customer experiences. With over 10,000 reviews, this dataset offers a solid foundation to evaluate the quality and effectiveness of Amazon's logistics services based on real customer feedback."

**ETL Process**

As part of the project, I followed an ETL (Extract, Transform, Load) approach to prepare the dataset for analysis:

Extract: The dataset, a CSV file, contained customer reviews from various regions, with fields such as Country, Review Date, Rating, Review Title, and Review Text.
Transform: This step took the most time, as I focused on ensuring the data's quality and consistency:
- Data Cleaning: Removed null values and reformatted fields where necessary.
- Duplicate Removal: Eliminated redundant records to maintain the integrity of the analysis.
- Handling Missing Values: Applied appropriate techniques, such as filling defaults or dropping incomplete records, to address gaps in the data.
- Text Preprocessing: For the review texts, I carried out tokenization, stopword removal, and standardization to ensure consistency, especially for dates and numerical values.
Load: Finally, I loaded the cleaned and transformed data into a PostgreSQL database, setting up a structured foundation for further analysis.
This structured ETL process was crucial in ensuring the dataset was ready for sentiment analysis and model development

**Sentiment Analysis Model**

In this project, I developed a sentiment analysis model to classify customer reviews into positive, negative, or neutral categories. Here's how I approached it:

Model Selection: I chose Multinomial Naive Bayes and Logistic Regression due to their effectiveness in text classification tasks:
- Multinomial Naive Bayes: Known for its speed and efficiency, especially when dealing with text data.
- Logistic Regression: Provides robust performance and interpretable results, which is valuable for understanding the impact of different features.
Preprocessing:
- Vectorization: I utilized CountVectorizer to convert the textual data into numerical format based on word frequency, making it suitable for model processing.
- Data Balancing (SMOTE): To ensure the dataset was balanced and to prevent model bias, I applied techniques like oversampling using SMOTE. This helped achieve more accurate and reliable predictions.
- Training and Testing: The dataset was split into training and testing sets, allowing me to evaluate the models' performance effectively and fine-tune them for better results.

**Conclusion**

The sentiment analysis conducted showed promising results in classifying Amazon customer reviews. Logistic Regression emerged as the stronger performer, achieving an accuracy of 89.09%, along with high precision (89.32%) and an F1-score of 89.12%. Its confusion matrix revealed fewer misclassifications, demonstrating consistency across all sentiment categories with minimal false positives and false negatives.

On the other hand, Multinomial Naive Bayes achieved an accuracy of 83.89% and a precision of 84.02%. However, it showed more misclassifications, particularly with higher false negatives, where some positive or neutral reviews were incorrectly labeled.

In conclusion, while both models were effective, Logistic Regression proved to be more reliable for this dataset, offering a more accurate and consistent classification of customer sentiments."

