# Import libraries
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
import random

# Generate sample dataset
days = ['Monday', 'Tuesday', 'Wednesday', 'Thursday', 'Friday', 'Saturday', 'Sunday']
light_conditions = ['Daylight', 'Darkness - lights lit', 'Darkness - no lighting', 'Darkness - lights unlit']
severity_levels = [1, 2, 3]  # 1=Fatal, 2=Serious, 3=Slight
weather_conditions = ['Fine no high winds', 'Raining no high winds', 'Snowing no high winds',
Fine + high winds', 'Raining + high winds', 'Fog or mist']
road_conditions = ['Dry', 'Wet or damp', 'Snow', 'Frost or ice', 'Flood over 3cm. deep', 'Oil or diesel']

df = pd.DataFrame(data)

# Map severity for readability
severity_map = {1: 'Fatal', 2: 'Serious', 3: 'Slight'}
df['Severity_Label'] = df['Accident_Severity'].map(severity_map)

# --- Chart 1: Accidents per Day ---
plt.figure(figsize=(10, 5))
sns.countplot(data=df, x='Day_of_Week', order=days)
"plt.title(""Number of Accidents by Day of the Week"")"
"plt.xlabel(""Day of Week"")"
"plt.ylabel(""Number of Accidents"")"
plt.xticks(rotation=45)
plt.tight_layout()
plt.show()

# --- Chart 2: Severity by Light Conditions ---
plt.figure(figsize=(12, 6))
sns.countplot(data=df, y='Light_Conditions', hue='Severity_Label')
"plt.title(""Accident Severity under Different Light Conditions"")"
"plt.xlabel(""Number of Accidents"")"
"plt.ylabel(""Light Conditions"")"
"plt.legend(title=""Severity"")"
plt.tight_layout()
plt.show()

# --- Summary Table: Accident counts by Road, Light, and Weather ---
summary = df.groupby(
['Road_Surface_Conditions', 'Light_Conditions', 'Weather_Conditions']
).size().reset_index(name='Accident_Count')

"print(""Summary of Accidents by Road Condition, Light Condition, and Weather:"")"
print(summary.to_string(index=False))  # Print summary without row indices

# --- Chart 3: Accident Counts by Road Condition and Weather ---
plt.figure(figsize=(14, 7))
sns.countplot(data=df, x='Road_Surface_Conditions', hue='Weather_Conditions')
plt.title('Accident Counts by Road Condition and Weather')
plt.xlabel('Road Surface Condition')
plt.ylabel('Number of Accidents')
plt.xticks(rotation=45)
plt.legend(title='Weather Conditions', bbox_to_anchor=(1.05, 1), loc='upper left')
plt.tight_layout()
plt.show()
