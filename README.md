# Querying and Processing Black Marble Data in R

## Introduction

This repository provides an R tutorial for querying and processing NASA's Black Marble data, designed to be generalizable and intuitive. The tutorial demonstrates how to download, process, and visualize nighttime light data using various R packages.

Black Marble data represents the Earth's surface and atmosphere visible light emissions at night, captured by the Visible Infrared Imaging Radiometer Suite (VIIRS) Day/Night Band (DNB). This data is valuable for applications in urbanization studies, disaster response, and socioeconomic research.

## Prerequisites

### R and RStudio
Ensure that you have R and RStudio installed on your system.

### NASA Earthdata Login and Bearer Token
You need a NASA Earthdata account to access Black Marble data. Follow these steps to obtain your bearer token:

1. Create an Earthdata Account: Register at [NASA Earthdata](https://urs.earthdata.nasa.gov/) if you don't have an account.
2. Generate a Bearer Token:
   - Log in to your Earthdata account.
   - Navigate to [LAADS DAAC](https://ladsweb.modaps.eosdis.nasa.gov/).
   - Click on "Create App Token" and follow the instructions.
   - Copy the generated bearer token.

### R Packages
Install the following R packages:
```install.packages(c("sf", "terra", "tmap", "blackmarbler", "raster", "exactextractr", "lubridate", "geodata", "tidyverse"))```


## Usage

1. Clone this repository:
   ```
   git clone https://github.com/yourusername/black-marble-r-tutorial.git
   ```
2. Open the R script in RStudio.
3. Replace the bearer token placeholder with your actual token.
4. Run the script step by step or source it entirely.

## Code Overview

The script includes the following main steps:

1. Clearing the workspace
2. Setting the bearer token
3. Defining the Region of Interest (ROI)
4. Downloading Black Marble Data
5. Data Processing
   - Imputing Missing Values
   - Transforming the ROI
   - Extracting and Summarizing Data
6. Visualization

For detailed code explanations, please refer to the comments in the R script.

## Notes

- The script uses Sydney, Australia as an example ROI. You can modify this to suit your research needs.
- Data quality flags are used to remove bad quality observations.
- Linear interpolation is applied to handle missing values in the raster data.

## References

- [NASA Black Marble Products](https://blackmarble.gsfc.nasa.gov/)
- [Black Marble User Guide](https://viirsland.gsfc.nasa.gov/PDF/BlackMarbleUserGuide_v1.2_20220916.pdf)
- [LAADS DAAC](https://ladsweb.modaps.eosdis.nasa.gov/)

## Author

Yohan Iddawela

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## Issues

If you encounter any problems or have suggestions, please open an issue in this repository.
