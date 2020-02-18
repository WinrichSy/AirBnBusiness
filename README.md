# **AirBnBusiness**  
## Description  
A deep dive into the Paris AirBnb dataset to get a better understanding on successful hosts on AirBnb. What is needed to gain Superhost status based on various attributes and predict if hosts are on their way to gain that status. 

## Table of Contents
[1. Background & Motivation](#Background&Motivation)<br>
[2. Data Source](#DataSource)<br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[2a. About The Data](#data)<br>
[3. Exploratory Data Analysis](#EDA)<br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[3a. Listings Based on Average Price](#3a)<br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[3b. Languages Spoken by Renters](#3b)<br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[3c. Number of Listings Per Month](#3c)<br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[3d. Number of Listings Per Host](#3d)<br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[3e. Hosts vs Superhosts](#3e)<br>
[4. Modeling](#Modeling)<br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[4a. Models without Verification Dummies](#4a)<br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[4b. Models WITH Verification Dummies](#4b)<br>
[5. Conclusions](#Conclusions)<br>
[6. Future Plans](#FuturePlans)<br>
[7. Dependencies](#Dependencies)<br>
[8. Contact](#Contact)<br>

## <a id="Background&Motivation">Background & Motivation</a>
AirBnb is an online marketplace that connects people who want to rent out their homes with people who are looking for accommodations in that location. There is a wide selection of properties for travelers to rent for a period of time. Hosts don't have to pay to list their properties on AirBnb's marketplace and they can also set their own pricing. Locals in the area can also list their services and guides to entertain guests as well. With over tens of millions of users a year, the number of listings as well as competitiveness of bringing in renters have increased. As of 2019, AirBnb was last evaluated at $31 billion. My project here is to get a better understanding of the ins and outs of being a successful host on Airbnb. 

---
## <a id="DataSource">DataSource</a>
AirBnb Paris Data Downloaded from   
http://insideairbnb.com/get-the-data.html  

### <a id="data">2a. About the Data</a>
Paris -   
1. listings.csv: (65493 rows, 106 columns) 241.3 MB  
Attributes: 
id, name, summary, space, description, host_id, host_since, host_about, host_response_time, host_response_rate, host_is_superhost, host_total_listings_count, host_verifications, host_has_profile_pic, host_identity_verified, latitude, longitude, property_type, accommodates, bathrooms, bedrooms, beds, amenities, price, security_deposit, cleaning_fee, minimum_nights, number_of_reviews, review_scores_rating, review_scores_accuracy, review_scores_cleanliness, review_scores_checkin, review_scores_communication, review_scores_location, review_scores_value, cancellation_policy, requires_license, reviews_per_month, require_guest_phone_verification, language.
   
2. reviews.csv: (1310351 rows, 6 columns) 441.3 MB  
Attributes:  
listing_id, date, reviewer_id, comments, language_code, language.
  
3. calendar.csv: (23905452 rows, 7 columns) 1.02 GB  
Attributes:  
listing_id, date, available, price, minimum_nights, maximum_nights, week (generated), month (generated), year (generated).
 
---
## <a id="EDA">Exploratory Data Analysis</a>
### <a id="3a">3a. Listings Based on Average Price</a>
The daily average price for AirBnb listings in Paris are below $300 USD per day. Some daily prices average out at the extreme
end, like $2700 USD.
<p align="center"><img src="AirBnb Capstone Graphs/1.1 Hist - Listings based on daily price.png"></p>

Looking further into the histogram bar of $0-$300, the daily average price falls mainly between $33 to $100. 
<p align="center"><img src="AirBnb Capstone Graphs/1.2 Hist - Inner Listings based on daily price.png"></p>

### <a id="3b">3b. Languages Spoken by Renters</a>
A huge majority of renters speak English or French. Primarily 66.19% of the renters speak English while 22.52% speak French.
Altogether, the remaining language spoken by renters visiting Paris totals only 11.29%.
<p align="center"><img src="AirBnb Capstone Graphs/2. Language Based of Renters.png"></p>

### <a id="3c">3c. Number of Listings Per Month</a>
The furture number of listings in Paris for 2020 fluxuates depending on the month. February 2020 currently had the least
amount of available listings. Whereas January, March, and May have the most listings available. 
<p align="center"><img src="AirBnb Capstone Graphs/3. Number of Listings per Month.png"></p>

### <a id="3d">3d. Number of Listings Per Host</a>
49580 AirBnb Hosts have between 1 to 12 listings. A few amount of hosts have more than 45 properties listed.
<p align="center"><img src="AirBnb Capstone Graphs/4.1 Number of Listings per host.png"></p>
Looking further into the 1 to 12 histogram bar, 42614 hosts only have one property listed. There are 4872 hosts with two properties listed.
<p align="center"><img src="AirBnb Capstone Graphs/4.2 Inner Number of Listings per host.png"></p>

### <a id="3e">3e. Hosts vs Superhosts</a>
Only 12.81% of AirBnb hosts in Paris are verified Superhosts.
<p align="center"><img src="AirBnb Capstone Graphs/5. Hist - Hosts vs Superhosts.png"></p>

---
## <a id="Modeling">Modeling</a>
### <a id="4a">4a. Models WITH Verification Dummies</a>
Fitted the dataset into a Logistic Regression, Gradient Boosting, Random Forest, and Decision Tree model. This ROC curve 
shows the true positive rate against the false positive rate.
<p align="center"><img src="AirBnb Capstone Graphs/6.1 ROC curve w verification dummies.png"></p>

<p align="center"><img src="AirBnb Capstone Graphs/6.1 Values from Models w verification dummies.png"></p>
 
### <a id="4b">4b. Models without Verification Dummies</a>
Modified model to take in training set without Dummies of Host Verifications and saw a slight increase in average accuracy 
and an increase in average recall.
<p align="center"><img src="AirBnb Capstone Graphs/6.2 ROC curve w_o verification dummies.png"></p>

<p align="center"><img src="AirBnb Capstone Graphs/6.2 Values from Models w_o verification dummies.png"></p>

---
## <a id="Conclusions">Conclusions</a>
In conclusion, the models have a good predictive accuracy on whether a host is on it's way to become a superhost based on certain attributes.

---
## <a id="FuturePlans">Future Plans</a>
1. If given more time, would try to tokenize based of language.  
2. Find a way to translate through all without hitting requests limit with googletrans module.
3. Add dataset of previous years  
4. Create a time series and predictor on pricing

---
## <a id="Dependencies">Dependencies</a>
https://pypi.org/project/iso-639/  
https://pypi.org/project/langdetect/  
https://pypi.org/project/langua/  

---
## <a id="Contact">Contact</a>
Feel free to contact me about any questions. I can be reached through these links.  
[LinkedIn](https://www.linkedin.com/in/winrichsy/)  
[Email](winrichsy@gmail.com)  
  
version 1.0 - EDA on Superhosts on Airbnb, number of listings available, average pricing. 
