


# Final Project - DATA ANALYSIS










## Question 1
```python
print("\nQuest 1: Data column types")
print(df.dtypes)
````
Unnamed: 0         int64
id                 int64
date              object
price            float64
bedrooms         float64
bathrooms        float64
sqft_living        int64
sqft_lot           int64
floors           float64
waterfront         int64
view               int64
condition          int64
grade              int64
sqft_above         int64
sqft_basement      int64
yr_built           int64
yr_renovated       int64
zipcode            int64
lat              float64
long             float64
sqft_living15      int64
sqft_lot15         int64
dtype: object




## Question 2
```python
df.drop(["id", "Unnamed: 0"], axis=1, inplace=True)
print("\nPregunta 2: Resumen estadístico después de eliminar columnas 'id' y 'Unnamed: 0'")
print(df.describe())

# Manejar valores faltantes en las columnas "bedrooms" y "bathrooms"
print("\nNAN values befor replace:")
print("bedrooms:", df['bedrooms'].isnull().sum())
print("bathrooms:", df['bathrooms'].isnull().sum())

mean_bedrooms = df['bedrooms'].mean()
df['bedrooms'].replace(np.nan, mean_bedrooms, inplace=True)
mean_bathrooms = df['bathrooms'].mean()
df['bathrooms'].replace(np.nan, mean_bathrooms, inplace=True)

print("\nNAN values after:")
print("bedrooms:", df['bedrooms'].isnull().sum())
print("bathrooms:", df['bathrooms'].isnull().sum())
````
              price      bedrooms  ...  sqft_living15     sqft_lot15
count  2.161300e+04  21600.000000  ...   21613.000000   21613.000000
mean   5.400881e+05      3.372870  ...    1986.552492   12768.455652
std    3.671272e+05      0.926657  ...     685.391304   27304.179631
min    7.500000e+04      1.000000  ...     399.000000     651.000000
25%    3.219500e+05      3.000000  ...    1490.000000    5100.000000
50%    4.500000e+05      3.000000  ...    1840.000000    7620.000000
75%    6.450000e+05      4.000000  ...    2360.000000   10083.000000
max    7.700000e+06     33.000000  ...    6210.000000  871200.000000



NAN values befor replace:
bedrooms: 13
bathrooms: 10

NAN values after:
bedrooms: 0
bathrooms: 0




## Question 3 

```python
print("\nPregunta 3: Conteo de casas por número de pisos")
floor_counts = df['floors'].value_counts().to_frame()
print(floor_counts)
````
 count
floors       
1.0     10680
2.0      8241
1.5      1910
3.0       613
2.5       161
3.5         8



## Quesiton 4
Below are some examples of simple arithmetic expressions:  
- Addition: `3 + 5`  
- Multiplication: `4 * 6`  
- Division: `10 / 2`  
- Combined: `(5 + 2) * 3`




# This is a simple arithmetic expression to multiply then add numbers
```python
(3 * 4) + 8
````



# This will convert 200 minutes to hours by dividing by 60
```python
minutes = 200
hours = minutes / 60
hours
````


# Objectives for this notebook
```python
objectives = [
    "List popular languages in Data Science",
    "List commonly used libraries",
    "Introduce Data Science tools",
    "Perform arithmetic operations using code",
    "Share notebook via GitHub"
]
for obj in objectives:
    print("-", obj)
````



## Author  
**Ivan Vega**

