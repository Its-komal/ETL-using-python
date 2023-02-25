# ETL-using-python

Create API URL from website
Most websites have API enabled and so we just need to create the URL for them as given in their documentation it may differ for different websites.
Setting parameters for the data to pull in from the API
There are different parameters which we need to set in the API to get the required data depending on the kind of data we want to get from the API.
Different parameters include: dates, filters, accounts, etc. We need to set these parameters to get the required data.
For example if we want to pull in the data for a specific area so we need to set a specific location code for the API.
Similarly if we want to get all the data from the website for a certain period of time (say, the last 30 days) so we can set this parameter in the API to get the required data.

Pulling in the Data
After setting all the parameters we need to pull the data in from the API and store it in a json format so that we can easily process the data and analyse it further for any specific insights.
This data is pulled by a function in code written in Python using pandas
Since the output we got from the API is in json format we need to parse the json string in Python Pandas dataframe
Transforming data using Pandas
The data can be present in the list or dictionary in JSON format but we need to convert it into a dataframe so that we can process the data easily for further analysis.
First we need to get a list of all the unique IDs present in the json data which will be in different columns and then populate the corresponding values for those IDs in the second column of the dataframe.
After this, we get the number of records present in our dataset which we need to keep as it is since it is the first record we will get from the API in subsequent requests.
Then we just need to iterate over all the records present in our dataset and add those unique IDs and corresponding values to the third column of our dataframe.
Once this is done we get the desired output and proceed with further processing of the data.

push the data into database using python sql connector
Now since we have all the data stored in a single dataframe we can proceed to push it into the database.
In order to do this we can use a python library called SQL Connector to easily push data into the database.


























