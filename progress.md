9th May 2025 4:21pm
Beginning scrape of ikman.lk. For the sake of conciseness, only 4-wheeled vehicles (cars, vans, etc.) were considered. Heavy vehicles and special vehicles were also ignored for this. 

4:33 pm 
Created GitHub repository. Excluded promoted ads from the scrape. 

12th May 2025 2:03pm
Decided to automate scrape using BeautifulSoup and a python script.

16th May 2025 5:24pm 
As the BeautifulSoup python script seemed to be working well for my purposes, I modified the script further to extract links from each page of ikman.lk's car ads itself. It does this by finding each element with the "card-link--3ssYv gtm-ad-item" class, extracting the href from each element, and saving it into a list. This list is then passed into the program created previously. 

11:00pm
Added all body types, removed invalid entries. Merged scraper2.py with scraper.py

17th May 2025 4:58pm
Removed duplicates from scrapes2.csv

7:52pm 
Began using the pandas library in python to import the csv and convert it to a dataframe. Read through pandas documentation

8:40pm
Removed commas from Engine Capacity, Mileage, and Price Columns in order for pandas to read it as floats

19th May 2025 11:03am
Converted object classes to numerical values that RandomForestRegressor can handle, using one-hot encoding

12:31pm 
Experimented with different filters (< Rs. 100 million, < Rs. 150 million, < Rs. 200 million) to test the impact of the high end vehicles on the accuracy of the system. Removed data entries with obviously invalid price entries.

Under Rs. 100 Million = RMSE = 5,195,997, 4669 entries
Under Rs. 50 Million = RMSE = 3,878,609, 4290 entries

2:28pm
Began work on scraper2.py, for riyasewana.com, in order to diversify the dataset

20th May 2025 11:59am
Finalized the Riyasewana dataset, cleaning up data entries and combining them in the model
Switched to logs for price values, as data was heavily right-skewed