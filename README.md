# Capstone-Project-4-Zomato-Restaurant-Clustering-And-Sentiment-Analysis
![cover](https://user-images.githubusercontent.com/66788381/230784282-9cf11484-bb93-406a-a4e8-58544066267b.png)


## Project Summary
Zomato is an Indian restaurant aggregator and food delivery start-up founded by Deepinder Goyal and Pankaj Chaddah in 2008. Zomato provides information, menus and user-reviews of restaurants, and also has food delivery options from partner restaurants in select cities.

The Zomato Restaurant Clustering and Sentiment Analysis Project is a machine learning project that involves clustering restaurants based on their features and performing sentiment analysis on customer reviews. The project uses unsupervised learning techniques to group similar restaurants and identifies patterns and similarities among them. Additionally, sentiment analysis is performed on the reviews of each restaurant to classify them as positive, negative, or neutral. The insights gained from this project can be useful for restaurant owners to understand customer preferences and improve their services accordingly. The Project focuses on Customers and Company, you have to analyze the sentiments of the reviews given by the customer in the data and make some useful conclusions in the form of Visualizations. Also, cluster the zomato restaurants into different segments: The data is visualized as it becomes easy to analyses data at instant The Analysis also solves some of the business cases that can directly help the customers finding the best restaurant in their locality and for the company to grow up and work on the fields, they are currently lagging in. This could help in clustering the restaurants into segments. Also, the data has valuable information around cuisine and costing which can be used in cost vs. benefit analysis Data could be used for sentiment analysis. Also, the metadata of reviewers can be used for identifying the critics in the industry.

## Problem Statement
The restaurant industry is highly competitive and dynamic, with new restaurants constantly entering the market. Restaurant owners face the challenge of understanding customer preferences and meeting their expectations to stay relevant in the market. In this context, there is a need for a data-driven approach that can help restaurant owners gain insights into customer preferences and improve their services accordingly. The Zomato Restaurant Clustering and Sentiment Analysis Project aims to address this problem by leveraging machine learning techniques to cluster restaurants based on their features and perform sentiment analysis on customer reviews to identify areas of improvement.

##  Understanding The Datasets
The project begins by understanding the variables in the restaurant and review data frames. The restaurant data frame has 105 rows and 6 columns, with information about restaurant names, links, cost, collections, cuisines, and timings. The review data frame has 10000 rows and 7 columns, with information about the restaurant reviews, such as restaurant name, reviewer name, review, rating, metadata, time, and pictures. The data wrangling process is then performed to find meaningful insights from the data.

**Restaurant Data**

---


|**Fields** | **Description**|
|-----------|--------------|
Name | Name of Restaurants
Links | URL Links of Restaurants
Cost | Per person estimated cost of dining
Collections |Tagging of Restaurants with respect to Zomato categories
Cuisines|Cuisines served by restaurants
Timings|Restaurant timings

---


**Review Data**


---


|**Fields** | **Description**|
|-----------|--------------|
Reviewer|Name of the reviewer
review|Review text
Rating|Rating provided
MetaData|Reviewer metadats-No of reviews and followers
Time|Date and Time of Review
Pictures| Number of pictures posted with review


## Data Wrangling & Data Preprocessing
### Overall Insights From Zomato Restaurant Dataset

* This dataset has a shape of (105, 6) with 54 null values in ‘Collection’ column and 1 null values in ‘Timing’ column.
* There are 44 different/unique Cuisines present in our dataset.
* There are 33 restaurants with 3 different cuisines, 26 restaurants with 2 different cuisines, 21 restaurants with 4 different cuisines, 12 restaurants with 5 different cuisines, 12 restaurants with only 1 cuisine and only 1 restaurant with 6 different cuisines.
* North Indian is the mostly available food on 61 number of different restaurants followed by Chinese and Continental food which is available on 43 and 21 restaurants. It means mostly people demands for this food as compared to other food like pizza, juices, malaysian food which is available on less number of restaurant.
* We found that, Beyond Flavours restaurant has a maximum number of different type of cuisine followed by Shah Ghouse Hotel & Restaurant. While Republic Of Noodles - Lemon Tree Hotel has only 4 types of cuisine available.
* We also found that North Indian, Chinese, Continental food are more in demand in Hyderabad city where there are 63 restaurants with Indian cuisine is available and 43 Restaurants with Chinese cuisine is available..
* Collage - Hyatt Hyderabad Gachibowli and Feast - Sheraton Hyderabad Hotel are the two most expensive restaurants with the cost of 2800 and 2500 rupees which is a average per person estimated cost of dining.
* Mohammedia Shawarma, Amul and Asian Meal Box Hotel are the most affordable Restaurants where the cost of 150 and 200 rupees which is a average per person estimated cost of dining.

### Overall Insights From Zomato Reviews Dataset
* From this dataset, we found that 5 star is the highest rating given by 3832 number of customer. At the same time, Lowest rating given by the customers is 1.5 star.
* We analyses the Top 20 Popular customers (With Highest number of followers) and their order timings. Here we got to know that Satwinder Singh has the highest number of followers with 13410 followers, followed by Eat_vth_me who has slightly less number of 13320.
* We found Top 20 Popular customers and restaurants (With Highest number of Review_count). Anvesh Chowdary has posted a high number of reviews i.e. 1031 reviews, while the hotel named Collage - Hyatt Hyderabad Gachibowli, Pista House and Labonel has 1031 number of reviews count.
* There are 968 orders on zomato application between the time frame of 10PM to 11PM which is highest among all. The time frame between 7PM to 12AM is the peak hour for the restaurants as well as zomato. Zomato can throw more offer in this time frame so that one can use more number of offers and this is how zomato can increase their customers.
* The first order is placed on Zomato is on: 2016-05-31 16:41:00. While the last order is placed on Zomato is on: 2019-05-25 20:23:00.
* Using Time column present in our dataset, we found that our overall dataset containing data of 1089 Days Three Hours and 42 Minutes.
* There are 7447 Different Customer who have ordered food From Zomato from which 6105 Customers Ordered food items only once on Zomato. While 1342 are the repeated customers or can say regular customer on Zomato.
* 'Kiran', 'Ankita', 'Parijat Ray', 'Vedant Killa', 'Jay Mehta‘ are the most valuable customers who have ordered food from Zomato more than 10 times.

# Data Visualization & Hypothesis Testing
Data visualization is used to present the findings in the form of ten different charts, including univariate, bivariate, and multivariate visualizations. These visualizations help in understanding the relationships between different variables and the overall trends in the data. 
Some of the visualization of important columns -
1. **Distribution of the ratings column:**

![image](https://user-images.githubusercontent.com/120029190/230606443-bef6197f-9f22-4eec-aad3-f348f08a8657.png) 

2. **Distribution of final column sentiments:**

![image](https://user-images.githubusercontent.com/120029190/230606469-8574f06a-7fb0-42e2-a51c-671cb7757bdd.png)

3. **No. of orders over different time slot:**

![image](https://user-images.githubusercontent.com/120029190/230606646-51ec4be6-0861-45b5-9212-de524f2d4992.png)

4. **Distribution of ratings v/s cost v/s reviews:**

![image](https://user-images.githubusercontent.com/120029190/230607035-18dc0d7b-94f8-4faa-8093-ecb47e11a1bb.png)


# Model Implementation

1. K-Means Clustering
2. Hierarchical Clustering (Agglomerative)
3. DBSCAN Clustering
4. PCA (Principal Component Analysis)
5. Content Based Recommendation System

# Future Work

AI-driven algorithms can be used to automatically generate summary reports of restaurant reviews in various languages and identify common trends in customer feedback.
Sentiment Analysis: Sentiment analysis can be used to identify what people really think about a restaurant based on reviews. This can help customers determine which restaurants are worth their time, and which ones should be avoided.
Online Learning: Currently, the system is trained on a batch of historical data. Future work can involve developing an online learning system that can adapt to the changing preferences of the users in real-time.
Multi-language support: Zomato is a global platform and supports multiple languages. Future work can involve developing a multi-language content-based recommendation system that can handle different languages and provide recommendations in the user's preferred language.
Computer Vision: Utilize computer vision techniques to identify objects and classify food items in restaurant photos. 
Deep Learning: Use deep learning algorithms to compare reviews between two different restaurants and generate comparison results.

# Conclusion
The conclusion of this Zomato restaurant clustering and metadata sentiment analysis project is that it is possible to use natural language processing and machine learning algorithms to build a model that can accurately cluster restaurants based on their reviews and sentiments. This project has helped identify customer preferences and restaurant ratings in order to better understand the impacts of customer feedback on the restaurant industry. This model can then be used to improve the decision-making process of a restaurant owner or manager in terms of advertising, pricing, customer acquisition, and other important business decisions. With this data, business owners can make more informed decisions about the quality of their restaurants and better understand the customer experience. We have seen that AI-based solutions provide a powerful tool for business owners to gain insight into the performance of their restaurants. After that sentiment analysis can be used to gain insights into customer preferences, providing data-driven understanding into how customers perceive different aspects of service quality. Furthermore, the insights provided by this project can be used for further business growth strategies.
