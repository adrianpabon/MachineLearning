
## Series and DataFrames

### Series
Series - 1 dimension 
```
serie = pd.Series(["Item 1", "Item2 2"])
color = pd.Series(["Red","Blue"])
car_make = pd.Series(["Toyota","BMW"])
```

### Dataframes
Dataframes 2 dimensons

```
df = pd.Dataframe({"Car make":car_make, "Color":color})
```

### Describing Data with pandas

```
df.mean(numeric_only=True)
```

### Viewing and Selecting Data