# Stroke-Prediction
Import Datasets
```python
df = pd.read_csv("healthcare-dataset-stroke-data.csv")
```
## Preprocessing<br>
### Check Missing value
```python
df.isnull().sum() #check missing value
```
Output
```
id                     0
gender                 0
age                    0
hypertension           0
heart_disease          0
ever_married           0
work_type              0
Residence_type         0
avg_glucose_level      0
bmi                  201
smoking_status         0
stroke                 0
```
Found a missing value namely BMI value.
### Handling Missing Values
Plot graph to see the frequency range of BMI values.<br><br>
![Screenshot 2567-03-03 at 03 01 08](https://github.com/Tanachock/Stroke-Prediction/assets/160312026/8cc04d35-3231-4119-947c-46c154e6be3b)<br>

The frequency of BMI values ​​is between 20 and 40.<br>
Use the mean instead of missing values.<br>
```python
avg = df['bmi'].mean()

df.bmi = (df.bmi.fillna(28.89))
print("AVG of this Adult BMI values = ", avg)
```
Output
```
28.89
```
Check target
