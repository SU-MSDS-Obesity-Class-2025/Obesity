# Socioeconomic and Lifestyle Determinants of Global Obesity Rates
>Analyzing how socioeconomic factors affect obesity rate across different countries 

## Project Overview


- **Objective:** This project aims to examine how economic status, lifestyle behaviors, and health indicators relate to national obesity rates. By analyzing these variables across countries, we seek to identify key predictors of obesity and understand how social and economic development influence population health outcomes.
- **Domain:** Health
- **Key Techniques:** Regression, Data Imputation, Exploratory Data Analysis



## Quick Start

### Local Setup

#### Mac Setup
```bash
# Install Homebrew (if not already installed)
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

# Install Git LFS via Homebrew
brew install git-lfs

# Clone the repository
git clone https://github.com/SU-MSDS-Obesity-Class-2025/Obesity.git
cd Obesity

# Initialize Git LFS and pull large files
git lfs install
git lfs pull

# Install Python dependencies (use pip3 if needed)
pip3 install -r requirements.txt

# Install nbstripout (strips notebook outputs from Git commits)
pip3 install nbstripout
nbstripout --install
```

#### Windows/Linux Setup
```bash
# Clone the repository
git clone https://github.com/SU-MSDS-Obesity-Class-2025/Obesity.git
cd Obesity

# Install Git LFS (required for large data files)
git lfs install
git lfs pull

# Install Python dependencies
pip install -r requirements.txt

# Install nbstripout (strips notebook outputs from Git commits)
pip install nbstripout
nbstripout --install
```

**Note:** Git LFS is required to download the large data file (`who_obesity_data.csv`). On Windows, download Git LFS from [git-lfs.github.com](https://git-lfs.github.com). 


### Google Colab Setup

**Note:** Large data files are included in the repository. The setup below connects Colab to your Drive so notebooks can access these local data files using relative paths.

1. **Clone to your Google Drive** (one time):
   ```bash
   git clone https://github.com/SU-MSDS-Obesity-Class-2025/Obesity.git
   ```
   This downloads all code and data files to your Drive.

2. **Open notebook from Drive**:
   - Navigate to `Obesity/code/` in your Drive
   - Double-click the notebook to open in Colab

3. **Edit setup collab cell** (one time):
   - Uncomment the setup lines
   - Change the path to where you cloned the repo
   - Example: `os.chdir('/content/drive/MyDrive/Obesity')`


## Project Structure

```
Obesity/
├── code/
│   └── Obesitty_Data_Collection.ipynb         # Download WHO indicator data
├── data/
│   ├── metadata/
│   │   ├── who_indicators_all.csv             # Complete indicator catalog
│   │   ├── who_indicators_obesity_core.csv    # Core indicator definitions
│   │   └── who_indicators_obesity_related.csv # Obesity-related indicators (819)
│   ├── who_obesity_data.csv                   # Main WHO dataset (~689 MB, tracked via LFS)
│   ├── who_obesity_core_data.csv              # Core obesity data (~24 MB)
│   └── Gross national income per capita.csv   # GNI per capita data
└── requirements.txt
```

## Data

The project uses WHO Global Health Observatory data:

### Main Datasets
- **who_obesity_data.csv** - Main dataset (~689 MB, managed with Git LFS) (https://www.who.int/data/gho)
- **who_obesity_core_data.csv** - Core obesity data subset (~46.3 MB) (https://github.com/SU-MSDS-Obesity-Class-2025/Obesity/blob/main/data/who_obesity_core_data.csv)
- **GDP_data.csv** - GDP data from World Bank Group (https://api.worldbank.org/v2/en/indicator/NY.GDP.MKTP.CD?downloadformat=csv)

### Metadata (Indicator Definitions)
- **who_indicators_all.csv** - Complete catalog of all WHO indicators
- **who_indicators_obesity_related.csv** - Curated list of 819 obesity-related indicators
- **who_indicators_obesity_core.csv** - Core indicator definitions (19 indicators)

### Describtion
   - The data in these datasets is from (1990-2022) year.
   - WHO Obesity dataset: 
      - The data in this dataset is collected from Global Health Observatory (GHO)
          (Web source: https://www.who.int/data/gho). The GHO is the WHO's main portal for health-related statistics, providing access to over 1,000 indicators out of them we have collected data for 9 most relavant indicators  
      - It contains Date, Dim1, Dim1Type, Dim2, Dim2Type, Dim3, Dim3Type, High, Id, IndicatorCode, IndicatorName, Low, NumericValue, ParentLocation, ParentLocationCode, SpatialDim, SpatialDimType, TimeDim, TimeDimType, TimeDimensionBegin, TimeDimensionEnd, TimeDimensionValue, Value as columns. It contains 146334 rows in csv format. 

   
   Most Relavent Indicators:

    | Indicator Code                         | Indicator Name                                                                                          |
    |----------------------------------------|---------------------------------------------------------------------------------------------------------|
    | NCD_BMI_30A.                           | Prevalence of obesity among adults, BMI ≥ 30 (age-standardized estimate, %).                            |
    | NCD_DIABETES_PREVALENCE_CRUDE          | Prevalence of diabetes, crude (%)                                                                       |
    | NCD_GLUC_03                            | Raised fasting blood glucose (≥ 7.0 mmol/L) (age-standardized, %)                                       |
    | NCD_PAA                                | Prevalence of insufficient physical activity among adults aged 18+ years (age-standardized estimate, %) |
    | SI_POV_DAY1                            | Proportion of population below the international poverty line (US$1.90/day, %)                          |
    | WHS5_512                               | Population using solid fuels (%).                                                                       |
    | WHOSIS_000001                          | Life expectancy at birth (years)                                                                        |
    | WSH_SANITATION_BASIC                   | Population using at least basic sanitation services (%)                                                 |
    | PHE_HHAIR_PROP_POP_POLLUTING_FUELS     | Proportion of population with primary reliance on polluting fuels (%)                                   |


    - GDP dataset: 
        - The GDP data is collected from World Bank Group (https://api.worldbank.org/v2/en/indicator/NY.GDP.MKTP.CD?downloadformat=csv). It contains GDP data of every country by year with following columns: Country Name, Country Code, Indicator Name, Indicator Code, Year and contains 265 rows in csv format.   

## Requirements
See `requirements.txt`.


