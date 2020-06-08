# Data Analysis with Pandas

## Basic Requirements on OS
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
### Set Header Row
```python
# Adding Header as default
df8=pandas.read_csv("supermarkets-commas.txt", header = None)
df8
```
### Set Column Names
```python
# Adding Header as default
df8.columns= ["ID", "Address", "City", "State", "Country", "Name", "Employees"]
df8
```
### Set Index Column
```python
df8.set_index("ID")
df8
# Assigning permanent value
df9 = df8.set_index("ID")
df9
#different way of assigning index
df8.set_index("ID", inplace=True)
df8

#don't drop column
df8.set_index("Name", inplace=True, drop=False)
df8
```
### Indexing and Slicing
```python
df7=pandas.read_json("http://pythonhow.com/supermarkets.json")
df7
# Label based indexing
df7=df7.set_index("Address")
df7.loc["735 Dolores St":"332 Hill St","Country":"ID"]

# Position based indexing
df7.iloc[:3,1:4]
```
### Deleting Columns and Rows
```python
# Dropping column
df7.drop("City",1)
#dropping based on indexing and columns
df7.drop(df7.index[0:3],0)
df7.drop(df7.columns[0:3],1)
```
### Updating and Adding new columns and Rows
```python
#Adding new column
len(df7.index)
df7["Continent"]=df7.shape[0]*["North Ameirca"]
df7
df7.shape[0]
# Modifying new column
df7["Continent"]=df7["Country"]+"," + "North America"
df7
# converting rows in columns
df7_t=df7.T
df7_t
# adding column which will convert to row
df7_t["My Address"]=["My City","My Country",10,7,"My Shop","My State","My Continent"]
df7=df7_t.T
df7
```
## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License
[MIT](https://choosealicense.com/licenses/mit/)
