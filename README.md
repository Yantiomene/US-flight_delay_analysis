# (US flight delay exploration)
## by (Yaninthé Tiomene)


## Dataset

The data consists of information regarding 14595137 flights in the US for 2006,and 2007, including:
Year, Month, Day of Month, Day of week, schedule Departure time, actual departure time, schedule arrival Time, 
actual arrival time, origin and destination of airline, and other flight informations. The dataset can 
be found on [Harvard dataverse] (https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/HG7NV7),
with variables description.
After gathering the Dataset, we reformated the Time feature from a float format to match the hhmm format 
as stated in the variable description. We also extracted 4 new features `ArrDayTime`, `DepDayTime`, `DepDelay_cat` 
and `ArrDelay_cat` from `CSRArrTime`, `CSRDepTime`, `DepDelay` and `ArrDelay` respectively.


## Summary of Findings

The majority of departure and arrival delays are short (earlier departures (and arrivals), 20 minutes before the scheduled time and late departure (and arrivals) less than 70 minutes), and the longest delays, while unusual, are more heavy loaded in time. 
We dsicover that ArrDelay is highly correlated with DepDelay which is normal. There is a litle variation of delay with month where busiest flight months like August, July and December seem to have more average flight delay. Is it also true for days of the week, where Saturday which was the less busiest flight day also has less average delay. 
We also discover that flights with higher average delay are flights scheduled in the evening(PM). There is no trend between delay and busiest airport. Amongst the busiest airports, ORD and EWR have more average flight delay than the busiest aiport (ATL). Is it also true with the unique carrier, EV and TZ which are not the most busiest carriers has the highest average delay, while WN which is the most busiest carrier is in the middle with an average of 5 minutes delay in arrival and 10 minutes in departure.

Cancelled and Diverted are not really correlated with any other variable, but cancelled and diverted flights are mostly flights scheduled in the evening (PM). The Variation of number of flight per month and year is prety the same for each top 10 busiest airport. ORD is the airport with more cancelled flights.
MQ is the carrier with more cancelled flights. December is the month with more cancelled flight for almost all carrier and airport.  Saturday seems to be the day with less cancelled flight for almost all carrier. 


## Key Insights for Presentation

> In this part of investigation, we will try to answer these questions:  
- What are origins with maximum delay / cancelation?
- What are destinations with maximum delay /cancelation?
- Month with maximum and minimum delay/ Cancelation?
- Airport with most delay /Cancelation?
- Airline with most delay / cancelation?
- What are the preferred times for flights to occur? Are there any changes over multiple years?
