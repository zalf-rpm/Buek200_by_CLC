# Buek200_by_CLC

These soil profile maps for Germany were created using the Buek200 (https://gdz.bkg.bund.de/index.php/default/digitale-geodaten/digitale-landschaftsmodelle/corine-land-cover-5-ha-stand-2018-clc5-2018.html) and the Corine Landcover Map 2018 (https://gdz.bkg.bund.de/index.php/default/digitale-geodaten/digitale-landschaftsmodelle/corine-land-cover-5-ha-stand-2018-clc5-2018.html). Where possible, soilprofiles were assigned selecting the profile according to the landusage codes. 
In case of mismatches, similar or neighboring profiles were selected. In areas, where the Buek does not provide profiles, neighboring profiles were selected.

# EPSG 4326
In the folder EPSG_4326 there are two resolutions - approximately 100m x 100m and 1000m x 1000m. The latter aligns with the weather data as NetCDF from DWD. 
It is not provided as ASCII grid since the grid cells are not perfect squares- a coversion is possible, but most software can not handle such ASCII grids. 

# EPSG 25832
In this CRS only one resolution is provided (1000m x 1000m). This grid perfectly aligns with grids used in MONICA.

# Soil data in the grid files
The information in BAND 1 of the files clc_buek_4326_100m.tif,  clc_buek_4326_1000m.tif and clc_buek_grid_profile_25832_general.asc contain the soilprofile_id of the database buek200_by_clc.db. The profiles can be retreived from the view soil_profile_all or from the table buek_soilprofile.

Four types of soil data maps are available:

no suffix: 	Profiles are selected based on the actual land use.
    '21': 	Where available in the Buek200, agricultural soil profiles are selected. 
    		All other areas are filled from the general map. This means that agricultural 
    		profiles might also be available for areas where the Buek200 does not provide any.
    '23': 	Where available in the Buek200, pasture soil profiles are selected. 
    		All other areas are filled from the general map. This means that pasture 
    		profiles might also be available for areas where the Buek200 does not provide any.
    '31': 	Where available in the Buek200, forest soil profiles are selected. 
    		All other areas are filled from the general map. This means that forest 
    		profiles might also be available for areas where the Buek200 does not provide any.
    		
   clc_buek_4326_21:	   	Band 1: buek_soilprofile_id
   clc_buek_4326_21_clc:	Band 1: Buek Corine Landcover Code
   clc_buek_4326_23:	   	Band 1: buek_soilprofile_id
   clc_buek_4326_23_clc:	Band 1: Buek Corine Landcover Code
   clc_buek_4326_4326_31:	Band 1: buek_soilprofile_id
   clc_buek_4326_31_clc:	Band 1: Buek Corine Landcover Code
   clc_buek_4326:	   	Band 1: buek_soilprofile_id	
   clc_buek_4326_clc: 		Band 1: Buek Corine Landcover Code

# Corine Landcover Codes (CLC)
|   |   |   | Name 1st digit | Name 2nd digit | Name 3rd digit |
| - | - | - | ------------------- | ----------------- | ----------------------- |
| 1 | 1 | 1 | Artificial surfaces | Urban fabric | Continuous urban fabric |
| 1 | 1 | 2 | Artificial surfaces | Urban fabric | Discontinuous urban fabric  |
|| 1| 2| 1| Artificial surfaces| Industrial, commercial and transport units| Industrial and commercial units |
| 1| 2| 2| Artificial surfaces| Industrial, commercial and transport units| Road and rail networks and associated land |
| 1| 2| 3| Artificial surfaces| Industrial, commercial and transport units| Port areas |
| 1| 2| 4| Artificial surfaces| Industrial, commercial and transport units| Airports |
| 1| 3| 1| Artificial surfaces| Mine, dump and construction sites| Mineral extraction sites |
| 1| 3| 2| Artificial surfaces| Mine, dump and construction sites| Dump sites |
| 1| 3| 3| Artificial surfaces| Mine, dump and construction sites| Construction sites |
| 1| 4| 1| Artificial surfaces| Artificial non-agricultural vegetated areas| Green urban areas |
| 1| 4| 2| Artificial surfaces| Artificial non-agricultural vegetated areas| Sport and leisure facilities |
| 2| 1| 1| Agricultural areas| Arable land| Non-irrigated arable land |
| 2| 1| 2| Agricultural areas| Arable land| Permanently irrigated land |
| 2| 1| 3|Agricultural areas| Arable land| Rice fields |
| 2| 2| 1| Agricultural areas| Permanent crops| Vineyards |
| 2| 2| 2| Agricultural areas| Permanent crops| Fruit trees and berry plantations |
| 2| 2| 3| Agricultural areas| Permanent crops| Olive groves |
| 2| 3| 1| Agricultural areas| Pastures| Pastures |
| 2| 4| 1| Agricultural areas| Heterogeneous agricultural areas| Annual crops associated with permanent crops |
| 2| 4| 2| Agricultural areas| Heterogeneous agricultural areas| Complex cultivation patterns |
| 2| 4| 3| Agricultural areas| Heterogeneous agricultural areas| Land principally occupied by agriculture, with significant areas of natural| vegetation |
| 2| 4| 4| Agricultural areas| Heterogeneous agricultural areas| Agro-forestry areas |
| 3| 1| 1| Forests and semi-natural areas| Forests| Broad-leaved forest |
| 3| 1| 2| Forests and semi-natural areas| Forests| Coniferous forest |
| 3| 1| 3| Forests and semi-natural areas| Forests| Mixed forest |
| 3| 2| 1| Forests and semi-natural areas| Shrub and/or herbaceous vegetation association| Natural grassland |
| 3| 2| 2| Forests and semi-natural areas| Shrub and/or herbaceous vegetation association| Moors and heathland |
| 3| 2| 3| Forests and semi-natural areas| Shrub and/or herbaceous vegetation association| Sclerophyllous vegetation |
| 3| 2| 4| Forests and semi-natural areas| Shrub and/or herbaceous vegetation association| Transitional woodland shrub |
| 3| 3| 1| Forests and semi-natural areas| Open spaces with little or no vegetation| Beaches, dunes, and sand plains |
| 3| 3| 2| Forests and semi-natural areas| Open spaces with little or no vegetation| Bare rock |
| 3| 3| 3| Forests and semi-natural areas| Open spaces with little or no vegetation| Sparsely vegetated areas |
| 3| 3| 4| Forests and semi-natural areas| Open spaces with little or no vegetation| Burnt areas |
| 3| 3| 5| Forests and semi-natural areas| Open spaces with little or no vegetation| Glaciers and perpetual snow |
| 4| 1| 1| Wetlands| Inland wetlands| Inland marshes |
| 4| 1| 2| Wetlands| Inland wetlands| Peatbogs |
| 4| 2| 1| Wetlands| Coastal wetlands| Salt marshes| 4| 2| 2| Wetlands| Coastal wetlands| Salines |
| 4| 2| 3| Wetlands| Coastal wetlands| Intertidal flats |
| 5| 1| 1| Water bodies| Inland waters| Water courses |
| 5| 1| 2| Water bodies| Inland waters| Water bodies |
| 5| 2| 1| Water bodies| Marine waters| Costal lagoons |
| 5| 2| 2| Water bodies| Marine waters| Estuaries |
| 5| 2| 3| Water bodies| Marine waters| Sea and ocean |
