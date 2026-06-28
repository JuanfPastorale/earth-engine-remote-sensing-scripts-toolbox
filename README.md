# earth-engine-remote-sensing-scripts-toolbox
Scripts for google earth engine, based on NASA ARSET courses. Updated and optimized.
### 🌿 Vegetation Monitoring Toolbox (`vegetation_indices_l8.js`)
* **Description:** Extracts, cleans, and processes a time-series of Landsat 8 Collection 2 (Surface Reflectance) imagery to calculate and compare three essential vegetation metrics over the San Francisco Bay Area.
* **Core Technical Implementation:**
  * **NDVI (Normalized Difference Vegetation Index):** Implemented via standard normalized differences to establish a baseline for chlorophyll activity and green biomass.
  * **EVI (Enhanced Vegetation Index):** Processed using custom `image.expression()` to de-noise atmospheric interference and prevent saturation in high-density forest canopies.
  * **SAVI (Soil-Adjusted Vegetation Index):** Configured with a soil-brightness correction factor ($L = 0.5$) to accurately measure canopy cover in areas with exposed or low-density soil backgrounds.
* **Key GEE Concepts Demonstrated:** Spatial (`filterBounds`) and temporal (`filterDate`) reduction, metadata filtering (`CLOUD_COVER_LAND`), bulk parallel processing using `.map()` on an `ImageCollection`, and temporal aggregation via `.mean()`.
