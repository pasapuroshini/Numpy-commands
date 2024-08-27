# Pandas
Useful for Data processing and analysis
**Pandas data frame:**
 2D Tabular data structure with labelled axes (rows and colmns)

 ```
#import pandas library
import pandas as pd
```
**Creating a Pandas Data frame**
```

import pandas as pd
#importing the boston house price data
from sklearn.datasets import load_boston
boston_datset=load_boston()
type(boston_dataset)
print(boston_dataset)
boston_df=pd.DataFrame(boston_dataset.data,columns=boston_dataset.feature_names)
boston_df.shape


```

Importing data from csv file to pandas dataframe
```
# csv file to pandas df
diabetes_df=pd.read_csv('filepath')
type(diabetes_df)
diabetes_df.head()
diabetes_df.shape


```
pandas=panel data ,python data analysis
Pandas allows us to analyze big data and make conclusions based on statistical theories.

Pandas can clean messy data sets, and make them readable and relevant.

Relevant data is very important in data science.

Pandas are also able to delete rows that are not relevant( cleaning of data)
Installation of pandas:
`
pip install pandas
`

`
import pandas 
`

```
import pandas as pd
mydataset={'cars':["BMW,"Volvo","Ford"],'passings':[3,7,2]}
mvar=pd.DataFrame(mydataset)
print(myvar)
```
Checking Pandas version:
```
import pandas as pd

print(pd.__version__)
```
# Series in pandas
A Pandas Series is like a column in a table.
It is a one-dimensional array holding data of any type.

```
import pandas as pd
a=[1,7,2]
myvar=pd.Series(a);
print(myvar)
```
output:
```
0    1
1    7
2    2
dtype: int64
```
```
import pandas as pd

a = [1, 7, 2]

myvar = pd.Series(a, index = ["x", "y", "z"])

print(myvar)
```
output:
```
x    1
y    7
z    2
dtype: int64
```

```
import pandas as pd

calories = {"day1": 420, "day2": 380, "day3": 390}

myvar = pd.Series(calories)

print(myvar)
```
output:

```
day1    420
day2    380
day3    390
dtype: int64
```

```
import pandas as pd

calories = {"day1": 420, "day2": 380, "day3": 390}

myvar = pd.Series(calories, index = ["day1", "day2"])

print(myvar)
```

output:

```
day1    420
day2    380
dtype: int64
```
