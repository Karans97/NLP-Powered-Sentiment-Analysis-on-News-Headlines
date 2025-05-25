# NLP-Powered-Sentiment-Analysis-on-News-Headlines

1. Introduction
This project leverages Natural Language Processing (NLP) to classify news headlines into three sentiment categories: positive, neutral, and negative. The primary goal is to automate the understanding of news tone, which can be valuable for investors, analysts, and researchers tracking public sentiment and market trends.

2. Data Overview
The dataset consists of news headlines and their metadata, including the date and a brief description. The main columns are:

publishedAt: Date and time of publication

title: News headline

description: Short summary of the article

Sample Data:

publishedAt	title	sentiment
2025-05-23T22:02:30Z	Former SafeMoon CEO Braden Karony convicted...	neutral
2025-05-23T22:01:32Z	Khosla Ventures among VCs experimenting with AI...	positive
2025-05-23T22:00:33Z	Lawyer Who Sued Federal Health Agency...	neutral
2025-05-23T22:00:27Z	CME Group Bets Big On XRP...	neutral
2025-05-23T22:00:27Z	Ethereum Holds Above Key Prices...	positive
3. Methodology
a. Data Preprocessing
Headlines are cleaned by removing special characters, converting text to lowercase, and eliminating stopwords.

Stemming is applied to reduce words to their root forms.

The cleaned text is vectorized using CountVectorizer to convert it into a numerical format suitable for machine learning models.

b. Model Training
The dataset is split into training and testing sets (80%/20%).

A Logistic Regression classifier is trained on the vectorized data.

Additional models like Gradient Boosting are considered for comparison.

c. Evaluation
The model's performance is measured using accuracy on the test set.

In the sample run, Logistic Regression achieved an accuracy of 75.7%, indicating effective sentiment classification.

4. Results Analysis
a. Sentiment Distribution
In the sample results, most headlines are classified as neutral or positive.

For example:

Legal or factual headlines (e.g., "Former SafeMoon CEO Braden Karony convicted...") are labeled neutral.

Headlines about investment and innovation (e.g., "Khosla Ventures among VCs experimenting with AI...") are labeled positive.

No negative headlines appear in the top results, which may reflect the dataset's content or the model's threshold settings.

b. Model Performance
The accuracy of 75.7% suggests the model is reliable for this task, though there is room for improvement.

The class distribution in the training data shows a predominance of neutral samples, which may influence the model's predictions.

c. Insights
The model effectively distinguishes between neutral reporting and positive developments.

The lack of negative predictions in the sample could indicate a need for more balanced data or refined thresholds.

5. Conclusion
This project demonstrates a robust workflow for automated sentiment analysis of news headlines. The model performs well in classifying headlines as positive or neutral, providing a valuable tool for summarizing news sentiment at scale. The approach can be further enhanced by:

Incorporating more negative samples for better class balance,

Experimenting with advanced models (e.g., transformers),

And visualizing sentiment trends over time.

