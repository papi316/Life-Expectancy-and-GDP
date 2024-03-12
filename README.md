# Life-Expectancy-and-GDP

import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

df= pd.read_csv(R"C:\Users\Cristian\Downloads\Life-Expectancy-and-GDP-Starter (1)\Life-Expectancy-and-GDP-Starter\all_data.csv")
print(df)

g=sns.FacetGrid(data=df, hue='Country',col="Country",col_wrap=3)
g.map(plt.plot, 'LEABY', 'GDP').add_legend()
