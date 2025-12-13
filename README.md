# ClimCompare
Google Earth Engine User Interface Comparing PRISM Monthly and DaymetV4 Daily Climate Datasets  
\
**Author:** Shobha L Khanna (skhanna4@ucmerced.edu)  
**Last Updated:** 12th Dec 2025  
**DOI:** TODO
## Description
ClimCompare is a data product from the Secure Water Future Grant that is a User Interface (UI) created using Google Earth Engine. ClimCompare compares the two prominent climate datasets for the western United States: the DaymetV4 daily climate dataset produced by NASA and the PRISM monthly climate dataset produced by Oregon State University. The ClimCompare UI allows you to see spatially where the Daymet model estimates higher(red), lower(blue) or similar(white) values of annual average temperature or annual total precipitation compared to PRISM. Differences in Daymet and PRISM values for annual average minimum temperature, annual average maximum temperature and annual total precipitation can be visualized. Additional visualizations include the difference in Daymet and PRISM values as a percentage of the PRISM values, for annual average minimum temperature, annual average maximum temperature and annual total precipitation. Lastly, differences in Daymet and PRISM values for minimum temperature degree days and maximum temperature degree days are also provided. All Daymet and PRISM comparisons were calculated for each year from 1980 to 2024. Users can select for the Daymet and PRISM comparisons and year using the bottom right panel. Additionally, clicking anywhere on the map will pull up a time-series of how the Daymet and PRISM comparison changed at the clicked location over time from 1980 to 2024.  
\
**Dependencies:** Google Earth Engine Code Editor (https://code.earthengine.google.com/)  
**Access UI:** TODO  
**Access Script:** TODO
## Utilization
TODO  
\
**License:** Apache 2.0
## Bands
|Band Name|Band Label|Description|
|---------|----------|-----------|
|rtmin|Tmin (degC)|DaymetV4 minus PRISM mean annual minimum temperature in degrees Celcius|
|rtmax|Tmax (degC)|DaymetV4 minus PRISM mean annual maximum temperature in degrees Celcius|
|dd_tmin|Tmin Degree Day|DaymetV4 minus PRISM annual sum of minimum temperature in degree days|
|dd_tmax|Tmax Degree Day|DaymetV4 minus PRISM annual sum of maximum temperature in degree days|
|rprcp|Precip (mm)|DaymetV4 minus PRISM annual sum of precipitation in millimeters|
|dif_tmin|Tmin ((Daymet - PRISM)/PRISM)|Difference ratio of DaymetV4 and PRISM mean annual minimum temperature|
|dif_tmax|Tmax ((Daymet - PRISM)/PRISM)|Difference ratio of DaymetV4 and PRISM mean annual maximum temperature|
|dif_prcp|Precip ((Daymet - PRISM)/PRISM)|Difference ratio of Daymet V4 and PRISM annual sum of precipitation|

## Data Sources
### PRISM
**Metadata:**  
https://developers.google.com/earth-engine/datasets/catalog/OREGONSTATE_PRISM_ANm#description (Google Earth Engine Link)  
https://www.prism.oregonstate.edu/documents/PRISM_datasets.pdf  
**References:**  
Daly, C., Halbleib, M., Smith, J.I., Gibson, W.P., Doggett, M.K., Taylor, G.H., Curtis, J., and Pasteris, P.A. 2008. Physiographically-sensitive mapping of temperature and precipitation across the conterminous United States. International Journal of Climatology, 28: 2031-2064  
Daly, C., J.I. Smith, and K.V. Olson. 2015. Mapping atmospheric moisture climatologies across the conterminous United States. PloS ONE 10(10):e0141140. doi:10.1371/journal.pone.0141140
### DaymetV4
**Metadata:**  
https://developers.google.com/earth-engine/datasets/catalog/NASA_ORNL_DAYMET_V4#description (Google Earth Engine Link)  
https://daac.ornl.gov/DAYMET/guides/Daymet_Daily_V4.html  
**References:**  
Thornton, M.M., R. Shrestha, Y. Wei, P.E. Thornton, S-C. Kao, and B.E. Wilson. 2022. Daymet: Daily Surface Weather Data on a 1-km Grid for North America, Version 4 R1. ORNL DAAC, Oak Ridge, Tennessee, USA. doi:10.3334/ORNLDAAC/2129  
Thornton, M.M., R. Shrestha, Y. Wei, P.E. Thornton, S. Kao, and B.E. Wilson. 2020. Daymet: Daily Surface Weather Data on a 1-km Grid for North America, Version 4. ORNL DAAC, Oak Ridge, Tennessee, USA. doi:10.3334/ORNLDAAC/1840
## Acknowledgements
Thanks to Nick Santos for providing UI code skeleton  
This work is supported by Agriculture and Food Research Initiative Competitive Grant no. 2021-69012-35916 from the USDA National Institute of Food and Agriculture

