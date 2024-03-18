# Hotel Booking Cancellation Prediction System

## Introduction
Many of us have canceled a hotel booking at least once and have likewise experienced giving up because the preferred hotel was fully booked. Hotel booking cancellation and the inability to satisfy potential consumers are widespread and worrisome problems that increase hotel operation costs and affect customer satisfaction. Hotel efficiency suffers severely, particularly when reservations are canceled at the last minute, leading to an irreversible underutilization of hotel resources. Given that this impact on the hospitality industry can be extremely bad, predicting hotel booking cancellation appears to be the only solution to help establish suitable operational strategies to avoid being affected. In particular, hoteliers can benefit from the prediction on individual cancellation, rather than overall cancellation rates, to identify customers at the highest risk of canceling in advance, thereby avoiding huge losses when it is not considerably late.

## Table of Content
- [Aim](#aim)
- [Information about the data source used in this project](#information-about-the-data-source-used-in-this-project)
  - [Acknowledgement](#acknowledgement)
  - [Data Dictionary](#data-dictionary)
- [Tools, Technologies and Libraries used in this project](#tools-technologies-and-libraries-used-in-this-project)
- [Project Implementation](#project-implementation)
  - [Project Code](#project-code)
  - [Implementation](#implementation)
- [Result](#result)

## Aim
The aim of this project is to develop a model that can accurately predict the likelihood of hotel room bookings being canceled. By analyzing historical data, the goal is to provide hoteliers with a tool that can identify bookings at risk of cancellation. This will enable them to implement proactive operational strategies to minimize resource wastage and financial losses. Ultimately, this project aims to improve customer satisfaction and operational efficiency in the hospitality industry.

## Information about the data source used in this project
I have used below dataset for this project :

[**hotel_bookings.csv**](https://github.com/moheenpatel/hotel-booking-cancellation-prediction-system/blob/main/Data/hotel_bookings.csv)

This dataset contains all the information regarding hotel bookings made by customers between the 1st of July 2015 and the 31st of August 2017 for a city hotel and a resort hotel. Since this is hotel real data, all data elements pertaining hotel or costumer identification were deleted.

#### Acknowledgement
The data is originally from the article [**Hotel Booking Demand Datasets**](https://www.sciencedirect.com/science/article/pii/S2352340918315191), written by Nuno Antonio, Ana Almeida, and Luis Nunes for Data in Brief, Volume 22, February 2019.

#### Data Dictionary
|variable                       |description |
|:------------------------------|:-----------|
|hotel                          |Hotel (H1 = Resort Hotel or H2 = City Hotel) |
|is_canceled                    |Value indicating if the booking was canceled (1) or not (0) |
|lead_time                      |Number of days that elapsed between the entering date of the booking into the PMS and the arrival date |
|arrival_date_year              |Year of arrival date|
|arrival_date_month             |Month of arrival date|
|arrival_date_week_number       |Week number of year for arrival date|
|arrival_date_day_of_month      |Day of arrival date|
|stays_in_weekend_nights        |Number of weekend nights (Saturday or Sunday) the guest stayed or booked to stay at the hotel |
|stays_in_week_nights           |Number of week nights (Monday to Friday) the guest stayed or booked to stay at the hotel|
|adults                         |Number of adults|
|children                       |Number of children|
|babies                         |Number of babies |
|meal                           |Type of meal booked. Categories are presented in standard hospitality meal packages: <br> Undefined/SC – no meal package;<br>BB – Bed & Breakfast; <br> HB – Half board (breakfast and one other meal – usually dinner); <br> FB – Full board (breakfast, lunch and dinner) |
|country                        |Country of origin. Categories are represented in the ISO 3155–3:2013 format |
|market_segment                 |Market segment designation. In categories, the term "TA" means "Travel Agents" and "TO" means "Tour Operators" |
|distribution_channel           |Booking distribution channel. The term "TA" means "Travel Agents" and "TO" means "Tour Operators" |
|is_repeated_guest              |Value indicating if the booking name was from a repeated guest (1) or not (0) |
|previous_cancellations         |Number of previous bookings that were cancelled by the customer prior to the current booking |
|previous_bookings_not_canceled |Number of previous bookings not cancelled by the customer prior to the current booking |
|reserved_room_type             |Code of room type reserved. Code is presented instead of designation for anonymity reasons |
|assigned_room_type             |Code for the type of room assigned to the booking. Sometimes the assigned room type differs from the reserved room type due to hotel operation reasons (e.g. overbooking) or by customer request. Code is presented instead of designation for anonymity reasons |
|booking_changes                |Number of changes/amendments made to the booking from the moment the booking was entered on the PMS until the moment of check-in or cancellation|
|deposit_type                   |Indication on if the customer made a deposit to guarantee the booking. This variable can assume three categories:<br>No Deposit – no deposit was made;<br>Non Refund – a deposit was made in the value of the total stay cost;<br>Refundable – a deposit was made with a value under the total cost of stay. |
|agent                          |ID of the travel agency that made the booking |
|company                        |ID of the company/entity that made the booking or responsible for paying the booking. ID is presented instead of designation for anonymity reasons |
|days_in_waiting_list           |Number of days the booking was in the waiting list before it was confirmed to the customer |
|customer_type                  |Type of booking, assuming one of four categories:<br>Contract - when the booking has an allotment or other type of contract associated to it;<br>Group – when the booking is associated to a group;<br>Transient – when the booking is not part of a group or contract, and is not associated to other transient booking;<br>Transient-party – when the booking is transient, but is associated to at least other transient booking|
|adr                            |Average Daily Rate as defined by dividing the sum of all lodging transactions by the total number of staying nights |
|required_car_parking_spaces    |Number of car parking spaces required by the customer |
|total_of_special_requests      |Number of special requests made by the customer (e.g. twin bed or high floor)|
|reservation_status             |Reservation last status, assuming one of three categories:<br>Canceled – booking was canceled by the customer;<br>Check-Out – customer has checked in but already departed;<br>No-Show – customer did not check-in and did inform the hotel of the reason why |
|reservation_status_date        |Date at which the last status was set. This variable can be used in conjunction with the ReservationStatus to understand when was the booking canceled or when did the customer checked-out of the hotel|
<br>

## Tools, Technologies and Libraries used in this project
1] Anaconda  
2] Jupyter Notebook  
3] Python  
4] Google Sheets / Microsoft Excel  
5] Python Libraries for Data Science used :  

- NumPy
- Pandas
- Matplotlib
- Seaborn
- Plotly
- SciKit-Learn
<br>

## Project Implementation

### Project Code
[ML_hotel_booking_Prediction.ipynb](https://nbviewer.org/github/moheenpatel/hotel-booking-cancellation-prediction-system/blob/b015c38d95790a550f47d55392b9654a39b8378c/ML_hotel_booking_Prediction.ipynb){:target="_blank"}

### Implementation
- [Importing necessary Data Science Python libraries for our Project](https://nbviewer.org/github/moheenpatel/hotel-booking-cancellation-prediction-system/blob/b015c38d95790a550f47d55392b9654a39b8378c/ML_hotel_booking_Prediction.ipynb#Importing-necessary-Data-Science-Python-libraries-for-our-Project)
- [Data Cleaning](https://nbviewer.org/github/moheenpatel/hotel-booking-cancellation-prediction-system/blob/b015c38d95790a550f47d55392b9654a39b8378c/ML_hotel_booking_Prediction.ipynb#Data-Cleaning)
- [Data Analysis](https://nbviewer.org/github/moheenpatel/hotel-booking-cancellation-prediction-system/blob/b015c38d95790a550f47d55392b9654a39b8378c/ML_hotel_booking_Prediction.ipynb#Data-Analysis)
  - [Analysis 1 - Where do the maximum guests come from ? (Spatial Analysis))](https://nbviewer.org/github/moheenpatel/hotel-booking-cancellation-prediction-system/blob/b015c38d95790a550f47d55392b9654a39b8378c/ML_hotel_booking_Prediction.ipynb#Analysis-1%5D-Where-do-the-maximum-guests-come-from-?-(Spatial-Analysis))
  - [Analysis 2 - How much do guests pay for a room per night?](https://nbviewer.org/github/moheenpatel/hotel-booking-cancellation-prediction-system/blob/b015c38d95790a550f47d55392b9654a39b8378c/ML_hotel_booking_Prediction.ipynb#Analysis-2%5D-How-much-do-guests-pay-for-a-room-per-night?)
  - [Analysis 3 - How does the price per night vary over the year?](https://nbviewer.org/github/moheenpatel/hotel-booking-cancellation-prediction-system/blob/b015c38d95790a550f47d55392b9654a39b8378c/ML_hotel_booking_Prediction.ipynb#Analysis-3%5D-How-does-the-price-per-night-vary-over-the-year?)
  - [Analysis 4 - Which months are the most busiest months or in which months bookings are high in number?](https://nbviewer.org/github/moheenpatel/hotel-booking-cancellation-prediction-system/blob/b015c38d95790a550f47d55392b9654a39b8378c/ML_hotel_booking_Prediction.ipynb#Analysis-4%5D-Which-months-are-the-most-busiest-months-or-in-which-months-bookings-are-high-in-number?)
  - [Analysis 5 - How long do guests stay at the hotels?](https://nbviewer.org/github/moheenpatel/hotel-booking-cancellation-prediction-system/blob/b015c38d95790a550f47d55392b9654a39b8378c/ML_hotel_booking_Prediction.ipynb#Analysis-5%5D-How-long-do-guests-stay-at-the-hotels?)
  - [Analysis 6 - Bookings by market segment](https://nbviewer.org/github/moheenpatel/hotel-booking-cancellation-prediction-system/blob/b015c38d95790a550f47d55392b9654a39b8378c/ML_hotel_booking_Prediction.ipynb#Analysis-6%5D-Bookings-by-market-segment)
  - [Analysis 7 - How many bookings were cancelled?](https://nbviewer.org/github/moheenpatel/hotel-booking-cancellation-prediction-system/blob/b015c38d95790a550f47d55392b9654a39b8378c/ML_hotel_booking_Prediction.ipynb#Analysis-7%5D-How-many-bookings-were-cancelled?)
  - [Analysis 8 - Which month have the highest number of Cancellations?](https://nbviewer.org/github/moheenpatel/hotel-booking-cancellation-prediction-system/blob/b015c38d95790a550f47d55392b9654a39b8378c/ML_hotel_booking_Prediction.ipynb#Analysis-8%5D-Which-month-have-the-highest-number-of-Cancellations?)
- [Selecting important numerical features(attributes) using Correlation-using-Correlation)](https://nbviewer.org/github/moheenpatel/hotel-booking-cancellation-prediction-system/blob/b015c38d95790a550f47d55392b9654a39b8378c/ML_hotel_booking_Prediction.ipynb#Selecting-important-numerical-features(attributes)-using-Correlation)
- [Refining numerical features](https://nbviewer.org/github/moheenpatel/hotel-booking-cancellation-prediction-system/blob/b015c38d95790a550f47d55392b9654a39b8378c/ML_hotel_booking_Prediction.ipynb#Refining-numerical-features)
- [Refining categorical features](https://nbviewer.org/github/moheenpatel/hotel-booking-cancellation-prediction-system/blob/b015c38d95790a550f47d55392b9654a39b8378c/ML_hotel_booking_Prediction.ipynb#Refining-categorical-features)
- [Feature Encoding](https://nbviewer.org/github/moheenpatel/hotel-booking-cancellation-prediction-system/blob/b015c38d95790a550f47d55392b9654a39b8378c/ML_hotel_booking_Prediction.ipynb#Feature-Encoding)
- [Preparing Data for Machine Learning](https://nbviewer.org/github/moheenpatel/hotel-booking-cancellation-prediction-system/blob/b015c38d95790a550f47d55392b9654a39b8378c/ML_hotel_booking_Prediction.ipynb#Preparing-our-Data-for-Machine-Learning)
  - [Handling the Outliers in the data](https://nbviewer.org/github/moheenpatel/hotel-booking-cancellation-prediction-system/blob/b015c38d95790a550f47d55392b9654a39b8378c/ML_hotel_booking_Prediction.ipynb#Handling-the-Outliers-in-the-data)
- [Feature Importance](https://nbviewer.org/github/moheenpatel/hotel-booking-cancellation-prediction-system/blob/b015c38d95790a550f47d55392b9654a39b8378c/ML_hotel_booking_Prediction.ipynb#Feature-Importance)
- [Splitting the data and Builing the Model](https://nbviewer.org/github/moheenpatel/hotel-booking-cancellation-prediction-system/blob/b015c38d95790a550f47d55392b9654a39b8378c/ML_hotel_booking_Prediction.ipynb#Splitting-the-data-and-Builing-the-Model)
  - [Implementing logistic regression](https://nbviewer.org/github/moheenpatel/hotel-booking-cancellation-prediction-system/blob/b015c38d95790a550f47d55392b9654a39b8378c/ML_hotel_booking_Prediction.ipynb#Implementing-logistic-regression)
  - [Implementing different classification algorithms to decide which one is best](https://nbviewer.org/github/moheenpatel/hotel-booking-cancellation-prediction-system/blob/b015c38d95790a550f47d55392b9654a39b8378c/ML_hotel_booking_Prediction.ipynb#Implementing-different-classification-algorithms-to-decide-which-one-is-best)
- [Conclusion](https://nbviewer.org/github/moheenpatel/hotel-booking-cancellation-prediction-system/blob/b015c38d95790a550f47d55392b9654a39b8378c/ML_hotel_booking_Prediction.ipynb#As-per-above-results-we-can-conclude-that-Random-Forest-is-the-best-model-we-can-use-to-predict-the-Hotel-Booking-Cancellation-of-potential-customers-as-this-model-has-the-highest-accuracy-of-92%.)


## Result
Based on the results obtained from the project implementation, it can be concluded that the **Random Forest model** outperforms other models in predicting hotel booking cancellations, achieving an impressive **accuracy rate of 92%**. This high accuracy suggests that the Random Forest model is a reliable tool for identifying bookings at risk of cancellation.

Utilizing this model, hotels can implement proactive operational strategies to minimize resource wastage and financial losses associated with cancellations. By identifying potential cancellations in advance, hotels can optimize their booking management processes, allocate resources more efficiently, and enhance customer satisfaction by reducing the likelihood of overbooking.

In conclusion, the Random Forest model stands out as an effective solution for predicting hotel booking cancellations, offering valuable insights that can help hotels improve their overall operational efficiency and customer experience.
