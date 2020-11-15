# web-design-challenge
Version 1.0.0

**[Website](https://rebekahcallkacz.github.io/wardrobe-data-analysis/)**

## Description
This project analyzes my personal wardrobe data for purchasing and wear trends. I used gspread to pull in data from Google Sheets, Pandas to clean and analyze data and matplotlib to create visuals.

## Background
In the past few years, I became interested in personal style, and I decided to better understand and thus refine my style (and my fashion purchasing decisions) by tracking what is in my closet, how much it cost me, and how regularly I wear it. 

## Methods

### Data Collection
The original data is stored in Google Sheets. I have a sheet for each area of my wardrobe (tops, bottoms, outerwear, dresses and shoes). In these sheets, I keep metadata on all individual items in my wardrobe included the brand, the type of acquisition (e.g. hand-me-down vs. gift vs. personal purchase), the cost, and the date the item was acquired. I also track how many times I wear items each month. I update my wear counts every time I get dressed to ensure that I do not forget wearing an item. I started tracking this information on 12/18/2018.  

### Data Cleaning
Once the data was pulled in from Google Sheets, column names were standardized so that the five sheets could be merged correctly. Once merged, the initial dataset was stored as a csv and then loaded into a Pandas DataFrame. The data was then cleaned for missing or inconsistent values, and datatypes were corrected. For the purpose of this analysis, I only included wear counts for 1/2019 - 10/2020 because 12/2018 and 11/2020 did not include wear counts for the entire month at the time of the analysis. Since the Google Sheets version calculates total wears, cost per wear and wears per month based on all months in the dataset, these columns also had to be removed. 

You can view the cleaned dataset [here](https://rebekahcallkacz.github.io/wardrobe-data-analysis/Assets/data.html).

### Data Analysis
Three metrics were calculated for each inidividual clothing item: total wears, cost per wear and wears per month. Cost per wear is calculated using the formula *(initial cost + cost of repairs/tailoring)/(total wears)*. Wears per month norms wear frequency by the age of the item and is calculated using the formula *(total wears)/(months owned since 1/2019)*. The actual age of the item is not used in this analysis since wear count data was not available before 1/2019.

## Results
As can be seen in the boxplot below, outside of a few outliers, most items are not worn more than once or twice a month.

#### Wears per Month
![alt text](https://github.com/rebekahcallkacz/wardrobe-data-analysis/blob/main/Assets/Images/wpmcatbox.png "Boxplot Wears per Month")

Although items are not worn frequently, the cost per wear of most items in my wardrobe is relatively low. Most outliers are items that have been acquired recently and thus have not yet been worn more than a few times. 

#### Cost per Wear
![alt text](https://github.com/rebekahcallkacz/wardrobe-data-analysis/blob/main/Assets/Images/cpwcatbox.png "Boxplot Cost per Wear")

Weather also seems to influence at least some categories of clothing including jackets and boots which is not surprising. 

#### Wears per Calendar Month
![alt text](https://github.com/rebekahcallkacz/wardrobe-data-analysis/blob/main/Assets/Images/wpmmonthline.png "Line Graphs Average Wears per Calendar Month")

In addition to wear data, I also analyzed how I acquire items. As can be seen below, these patterns have changed since I started tracking. I am acquiring more slow fashion and less fast fashion which was one of my goals when I started this project. 

#### Item Acquisition
![alt text](https://github.com/rebekahcallkacz/wardrobe-data-analysis/blob/main/Assets/Images/acquisitiontypes.png "Nested Pie Chart Item Acquisitions")

## Instructions
Due to the Google Sheets API requiring authentication, you will not be able to run the code in data_retrieval.ipynb. You can download and run the code in data_cleaning.ipynb. All other Jupyter Notebooks should run without an issues since they only pull in data from CSV files included in this repo.

## Contributors
Rebekah Callari-Kaczmarczyk

## License and Copyright
&copy; Rebekah Callari-Kaczmarczyk