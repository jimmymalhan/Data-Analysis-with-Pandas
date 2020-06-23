# Geocoding Address with Pandas and Geopy

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
```
### Importing file
```python
import pandas
df7=pandas.read_json("http://pythonhow.com/supermarkets.json")
df7
```

## Installation of Jupyter Notebooks
``` bash
pip install geopy
```
### Fetching coordinated of the 1 row
```python
import geopy
dir(geopy)
from geopy.geocoders import ArcGIS
nom=ArcGIS()
nom.geocode("3995 23 St, San Francisco, CA 94114")
n = nom.geocode("3995 23 St, San Francisco, CA 94114")
n.latitude
n.longitude
type(n)
```
### Fetching coordinates of the whole list
```python
df=pandas.read_json("http://pythonhow.com/supermarkets.json")
df["Address"]=df["Address"]+", "+df["City"]+", "+df["State"]+", " +df["Country"]
df
df["Coordinates"]=df["Address"].apply(nom.geocode)
df
df["Coordinates"]=df["Address"].apply(nom.geocode)
df.Coordinates[0].latitude
# Fetching the list to add Latitude and longitude Column 
df["Latitude"]=df["Coordinates"].apply(lambda x: x.latitude if x !=None else None)
df["Longitude"]=df["Coordinates"].apply(lambda x: x.latitude if x !=None else None)
df
```

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.