# Change Log

## For all .csv files named `2022xx-divvy-tripdata`

- Save a copy of the original .csv as an .xlsx
- Highlight all cells and remove duplicates using Data tab > Data Tools > Remove Duplicates
- Added new column `ride_length` and used `=D2-C2` to calculate time between start and end times. Then changed format to `[h]:mm:ss` to get the length of the ride
- Added new column `ride_distance` and used `=ACOS(COS(RADIANS(90-K2)) *COS(RADIANS(90-I2)) +SIN(RADIANS(90-K2)) *SIN(RADIANS(90-I2)) * COS(RADIANS(L2-J2))) *3959` to calculate the ride distance in miles.
> got the formula [here](https://www.exceldemy.com/calculate-distance-between-two-gps-coordinates-excel/)
- Added new column `day_of_week` and used `=WEEKDAY(C2,1)` to determine which day of the week the ride took place. 1 = Sunday, 7 = Saturday
- Copied the ride length, ride distance, and day of week columns and then pasted them as values only

## Created a single workbook `2022_tripDataCombined`

- moved each individual workbook into a sheet
- rename each sheet to be the corresponding month name
- colored the tabs so that each quarter of the year was a different color
