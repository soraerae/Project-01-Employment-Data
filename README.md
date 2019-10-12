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
- 
- 
- 
- 
- 
- 
- 
- 
- 
- 
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

### Age Demographic Data Handling: 

### Age Demographic Findings: 
