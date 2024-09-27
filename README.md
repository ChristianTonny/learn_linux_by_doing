# Temperature Data Analysis Project

## Team Workflow and Commands Used

### 1. Branch Creation and Initial Setup (Tonny)
git checkout -b temperature-analysis

### 2. File Movement (Alice)
mv top-5-lowest-temparatures.csv analyzed/

### 3. Naming Convention (Ariane)
mv analyzed/top-5-highest-temperatures.csv analyzed/top-5-highest-temperatures.csv
mv analyzed/top-5-lowest-temparatures.csv analyzed/top-5-lowest-temperatures.csv

### 4. Removing Useless File (Not in your commands, but required by assignment)
rm data/test-1

### 5. Removing Duplicate Rows (Noel)
sort -u data/satellite_temperature_data.csv > data/deduplicated_data.csv

### 6. Extracting Top 5 Highest Temperatures (Larissa and Tonny)
tail -n +2 data/deduplicated_data.csv | sort -t',' -k3 -nr | head -n 5 > analyzed/top-5-highest-temperatures.csv

### 7. Extracting Top 5 Lowest Temperatures (James)
tail -n +2 data/deduplicated_data.csv | sort -t',' -k3 -n | head -n 5 > analyzed/top-5-lowest-temperatures.csv

### 8. Counting Rows (Optional)
wc -l data/satellite_temperature_data.csv

### 9. Extracting Country-Specific Data (Optional)
grep "Rwanda" data/deduplicated_data.csv > analyzed/country-heat-data.csv
