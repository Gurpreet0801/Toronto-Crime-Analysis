# Project-3
## **<span style="text-decoration:underline;">Participants</span>**

* Adam Tuor
* Aditya Parmar
* Gurpreet Singh Dhameja
* Bowen Pang (Jasper)

## **<span style="text-decoration:underline;">Table of Contents</span>**



* Overview
* Questions
* Data
* API

## **<span style="text-decoration:underline;">Overview</span>**

This project examines different categories for crime data for each of the 158 neighborhoods in Toronto.

The goal of our project is to help the population visualize crime trends in their neighborhood.  Our dashboard displays interactive charts that show how a particular type of crime occurrence has changed over a range of years, the distribution of crimes in a given neighborhood, and how that neighborhood ranks among all neighborhoods based on the chosen crime.

## **<span style="text-decoration:underline;">Questions</span>**



* What types of crime are most prevalent in each neighborhood?
* Which neighborhoods would be considered the safest based on certain types of crime?
* How has the occurence of crime changed in each neighborhood?
* Are there crime hotspots or is crime evenly distributed?

## **<span style="text-decoration:underline;">Data</span>**

All data was sourced from the Toronto Police Service Public Safety Data Portal



* Assault:
    * ([https://data.torontopolice.on.ca/datasets/TorontoPS::assault-open-data/about](https://data.torontopolice.on.ca/datasets/TorontoPS::assault-open-data/about))
* Auto Theft:
    * ([https://data.torontopolice.on.ca/datasets/TorontoPS::auto-theft-open-data/about](https://data.torontopolice.on.ca/datasets/TorontoPS::auto-theft-open-data/about))
* Break and Enter:
    * ([https://data.torontopolice.on.ca/datasets/TorontoPS::break-and-enter-open-data/about](https://data.torontopolice.on.ca/datasets/TorontoPS::break-and-enter-open-data/about))
* Homicide:
    * ([https://data.torontopolice.on.ca/datasets/TorontoPS::homicides-open-data-asr-rc-tbl-002/about](https://data.torontopolice.on.ca/datasets/TorontoPS::homicides-open-data-asr-rc-tbl-002/about))
* Robbery
    * ([https://data.torontopolice.on.ca/datasets/TorontoPS::robbery-open-data/about](https://data.torontopolice.on.ca/datasets/TorontoPS::robbery-open-data/about))
* Theft Over:
    * ([https://data.torontopolice.on.ca/datasets/TorontoPS::theft-over-open-data/about](https://data.torontopolice.on.ca/datasets/TorontoPS::theft-over-open-data/about))
* Bicycle Thefts:
    * ([https://data.torontopolice.on.ca/datasets/TorontoPS::bicycle-thefts-open-data/about](https://data.torontopolice.on.ca/datasets/TorontoPS::bicycle-thefts-open-data/about))

## **<span style="text-decoration:underline;">API</span>**

Routes:
* '/neighborhoods':
   * Returns the list of neighborhood names and associated ID numbers to populate the dropdown
* '/crime_data':
   * Format for request = /crime_data?crime_type=<YourCrimeType>&?neighborhood=<NumberOfNeighborhood>&?start_year=<Year>&?end_year=<Year>
   * Returns all data from the selected crime table matching the neighborhood and date range.
* '/radial':
   * Format for request = /radial?neighborhood=<NumberOfNeighborhood>&?start_year=<Year>&?end_year=<Year>
   * Returns the table name and count of occurences for the selected neighborhood and date range.
* '/top5':
   * Format for request = /top5?crime_type=<YourCrimeType>&?start_year=<Year>&?end_year=<Year>
   * Returns the top cities with the lowest occurence of the selected crime within the date range.
   
***NOTE*** If you would like to run this, your postgres table names should match the values in the crime-type selector as they're used to build the queries.
