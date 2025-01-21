# BasicSQLQueries - AirbnbListings 🏡

This project focuses on executing basic SQL queries on the Airbnb Listings dataset to extract valuable insights. Below is a breakdown of the steps followed in this project:

# Steps:

# 1 TableCreation & DataInsertion 🛠️
- Created the airbnb_listings table with essential columns:
- Inserted sample data for cities such as Paris, Tokyo, New York, and others.

# 2 BasicSQLQueries 💻
- FetchingAllData:
- FilteringListingsByRooms:
- SortingDataByRooms:
- CitySpecificFilters:
- AggregatingData:
- AverageRoomsPerListing:
- ConditionalFilteringWithANDorOR:

# 3 AdvancedQueryTechniques 🔍
- GroupingData
- FilteringGroupedData:
- SortingWithAggregatedResults:

```sql

CREATE TABLE airbnb_listings (
    id INT PRIMARY KEY,
    city VARCHAR(50),
    country VARCHAR(50),
    number_of_rooms INT,
    year_listed INT
);

INSERT INTO airbnb_listings (id, city, country, number_of_rooms, year_listed)
VALUES 
(1, 'Paris', 'France', 5, 2018),
(2, 'Tokyo', 'Japan', 2, 2017),
(3, 'New York', 'USA', 2, 2022);

-- Data verify karne ke liye
SELECT * FROM airbnb_listings;

-- Get all the coloumn from a table:

select * from airbnb_listings;

-- Return the city coloumn from the table 

select city from airbnb_listings;

-- Get the city and year_listed coloumn from the table:

select city, year_listed from airbnb_listings;

-- Get the listing id, city, ordered by the number_of_rooms in ascending order

select id,city
from airbnb_listings
order by number_of_rooms asc;

-- Get the listing id, city, ordered by the number_of_rooms in descending order

select id,city
from airbnb_listings
order by number_of_rooms desc;

-- Get the first 2 rows from the airbnb_listings table

SELECT * 
FROM airbnb_listings
LIMIT 2;

-- get all the listing whare numbers_of_rooms is more or equal to 3 

SELECT * 
FROM airbnb_listings
WHERE number_of_rooms >= 3;

-- get all the listing whare numbers_of_rooms is more then 3 

SELECT * 
FROM airbnb_listings
WHERE number_of_rooms > 3;

-- get all the listing whare numbers_of_rooms is exactly equal to 3 

SELECT * 
FROM airbnb_listings
WHERE number_of_rooms = 3;

-- get all the listing whare numbers_of_rooms is lower or equal to 3 

SELECT * 
FROM airbnb_listings
WHERE number_of_rooms <= 3;

SELECT * 
FROM airbnb_listings
WHERE number_of_rooms < 3;

-- get all the listings where number_of_rooms is greater than 2 and less than or equal to 5

SELECT * 
FROM airbnb_listings
WHERE number_of_rooms > 2 AND number_of_rooms <= 5;

-- inserted extra row in airbnb_listings

INSERT INTO airbnb_listings (id, city, country, number_of_rooms, year_listed)
VALUES (4, 'Sydney', 'Australia', 1, 2020);

-- get all the listings with 1 to 3 rooms 

select * from airbnb_listings
where number_of_rooms between 1 and 3;

-- get all the listings that are based in "Paris'

select * from airbnb_listings
where city = 'paris';

-- get all the listings based in the 'USA'  and in 'France'

select * from airbnb_listings
where country in ('USA', 'France');

-- Get all the listings where city starts with 'N' and does not end with 'k'

SELECT * 
FROM airbnb_listings
WHERE city LIKE 'N%' AND city NOT LIKE '%k';

-- Get all the listings in 'Paris' where number_of_rooms is greater than 3

SELECT * 
FROM airbnb_listings
WHERE city = 'Paris' AND number_of_rooms > 3;

-- Get all the listings in 'Paris' or the ones that were listed after 2012

SELECT * 
FROM airbnb_listings
WHERE city = 'Paris' OR year_listed > 2012;

-- retrun the listings where number_of_rooms is missing

select *
from airbnb_listings
where number_of_rooms is null;

-- retrun the listings where number_of_rooms is not missing

select *
from airbnb_listings
where number_of_rooms is not null;

-- Get the total number of rooms available across all listings

SELECT SUM(number_of_rooms) AS total_rooms
FROM airbnb_listings;

-- Get the average number of rooms per listing across all listings

SELECT AVG(number_of_rooms) AS average_rooms
FROM airbnb_listings;

-- get the listings with the highest number of rooms across all listings

select MAX(number_of_rooms)
from airbnb_listings;

-- get the listings with the lowest number of rooms across all listings

select MIN(number_of_rooms)
from airbnb_listings;

-- get the total number of rooms for each country 

select country, SUM(number_of_rooms)
from airbnb_listings
group by country;

-- for each country get the avarge number of rooms per listing sorted by ascending order

SELECT country, AVG(number_of_rooms) AS average_rooms
FROM airbnb_listings
GROUP BY country
ORDER BY average_rooms ASC;

-- for japan and the USA , get the average number of rooms per listings in each country 

SELECT country, AVG(number_of_rooms) AS average_rooms
FROM airbnb_listings
WHERE country IN ('Japan', 'USA')
GROUP BY country;

-- get the number of cities per country where there are listings

select country, count(city) as number_of_cities
from airbnb_listings
group by country;

-- get all the years where there were more then 100 listing per year 

select year_listed
from airbnb_listings
group by year_listed
having count(id) > 100;

-- For Japan and the USA, get the average number of rooms per listing in each country where the average is greater than 3

SELECT country, AVG(number_of_rooms) AS average_rooms
FROM airbnb_listings
WHERE country IN ('Japan', 'USA')
GROUP BY country
HAVING AVG(number_of_rooms) > 3;

-- For Japan and the USA, get the average number of rooms per listing in each country where the average is greater than or equal to 4

SELECT country, AVG(number_of_rooms) AS average_rooms
FROM airbnb_listings
WHERE country IN ('Japan', 'USA')
GROUP BY country
HAVING AVG(number_of_rooms) >= 4;
```
# 4 FinalInsights & Output 📊
- Gained valuable insights into room availability and country-wise trends.
- Prepared the dataset for further analysis or visualization.




























