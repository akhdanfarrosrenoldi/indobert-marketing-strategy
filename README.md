# Sentiment Analysis using IndoBERT as a Marketing Strategy
## Research Flow
![Screenshot 2025-03-13 013112](https://github.com/user-attachments/assets/396e9ae1-3a6e-4379-9017-43a0ceee5e54) 

This diagram illustrates the workflow in sentiment analysis using the IndoBERT model.
- Data Crawling - Data is collected and stored in the form of datasets.
- Pre-processing & Labeling - Data is processed with techniques such as text cleaning, case folding, text normalisation, tokenisation, stopwords removal, and utilisation of InSet Lexicon to provide sentiment labels.
- Model Train & Test - IndoBERT model is utilised and fine-tuned to improve the accuracy of sentiment analysis.
- Model Evaluation - Model results were evaluated using Confusion Matrix to measure classification performance.
- Implementation & Results - Analysis results are visualised to further understand model performance.


## Dataset
Data that has been crawled previously is preprocessed so that it is ready to be processed in the algorithm used, there are 6 stages of data preprocessing used in this research.

![image](https://github.com/user-attachments/assets/7ece13f0-7118-477f-a2b5-dbc293e4819a)

this is the content of the tokopedia.csv dataset

## Pre-processing
### Text Cleaning
Remove unnecessary characters or symbols, such as punctuation marks, numbers, or special characters, to improve the quality of text data.

![image](https://github.com/user-attachments/assets/3e9c5963-ec2d-4099-bd60-b69908d0876b)

### Case Folding
Convert all letters to lowercase so that there is no distinction between uppercase and lowercase letters (for example, ‘Product’ and ‘product’ are considered the same).

![image](https://github.com/user-attachments/assets/ef70d96b-8f52-4adb-8682-0bef6a4c8338)

### Text Normalization
Text normalisation is used to convert nonstandard or slang words into standard word forms according to the Indonesian formal language dictionary.

![image](https://github.com/user-attachments/assets/e0c20215-9ea2-469c-930e-61d609b7b6ce)

### Tokenization
Tokenising is used to separate a sentence into tokens.

![image](https://github.com/user-attachments/assets/0f1677cb-8069-41c8-8578-ec14298efa95)

### Stopwords Removal
Stopwords removal is used to remove common words (stopwords) that do not provide significant information value.

![image](https://github.com/user-attachments/assets/d666267f-6be3-44a1-958f-4cc8df4542b1)

## Labeling InSet Lexicon
InSet Lexicon is a collection of words to give a specific label, such as positive, negative, or neutral.

![image](https://github.com/user-attachments/assets/88810059-5ebe-4119-afbf-7daf3955cd34)

## Train 
### Classification report 
From the classification model with three classes of positive, neutral, and negative. The model performed well with an overall accuracy of 0.89, which means that 89% of all model predictions were correct. In terms of precision, the model showed the highest value in the negative class (0.94), followed by neutral (0.83) and positive (0.77), which indicates that the model is very accurate in predicting the negative class. For recall, the model did well in detecting the positive and negative classes, with values of 0.86 and 0.94 respectively, but slightly less well in detecting the neutral class (0.71). F1-score, which combines precision and recall, shows good results for the negative (0.94) and positive (0.81) classes, but there is a slight decrease in the neutral class (0.76). Macro average and weighted average showed average f1-score values of 0.84 and 0.89 respectively, indicating that despite the imbalance in class distribution, the model still performed well on the more dominant data. Overall, although there is room for improvement in detecting the neutral class, the model managed to provide excellent results, especially in predicting the negative class.

![image](https://github.com/user-attachments/assets/5c94c061-d94e-4b82-b42d-d214fa549434)
### Loss Curve
Loss graph depicting the development of training loss, validation loss, and test loss over five training epochs of the fine-tuned IndoBERT model. In this graph, the training loss (blue line) decreases consistently from epoch 1 to epoch 5, indicating that the model is getting better at learning the training data over time. The validation loss (green line) also decreases, albeit slower than the training loss, indicating that the model is getting better at generalising patterns in the data that were not seen before. Meanwhile, the test loss (red line) follows a similar pattern to the validation loss, albeit with slight fluctuations, indicating that the model can make better predictions on the test data, but there is a slight instability compared to the training data. The consistent decrease in these three types of loss indicates that the fine-tuned IndoBERT model shows good progress in learning patterns from the data, as well as the ability to generalise to data not seen during training.

![image](https://github.com/user-attachments/assets/ca07e15d-81eb-4441-aeef-9cb2b641f6fb)

## Evaluation model
### Confusion matrix 
For the classification model with three classes positive, neutral, and negative. Based on this matrix, the model performed best in classifying the negative class, with 638 negative data correctly predicted as negative. However, there were some misclassifications in the positive and neutral classes. A total of 21 positive data were incorrectly predicted as negative, and there were 6 positive data that were predicted as neutral. On the other hand, the model also misclassified some neutral data, with 19 neutral data incorrectly predicted as negative and 21 neutral data predicted as positive. Despite this, the model performed well in identifying the negative class, but these errors show that the model needs to be improved, especially in distinguishing between positive and neutral.

![image](https://github.com/user-attachments/assets/0b720fa2-584c-491b-8d97-69bff6bf6687)

## Implementation and Visualisation of Results
### Display 5 words that present Positive sentiment 
![image](https://github.com/user-attachments/assets/da2f29eb-9717-4059-848a-87a86ca0fe70)
![image](https://github.com/user-attachments/assets/20ef9ad0-7183-49e7-ae0b-3d8fcd892376)

‘Showing 5 words that present Positive sentiment’ shows a word cloud depicting the words that appear most frequently in reviews with positive and negative sentiment. In the first image, which is themed around positive sentiment, words such as ‘good’, ‘fast’ appear at a larger size, indicating that customers who leave positive reviews use those words more often to describe the products or services they praise.

### Display 5 words that present Negative sentiment 
![image](https://github.com/user-attachments/assets/98186553-ac5f-45e3-95b1-aa58339cc855)
![image](https://github.com/user-attachments/assets/6b69de95-347f-4af4-acd4-1d53f19242ab)

‘Showing 5 words that present Negative sentiment’ shows words such as “goods” “defective,” “disappointing” as the words that appear the most. This shows that dissatisfied customers tend to use these words to express their disappointment with the product or service.

### Displaying Marketing Strategy Suggestions
![image](https://github.com/user-attachments/assets/382b0590-fa5e-46cc-8391-f02981c5d5f5)


‘Displaying marketing strategies’ shows a table containing review data, which includes columns such as merge_text (review content), sentiment (review sentiment), and marketing_strategy (suggested marketing strategies based on sentiment and keyword analysis). This table includes reviews with negative, positive, and neutral sentiments, and suggested marketing strategies such as apologising and returning items for negative sentiments, giving discounts or coupons for positive sentiments, and saying thank you for neutral reviews. This table helps to formulate marketing strategies that match the sentiments present in customer reviews. Overall, these figures provide useful insights into how sentiment in reviews can be used to design more effective marketing strategies.

## Conclusion
The model showed a significant improvement in performance, with the accuracy value reaching 0.89. This reflects the model's better ability to understand and analyse product review data. 3. Marketing strategies based on the analysis results. Based on the findings from the word cloud and review table, it can be concluded that customers with positive sentiments tend to rate products or services favourably, using words such as ‘fast,’ ‘satisfied,’ and ‘steady,’ indicating high satisfaction with the quality and service provided. Therefore, companies can utilise these positive reviews to offer discounts or coupons as a form of appreciation or incentive for future purchases. In contrast, customers with negative sentiments tend to use words such as ‘defective,’ ‘disappointing,’ and ‘broken,’ which indicate dissatisfaction with the quality of the product or service. For this reason, the suggested marketing strategy is to apologise and return goods as a step to improve customer relations and maintain the company's reputation.









