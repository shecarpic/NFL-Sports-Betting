# NFL Sports Betting :  An Analysis of Factors that Affect how Sportsbooks set Game Spreads and Over/Under Totals

### Repository Overview
- All data used in this analysis can be found in the "Data" folder
- Individual files for each visualization and summary can be found in the "Output Data" folder
- The script used to aggregate the data can be found in the folder labeled "NFL Betting Analysis"
- Link to presentation: https://www.canva.com/design/DAF8C8SzbyA/NkdAK7MRdvNuGN-HHHwVLg/view?utm_content=DAF8C8SzbyA&utm_campaign=designshare&utm_medium=link&utm_source=editor

### Background 
With the legalization of sports betting spread across the country rapidly starting in 2018 when the Supreme Court overturned the Professional and Amateur Sports Protection Act (PASPA). The law effectively made sports betting legal in Nevada and a few other states. With the upcoming Superbowl LVIII (58); our project will focus on how various factors pertaining to how sportsbook set game spreads and over/under total.

## Technology Used and Data Cleaning Process - Miranda Melton

### Data Location 
The original datasets were found in a Kaggle Notebook called "NFL Scores and Betting Data" ("https://www.kaggle.com/datasets/tobycrabtree/nfl-scores-and-betting-data"). 

This data included game results since the 1966 season with betting odds information since 1979. Additional datasets included weather information from NOAA data and NFLweather.com Betting data was used from http://www.repole.com/sun4cast/data.html for 1978-2013 seasons. Pro-football-reference.com data was then cross referenced for betting lines and odds as well as weather data. From 2013 on betting data reflects lines available at sportsline.com and aussportsbetting.com.

The Kaggle Notebook included 3 data sets 
- nfl_stadiums (includes data on location, climate, type, capacity, etc)
- nfl_teams (includes data on historical team names and division/conference placement pre and post 2002)
- spreadspoke_scores (includes game results, spead and over/under information, etc)

### Technology Used 
- Jupyter Notebook
- Python
- Pandas
- MatplotLib
- Numpy
- Pathlib
- Scipy.stats
- Seaborn
- Warnings.filterwarnings

### Cleaning Process 
- Upload the .csv files
- Merge the nfl_stadium and nfl_teams to create a DataFrame called "team_stadium_merged"
- Change the names of the columns to make them easier to read
- Create new DataFrame called "renamed_team_stadium_merged"
- Export that data into a .csv file called "new_team_stadium_data"
- Add any missing relevant data
- Drop columns that were not needed for the analysis
- Reformat the 'Stadium Capacity' numbers so that they match to make analysis easier
- Locate and drop duplicates
- Locate and drop un-needed columns


## Stadium and Team Summaries - Sheena Pickett

### Stadium Summary 

### Quick Facts 
- There are 120 stadiums that have historically be used by the NFL
- Stadiums can be found mostly in the Unitied States with a small percentage located in other countries such as England, Germany, and Mexico
- This data set includes college stadiums which have been used as a team's first location or as a temporary location during a stadium renovation

### Stadium Capacity 

74 stadiums (~62%) have a seating capacity of 50K to 75K. On both extremes, only 4 NFL stadiums have a seating capacity of less than 25K and only 2 NFL stadiums can sit between 100K to 125K spectators. 

![Stadium Capacity Ranges](Output-Data/Stadium-Capacity-Ranges.png)

### Stadium Climate 

Most stadiums in the NFL are located in cold climates (48). It can be noted that there is a significant number of fields where climate does not matter as they are closed-roof, indoor stadiums. 

![Stadium Climates](Output-Data/Stadiums-Climate.png)


### Stadium Field Type

The most popular type of field surface used by the NFL is grass, specifically Bermuda Grass. Only a small percentage of stadiums use various types of artifical turf.

![Stadium Field Type](Output-Data/Stadiums-Surface-Type.png)

### Stadium Type 

Almost all NFL stadiums are considered outdoor stadiums (no roof). It can be theorized that having stadiums that have a stationary or retractable roof are less popular due to extra cost.

![Stadium Type](Output-Data/Stadium-Types.png)


### Team Summary 

### Quick Facts 
- There are a total of 32 teams in the NFL
- There are two conferences (NFC and AFC)
- Each conference is divided into four divisions with four teams in each

### Team Climate
Over half of the teams in the NFL play in moderate to warm climates. What skews this data are the number of teams who play in exlusively indoor stadiums 

![Team Climate](Output-Data/Teams-Climate.png)

### Home Stadium Field Type 
Just like in the Stadium Field Type chart, most teams play on grass fields while the small percentage play any of the various types of artifical turf. 

![Team Field](Output-Data/Team-Surface-Type.png)

### Home Stadium Type
An overwhelming majority of teams play in an outdoor stadium. This makes sense as over half of the teams play in moderate to warm climates.

![Team Stadium](Output-Data/Team-Stadium-Type.png)

### Combined Stadium Capacity by Division 
When comparing the combined stadium capacities for each of the 8 divisions in the NFL, the NFC East is barely ahead of the NFC North (300,944 seats) and AFC East (300,576) divisions with the largest combined stadium capacity of 312,094 seats. 

The division with the lowest total combined stadium capacity of only 209,258 seats is the NFC West. 

![Combined Capacity](Output-Data/Division_Combined_Capacity.png)

## Betting Analysis - Owen Pollard

### Defintions

Spread Betting:
- Where you wager on the margin of victory and the payout is based on the accuracy of the bet.
- Example: or Superbowl 58, the SF 49ers are a 2- point favorite over the KC Chiefs. They are expected to win by 2 or more points

Over/Under Betting:
- A Total Bet aka “Bet” on the amount of points both teams will combine to more or less then the projected total.
- Example: As of 2/6/24, BetMGM has the O/U for SB58 set at 47.5. They expect the Chiefs & 49ers to total 47.5 Points between them. If the score is 24-23, there would be a combined score of 47 ( which is under the line)

### Temperature vs. Over/Under Totals
According to the data there is a slight correlation between temperature and over/under totals. Warmer temperatures lead to slightly higher O/U tptals.

![Temperature](Output-Data/Schedule-Temperature.png)
![Temperature Regression](Output-Data/Schedule-Temperature-Regression.png)

### Week of Season vs. Over/Under Totals
There is no evidence that the week a game is played has any effect on the Over/Under Total.

![Totals](Output-Data/Schedule-Totals.png)
![Totals Regression](Output-Data/Schedule-Totals-Regression.png)
