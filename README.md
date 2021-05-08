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

|                       Data Description                       |                     File Location                   |    File Type   | Source  |
| :----------------------------------------------------------: | :-------------------------------------------------: | :------------: | :---------------: |
|      Boundaries of Massachusetts Planning Organizations      |       data > vector > MassDOT > MPO_Boundaries      | ESRI Shapefile | [MassDOT](https://geo-massdot.opendata.arcgis.com/datasets/mpo-boundaries) |
|                Massachusetts ZCTA Boundaries                 |     data > vector > Census > tl_2010_25_zcta510     | ESRI Shapefile | [US Census Bureau](https://www.census.gov/cgi-bin/geo/shapefiles/) |
|                    ACS Age & Sex Estimates                   |          data > tabular > ACSST5Y2019.S0101         |       csv      | [US Census Bureau](https://www.census.gov/acs/www/data/data-tables-and-tools/subject-tables/) |
|                Massachusetts Farmers Markets                 |      data > vector > MassGIS > FARMERSMARKETS_PT    | ESRI Shapefile | [MassGIS](https://docs.digital.mass.gov/dataset/massgis-data-farmers-markets) |
|                Massachusetts Public Libraries                |        data > vector > MassGIS > LIBRARIES_PT       | ESRI Shapefile |[MassGIS](https://docs.digital.mass.gov/dataset/massgis-data-libraries)|
|                 Massachusetts State Outline                  |      data > vector > MassGIS > OUTLINE25K_POLY      | ESRI Shapefile |[MassGIS](https://docs.digital.mass.gov/dataset/massgis-data-state-outlines)|
|                Boston Region MPO Restaurants                 |                    OpenStreetMap                    |  |[OpenStreetMap](https://www.openstreetmap.org/)|
|                 Impervious Surface, Boston                   |  data > raster > NLCD > NLCD_2016_Impervious_Boston |     GeoTIFF    |[Multi-Resolution Land Characteristics Consortium (MRLC)](https://www.mrlc.gov/data/nlcd-2016-percent-developed-imperviousness-conus)|
|                      Land Cover, Boston                      |  data > raster > NLCD > NLCD_2016_Land_Cover_Boston |     GeoTIFF    |[MRLC](https://www.mrlc.gov/data/nlcd-2016-land-cover-conus)|
|                      Tree Canopy, Boston                     | data > raster > NLCD > NLCD_2016_Tree_Canopy_Boston |     GeoTIFF    |[MRLC](https://www.mrlc.gov/data/nlcd-2016-usfs-tree-canopy-cover-conus)|

### Packages used
- rasterio
- numpy
- geopandas
- pandas
- matplotlib.pyplot
- scipy (ndimage)
- rasterstats (zonal_stats)

### Acknowledgments
- OpenStreetMap

### Resources Used

- UEP239 previous homework exercises 
- Uku Uustalu's brain
- https://stackoverflow.com/questions/20970279/how-to-do-a-left-right-and-mid-of-a-string-in-a-pandas-dataframe#20970328