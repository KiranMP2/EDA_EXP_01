**##Experiment 1: EDA in IPL Dataset**

**Aim:**
To perform Exploratory Data Analysis (EDA) on the IPL matches dataset and derive insights about matches per season, winning teams, toss decisions, and top venues.

**Algorithm / Procedure:**

**1.Import Libraries**
  Import pandas for data handling.
  Import matplotlib and seaborn for visualization.
**2.Load Dataset**
  Use pd.read_csv() to load the IPL matches dataset.
  Check dataset shape using .shape.
  View first 5 rows using .head().
**3.Matches per Season (Univariate Analysis)**
  Group data by season and count matches.
  Plot a bar chart to visualize growth/decline in matches.
**4.Top Winning Teams (Univariate Analysis)**
  Use value_counts() on the winner column.
  Plot top 5 winning teams in a bar chart.
**5.Toss Decisions (Univariate Analysis)**
  Count toss decision preferences (bat vs field).
  Plot results using a bar chart.
**6.Top Venues (Univariate Analysis)**
  Count matches per venue.
  Display top 5 venues with a horizontal bar chart.
**7.Draw Insights**
  Observe patterns in toss decisions.
  Identify teams with consistent winning trends.
  
  **Program**
```import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
matches = pd.read_csv("matches.csv")
print("Dataset Shape:",matches.shape)
print("columns:",matches.columns)
print(matches.head())
matches_per_season = matches['season'].value_counts().sort_index()
matches_per_season
plt.figure()
matches_per_season.plot(kind='bar')
plt.xlabel("Season")
plt.ylabel("Number of Matches")
plt.title("Matches Played Per IPL Season | SYED SAIF : 212224230286")
plt.show()
team_wins = matches['winner'].value_counts()
team_wins
top_5_teams = team_wins.head(5)
top_5_teams
plt.figure()
top_5_teams.plot(kind='bar')
plt.xlabel("Team")
plt.ylabel("Number of Wins")
plt.title("Top 5 Winning Teams in IPL | SYED SAIF : 212224230286")
plt.xticks(rotation=45)
plt.show()
toss_decision_counts = matches['toss_decision'].value_counts()
toss_decision_counts
plt.figure()
toss_decision_counts.plot(kind='bar')
plt.xlabel("Toss Decision")
plt.ylabel("Number of Times Chosen")
plt.title("Toss Decision Preference in IPL | SYED SAIF : 212224230286")
plt.show()
venue_counts = matches['venue'].value_counts()
venue_counts
```
  **Output**
  ![SDKH](https://github.com/user-attachments/assets/8513925c-67ac-4cad-9869-91f5d7cb5e22)
![KJCSB](https://github.com/user-attachments/assets/feb6a005-13ea-46a6-b340-cf9db90310c8)
![HWJCS](https://github.com/user-attachments/assets/62c1d358-d530-45d0-8664-6fa07e95d241)
![HWVJD](https://github.com/user-attachments/assets/e067e2c0-79c0-430a-896f-3d1914462f3a)
![DWKG](https://github.com/user-attachments/assets/05906d96-72d8-42e8-9f4d-2e08f77d551b)
![JV](https://github.com/user-attachments/assets/ebe9213f-f2ce-45ed-bde3-82dd84a07899)


 ** Result**
  This experiment is executed successfully



Highlight the stadiums hosting maximum matches.
