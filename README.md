Thanks for visiting :-) This project is much work in progress at the moment... 

## London Cycle Hire Schema

The data has been processed to remove trips that:
 - are taken to/from any of *test* stations 
 - were below 60 seconds in length (potentially false starts or users trying to re-dock a bike to ensure it's secure).

Milage estimates are calculated using an assumed speed of 7.456 miles per hour, up to two hours. Trips over two hours max-out at 14.9 miles.


### Scripts sequence
1. Set up 
    1. sql tables
    1. 
    1. 
1. ETL
    1. update
    1. load data
1. EDA
    1. find postcode.  
       When checking for the *best* postcode, the choice is made against *active* postcode, so the final choice could be different from what found on other web services, like Google Maps (see, for example, station 821, for which GM report a *terminated* postcode **SW8 4NN**, instead of the currently active **SW118NR**) 
    1. 
1. Output Data
    1. Stations.csv
    1. Distances.csv
    1. Summary.csv
    1. SummaryS.csv
    1. SummaryE.csv
    1. SummarySE.csv  
       This is too much information to store on GitHub. Ask me for  

### Data Modeling

Factors potentially affecting bike usage:
 - Weather: temperatures, rain, wind
 - local terrain elevation




### Credits

 - Cycle Data.
   - Core datasets at [TFL](http://cycling.data.tfl.gov.uk/)
   - Live data at [TFL API](https://api.tfl.gov.uk/bikepoint)
   - [List of all current bike stations](https://tfl.gov.uk/tfl/syndication/feeds/cycle-hire/livecyclehireupdates.xml)
   - Text to display: **Santander Cycles data supplied at (time) on (date) by Transport for London**
   - Use the Santander Cycles logo to represent the scheme on all applications and services
   - Use this cycle [pushpin icon](http://tfl.gov.uk/cdn/static/cms/images/promos/cycle-hire-pushpin-icon.gif) to indicate the location of Santander Cycles docking stations
 - *postcodes...*
 - *geographic lookups...*
 - *boundaries...*
 - Commuter Work Flow. Census Data. **Source: Office for National Statistics**
 - *Weather Data...* ???
 - Elevation data for the UK at a a resolution of 50 metres at [Ordnance Survey](https://www.ordnancesurvey.co.uk/opendatadownload/products.html#TERR50)
 - The overall design for the shiny app is adapted from [SuperZIP demo @ RStudio Shiny Example](http://github.com/rstudio/shiny-examples/blob/master/063-superzip-example/).



