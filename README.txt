ANLY580 Project 2
Group: InsightX 
Group Member: Beixuan Jia (bj256@georgetown.edu)
              Zhenkun Wang(zw206@georgetown.edu)
              Qian Yi (qy55@georgetown.edu) 
              Jingyu Zhang (jz649@georgetown.edu)

Directed by Professor Marck Vaisman

##########################################################################################
(1)Introduction of the files in this zip: 

Womens Clothing E-Commerce Reviews.csv: This is the original raw data set. 

Not_Cleaned.txt:This is the in-between file during data cleaning process. 
                In this file, each row has one-paragraph reviews. 

Cleaned.txt:This is the cleaned dataset ready for modeling process. 
Cleaned.csv:This is the cleaned dataset ready for modeling process. 

1star.jpg: This is the word cloud visualization for all the 1-star reviews.
5star.jpg: This is the word cloud visualization for all the 5-star reviews.
wordcloud1.png: This is the word cloud visualization for all the reviews. 
Word_Frequency.png: This is the visualization for word frequency of all review text. 

eda1.jpg: This graph was drawn by Tableau and will be inserted in jupytor notebook
eda2.jpg: This graph was drawn by Tableau and will be inserted in jupytor notebook

***important: 
580_project2_insightx.ipynb：All the python code and explanation, report are in this file. 

##########################################################################################
(2)Understanding the data (Column name: description)
Womens Clothing E-Commerce Reviews.csv:
1.id: the id of the review (notice: id is NOT the index number) 
2.Clothing ID: each product has unique clothing ID, same Clothing ID means same product 
3.Age: the age of this customer 
4.Title: (Optional) the title of the text review 
5.Rating: the rating of this review (range from 1 to 5)
6.Recommend: recommend or not: (1:recommend, 0:not recommend)
7.Positive Feedback Count: how many people clicked the "helpful" button for this review
8.Division Name: the division of this product 
9.Department:the department of this product 
10.Class Name: the class of this product 


Not_Cleaned.txt: 
1.index:the index of the dataset
2.Rating: the rating of this review (range from 1 to 5)
3.Recommend: recommend or not (1:recommend, 0:not recommend)

Cleaned.txt: 
1.index:the index of the dataset
2.Rating: the rating of this review (range from 1 to 5)
3.Recommend: recommend or not (1:recommend, 0:not recommend)

##########################################################################################
(3)Project analysis steps: 
1.Use tableau to draw visualization graphs to develop basic understanding about the data.
  This step has 2 output for visualization. 
2.Data Cleaning.
  This step has 1 graph output about word frequency.  
3.Apply word cloud to explore the word frequency and compare the 1-star vs. 5-star reviews 
  This step has 3 output for word cloud visualization. 
4.Analyze positive feedback counts, set assumptions and compare the results with assumptions.
  This step has 1 box-plot and 7 pie charts output.  
5.Build Multinomial Naive Bayes models and Logistic Regression models for "recommend or not". This step has 2 output of confusion matrix.
6.Build Multinomial Naive Bayes models and Logistic Regression models for star-ratings
  This step has 2 output of confusion matrix.
7.Integrate and draw conclusion, combine data-driven results with application-side business insights 

##########################################################################################
(4)Conclusion: 

According to the analysis, we explored top 3 clothing categories that customers may provide insights for online shopping website to generate marketing strategies and promotion plans. 

Among all the clothing categories, the Department of Jackets has the largest proportion of 5-star ratings(61.6%) while the Department of Trends has the least proportion of 5-star ratings(43.7%). 

While comparing the 1-star wordcloud and 5-star wordcloud, the major customers' complains were detected. The online selling website could provide more detailed instructions for customers about "how to find the fit sizes".

For exploratory of positive feedback counts analysis, whether a review will be recognized as "helpful" actually depends more on how much useful and detailed information provided in the reviews.

For the modeling section, For predicting whether a customer will recommend the product, the models achieved 90% and 93% accuracy. For predicting how many star will a customer give, the models reached accuracy of 72% and 76%, respectively. 

These models and findings are meaningful because they could help the online business predict the overall product performance and explore customers' unmet needs, which will further help the business for long-term development while building positive brand images.

##########################################################################################
（5）Models for predicting “recommend or not" 
Multinomial Naive Bayes: 
                  precision    recall  f1-score   support

0: Not Recommend       0.72      0.76      0.74      3665
    1: Recommend       0.95      0.93      0.94     16711

       micro avg       0.90      0.90      0.90     20376
       macro avg       0.83      0.85      0.84     20376
    weighted avg       0.91      0.90      0.90     20376

0.9033667059285434

Logistic Regression: 

                  precision    recall  f1-score   support

0: Not Recommend       0.87      0.72      0.79      3665
    1: Recommend       0.94      0.98      0.96     16711

       micro avg       0.93      0.93      0.93     20376
       macro avg       0.90      0.85      0.87     20376
    weighted avg       0.93      0.93      0.93     20376

0.9296230859835101

（6）Models for predicting star rating

Multinomial Naive Bayes: 

              precision    recall  f1-score   support

           1       0.78      0.36      0.49       659
           2       0.71      0.38      0.49      1225
           3       0.55      0.62      0.58      2238
           4       0.56      0.50      0.53      3903
           5       0.80      0.89      0.84     10087

   micro avg       0.72      0.72      0.72     18112
   macro avg       0.68      0.55      0.59     18112
weighted avg       0.71      0.72      0.71     18112

0.7180874558303887

Logistic Regression: 

              precision    recall  f1-score   support

           1       0.88      0.58      0.70       659
           2       0.75      0.56      0.64      1225
           3       0.69      0.63      0.66      2238
           4       0.67      0.51      0.58      3903
           5       0.81      0.94      0.87     10087

   micro avg       0.77      0.77      0.77     18112
   macro avg       0.76      0.64      0.69     18112
weighted avg       0.76      0.77      0.76     18112

0.7707045053003534

##########################################################################################
(6) Contact
We have comments and explanation in jupytor notebook for understanding the process of our project. If you have any questions or concerns about this project, we can be contacted at 
qy55@georgetown.edu 
jz649@georgetown.edu
zw206@georgetown.edu
bj256@georgetown.edu


