_Jacob Baker HPV212_

Professor Wu

# ­­Dataset 1 – Monthly Average Home Prices in Chattanooga Vs. Average US Salary from 2000 – 2022

With home prices rising and it is becoming more and more challenging for Americans to purchase a home. I wanted to investigate the housing market here in Chattanooga and compare that to the average salary. I was hoping to be able to find the gap stay consistent but that was not the case. I was able to find the Zillow dataset [here](https://www.zillow.com/research/data/). This dataset contains average monthly home prices that are currently for sale on Zillow for pretty much every locality in the USA. According to figure 2.4, both of these datasets would be considered tables, due to them having rows and columns. They were in the .csv format. Due to the fact that these datasets are both tables, they contain the data types of items and attributes. This dataset displays the data type of ordered quantitative (the price and salaries), as well as sequential data (the time series date range). Since we are working with time series datasets, the semantics would be classified as temporal. That&#39;s because time is the key and is recorded at a specified interval. The first thing after loading in my two datasets was getting it to a workable format. That mainly included filtering out rows that I didn&#39;t need and making sure that dates were actually datetime values and not just strings. Thankfully, these datasets were already averages so I did not need to compute anything. I just needed to plot them correctly. Below you can see the outcome of plotting these two datasets. For visualizing, I used plotly express which looks very nice with a lot of themes to choose form. As well as it being simple and fast to use. The average income was not adjusted for inflation. As you can see housing has steadily risen with a sharper increase during the pandemic, conversely average income has not risen with the cost of housing. The gap only seems to be growing.

![Picture 2](https://i.imgur.com/tZoxWjV.png)

# ­­Dataset 2 – Comparing Apple [AAPL] opening stock prices to Microsoft [MSFT] opening stock prices from 2015 to 2020

For this visualization, I chose to compare two different stocks over a period of 5 years. I found a time series for both Apple and Microsoft stock prices that included opening, closing, high and low prices recorded daily. You can find the datasets both [here](https://www.kaggle.com/tarunpaparaju/apple-aapl-historical-stock-data) and [here](https://www.kaggle.com/vijayvvenkitesh/microsoft-stock-time-series-analysis). The data source is directly from NASDAQ and was downloaded through Kaggle.com. Both datasets were in the form of CSVs, as were all of these time series in this assignment making their type tables with rows and columns. For dataset 2&#39;s data types, they contain both attributes and item types due to their type of table. Again, since we are working with time series, their attribute type would be ordered quantitative, and their semantic type would be temporal since they are time series datasets. For preprocessing I first needed to load in the csv files as separate data frames. The first thing I needed to clean up was making sure that the date columns were datetime values. The extra step that I encountered this time was that in the Microsoft data frame, the date value also hade the timestamp of 14:00 for each row. I needed to remove that time stamp. Next I needed to remove the dollar sign from the apple stick prices and make sure they were floats instead of strings. After that I was able to merge the two data frames on the date column and plot it. Again, using plotly express. I decided not to do any sort of averages as stock prices change so much I wanted to see if there were any drastic dips rather than a smoothed line. As expected, stock prices for both companies steadily increased over the past few years before they drip down very sharply at the start of the pandemic in January of 2020.

![Picture 3](https://i.imgur.com/CCQbGSc.png)

# ­­

#

# Dataset 3 – Comparing Car Crashes in TN, GA, NC with Severity of 4 from 2016-2020

![](https://i.imgur.com/9zRSh3W.png)
The last dataset I chose was &quot;US Accidents &quot;dataset that is [available](https://www.kaggle.com/sobhanmoosavi/us-accidents) on Kaggle.com. This dataset contains every car crash incident from 2016-2020 in 49 states. The team that created this dataset &quot;used multiple APIs that provide streaming traffic incident (or event) data. These APIs broadcast traffic data captured by a variety of entities, such as the US and state departments of transportation, law enforcement agencies, traffic cameras, and traffic sensors within the road-networks. Currently, there are about 1.5 million accident records in this dataset.&quot; The dataset type would be considered a table with its rows and columns. It was made available as a CSV file. Since this is a table, it contains the datatypes of attributes and items. However, this dataset also contains GPS coordinates which I utilized to visualize these crashes, meaning that it also has the position data type. The dataset attributes include categorical with the column of severity, state names, weather conditions, etc. Most of the columns contain categorical data. Even though a lot of the data is numerical we don&#39;t get any meaning from taking one crash severity and say adding to another crash severity. Furthermore, this would be considered a time-varying dataset since crashes are not being recorded in set intervals like a time series but rather as they happen over a period of time. This dataset was by the biggest one io worked with in this assignment, so it required a little bit of work to get it ready for visualization. The first this was obviously getting the data into a pandas data frame. After that I needed to filter it by the states of interest. After it was narrowed down to the three states, I needed to further trim it down to just crashes of severity 4. After that I was ready to pass that through to plot. Using plotly express and a scatter plot, I plotted the gps coordinates of each crash overlayed on a map through mapbox. Thankfully plotly express has all of this built in to the scater.mapbox function. Being a plotly graph, this is a way better experience once in jupyter lab as you can move around and zoom in and out. Furthermore each point will tell you description of the accident. As expected, you will see higher density of sever crashes around major cities like Memphis, Atlanta, Nashville, and Charlotte. I also wanted to see the count of each state&#39;s severity 4 crashes, so I created this simple bar chart with the states grouped by severity.

![](https://i.imgur.com/mGBMX7x.png)
