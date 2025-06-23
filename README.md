# Grouping-and-aggregation# Grouping-and-aggregation

import pandas as pd

data={'Name':['alice','bob','charlie','david','eve'],

'Age':[25,30,35,40,28],

'Salary':[50000,60000,55000,70000,62000],

'Allowences':[2000,3000,2000,2000,4000]

}

df=pd.DataFrame(data)

print("Groups by column and calculates

mean:\n",df.groupby('Name').mean())

print("performs multiple

aggregations:\n",df.groupby('Name').agg(['mean','sum']))

print("Groups by column and calculates

mean:\n",df.pivot_table(values='Salary',index='Name'))

O/P:

Groups by column and calculates mean:

Age Salary Allowences

Name

alice 25.0 50000.0 2000.0

bob 30.0 60000.0 3000.0

charlie 35.0 55000.0 2000.0

david 40.0 70000.0 2000.0

eve 28.0 62000.0 4000.0

performs multiple aggregations:

Age Salary Allowences

mean sum mean sum mean sum

Name

alice 25.0 25 50000.0 50000 2000.0 2000

bob 30.0 30 60000.0 60000 3000.0 3000

charlie 35.0 35 55000.0 55000 2000.0 2000

david 40.0 40 70000.0 70000 2000.0 2000

eve 28.0 28 62000.0 62000 4000.0 4000

Groups by column and calculates mean:

Salary

Name

alice 50000

bob 60000

charlie 55000

david 70000

eve 62000
