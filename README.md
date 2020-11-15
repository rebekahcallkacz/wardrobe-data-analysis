# web-design-challenge
Version 1.0.0

[Website](https://rebekahcallkacz.github.io/wardrobe-data-analysis/)

## Description
This project analyzes my personal wardrobe data for purchasing and wear trends. I used gspread to pull in data from Google Sheets, Pandas to clean and analyze data and matplotlib to create visuals.

## Background
In the past few years, I became interested in personal style, and I decided to better understand and thus refine my style (and my fashion purchasing decisions) by tracking what is in my closet, how much it cost me, and how regularly I wear it. 

## Methods

### Data Collection
I keep all of my wardrobe data in a master spreadsheet in Google Sheets. I have a sheet for each area of my wardrobe (tops, bottoms, outerwear, dresses and shoes). In these sheets, I keep metadata on all individual items in my wardrobe included the brand, the type of acquisition (e.g. hand-me-down vs. gift vs. personal purchase), the cost, and the date the item was acquired. I also track how many times I wear items each month. I update my wear counts every time I get dressed to ensure that I do not forget wearing an item. I started tracking on 12/18/2018.  

The data was pulled from Google Sheets using gspread. 

### Data Cleaning
Once the data was pulled in, column names were standardized so that the five sheets could be merged correctly. Once all five sheets were merged, the initial dataset was stored as a csv and then loaded into a Pandas DataFrame. The data was then cleaned for missing rows/values and datatypes were corrected. For the purpose of this analysis, I only included wear counts for 1/2019 - 10/2020 because 12/2018 and 11/2020 did not include wear counts for the entire month at the time of the analysis. Since the Google Sheets version updates total wears, cost per wear and wears per month based on all months in the dataset, these columns also had to be removed. 

You can view the cleaned dataset [here](https://rebekahcallkacz.github.io/wardrobe-data-analysis/Assets/data.html).

### Data Analysis
Three metrics were calculated for each inidividual clothing item: total wears, cost per wear and wears per month. Cost per wear is calculated using the formula *(initial cost + cost of repairs/tailoring)/(total wears)*. Wears per month norms wear frequency by the age of the item and is calculated using the formula *(total wears)/(months owned since 1/2019)*. The actual age of the item is not used in this analysis since wear count data was not available before 1/2019.

## Results
As can be seen in the boxplot below, outside of a few outliers, most items are not worn more than once or twice a month.

#### Wears per Month
![alt text](https://github.com/rebekahcallkacz/wardrobe-data-analysis/blob/main/Assets/Images/wpmcatbox.png "Boxplot Wears per Month")

Although items are not worn frequently, the cost per wear of most items in my wardrobe is relatively low. Most outliers are items that have been acquired recently and thus have not been worn regularly yet. 

#### Cost per Wear
![alt text](https://github.com/rebekahcallkacz/wardrobe-data-analysis/blob/main/Assets/Images/cpwcatbox.png "Boxplot Cost per Wear")

#### Average Wears per Calendar Month
![alt text](https://github.com/rebekahcallkacz/wardrobe-data-analysis/blob/main/Assets/Images/wpmmonthline.png "Average Wears per Calendar Month")

Commentary here. 

## Instructions
Before running this code, you should create an API Key for the News API. You should then run the code in the Jupyter Notebooks in the following folders in this order: 1) data_collection, 2) data_cleaning, and 3) data_analysis. You can customize your API calls to your domains and keywords of interest. 

## Contributors
Rebekah Callari-Kaczmarczyk

## License and Copyright
&copy; Rebekah Callari-Kaczmarczyk