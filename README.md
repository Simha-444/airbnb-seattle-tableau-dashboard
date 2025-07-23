# airbnb-seattle-tableau-dashboard
Interactive Tableau dashboard using Seattle Airbnb data to analyze price trends, bedroom impact, and revenue patterns for potential investors

# 📊 Tableau Airbnb Full Project (Seattle)

## 🎯 Project Use Case

You're placed in the shoes of a real estate investor seeking to identify the **best locations and time periods to invest in Airbnb rentals** for maximum profitability. The analysis focuses on key investment factors like:

- Number of bedrooms  
- Zip code (location)  
- Potential daily rental price  

---

## 📁 Data Source

The project uses the **Seattle Airbnb Open Dataset**.

### Files involved:
- `listings.csv`, `calendar.csv`, and `reviews.csv`
- Combined into one Excel workbook provided via GitHub

### Notes:
- A newer version is available in `.csv.gz` format (needs conversion)

### Key Data Tables:
- `listings`: Includes zip code, property type, bathrooms, bedrooms, price, fees, etc.
- `calendar`: Availability, daily prices, booked status
- `reviews`: Review IDs, listing IDs, text reviews

---

## 🧰 Tools Used

- **Tableau** – for visualisation  
- **Microsoft Excel** – for combining datasets  

---

## 📈 Visualisations in the Final Dashboard

This project consists of five visualisations designed to support real estate investment decisions:

### 1. 📍 Average Price by Zip Code (Bar Chart)
- Shows average daily price for each zip code  
- Sorted from highest to lowest  
- Color scale matches the map for consistency  

### 2. 🗺️ Price by Zip Code Map (Filled Map)
- Map of Seattle showing average prices per zip code  
- Color-coded like the bar chart  

### 3. 📆 Revenue Over Year (Line Chart)
- Weekly revenue trends for 2016  
- Highlights peak seasons like summer and holidays  

### 4. 🛏️ Average Price Per Bedroom (Bar Chart)
- Shows how average price changes by bedroom count  
- Larger homes (5–6 BR) have significantly higher average prices  

### 5. 📊 Count of Bedroom Listings (Bar Chart)
- Number of listings for each bedroom count  
- Larger homes have fewer listings → less competition  

![image alt](https://github.com/Simha-444/airbnb-seattle-tableau-dashboard/blob/ed3a05446392c4866e74d4956e245a107c94f803/AirBnb%20Dashboard%20.png)
---

## 🧪 How to Replicate This Project

### 🔗 1. Download & Load Data
- Download Excel file from GitHub  
- Open Tableau and connect to the Excel file  

### 🔗 2. Join Tables Properly (Super Important)
- Drag `listing` as base  
- Join `calendar`:  
  - Use `listing_id` from `calendar` and `id` from `listing`  
  - Avoid default `price` join  
- Join `reviews` (optional):  
  - Use `listing_id` from `reviews` and `id` from `listing`  

✅ Use **inner joins**  
⚠️ Avoid joining on `id = id` unless both are listing IDs  

### 🔗 3. Handle Tableau Public Row Limit
- Tableau Public has a **15 million row limit**  
- `reviews` is unused in visuals → **can be excluded**  

### 🔗 4. Build the Visuals
- Convert `bedrooms` to **dimension**
- Set `price` to **average**, not sum  
- Filter out `null` or `0` values for `zip code`, `bedrooms`  

### 🔗 5. Design the Dashboard
- Arrange all 5 visuals logically  
- Ensure color consistency between map and bars  
- Add interactivity (filters) if needed  


---

## 🚀 Suggestions for Expansion

This dataset includes over 30 unused fields. Explore additional ideas:

- Try new chart types (treemap, scatter plot, box plot)  
- Analyse:
  - Weekly/monthly rental prices  
  - Cleaning fees, deposits, amenities  
  - Review counts or sentiments  
- Create **custom dashboards** from scratch  
- Use the **latest Seattle Airbnb data** for real-time insights  

---

## 💼 Final Thoughts

This project is your **foundation** for developing real-world analytics skills. In the real world, clients will ask for:

- More filters  
- More KPIs  
- More dashboards  
- More insights  

Use this as a starting point. Continue building and improving your Tableau and storytelling skills to stand out in the job market.

---
