# Data Analysis with Pandas

## Requirements on OS
* pip
* python

## Installing ipython
```bash
pip install ipython
```
* IPython is just like the normal shell you get when you run `python`, but IPython provides better printing for large text. This ability makes IPython suitable for data analysis because the program prints data in a well-structured format.

## Installation of Pandas
``` bash
pip install pandas
```

## Basic Usage of ipython and pandas
```python
ipython #(Interactive Shell)

import pandas

df1 = pandas.DataFrame([[2,4,6],[10,20,30]],columns=["Price","Age","Value"],index=["First","Second"])
df1

df2= pandas.DataFrame([{"Name":"John","Surname":"Snow"},{"Name":"Jack"}])
df2
```
## Installation of Jupyter Notebooks
``` bash
pip install jupyter
```
## Basic Usage of jupyter
```bash
jupyter notebook # Opens a website as empty notebook
#inside the notebook, select environment as python 3 that you have installed on your machine.
#Top Right, Select for New as dropdown and choose python 3.
```
```python
import os
os.listdir()

import pandas
df1=pandas.read_csv("supermarkets.csv")
df1

df2=pandas.read_json("supermarkets.json")
df2
```
* Check jupyter.ipynb file as Output

### Note on Loading Excel Files

```bash
pip install xlrd
```
```python
df3=pandas.read_excel("supermarkets.xlsx",sheet_name=0)
df3

df4=pandas.read_csv("supermarkets-commas.txt")
df4

df5=pandas.read_csv("supermarkets-semi-colons.txt",sep=";")
df5
```
### Check correct attributes to use in pandas module
```python
pandas.read_csv?
```
### Set Header Row ...cont

### Set Column Names ..cont

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License
[MIT](https://choosealicense.com/licenses/mit/)