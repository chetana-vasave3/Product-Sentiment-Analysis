

# Electronics Products Review Analysis



## Index

 - Objective 
 - Data Understanding
 - Dataset Description
 - Exploratory Data Analysis
 - Conclusion




## Objective

The reviews provide valuable insights into customers' experiences, opinions, and satisfaction levels with the respective products. This dataset can be used for various purposes, such as sentiment analysis, customer feedback analysis, product recommendation systems, or building predictive models to estimate product ratings or review sentiment.

## Data Understanding

The dataset includes reviews from different product categories, such as electronics, drugstore, wireless, shoes, home, kitchen, luggage, office_product, pc, toy, industrial_supplies, furniture, pet_products, and sports and customers have provided feedback on that products. The dataset includes several columns that provide information about each review, such as the review ID, product ID, reviewer ID, star rating, review body, review title, language, and product category.


##  Dataset Description

•	review_id: A unique identifier for each review.
•	product_id: A unique identifier for each product.
•	reviewer_id: A unique identifier for each reviewer.
•	stars: The rating given by the reviewer, ranging from 1 to 5 stars.
•	review_body: The main content of the review, where the reviewer shares their opinion or experience.
•	review_title: A summarized title or heading for the review.
•	language: The language in which the review is written.
•	product_category: The category or type of the reviewed product.







##  Exploratory Data Analysis

•	Product Performance: Analyzing the star ratings and review bodies can provide insights into how customers perceive the products.

•	Customer Satisfaction: By analyzing the review sentiments and feedback, stakeholders can gain an understanding of overall customer satisfaction levels.


•	Analyzing the review titles and bodies can provide insights into specific features, functionalities, or aspects of the products that customers value or desire. 

•	Product Categories: By examining the distribution of reviews across different product categories, stakeholders can identify which categories receive more customer attention or engagement. This information can guide decision-making regarding product development, marketing strategies, and resource allocation.


•	Language and Localization: Analyzing the language distribution in the dataset can help stakeholders identify the primary languages used by customers. This information can be utilized for localization efforts, such as translating product descriptions, improving customer support in specific languages, or targeting specific markets.






##Conclusion

•	Stakeholders can identify the products with consistently positive reviews and those with negative feedback. This information can help them understand which products are well-received by customers and which may need improvements.

•	They can identify common issues or concerns raised by customers and take necessary actions to address them. Additionally, they can identify highly satisfied customers and leverage their positive experiences for marketing and brand building.

•	Product Quality and Reliability: Stakeholders can investigate the root causes to improve product quality and reliability. This can lead to better customer experiences and enhanced reputation. Customer Preferences and Needs: Stakeholders can use this information to identify customer preferences and adapt their product offerings or develop new products that align with customer needs.


•	Overall, the insights and conclusions drawn from this project can help stakeholders make data-driven decisions to enhance product quality, customer satisfaction, and business performance. They can prioritize product improvements, optimize marketing strategies, and tailor their offerings to meet customer preferences and needs, ultimately leading to better customer experiences and business success.

## Index

 - Objective 
 - Data Understanding
 - Dataset Descriprition
 - Exploratory Data Analysis
 - Conclusion




## Objective

Analyze customer spending patterns, payment habits, credit utilization, and other credit card-related metrics. Understanding these patterns and behaviors can help identify customer segments, predict default rates, or develop targeted marketing strategies, among other applications in the credit card industry.

## Data Understanding
The dataset appears to be related to credit card usage and customer behavior. It contains various features that describe the financial attributes and behaviors of customers..

 
 
##  Dataset Descriprition

