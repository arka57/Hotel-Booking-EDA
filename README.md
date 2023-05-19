## Hotel-Booking-EDA
# Objective<br>
The project is based on a dataset containing information about two type hotels, City and Resort and their booking details.Main objective is to perform EDA on the given dataset and understand and infer the booking trends and the various factors affecting it.

# Data Overview<br>
The dataset is publicly available in Kaggle. It contains hotel booking information about two types of hotel City and Resort namely over three years starting from 2015 

Total number of rows in data: 119390
Total number of columns: 32

# Features in Dataset<br>

**hotel** : Name of the hotel (Resort Hotel or City Hotel)<br>
**is_canceled** : If the booking was canceled (1) or not (0)<br>
**lead_time**: Number of days before the actual arrival of the guests<br>
**arrival_date_year** : Year of arrival date<br>
**arrival_date_month** : Month of month arrival date<br>
**arrival_date_week_number** : Week number of year for arrival date<br>
**arrival_date_day_of_month** : Day of arrival date<br>
**stays_in_weekend_nights** : Number of weekend nights (Saturday or Sunday) spent at the hotel by the guests<br>
**stays_in_week_nights** : Number of weeknights (Monday to Friday) spent at the hotel by the guests<br>
**adults** : Number of adults among guests<br>
**children** : Number of children among guests<br>
**babies** : Number of babies among guests<br>
**meal** : Type of meal booked<br>
**country** : Country of guests<br>
**market_segment** : Designation of market segment<br>
**distribution_channel** : Name of booking distribution channel<br>
**is_repeated_guest** : If the booking was from a repeated guest (1) or not (0)<br>
**previous_cancellations** : Number of previous bookings that were cancelled by the customer prior to the current booking<br>
**previous_bookings_not_canceled** : Number of previous bookings not cancelled by the customer prior to the current booking<br>
**reserved_room_type** : Code of room type reserved<br>
**assigned_room_type** : Code of room type assigned<br>
**booking_changes** : Number of changes/amendments made to the booking<br>
**deposit_type** : Type of the deposit made by the guest<br>
**agent** : ID of travel agent who made the booking<br>
**company** : ID of the company that made the booking<br>
**days_in_waiting_list** : Number of days the booking was in the waiting list<br>
**customer_type** : Type of customer, assuming one of four categories<br>
**adr** : Average Daily Rate, as defined by dividing the sum of all lodging transactions by the total number of staying nights<br>
**required_car_parking_spaces** : Number of car parking spaces required by the customer<br>
**total_of_special_requests** : Number of special requests made by the customer<br>
**reservation_status** : Reservation status (Canceled, Check-Out or No-Show)<br>
**reservation_status_date** : Date at which the last reservation status was updated<br>


# Data Pre-processing and Feature Engineering

1)Duplicate Rows:<br>
--**Removed**

2)Handling missing values:<br>
--**company**: has 93% null values so the column was dropped.<br>
--**children**: is actually categorical feature. Replaced NULL with 0 as it is mode.<br>
--**country**: NULL values replaced with "Other".<br>
--**agent**: Has 13% null values.Replaced with median values as the field is continuos.<br>

3)Outliers handling:<br>
--**adr** had one big outlier value. Replaced with median

4)Feature Engineering:<br>
--New column **total_stay** was created by adding **stays_in_weekend_nights**+**stays_in_week_nights**

# Exploratory Data Analysis

EDA was performed on the dataset and many insights were drawn from it
Seaborn and Matplotlib libraries were mainly used for the visualizations. 
The different types of Graphs used were:<br>
--Bar Plot<br>
--Histogram<br>
--Line Plot<br>
--Count Plot<br>
--Box Plot<br>
--Heatmap<br>

Along with them the Pandas and NumPy libraries were used for performing the EDA

# Insights/Conclusions

1)More City Hotel Bookings are done in comparison to Resort Hotel

2)As per given data hotel booking increased from 2015 to 2016 and then decreased on 2017. Also more percentage of hotels are cancelled in 2016 and 2017

3)Bookings(Arrivals) consistently increased from January and peaked in July(Summer Months) and August .On subsequent months it got reduced Data is vastly differing over the years. But winter has less demand in each years

4)ADR over the years have increased. More ADR during summer months. It reduces during the winter months corroborating with lesser hotels booked in winters

5)No trend between cancellation and weekend staying

6)Highest number of bookings are from Portugal

7)Most of the data fall into market segment of Online TA whether City or Resort Hotel


8)Most reserved room is A .It has the highest demand among customers


9)Repeated guests are very very less in number in comparison to total no of bookings

10)Repeated guests tend to cancel hotel booking lesser compared to non repeated guests


11)Most of the hotel bookings are done without any advance payment

12)In City hotel there is slight higher trend of cancellation among Transient Customers

13)Agent 9 has highest bookings. 2-3 agents have more than 10000 bookings. Rest are in range of 1000 and less. Agents are divided into 2-3 bigger players

Agent 9 is specialized more into Hotel Booking. 99% of booking through 9 are of City type
Agent 240 is specialized more into Resort Booking. 95% of booking through 240 are of Resort type

14)Majority of users prefer BB type meal

HB -though very less but still more preferred in Resort Hotel BB meal bookings have slightly has less ADR and that's why may be has highest consumption


15)ADR of city hotels are more than Resort Hotel. There is no relation between canceling and adr


16)Median adr of Room F is highest but its demand is less.


17)For repeated guests the median adr is lower


18)Most number of total stays are under 5 days. Above 10 are negligible . Trend is if stay is more than 10 days the median adr is slightly less


19)Slight increase in ADR if weekend nights are stayed in hotel
Median ADR is increasing consistently with passage of year

# Business Suggestions
 --Rates can be reduced to fill occupancy in winter months
 --More rooms of type A should be introduced in the hotels because of high demand
 --Strive to get more repeated guests as they have lesser trend of cancellations
 
# Challenges
--Presence of Duplicate Data
--Variation in data

