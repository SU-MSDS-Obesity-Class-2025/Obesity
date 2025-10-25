# Obesity Research Project

Analyzing how socioeconomic factors affect obesity

## Quick Start

### Local Setup
```bash
git clone https://github.com/SU-MSDS-Obesity-Class-2025/Obesity.git
cd Obesity
pip install -r requirements.txt
```

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
│   └── Obesitty_Data_Collection.ipynb    # Download WHO indicator data
├── data/
│   ├── who_data_part*.csv                # WHO data (split into <75MB files)
│   ├── indicator_catalog.csv             # Catalog of all indicators
│   └── obesity_related_indicators.csv    # List of 808 obesity indicators
└── requirements.txt
```

## Data Files

The project uses WHO Global Health Observatory data split into multiple files:
- **Part files** (`who_data_part1.csv`, etc.) - Main dataset split to stay under 75 MB each
- **Indicator catalog** - Tracks all indicators and their data availability
- **Obesity indicators** - Curated list of 808 obesity-related indicators



