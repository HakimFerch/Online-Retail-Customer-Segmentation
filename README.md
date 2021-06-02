# Online Retail Customer Segmentation and data analysis

This project is part of my data analysis/science portfolio that helped me make use of what i learned and improve my business sense. I wanted to combine machine learning techniques, statistics and business
intelligence methods to draw insightful interpretations and analyze a business case of an online retail.
The dataset's source: https://www.kaggle.com/janiobachmann/bank-marketing-dataset

#### -- Project Status: Completed

## Project Intro/Objective

Online retail has become an essential part of any economy's fabric, and thus, it's important to keep it moving forward with more sophisticated types of marketing strategies and business decision.
Fortunately, data analysis proved to be a crucial tool to do just that, it helps us uncover details that may contribute to the business's propseprity and avoid multiple roadblocks.

In this project i take on the challenge of analyzing a UK based online retail dataset that contains over 500000 invoices and more than 4000 customers with the objective of segmenting clients according to their behavioural patterns using the RFM technique and machine learning clustering models.

### Methods Used

* Descriptive statistics
* Statistical modelling
* Feature Engineering
* Machine Learning
* Data Visualization
* Marketing Strategy
* RFM Analysis

### Technologies

* Python
* Pandas, jupyter
* Matplotlib,Seaborn
* Scikit-learn 
* numpy
* scipy

## Project Overview

The dataset lists over 500000 invoices recorded over a period of 23 months of 4339 customers mainly from united kingdom. My goal is to group clients by their common transactional traits into different ordinal levels to facilitate the marketing process and not waste resources on the wrong targets. I will use RFM method and machine learning clustering then conduct a comparative analysis between the 2.

The dataset consists of 8 features:

* InvoiceNo           
* StockCode           
* Description      
* Quantity            
* InvoiceDate         
* UnitPrice           
* CustomerID     
* Country

![image](https://user-images.githubusercontent.com/60581207/120548752-fed7f580-c3f2-11eb-8089-482dfc42ae0d.png)

The first part of the project starts with an exploratory analysis of the dataset to assess its quality (null values, odd values) to clean it accordingly then visualize primary patterns  of different features.

![image](https://user-images.githubusercontent.com/60581207/120555288-28951a80-c3fb-11eb-82f0-52628671a3ad.png)

![image](https://user-images.githubusercontent.com/60581207/120555901-0e0f7100-c3fc-11eb-9df5-ae2f7f32fe37.png)

As stated in the intro, i used the **RFM** technique to group customers,the name of the method is an abbreviation of the 3 numerical factors involved in the clustering process:

* **Recency** : How recently a customer made a transaction.
* **Frequency** : How often a customer buys from the store.
* **Monetary** : How much does the customer spends

These three parameters altogether determine the importance of a customer for the retail shop. RFM Analysis is useful due to its simplicity, intuitiveness, and utilization of objective on numerical scales, that yields a comprehensive and informative depiction of customers. The output of this segmentation method is easy to interpret and adapt.

It provides a simple intuitive way of calculating each of the three aspects in a simple rating of 1-5, where 1 is the least important and 5 is the most important one. For example, a customer with R=5, F=5, and M=5 is the most profitable and loyal customer, while a customer with R=1, F=1, and M=1 is the least contributing one.Then dividing the customers using quantiles into ordinal levels.

The resulting dataframe looks as follows:

![image](https://user-images.githubusercontent.com/60581207/120558153-567c5e00-c3ff-11eb-8052-4aadc6611053.png)

The distribution of the customers within each level based on dimensions score:

![image](https://user-images.githubusercontent.com/60581207/120558539-e91cfd00-c3ff-11eb-8140-2051df2788af.png)

![image](https://user-images.githubusercontent.com/60581207/120558593-ffc35400-c3ff-11eb-9af9-397785d2ebb0.png)

![image](https://user-images.githubusercontent.com/60581207/120558654-15d11480-c400-11eb-88c3-fef7d41c3dad.png)

The second approach i used was the ML clustering modelling,specifically the KMeans algorithm using the RFM dataframe as training data. To ensure the a better peformance of the model, it's critical to preprocess the data, as shown on the figure below, all 3 dimensions are highly skewed. Therefore i had to normalize all 3 features using logarithmic transformation before feeding it to the model.

![image](https://user-images.githubusercontent.com/60581207/120560708-82014780-c403-11eb-88d6-96632c396977.png)

![image](https://user-images.githubusercontent.com/60581207/120560866-d60c2c00-c403-11eb-8020-f0ab3f6ee15e.png)

Next phase was to determine the optimal number of clusters for the model. For this task i used both the elbow method and slihouette score and both approaches delivered 2 as seen in the scatterplot below.

![image](https://user-images.githubusercontent.com/60581207/120561436-d1944300-c404-11eb-9abb-7efda1d6bd63.png)















