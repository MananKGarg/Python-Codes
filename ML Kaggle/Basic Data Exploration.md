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
### Interpreting data description
