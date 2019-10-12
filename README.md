# Data Analysis of Employment Trends in the US

Using data from the US Bureau of Labor Statistics (BLS), we analyzed employment trends broken down three different ways: region, age demographic, and industry for the past ten years. We wanted to see gross trends in these areas, how the totals further broke down by percentage, and determine what it might look like moving forward based on trends. 

## Dependencies: 
- NumPy
- IPython
- Pandas
- Matplotlib
- Requests
- Scipy
- Xlrd
- OS
- Pathlib

## Technical Work Completed:
- Pulled data from BLS using API and Excel Downloads
- Explored data using Jupyter Notebook
- Used Pandas to clean and format data sets
- Used Matplotlib to create visualizations of data

# Employment Hypotheses and Findings: 
## Regional Data
### BLS Regional Definitions (included 50 states only in analyses): 
- New England— Connecticut, Maine, Massachusetts, New Hampshire, Rhode Island, Vermont
- New York-New Jersey— New Jersey, New York
- Mid-Atlantic— Pennsylvania, Delaware, Maryland, Virginia, West Virginia
- Southeast— Alabama, Florida, Georgia, Kentucky, Mississippi, North Carolina, South Carolina, Tennessee
- Midwest— Illinois, Indiana, Iowa, Michigan, Minnesota, Nebraska, North Dakota, Ohio, South Dakota,  Wisconsin
- Southwest— Arkansas, Louisiana, New Mexico, Oklahoma, Texas
- Mountain-Plains— Colorado, Kansas, Missouri, Montana, Utah, Wyoming
- Western— Alaska, Arizona, California, Hawaii, Idaho, Nevada, Oregon, Washington

### Regional Hypothesis: 
Southwest and West have shown the greatest job growth and the Midwest has shown the greatest job loss.

### Regional Data Handling: 
Unfortunately continuously hitting the BLS API rate limit made pulling the data directly from the API impossible. Fortunately the BLS has options to pull data into Excel files. 

Data on the number of employed persons (non-Farm) was pulled for all 50 states, monthly, for 2008-2018 to be read into a Pandas DataFrame. Once the states information was cleaned the data could be broken down into the BLS regions for ease of analysis. 

### Regional Findings: 
It was surprising that the Midwest was the largest region of employment, as we had expected one of the coastal regions to be the largest. 

As expected, the Western and Southwest regions were among the top growing regions, though Southeast was actually growing at a faster rate thean the Southwest. While the Midwest's growth lagged behind several other regions, enough that the West is becoming the largest employing region, it it not as slow as expected. 

The Mid-Atlantic and New England regions are the slowest growing regions. 

## Industry Data
### Top 10 Industries Analysed: 
- Education and health services
- Wholesale and retail trade
- Health care and social assistance
- Professional and business services
- Retail trade
- Manufacturing
- Leisure and hospitality
- Educational services
- Professional and technical services
- Accommodation and food services

### Industry Hypothesis: 
The tech industry has shown the highest growth, and the retail industry has shown the greatest decline.

### Industry Data Handling: 

### Industry Findings: 

## Age Demographic Data
### Age Group Breakdown: 
- 16-24
- 25-34
- 35-44
- 45-54
- 55-64
- 65+

### Age Demographic Hypothesis: 
Age groups 55+ have seen the highest job growth.
I had several questions I wanted to answer: what was the overall trend in employment, both by age group and overall, what was the percentage of emplyment by age group and has this changed, and what trends might look like moving forward. Line charts show the employment trends clearly. Pie charts breakdown percentage employment by age group. Regression may show trends.

### Age Demographic Data Handling: 
I wanted to look a employment trends based on age demographics. There are two primary sources for this data in the US: the Bureau of Labor Statistics(BLS) and the FRED database from the the St. Louis branch of the US Federal Reserve. After inspecting the two databases, the data I wanted and the functionality of the database pointed to the BLS. The BLS API had example code to perform a request, which I used to pull data on persons employed in six age groups from 2009 to 2018. The API request was relatively straighforward but manipulating the json data into an orgainzed, usable dataframe was more complicated. Once I formed a df that was usable, I saved it to a csv file. This proved beneficial as I started receiving messages I had used my daily allotments of daily requests (even though I hadn't made any that day). I started a new notebook and used the csv file to further clean and then analyze the data. This proved much easier to use.

### Age Demographic Findings: 
All age groups experienced and increase in employment execept the 45-54 group. This was unexpected as this is typically considered part of the peak time frame for employment and earning over a lifetime. Older groups (55-64 and 65 and over) experienced the largest increase in employment and percentage of the population employed. Again, this was taken from the 45-54 group. The other groups remained relatively stable. Total employment was decreasing early in the time period (2009-2010) but has been steadily increasing since. Regression analysis points to ths trend continuing. To much weight on this analysis should be cautioned against however, as time is independent and future trends in employment do not necissarily depend on what has happenbed in the past.
