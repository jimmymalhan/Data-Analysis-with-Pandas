# Data Analysis with Pandas

## Installing ipython
```bash
pip install ipython
```
* IPython is just like the normal shell you get when you run `python`, but IPython provides better printing for large text. This ability makes IPython suitable for data analysis because the program prints data in a well-structured format.

## Installation of Pandas
``` bash
pip install pandas
```

## Basic Usage
```python
ipython #(Interactive Shell)

import pandas

df1 = pandas.DataFrame([[2,4,6],[10,20,30]],columns=["Price","Age","Value"],index=["First","Second"])
df1

df2= pandas.DataFrame([{"Name":"John","Surname":"Snow"},{"Name":"Jack"}])
df2
```

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License
[MIT](https://choosealicense.com/licenses/mit/)