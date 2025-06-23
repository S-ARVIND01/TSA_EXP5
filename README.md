### DEVELOPED BY: ARVIND S
### REGISTER NO: 212222240012
# Ex.No: 05  IMPLEMENTATION OF TIME SERIES ANALYSIS AND DECOMPOSITION
### Date: 


### AIM:
To Illustrates how to perform time series analysis and decomposition on the monthly average temperature of a city/country and for airline passengers.

### ALGORITHM:
1. Import the required packages like pandas and numpy
2. Read the data using the pandas
3. Perform the decomposition process for the required data.
4. Plot the data according to need, either seasonal_decomposition or trend plot.
5. Display the overall results.

### PROGRAM:
```python
!pip install pandas

import pandas as pd
import matplotlib.pyplot as plt
from statsmodels.tsa.seasonal import seasonal_decompose

# Load dataset (replace with your data)
data = pd.read_csv('/content/AirPassengers.csv')

# Convert 'date' column to datetime format and set as index
data['Month'] = pd.to_datetime(data['Month'])
data.set_index('Month', inplace=True)

# Specify the period for decomposition
period = 12  # Change this to the appropriate period for your data

# Perform decomposition
result = seasonal_decompose(data, model='multiplicative', period=period)

# Plot the decomposition
result.plot()
plt.show()
```

### OUTPUT:
![image](https://github.com/manojvenaram/TSA_EXP5/assets/94165064/d2952d7a-1ff9-42c5-8b54-279190c1f9b2)

### RESULT:
Thus we have created the python code for the time series analysis and decomposition.
