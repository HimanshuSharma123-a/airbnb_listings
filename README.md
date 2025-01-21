#BasicSQLQueries - #AirbnbListings 🏡
This project focuses on executing basic SQL queries on the Airbnb Listings dataset to extract valuable insights. Below is a breakdown of the steps followed in this project:

#Steps:
#1 TableCreation & #DataInsertion 🛠️
Created the airbnb_listings table with essential columns:
id, city, country, number_of_rooms, and year_listed.
Inserted sample data for cities such as Paris, Tokyo, New York, and others.
#2 BasicSQLQueries 💻
FetchingAllData:
SELECT * FROM airbnb_listings;
FilteringListingsByRooms:
Applied WHERE clause for specific room counts:
WHERE number_of_rooms > 3;
SortingDataByRooms:
Used ORDER BY to sort the listings in ascending/descending order:
ORDER BY number_of_rooms DESC;
CitySpecificFilters:
Filtered listings from cities like Paris using LIKE or IN:
WHERE city = 'Paris';
AggregatingData:
Calculated total rooms using SUM(number_of_rooms):
SELECT SUM(number_of_rooms) FROM airbnb_listings;
AverageRoomsPerListing:
Used AVG(number_of_rooms) to get the average room count:
SELECT AVG(number_of_rooms) FROM airbnb_listings;
ConditionalFilteringWithANDorOR:
Combined multiple conditions to filter listings effectively:
WHERE city = 'Paris' AND number_of_rooms > 3;
#3 AdvancedQueryTechniques 🔍
GroupingData:
Used GROUP BY to aggregate data by countries and cities:
GROUP BY country;
FilteringGroupedData:
Applied HAVING to filter groups based on conditions:
HAVING AVG(number_of_rooms) > 3;
SortingWithAggregatedResults:
Sorted results of group-based queries:
ORDER BY AVG(number_of_rooms) ASC;
#4 FinalInsights & #Output 📊
Gained valuable insights into room availability and country-wise trends.
Prepared the dataset for further analysis or visualization.
