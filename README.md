# Temperature Data Analysis Project

## Team Workflow and Commands Used

### 1. Branch Creation and Initial Setup (Tonny)
git checkout -b temperature-analysis

### 2. File Movement (Alice)
mv data/top-5-highest-temperatures.csv analyzed/
mv data/top-5-lowest-temperatures.csv analyzed/

### 3. Naming Convention (Ariane)
mv analyzed/top-5-highest-temperatures.csv analyzed/top-5-highest-temperatures.csv
mv analyzed/top-5-lowest-temperatures.csv analyzed/top-5-lowest-temperatures.csv

### 4. Removing Duplicate Rows (Noel)
sort -u data/satelite_temperature_data.csv > data/deduplicated_data.csv

### 5. Extracting Top 5 Highest Temperatures (Larissa and Tonny)
grep -v "Country" data/deduplicated_data.csv | sort -t',' -k3 -rn | head -n 5 > analyzed/top-5-highest-temperatures.csv

### 6. Extracting Top 5 Lowest Temperatures (James)
grep -v "Country" data/deduplicated_data.csv | sort -t',' -k3 -n | head -n 5 > analyzed/top-5-lowest-temperatures.csv

### 7. Counting Rows (Optional)
wc -l data/satelite_temperature_data.csv

### 8. Extracting Country-Specific Data (Optional)
grep "Rwanda" data/deduplicated_data.csv > analyzed/country-heat-data.csv
