Sentinel-2 Cloud-Free Time Series Extraction Using Google Earth Engine:)
This GEE script processes Sentinel-2 surface reflectance imagery for a specified tile and time period. It includes cloud and cirrus masking based on the QA60 band and bilinear resampling of the B8A band to 10m resolution. The final output is a time series chart of mean B8A reflectance over user-defined points or polygons.

📌 Features
1. Cloud and cirrus removal using QA60 bitmasks

2. Resampling of B8A band to 10m resolution

3. Time series chart of reflectance values over user-defined regions

🛠 How to Use
1. Set your study area tile
   Replace the tile code in the line:

   var tiles = ['29UPA']; // Change this to your tile code(s)
2. Upload and use your point or polygon shapefile
   Add your own points or regions to your GEE assets, and update this line accordingly:

   var shp1 = ee.FeatureCollection('projects/minyanaddtionlparameters/assets/10_29UPA');
Example:
    If you uploaded a shapefile of points for tile 33UXP, the path might be:
    'users/your_username/points_33UXP'

3. Run and visualize
    The script will produce a time series chart of mean B8A reflectance for each region in your shapefile.

📊 Output
Interactive chart showing reflectance trends over time for each region (FID_ used as series label)

Feel free to modify the band selection, date range, or reducer to suit your study needs:)
