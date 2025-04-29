# The World Database
SQL | Analysis

**What is the 20 Most Populated Cities in the world**

> SELECT Name, CountryCode, District, Population from city 
ORDER BY Population DESC 
LIMIT 20;

> Select* from countrylanguage;
> Select* from city;

**What is the total number of Official Languages in the world**, *where official languages are marked by 'T' and unofficial languages 'F'*

> Select Count(distinct Language) 
from countrylanguage where Isofficial = 'T';

**Using the Database. What are the languages in the world? How many nations speak the available languages**

> Select distinct language 
from countrylanguage;

> Select count(distinct countrycode) 
from countrylanguage;

> Select distinct countrycode
from countrylanguage;

**Using the Database, how many languages are there by country? [In a nation, how many languages are being spoken?]**

> Select Countrycode, 
count(language) 
AS NoOfSpokenLanguage 
from countrylanguage 
GROUP BY CountryCode
ORDER BY NoOfSpokenLanguage ASC;

> SELECT Sum(Language) from countrylanguage;

> select* from countrylanguage;
Select count(Language) 
from countrylanguage;

**What is the total population by continent?**

> SELECT continent, SUM(population) AS PopulationTotal
FROM Country
GROUP BY continent
ORDER BY PopulationTotal DESC;

**What are the 10 least populated countries?**

> SELECT Code, Name, Population
FROM Country
ORDER BY population ASC
LIMIT 10;
