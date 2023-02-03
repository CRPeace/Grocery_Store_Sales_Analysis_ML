# Grocery Store Sales Analysis and Predictive Modeling
---
### Analyzing the Factors that Drove Sales in 2013 Big Mart Stores

**Cameron Peace**

#### The purpose of this analysis was to tease apart the various factors that influenced the sales of supermarket/grocery items in 2013 for select stores belonging to the international chain Big Mart.
---
### Quick Summary:
* **One specific store in the dataset clearly outperformed the others in terms of sales**.  From the information found in the dataset, it was difficult to discern what additional factors where driving sales.
* **The Machine Learning models utilized here have limited effectiveness** in predicting items sales based on the information found in the dataset.
### Quick Recommendations:
* **I would recommend collecting additional data and analysis on the specific top performing store** (e.g. location, store layout, local demographics, HR data, etc.). Doing so would further illuminate what is contributing to its success.  Big Mart could then attempt to recreate the results in additional locations.
* Additional ML models could be explored on this dataset if prediction is desired.  **However, I would recommend reserving predictive modeling resources for a more detailed dataset that includes both more data and more relevant data.** In my opinion, there is key data missing from this dataset that limits its usefulness.
---

### Data:
The dataset used in this analysis was originally provided by [Analytics Vidhya](https://datahack.analyticsvidhya.com/) for use in a data analysis [practice competition](https://datahack.analyticsvidhya.com/contest/practice-problem-big-mart-sales-iii/#About).  It includes data on products from the grocery store chain [Big Mart](https://www.bigmart.ae/index.html), which has locations mostly in India and the United Arab Emirates. From [Analytics Vidhya](https://www.analyticsvidhya.com/blog/2016/02/bigmart-sales-solution-top-20/): **"The data scientists at BigMart have collected 2013 sales data for 1559 products across 10 stores in different cities."*

#### Data Dictionary:
* ***Variable Name: --	Description***
* Item_Identifier: --	Unique product ID
* Item_Weight: --	Weight of product
* Item_Fat_Content: --	Whether the product is low fat or regular
* Item_Visibility: --	The percentage of total display area of all products in a store allocated to the particular product
* Item_Type: --	The category to which the product belongs
* Item_MRP: --	Maximum Retail Price (list price) of the product
* Outlet_Identifier: --	Unique store ID
* Outlet_Establishment_Year: --	The year in which store was established
* Outlet_Size: --	The size of the store in terms of ground area covered
* Outlet_Location_Type: --	The type of area in which the store is located
* Outlet_Type: --	Whether the outlet is a grocery store or some sort of supermarket
* Item_Outlet_Sales: --	Sales of the product in the particular store. This is the target variable to be predicted.
---
## Methods
#### The data was first examined, cleaned and then the following steps and processes were performed:
* Exploratory Data Analysis
* Explanatory Data Analysis
* Modeling with 2 Supervised Machine Learning Models:
  * Linear Regression
  * Decision Tree Regression
---
### Exploratory Data Analysis
* The data was explored using:
  * Sorting and Filtering with pandas
  * A seaborn heatmap using correlation(r) values
  * Histograms, Barcharts, and Boxplots

#### Boxplot Visualization

#### **This visualization revealed that one specific store was outcompeting the others in terms of sales (OUT027, Supermarket Type3)**
![Boxplots](https://github.com/CRPeace/Grocery_Store_Sales_Analysis_ML/blob/3686b3a63e101c75e49ed72d1102225a8941e0dc/Boxplots.png)

---
### Explanatory Data Analysis
* In order to present the information distilled from the analysis, the following charts were created:
#### **This barplot shows shows that we have one store outperforming the rest**
![Top Store.png](https://github.com/CRPeace/Grocery_Store_Sales_Analysis_ML/blob/3686b3a63e101c75e49ed72d1102225a8941e0dc/Top%20Store.png)


#### **This visualization shows that the top performing store is outcompeting the others across nearly all categories of grocery item types.**
![Average Maximum Sales in Each Item Category](https://github.com/CRPeace/Grocery_Store_Sales_Analysis_ML/blob/3686b3a63e101c75e49ed72d1102225a8941e0dc/Top%20Items.png)
---
### Machine Learning Models
* The following models were assessed on the dataset
  * Linear Regression
  * Decision Tree Regression

#### Linear Regression
* The model displayed the following metrics:
  * Root Mean Squared Error on Training Set:	1,140.13
  * R Squared on Training Set:	0.560
  * Root Mean Squared Error on Testing Set:	1,092.72
  * R Squared on Testing Set:	0.567

#### Decision Tree Regression
* After tuning, the model displayed the following metrics:
  * Root Mean Squared Error on Training Set:	1,051.66
  * R Squared on Training Set:	0.626
  * Root Mean Squared Error on Testing Set:	1,043.561
  * R Squared on Testing Set:	0.605

### **The Decision Tree model is the top performer between the two models utilized to attempt to predict item sales.  However, the size of the errors in the model limit its usefulness.  At best it could potentially account for around 60% of the item price based on the accompanying data.**
---
## Recommendations:

***Overall, I believe the most useful piece of information that can be taken from this analysis is to identify a top performing store within the dataset.***  
* I would recommend collecting more data on this specific store in order to identify the factors that are most contributing to its success in sales (and additional stores for comparison).  Furthermore, knowing the specific location for each store in the dataset would open up quite a bit that could explain the trends we're seeing in this collection of Big Mart stores.
* I would not recommend allocating more resources to machine learning models unless the quantity and quality of the dataset is improved.  Additionally, there are more sophisticated models that could be deployed that would likely provide a better predictive result, but I believe that overall data quality would continue to be a limiting factor.


## Limitations & Next Steps

It is my opinion that the most significant limitation we'll encounter in any sort of follow up analysis is the **age of the dataset**.  With additional data there may be useful insights still to be obtained, but I think resources would be better allocated to obtaining and analyzing more recent data.  Despite that, circling back to this dataset could potentially help reveal longterm trends, so this data should be kept on the shelf to aid in future analyses.

---
### For further information

For any additional questions, please contact CPeaceData@gmail.com
