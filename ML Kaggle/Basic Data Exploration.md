We use pandas for data interpretation with python

```python

import pandas as pd

```

Most important part of pandas is DataFrame. It holds the table like data.We look at house prices in melbourne data.in here, the data is at the file path '../input/melb_data.csv'
<br>
We load the data with following commands

```python

#save filepath to variable for easier access
melbourne_file_path = '../input/melb_data.csv'

#read the data and store data in DataFrame titled melbourne_data
melbourne_data = pd.read_csv(melbourne_file_path)

#print a summary of data in Melbourne Data
melbourne_data.describe()

```
### Selecting Data for Modeling
We start by picking a few variables from a large set of data. To choose variables/columns, we use columns property of DataFrame

```python

melbourne_file_path = '../input/melb_data.csv'
melbourne_data = pd.read_csv(melbourne_file_path)
melbourne_data.columns

Output - 

Index(['Suburb', 'Address', 'Rooms', 'Type', 'Price', 'Method', 'SellerG',
       'Date', 'Distance', 'Postcode', 'Bedroom2', 'Bathroom', 'Car',
       'Landsize', 'BuildingArea', 'YearBuilt', 'CouncilArea', 'Lattitude',
       'Longtitude', 'Regionname', 'Propertycount'],
      dtype='object')

```
This prints the variables(column headings) in our data
<br>
<br>

missing values are values in data that weren't recorded for some reasons. Melbourne data has some missing values

```python

#For now we would just drop the houses from data
#dropna drops missing values ( think of na as 'not available )

melbourne_data.dropna(axis = 0)

```

There are many ways to select a subset of your data but we will focus on two approaches for now.
<br>
<br>
* Dot notation, which we use to select the "prediction target"
* Selecting with a column list, which we use to select the "features"

<br>

### Selecting the Prediction Target

we can pull out a variablewith dot notation. This single columnis stored in **Series**, which is broadly like a dataFrame with only a single column of data.

<br>
<br>
















