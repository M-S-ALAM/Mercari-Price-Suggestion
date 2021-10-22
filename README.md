# <span style='color:Blue'> Mercari Price Suggestion  </span>
Machine Learning/Deep Learning
## 1.Business Problem
### 1.1 Problem Description
<pre>Mercari japan biggest online shopping community launched in 1991 powered market place with JPY(jappan currency)10 million in transactions carried out on the platform each month.Mercari expands to the United state in 2014 and United Kingdom in 2016.The main product of mercari is mercari marketplace app which has been downloaded over 100 million times worldwide.People can sell or purchase items easily.user have freedom to choose the price while purchasing the items.There is higher risk since both the customer.small details can mean big diffrences in prices like:-
    
(1) baby iphone 6/6s plus case. price (20$).

(2) Ultra thin rose gold plating clear case for iphone 6/6s price(75$).</pre>

### 1.2  Features in the Dataset
<pre>
(1) name  - the title of the listing. Note that we have cleaned the data to remove text that look like prices (e.g. Nice product at $20) to avoid leakage. These removed prices are represented as (Nice product at).
(2) item_condition_id - the condition of the items provided by the seller.
(3) category_name - category of the listing.
(4) brand_name- Name of brand.
(5) price - the price that the item was sold for. This is the target variable that you will predict. The unit is USD. This column doesn't exist in test.tsv since that is what you will predict.
(6) shipping - 1 if shipping fee is paid by seller and 0 by buyer.
(7) item_description - the full description of the item. Note that we have cleaned the data to remove text that look like prices (e.g. $200).
</pre>

### 1.3 Source
<li> https://www.kaggle.com/c/mercari-price-suggestion-challenge </li>
<li> https://www.kaggle.com/lopuhin/mercari-golf-0-3875-cv-in-75-loc-1900-s </li>
<li> https://arxiv.org/abs/1711.00489 </li>
<li> https://medium.com/swlh/mercari-price-suggestion-challengean-end-to-end-machine-learning-case-study-4a6d833fa1c7</li>
<li> https://www.kaggle.com/valkling/mercari-rnn-2ridge-models-with-notes-0-42755 </li>
<li> https://machinelearningmastery.com/power-transforms-with-scikit-learn </li>

### 1.4 Bussnies Objective and Constraint
<pre>Data is provided by kaggle https://www.kaggle.com/c/mercari-price-suggestion challenge,to predict the price of a given product.This problem is regression problem(Supervised Learning).The features we have in train data train_id,name,item_condition_id,category_name,brand_name,shipping, item-description,price in test data except price feature which is our target feature.The feature contain categorical,Numerical and Text.
<li> The target is to solve the problem suggest the resonable price of products.</li>
<li> No strict latency constraints,because the problem demand to suggest a highly.</li> </pre>

## 2.Machine Learning Problem

### 2.1 Data Overview
Get data from https://www.kaggle.com/c/mercari-price-suggestion-challenge
<tr> Data files </tr>
<li> train.tsv </li>
<li> test.tsv </li>

### 2.2 Example Data Point
<pre>train_id name item_condition_id category_name brand_name price	shipping item_description
0 MLB Cincinnati Reds T Shirt Size XL 3	Men/Tops/T-shirts 10.0	1 No description yet 
-------------------------------------------------------------------------------------------------
1 Razer BlackWidow Chroma Keyboard	3 Electronics/Computers & Tablets/Components & Parts Razer	52.0 0 This keyboard is in great condition and works like it came out of the box.All of the ports are tested and work perfectly.The lights are customizable via the Razer Synapse app on your PC.
-------------------------------------------------------------------------------------------------
2 AVA-VIV Blouse 1 Women/Tops & Blouses/Blouse	Target	10.0 1	Adorable top with a hint of lace and a key hole in the back! The pale pink is a 1X, and I also have a 3X available in white!
3 Leather Horse Statues	1 Home/Home DÃ©cor/Home DÃ©cor Accents	35.0 1 New with tags. Leather horses. Retail for [rm] each. Stand about a foot high. They are being sold as a pair. Any questions please ask. Free shipping. Just got out of storage</pre>
### 2.3 Type of Machine Learning Problem
<pre> It is a Regression problem,for a given product we need to predict price of the product.</pre>
### 2.4 Performance metric
<pre> Metric is Root Mean Squared Logarithmic Error(RMSLE).

https://stats.stackexchange.com/questions/56658/how-do-you-interpret-rmsle-root-mean-squared-logarithmic-error
 </pre>

### Blog link:- https://medium.com/@mdshahbazpatna012/mercari-price-suggestion-an-end-to-end-case-study-1d1c3a6c80b2
