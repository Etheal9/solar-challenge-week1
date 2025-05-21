☀️ Solar Challenge - Week 1

This is my submission for the Solar Data Discovery challenge - Week 1. The goal was to explore solar energy production data and find interesting patterns using Python and data analysis tools.

 Description

I worked on cleaning the raw dataset, finding trends, and trying to understand how weather conditions like temperature and clouds affect solar power. I also did some simple plots and EDA.

🛠️ Setup

To run this project:

1. Clone the repo:

2. Install the needed libraries:

3. Run the notebook in Jupyter or VS Code.

Data Cleaning

- Converted the timestamps to datetime format
- Removed duplicates
- Filled missing values using forward fill or dropped them if too many
- Removed extra columns that were not related to solar power

Exploratory Data Analysis (EDA)
![Screenshot (724)](https://github.com/user-attachments/assets/5990fb08-af55-4f6d-af69-ed1733f80e6b)
![image](https://github.com/user-attachments/assets/8d8eb163-9c71-48b1-9476-343693084a26)

df_clean.groupby('Cleaning')[['ModA', 'ModB']].mean().plot(kind='bar', title='Effect of Cleaning on ModA & ModB')

![image](https://github.com/user-attachments/assets/a55c7566-107b-4f5b-b3d4-079db1a2fc6a)


import seaborn as sns

corr = df_clean[['GHI', 'DNI', 'DHI', 'TModA', 'TModB']].corr()
sns.heatmap(corr, annot=True, cmap='coolwarm')

![image](https://github.com/user-attachments/assets/b7d7b507-035e-4edf-ab5d-3978d60c3445)



- Found daily and hourly trends in solar output
- Noticed that sunny days had higher power than cloudy ones
- Some weird spikes/outliers were found and ignored during visuals

Files

- `solar_analysis.ipynb`: Main notebook for cleaning + EDA
- `README.md`: This file!

📌 Note

I’m still learning, so this project is more about practicing than perfection. Feedback is welcome!

