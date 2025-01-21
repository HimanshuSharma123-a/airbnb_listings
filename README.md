#Project Description: Basic SQL Queries - Airbnb Listings 🏡

##In this project, I have implemented and executed a series of basic SQL queries to analyze the Airbnb Listings dataset. Below are the steps I followed to explore and gain insights from the dataset:

Steps:
- 1. Table Creation & Data Insertion 🛠️
Created the airbnb_listings table with columns like id, city, country, number_of_rooms, and year_listed.
Inserted sample data for cities like Paris, Tokyo, New York, Sydney, etc.
- 2. Basic SQL Queries 💻
Get all data from the table: SELECT * FROM airbnb_listings;
Filter listings by number of rooms: Used WHERE clause to filter listings with specific room counts, such as number_of_rooms > 3.
Sort data by number of rooms: Applied ORDER BY to sort listings based on room numbers, in ascending or descending order.
Get data for specific cities: Used LIKE and IN to filter listings from cities like Paris or Tokyo.
Aggregate data: Calculated the total number of rooms across all listings using SUM(number_of_rooms).
Average rooms per listing: Used AVG(number_of_rooms) to find the average number of rooms across listings.
Group and filter data: Grouped listings by country and applied HAVING clause to filter countries based on average room count.
- 3. Advanced Querying Techniques 🔍
Conditional queries with AND/OR: Combined multiple conditions using logical operators to filter data efficiently.
Data analysis by grouping: Grouped listings by country and applied aggregate functions like AVG and SUM.
- 4. Final Output & Conclusion 📊
Successfully derived useful insights from the dataset, including room availability, average room counts per country, and more.
Ready to use for further analysis or presentation.
