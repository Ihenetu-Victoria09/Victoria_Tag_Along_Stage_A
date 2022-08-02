# Victoria_Tag_Along_Stage_A
import pandas as pd

!pip install jupyter_contrib_nbextensions && jupyter contrib nbextension install

csv_df = pd.read_csv("/Users/Victoria Ihenetu/Desktop/FoodBalanceSheets_E_Africa_NOFLAG(4).csv")
csv_df.to_csv("/Users/Victoria Ihenetu/Desktop/FoodBalanceSheets_E_Africa_NOFLAG(4).csv")
csv_df.head()

FBS_df = pd.read_csv("/Users/Victoria Ihenetu/Desktop/FoodBalanceSheets_E_Africa_NOFLAG(4).csv")
FBS_df.dropna

FBS_df = pd.read_csv("/Users/Victoria Ihenetu/Desktop/FoodBalanceSheets_E_Africa_NOFLAG(4).csv")
FBS_df.to_csv("/Users/Victoria Ihenetu/Desktop/FoodBalanceSheets_E_Africa_NOFLAG(4).csv", index = False)
FBS_df.head(10)

# Total aggregate sum of Animal fat produced in the year 2014 and 2017:
# 2014 = 209460.54
# 2017 = 269617.53

FBS_df.groupby('Item')['Y2017'].sum()



# From the whole dataset the mean and the standard deviation for the year 2015 is: 
# mean in 3 decimal places =135.24
# Standrad deviation in 3 decimal places = 1603.404


FBS_df = pd.read_csv("/Users/Victoria Ihenetu/Desktop/FoodBalanceSheets_E_Africa_NOFLAG(4).csv")
FBS_df.describe(include= "all")




FBS_df.isnull().sum()


import matplotlib.pyplot as plt
import seaborn as sns
import matplotlib

#plt.figure(figsize=(7,4))
#plt.xticks(rotation=90)
#plot = pd.DataFrame(FBS_df)
#sns.barplot(data=plot, x = 'unit', y = 'count')
#plt.xlabel(plot)



#sns.barplot(FBS_df, x='unit', y='count')
#plt.show()

# The year 2017 has the highest sum of Import Quantity

FBS_df.groupby('Element')['Y2018'].sum()

# The total sum of production for the year 2014 = 1931287.75

FBS_df.groupby('Element')['Y2014'].sum()

# In year 2018, Domestic supply quantity has the highest sum = 2161192.10

FBS_df.groupby('Element')['Y2018'].sum()

# In year 2018, Protein supply quantity (g/capita/day) is the third to the lowest 

FBS_df.groupby('Element')['Y2018'].sum()

print(FBS_df['Area'])

FBS_df.groupby('Element')['Area'].count()

FBS_df.groupby('Area'),('Element)['Import Qunatity'].first()



# Total Number of unique countries is 49

FBS_df.groupby('Area')['Area'].count()

