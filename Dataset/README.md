# Rehal Travel Recommendation System

## Team Members 
- **Refal Abutheeb** (Student ID: 443200792)

## 1. Introduction  
Traveling can be an overwhelming process, especially when trying to balance budget, timing, and preferences. "Rehal" is a smart travel recommendation system designed to simplify the decision-making process by providing personalized travel suggestions based on data. Whether users are looking for the best time to travel, affordable hotels, or practical itineraries, Rehal makes planning seamless and efficient.

---

## 2. Problem Statement  
Travelers often struggle with:
1. Identifying the most cost-effective travel options.
2. Planning trips that align with their preferences and budget.
3. Finding relevant and reliable information in one place.

These challenges inspired the creation of "Rehal" to act as a personalized travel advisor that leverages data to offer actionable insights.

---

## 3. Objectives  
- **Empower Travelers with Data-Driven Decisions:** Enable users to make smarter travel choices by providing detailed recommendations for destinations, flights, and accommodations based on analyzed data.
- **Optimize Budget Management:** Help users plan their trips within a specific budget by offering insights into cost-effective travel options, including flights and hotels.
- **Identify Seasonal Trends:** Provide clear guidance on the best times to travel, leveraging seasonal trends in flight and hotel pricing for better planning.
- **Simplify the Travel Planning Process:** Streamline the complexity of planning a trip by consolidating key travel information in a user-friendly system.
- **Personalize Recommendations:** Tailor travel advice based on user preferences, such as preferred destinations, travel dates, and spending limits.

---

## 4. Dataset Overview  
The dataset used for this project is sourced from **Kaggle** and simulates real-world corporate travel systems, focusing on flights and hotels.

### **Source:**  
- Dataset from Kaggle by Argo Solutions.

### **Main Files:**  
- `flights.csv`: Contains detailed records of flight bookings and prices.  
- `hotels.csv`: Contains hotel booking and pricing information.  
- `users.csv`: Contains user profile data.

---

### **Dataset Summaries**

#### **1. flights.csv**  
- **Number of rows:** 271,888  
- **Number of columns:** 10  
- **Features:**  
  - `travelCode`: Travel identifier (integer)  
  - `userCode`: User identifier (integer)  
  - `from`: Departure location (string)  
  - `to`: Destination location (string)  
  - `flightType`: Type of flight (e.g., first class)  
  - `price`: Price of the flight (float)  
  - `time`: Duration of the flight (float, hours)  
  - `distance`: Distance between locations (float)  
  - `agency`: Travel agency name (string)  
  - `date`: Travel date (string, needs conversion to datetime)  

---

#### **2. hotels.csv**  
- **Number of rows:** 40,552  
- **Number of columns:** 8  
- **Features:**  
  - `travelCode`: Travel identifier (integer)  
  - `userCode`: User identifier (integer)  
  - `name`: Hotel name (string)  
  - `place`: Hotel location (string)  
  - `days`: Number of days booked (integer)  
  - `price`: Price per day (float)  
  - `total`: Total booking price (float)  
  - `date`: Booking date (string, needs conversion to datetime)  

---

#### **3. users.csv**  
- **Number of rows:** 1,340  
- **Number of columns:** 5  
- **Features:**  
  - `code`: Unique user identifier (integer)  
  - `company`: Company the user belongs to (string)  
  - `name`: User's full name (string)  
  - `gender`: User's gender (string)  
  - `age`: User's age (integer)  

---

## 5. Data Quality Summary  
1. **flights.csv**
   - **Missing Values:** No missing values.
   - **Duplicate Rows:** No duplicate rows.
   - **Data Types:** All data types are correct except for the date column, which can be converted to a datetime format.

2. **hotels.csv**
   - **Missing Values:** No missing values.
   - **Duplicate Rows:** No duplicate rows.
   - **Data Types:** All data types are correct except for the date column, which can be converted to a datetime format.

3. **users.csv**
   - **Missing Values:** No missing values.
   - **Duplicate Rows:** No duplicate rows.
   - **Data Types:** All data types are correct.

---

## 6. Methodology  
1. **Data Exploration:**  
   - Understand the structure of the dataset (columns, data types, and ranges).
   - Identify trends, such as average costs for specific destinations and seasonal price variations.

2. **Data Cleaning:**  
   - Handle missing or inconsistent values.
   - Remove outliers to ensure the quality of recommendations.

3. **Analysis:**  
   - Use statistical and visual tools to analyze travel patterns.
   - Group destinations based on cost, popularity, and travel season.

4. **Recommendation System:**  
   - Build rules to recommend destinations, hotels, and flights.
   - Prioritize affordability, convenience, and travel preferences.

---