#### Take a first look of our data
- CUST_ID: Unique identifier for each customer.
- BALANCE: The outstanding balance amount on the credit card.
- BALANCE_FREQUENCY: Frequency of balance updates, measured as the ratio of the number of times the balance was updated to the total number of transactions.
- PURCHASES: Total amount of purchases made on the credit card.
- ONEOFF_PURCHASES: Total amount of one-time purchases (not installments) made on the credit card.
- INSTALLMENTS_PURCHASES: Total amount of purchases made in installments on the credit card.
- CASH_ADVANCE: Total amount of cash advances taken from the credit card.
- PURCHASES_FREQUENCY: Frequency of purchases, measured as the ratio of the number of purchase transactions to the total number of transactions.
- ONEOFF_PURCHASES_FREQUENCY: Frequency of one-time purchases, measured as the ratio of the number of one-time purchase transactions to the total number of transactions.
- PURCHASES_INSTALLMENTS_FREQUENCY: Frequency of purchases in installments, measured as the ratio of the number of installment purchase transactions to the total number of transactions.
- CASH_ADVANCE_FREQUENCY: Frequency of cash advances, measured as the ratio of the number of cash advance transactions to the total number of transactions.
- CASH_ADVANCE_TRX: Number of cash advance transactions.
- PURCHASES_TRX: Number of purchase transactions.
- CREDIT_LIMIT: Credit limit on the credit card.
- PAYMENTS: Total amount of payments made.
- MINIMUM_PAYMENTS: Minimum amount of payments due.
- PRC_FULL_PAYMENT: Percentage of the full payment made on the credit card.
- TENURE: Number of months the customer has been a cardholder.

## Exploratory Data Analysis

 We checked for duplicate values, Missing values and Outliers in the dataset . We removes all the duplicate values from the daatset and filled missing values by using some statistical methods like mean, median and mode.Removed unwanted Columns like customer Id.we did univariate and bivariate anlysis on Numerical as well as categorical data.


 ## Kmeans Clustering algorithm


 We have used Kmens clustering algorithm to make clusters of the similar data points so that we can separate the customers segments..we made 4 clusters.the main task here was to find the appropriate value of k that is no. of clusters.. so we used Elbow method to find the no. of clusters.before that we used PCA algorithm to convert the datframe into 2D form so that the visualiztion will be easy for us.
 

 ## Training and Testing the model accuracy using Decision Tree Algorithm
 

 We used Decision Tree algorithm to check the model performance ..we devided the data into training and test sets.fit the data into Decision Tree model and calculate the performace with the help of the confusion matrix .. we used Performance metrics like precision, Recall and F1 score.finaly we got the accuracy above 90%.. After that we saved the model with the help of the joblib module.

#### joblib module: 
The joblib module is a part of the scikit-learn library and is used for efficiently storing and loading Python objects, such as machine learning models, to disk. It provides utilities for serializing Python objects into a binary format and deserializing them back into memory.
 

 After saving the model we created web application with the help of the software team in our orgnization and for that we used stremlit web frame wrok.

#### stremlit web framework

Streamlit is an open-source Python library used for building interactive web applications. It allows you to create data-driven applications and easily deploy them for others to access and interact with through a web browser. Streamlit simplifies the process of creating web interfaces for your Python scripts, making it ideal for prototyping, data exploration, and building interactive visualizations.

 #### To get started with Streamlit, you can follow these general steps:

- Install Streamlit: You can install Streamlit using pip, Anaconda, or any other preferred method.

- Create a Python script: Write your Python code that generates the content and functionality of your application. This can include data loading, preprocessing, visualization, and interaction logic.

- Use Streamlit API: Import the Streamlit library and use its API functions to define the elements and behavior of your application. You can add widgets, charts, text, and other interactive components.

- Run the Streamlit app: Execute the Streamlit command in your terminal or command prompt, pointing it to your Python script. Streamlit will start a local server and open your application in a web browser.

- Interact with the app: You can now interact with your Streamlit application through the web interface. Any changes you make to your Python script will automatically update the application in real-time.



## Conclusion

- We made the clusters of customers
- We created the model which predicts the customer cluster with the help of the selected features.
- In the web app we have to fill feature values after that model will tell us in which cluster that customer is belong to.