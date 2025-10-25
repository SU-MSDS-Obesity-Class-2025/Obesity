# Obesity Research Project

Analyzing how socioeconomic factors affect obesity

## Quick Start

### Local Setup
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

**Note:** Git LFS is required to download the large data file (`who_obesity_data.csv`). 


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

## Data Files

The project uses WHO Global Health Observatory data:

### Main Datasets
- **who_obesity_data.csv** - Main dataset (~689 MB, managed with Git LFS)
- **who_obesity_core_data.csv** - Core obesity data subset (~24 MB)
- **Gross national income per capita.csv** - GNI per capita data

### Metadata (Indicator Definitions)
- **who_indicators_all.csv** - Complete catalog of all WHO indicators
- **who_indicators_obesity_related.csv** - Curated list of 819 obesity-related indicators
- **who_indicators_obesity_core.csv** - Core indicator definitions (19 indicators)



