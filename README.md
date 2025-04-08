# Olamide's Portfolio

# The World Database (https://olamideolanrewaju.github.io/My-Data-Analysis_Profile/)
SQL | Analysis

-- 20 Most Populated Citied
SELECT Name, CountryCode, District, Population from city 
ORDER BY Population DESC 
LIMIT 20;

Select* from countrylanguage;
Select* from city;

-- No of Official Languages in the world
Select Count(distinct Language) 
from countrylanguage where Isofficial = 'T';

Select * from countrylanguage;

-- Using the DB. What are the languages in the world? How many nations speak the available languages
Select distinct language 
from countrylanguage;

Select count(distinct countrycode) 
from countrylanguage;

SELECT Countrycode, language from countrylanguage;

Select distinct countrycode
from countrylanguage;

-- Using the DB, how many languages are there by country? [In a nation, how many languages are being spoken?]
Select * from countrylanguage;
Select Countrycode, 
count(language) 
AS NoOfSpokenLanguage 
from countrylanguage 
GROUP BY CountryCode
ORDER BY NoOfSpokenLanguage ASC;

SELECT Sum(Language) from countrylanguage;

select* from countrylanguage;
Select count(Language) 
from countrylanguage;

-- What is the total population by continent?
SELECT continent, SUM(population) AS PopulationTotal
FROM Country
GROUP BY continent
ORDER BY PopulationTotal DESC;

-- What are the 10 least populated countries?
Select* from country;
SELECT Code, Name, Population
FROM Country
ORDER BY population ASC
LIMIT 10;
