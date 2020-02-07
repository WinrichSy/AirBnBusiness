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
