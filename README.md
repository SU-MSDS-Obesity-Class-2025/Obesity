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
```

**Note:** Git LFS is required to download the large data file (`who_obesity_data.csv`, ~689 MB). 
- **Windows:** Download from [git-lfs.github.com](https://git-lfs.github.com/)
- **Mac:** `brew install git-lfs`
- **Linux:** `sudo apt-get install git-lfs` or `sudo yum install git-lfs`

### Google Colab Setup

**Note:** Data files (~600MB) are included in the repository. The setup below connects Colab to your Drive so notebooks can access these local data files using relative paths.

1. **Clone to your Google Drive** (one time):
   ```bash
   git clone https://github.com/SU-MSDS-Obesity-Class-2025/Obesity.git
   ```
   This downloads all code and data files to your Drive.

2. **Open notebook from Drive**:
   - Navigate to `Obesity/code/` in your Drive
   - Double-click the notebook to open in Colab

3. **Edit the first cell** (one time):
   - Uncomment the setup lines
   - Change the path to where you cloned the repo
   - Example: `os.chdir('/content/drive/MyDrive/Obesity')`

4. **Run the setup cell**:
   - Mounts Drive, sets working directory to project root
   - Installs packages from requirements.txt
   - Now relative paths like `../data/` work correctly!


## Project Structure

```
Obesity/
├── code/
│   └── Obesitty_Data_Collection.ipynb         # Download WHO indicator data
├── data/
│   ├── who_obesity_data.csv                   # Main WHO dataset (~689 MB, tracked via LFS)
│   ├── who_obesity_core_data.csv              # Core obesity data (~24 MB)
│   ├── who_obesity_core_indicators.csv        # Core indicator definitions
│   ├── who_indicators_all.csv                 # Complete indicator catalog
│   ├── who_indicators_obesity_related.csv     # Obesity-related indicators
│   ├── indicators_downloaded_log.csv          # Download tracking log
│   └── Gross national income per capita.csv   # GNI per capita data
└── requirements.txt
```

## Data Files

The project uses WHO Global Health Observatory data:
- **who_obesity_data.csv** - Main dataset (~689 MB, managed with Git LFS)
- **who_obesity_core_data.csv** - Core obesity data subset (~24 MB)
- **who_obesity_core_indicators.csv** - Core indicator definitions
- **who_indicators_all.csv** - Complete catalog of all WHO indicators
- **who_indicators_obesity_related.csv** - Curated list of obesity-related indicators
- **indicators_downloaded_log.csv** - Tracks download history and data availability



