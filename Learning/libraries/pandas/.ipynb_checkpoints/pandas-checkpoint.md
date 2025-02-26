
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
df.sum()
df["column"].sum()
```

### Viewing and Selecting Data
#### crosstab
```
pd.crosstab(cars["Make"], cars["Colour"])
```
#### logic

```
cars[(cars["Make"] == "Toyota") & (cars["Colour"]=="White") ]
```
```
cars[cars["Odometer (KM)"] > 100000]
```
#### groupby
```
cars.groupby(["Make"]).mean(numeric_only=True)
```

#### Convert datatype
```
cars["Price"] = cars["Price"].str.replace('[$,.]','', regex=True).astype(int)
```


### Manipulating Data
```
cars["Make"]=cars["Make"].str.lower()
```
```
missing_data["Odometer"]=missing_data["Odometer"].fillna(missing_data["Odometer"].mean())
```
```
missing_data.dropna(inplace=True)
```
```
seats_column = pd.Series([5,5,5,5,5])
car_clean["Seats"]=seats_column
```

#### Delete a column
```
car_clean.drop("Number of wheels", axis=1)
```
```
car_clean["Total fuel"] = car_clean["Odometer"]*car_clean["fuel"]
```