# uep239-FinalProject

### Summary

This short notebook is a preliminary attempt to find my ideal neighborhood in Boston. Having lived in Somerville 
for half a year pre-Covid, I was interested to find out if there was in fact a more suitable area. I was most interested 
in the following variables, for the reasons below:  

- amount of impervious surface area
    - I'd like to live somewhere with a good amount of green space
- tree canopy
    - The more trees, the better. I'd rather live in a forest, but this is where we are for now.
- proximity to farmer's markets
    - Who doesn't like fresh veggies?
- proximity to libraries
    - I've spent too much on books in grad school, I need to borrow for a while
- proximity to restaurants
    - all that money I'm not spending on books, I can spend on food! Right? 
- Boston land cover
    - I'm curious to see if there's a way to live in a low intensity developed area - but it's not a dealbreaker.
- age data from the 2019 ACS 5-year estimates
    - It'd be nice to hang out with people around my age. But also not a dealbreaker.


### If you want to do something similar:
Create an environment (mine is python-based, but I added a few things), activate it, launch jupyter lab, and get that notebook fired up!

You're welcome to use my data, but I'm guessing your wants and desires are slightly different from mine. Maybe you don't ride a 
bike everywhere and you want to account for metro stop proximity - or a hundred other things. You can replace similar data 
(vector for vector, raster for raster, tabular for tabular) within the analysis and do your own thing. Just make sure 
you change your ranking system accordingly.


### Data used 
I did not personally do any pre-processing on these data; everything you see below was loaded into the notebook and processed there. 
However, the raster data was clipped and projected before I got to it (thanks Uku!). 
- with short descriptions and 
- where the data directory is
- what they are, where they come from

|                   Data Description                 |               File Location              |    File Type   | Source  | Link |
| :------------------------------------------------: | :--------------------------------------: | :------------: | :---------------: | :---------------: |
| Boundaries of Massachusetts Planning Organizations | data > vector > MassDOT > MPO_Boundaries | ESRI Shapefile | [MassDOT](https://geo-massdot.opendata.arcgis.com/datasets/mpo-boundaries) | https://geo-massdot.opendata.arcgis.com/datasets/mpo-boundaries |
|               10%              |                20%             |    High suitability   |          4        |
|               20%              |                60%             |   Medium suitability  |          3        |
|               60%              |                100%            |    Low suitability    |          2        |
|               100%             |                ...             | Very low suitability  |          1        |

```{list-table}
:header-rows: 1
:widths: 10 20 5 5 5 5

* - Filename
  - Description
  - Format
  - Feature
  - CRS
  - Source
* - `MPO_Boundaries`
  - Boundaries of Massachusetts Metropolitan Planning Organizations
  - ESRI Shapefile
  - Polygon
  - [EPSG:3857](https://epsg.io/3857)
  - [MassDOT](https://geo-massdot.opendata.arcgis.com/datasets/mpo-boundaries)
* - `tl_2010_25_zcta510`
  - 2010 Massachusetts 5-Digit Zip Code Tabulation Area (ZCTA) Boundaries
  - ESRI Shapefile
  - Polygon
  - [EPSG:4269](https://epsg.io/4269)
  - [Census Bureau](https://www.census.gov/cgi-bin/geo/shapefiles/)
```



### Brief overview of packages used

### Acknowledgments
- OpenStreetMap

### Resources Used

- UEP239 previous homework exercises 
- Uku Uustalu's brain
- https://stackoverflow.com/questions/20970279/how-to-do-a-left-right-and-mid-of-a-string-in-a-pandas-dataframe#20970328