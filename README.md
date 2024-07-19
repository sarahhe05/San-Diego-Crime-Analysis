# San Diego Crime Analysis 🚓
We are interested in the trends that are present in San Diego crimes, included the location and times these crimes occur. To explore these correlations, we downloaded the dataset from https://data.sandiego.gov/datasets/police-nibrs/.

## Data Cleaning
We removed columns that didn't have relevant information. The columns we kept are:
- `case_number`: the SDPD case number used for tracking purposes within the SDPD's records management system
- `occured_on`: the date and time the offense occurred
- `pd_offense_category`: the category the offense falls under
- `neighborhood`: the neighborhood the offense occurred in
- `division`: the SDPD division where the offense occurred
- `city`: the city the offense occurred in
- `latitude`: the latitude the offense occurred in
- `longitude`: the longitude the offense occurred in

Specifically, `pd_offense_category` consists of various crime types and a category called 'All Other Offenses'. We removed rows labeled as 'All Other Offenses' since the label did not give sufficient information about the specific type of crime that occurred.

## Exploratory Data Analysis
To begin our EDA, we started by finding the neighborhoods with the most crime occurrences. We found that neighborhoods like East Village, Pacific Beach, and the Midway District had the most crime occurrences. This makes sense since these areas are the downtown areas in San Diego. 

We then looked at the hours during the day when most crimes occurred. We found that most crimes happened during the afternoon and continued into the evening. This is due to the fact that more people are awake and outside to witness and report the crimes.

Lastly, we looked at which of the crimes were the most common. We found that larceny and vandalism were the most common types of crimes followed by simple assault and drug violations. 

## [Dashboard](https://public.tableau.com/app/profile/sarah.he8574/viz/SanDiegoCrimeAnalysis_17214224864360/SanDiegoCrimeAnalysis)
We created a dashboard to showcase key summary statistics and relevant trends. Users can filter through specific crime types using the drop down menu, and the dashboard would display information relevant to those categories.

For summary statistics, our dashboard includes the total case count of the crime that occurred in 2023, the percent change compared to 2021, and the top 3 neighborhoods in which the crime occurred the most over the past four years. While we have data starting from 2020 until now, we believe that the data is disproportionate due to the outbreak of COVID-19 and the fact that 2024 has not yet ended. With those considerations, we used data from 2021 and 2023 for a more informative comparison.

The heatmap displays the locations that each individual case occurred, highlighting areas with the most crime occurrence in red and the least crime occurrence in green.

The Trends Per Hour of Day chart shows what percentage of crimes occurs at a specific time, aggregated by each hour. The Trends Over Time chart shows how crime occurrence changed over the past four years, aggregated by each month. We left out data from July 2024 for this plot since we don’t have data for the full month at the time of creating this project. Users can select multiple crime types and compare trends of selected types on the same plot.

[![San-Diego-Crime-Analysis](https://github.com/user-attachments/assets/c25240d1-7ada-4037-b4de-8816fbc4b532)](https://public.tableau.com/app/profile/sarah.he8574/viz/SanDiegoCrimeAnalysis_17214224864360/SanDiegoCrimeAnalysis)
