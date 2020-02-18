# **AirBnBusiness** 
> **By**: [Winrich Sy](https://www.linkedin.com/in/winrichsy/)

## Description
Exploratory data analysis on AirBnb dataset on Paris and a predictor on up and coming SuperHosts.


## Table of Contents
[1. Background & Motivation](#Background&Motivation)<br>
[2. Data Source](#DataSource)<br>
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
The **goal of this project** blahblabhalbha

---
## <a id="DataSource">DataSource</a>
Obtained dataset from 

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
<p align="center"><img src="AirBnb Capstone Graphs/4.1 Number of Listings per host.png"></p>

### <a id="3e">3e. Hosts vs Superhosts</a>
<p align="center"><img src="AirBnb Capstone Graphs/4.2 Inner Number of Listings per host.png"></p>

---
## <a id="Modeling">Modeling</a>
<p align="center"><img src="AirBnb Capstone Graphs/1.1 Hist - Listings based on daily price.png"></p>

### <a id="4a">4a. Models without Verification Dummies</a>
 <p align="center"><img src="AirBnb Capstone Graphs/1.1 Hist - Listings based on daily price.png"></p>

### <a id="4b">4b. Models WITH Verification Dummies</a>
<p align="center"><img src="AirBnb Capstone Graphs/1.1 Hist - Listings based on daily price.png"></p>

---
## <a id="Conclusions">Conclusions</a>


---
## <a id="FuturePlans">Future Plans</a>


---
## <a id="Dependencies">Dependencies</a>


---
## <a id="Contact">Contact</a>




<p align="center"><img src="AirBnb Capstone Graphs/1.1 Hist - Listings based on daily price.png"></p>




--



















# **AirBnBusiness** 

AirBnb is an online marketplace that connects people who want to rent out their homes with people who are looking for accommodations in that location. There is a wide selection of properties for travelers to rent for a period of time. Hosts don't have to pay to list their properties on AirBnb's marketplace and they can also set their own pricing. Locals in the area can also list their services and guides to entertain guests as well. With over tens of millions of users a year, the number of listings as well as competitiveness of bringing in renters have increased. As of 2019, AirBnb was last evaluated at $31 billion. My project here is to get a better understanding of the ins and outs of being a successful host on Airbnb. 
  
Data Downloaded from   
http://insideairbnb.com/get-the-data.html  
  
Data:  
Paris -   
1. listings.csv: (65493 rows, 106 columns) 241.3 MB  
root  
 |-- c0: string (nullable = true)  
 |-- id: string (nullable = true)  
 |-- name: string (nullable = true)  
 |-- summary: string (nullable = true)  
 |-- space: string (nullable = true)  
 |-- description: string (nullable = true)  
 |-- host_id: string (nullable = true)  
 |-- host_since: string (nullable = true)  
 |-- host_about: string (nullable = true)  
 |-- host_response_time: string (nullable = true)  
 |-- host_response_rate: string (nullable = true)  
 |-- host_is_superhost: string (nullable = true)  
 |-- host_total_listings_count: string (nullable = true)  
 |-- host_verifications: string (nullable = true)  
 |-- host_has_profile_pic: string (nullable = true)  
 |-- host_identity_verified: string (nullable = true)  
 |-- latitude: string (nullable = true)  
 |-- longitude: string (nullable = true)  
 |-- property_type: string (nullable = true)  
 |-- accommodates: string (nullable = true)  
 |-- bathrooms: string (nullable = true)  
 |-- bedrooms: string (nullable = true)  
 |-- beds: string (nullable = true)  
 |-- amenities: string (nullable = true)  
 |-- price: string (nullable = true)  
 |-- security_deposit: string (nullable = true)  
 |-- cleaning_fee: string (nullable = true)  
 |-- minimum_nights: string (nullable = true)  
 |-- number_of_reviews: string (nullable = true)  
 |-- review_scores_rating: string (nullable = true)  
 |-- review_scores_accuracy: string (nullable = true)  
 |-- review_scores_cleanliness: string (nullable = true)  
 |-- review_scores_checkin: string (nullable = true)  
 |-- review_scores_communication: string (nullable = true)  
 |-- review_scores_location: string (nullable = true)  
 |-- review_scores_value: string (nullable = true)  
 |-- cancellation_policy: string (nullable = true)  
 |-- requires_license: string (nullable = true)  
 |-- reviews_per_month: string (nullable = true)  
 |-- require_guest_phone_verification: string (nullable = true)  
 |-- language: string (nullable = true)  
   
2. reviews.csv: (1310351 rows, 6 columns) 441.3 MB
root  
 |-- c0: string (nullable = true)  
 |-- listing_id: string (nullable = true)  
 |-- date: string (nullable = true)  
 |-- reviewer_id: string (nullable = true)  
 |-- comments: string (nullable = true)  
 |-- language_code: string (nullable = true)  
 |-- language: string (nullable = true)  

3. calendar.csv: (23905452 rows, 7 columns) 1.02 GB
root  
 |-- c0: integer (nullable = true)  
 |-- listing_id: integer (nullable = true)  
 |-- date: timestamp (nullable = true)  
 |-- available: string (nullable = true)  
 |-- price: string (nullable = true)  
 |-- minimum_nights: double (nullable = true)  
 |-- maximum_nights: double (nullable = true)
 |-- week: int (nullable = true)
 |-- month: int (nullable = true)
 |-- year: int (nullable = true)

Modules used:  
https://pypi.org/project/iso-639/  
https://pypi.org/project/langdetect/  
https://pypi.org/project/langua/  
  
Future Plans:  
1. If given more time, would try to tokenize based of language.  
2. Find a way to translate through all without hitting requests limit with googletrans module.
3. Add dataset of previous years  
4. Create a time series and predictor on pricing

version 1.0 - EDA on Superhosts on Airbnb, number of listings available, average pricing. 
