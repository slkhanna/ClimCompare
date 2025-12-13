# ClimCompare
Google Earth Engine User Interface Comparing PRISM Monthly and DaymetV4 Daily Climate Datasets  
\
**Author:** Shobha L Khanna (skhanna4@ucmerced.edu)  
**Last Updated:** 12th Dec 2025  
**DOI:** TODO
## Description
ClimCompare is a data product from the Secure Water Future Grant that is a User Interface (UI) created using Google Earth Engine. ClimCompare compares the two prominent climate datasets for the western United States: the DaymetV4 daily climate dataset produced by NASA and the PRISM monthly climate dataset produced by Oregon State University. The ClimCompare UI allows you to see spatially where the Daymet model estimates higher(red), lower(blue) or similar(white) values of temperature or precipitation compared to PRISM. Differences in Daymet and PRISM values for annual average minimum temperature, annual average maximum temperature and annual total precipitation can be visualized. Additional visualizations include the difference in Daymet and PRISM values as a ratio of the PRISM values, for annual average minimum temperature, annual average maximum temperature and annual total precipitation. Lastly, differences in Daymet and PRISM values for minimum temperature degree days and maximum temperature degree days are also provided. All Daymet and PRISM comparisons were calculated for each year from 1980 to 2024, and clicking anywhere on the map will pull up a time-series of how the Daymet and PRISM comparison changed at the clicked location over time.  
\
**Dependencies:** Google Earth Engine Code Editor (https://code.earthengine.google.com/)  
**Access UI:** https://ee-skhanna4.projects.earthengine.app/view/climcompare    
**Access Script:** https://code.earthengine.google.com/?accept_repo=users/slkhanna4/prismvdaymet  
A copy is provide in .txt format as well
## Utilization
### For UI
The starting display of the UI is the annual total percipitation difference between Daymetv4 and PRISM of the western United States in the year 1980. In the bottom right there is panel with a slider that can be shifted to display a different year, and on top of it is another panel with which the desired climate comparison band can be chosen. On the right hand side is also a color bar signifiying the numerical values the colors correspond to. Additionally, clicking anywhere on the displayed image will pull up a time series graph on the bottom right of the display that shows how the current climate comparison band changed from 1980 to 2024.
### For Code
There are 4 modes that can be run from the Google Earth Engine Script:  
**(1) assetcreate:** Runs a loop to export the produced PRISM and Daymet annual comparison images to a google earth engine asset.  
**(2) assetview:** (DEFAULT) The UI runs using the imported PRISM and Daymet annual comparison image assets.  
**(3) rawview:** The UI runs using the realtime calculated PRISM and Daymet annual comparison images.  
**(4) finer_rawview:** The UI runs using the realtime calculated PRISM and Daymet annual comparison images while keeping Daymet's higher spatial resolution.  
\
To run a mode make sure its boolean is set to **True** and that all other modes are set to **False**. Additionally, both **rawview** and **finer_rawview** modes run slowly and cannot render the entire scene.
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

