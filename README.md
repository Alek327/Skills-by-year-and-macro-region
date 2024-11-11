# Skills Data Processing by Region (2010 - 2023)

This project provides R scripts to load, process, and analyze regional skills data across multiple years (2010-2023). The data is organized by skill level (low, middle, high, capitalist) and includes yearly estimates for each specified region.

## Overview

The code processes skill-level data for several regions across multiple years, using separate files for:
- **2014-2023** data: loaded with specific mappings for each year and skill level.
- **2011** data: used to interpolate values for the missing years (2010, 2012, and 2013) and incorporate adjustments.

### Key Functionalities

- **Loading Data**: Reads data from Excel files for specific regions.
- **Mapping and Transformation**: Maps columns to corresponding years and distributes `Total_Wealth` across skill levels.
- **Interpolation**: Estimates missing years (2010, 2012, and 2013) based on existing 2011 data.
- **Saving Results**: Outputs combined data in Excel format for each region and year.

## File Structure

- `Skills_by_region_2014_2023.xlsx`: Input file containing skill-level data from 2014 to 2023.
- `Skills_1995_2011_by_region.xlsx`: Input file containing skill-level data up to 2011, specifically used to estimate values for 2010, 2012, and 2013.
- `Combined_Skills_by_Region_2014_2022.xlsx`: Output file containing processed data for 2014-2022.
- `Completed_Skills_Data_2010_2013.xlsx`: Output file containing interpolated and processed data for 2010-2013.

## Usage

### Prerequisites

Ensure you have the following R libraries installed:

```r
install.packages(c("readxl", "dplyr", "tidyr", "openxlsx"))

## Running the Code

Clone the repository and open the R scripts in your R environment.
Execute each block of code as follows:
For 2014-2023 Data Processing:
Run the first section of the script to load data from Skills_by_region_2014_2023.xlsx.
The processed data will be saved as Combined_Skills_by_Region_2014_2022.xlsx.
For 2010-2013 Data Processing:
Run the second section of the script to load and interpolate the data from Skills_1995_2011_by_region.xlsx.
This will generate the interpolated output file Completed_Skills_Data_2010_2013.xlsx.

## Parameters and Customization

Adjust the national_2010_value in the script if you have a specific national proxy value for 2010.
Modify the skill level distribution percentages if different proportions are needed.

##  Code Structure

The script contains several main functions:

load_data_from_specific_row(): Loads and processes data for each row corresponding to a specific region and year range.
load_2011_data(): Loads data specifically for 2011, used for interpolation.
Skill Distribution Calculation: Applies a 30% (low), 40% (middle), 29.9% (high), and 0.1% (capitalist) distribution to Total_Wealth.
File Export: Saves processed data to Excel files for easy sharing and further analysis.

##  Contributing

Contributions are welcome! Please feel free to submit a pull request or open an issue with any suggestions or improvements.

##  License

This project is licensed under the GNU General Public License.

## Contact

Project developed by Oleksandr Galychyn.  
For questions or further information, feel free to connect through LinkedIn

- LinkedIn: [Oleksandr Galychyn](https://www.linkedin.com/in/oleksandr-galychyn-05187483/)

This `README.md` provides a comprehensive overview, usage instructions, code structure, and sample output to help others understand and run your project easily.


