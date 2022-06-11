# Sports Salaries

## Description

- What was your motivation?
As a data analyst, particularly one considered a novice or new to data analyzing, it is key to continue to practice the various aspects data analysis and visualization. During this instance, the focus is improvement of Extraction, Transformation and Load skills.
- Why did you build this project?
We created this project to gain more knowledge and understanding of the Extract, Transform and Load process through analysis of Sports Salaries. Sports is an important aspect of the lives for most people. Whether having participated in or only enjoying it from the stands, sports touch the competitiveness that lives inside most people. Sports reaches a multitude of people and can evoke a wide range of emotions in those follow them. As avid sports fans who both participated and still closely follow, we were interested in the financial aspect from player salaries standpoint. Sports has become a big business and generated wealth for those that play at the professional level. These were key items that aided the attentiveness to the details used in the project which enhanced the overall understanding of process steps.
- What problem does it solve?
The project provides various information regarding athletes in the professional sports leagues of basketball, baseball, and football. The primary category of interest being yearly salaries.
- What did you learn?
From this project there were things learned during the steps of the project creation. The first was to validate the expectations and requirements of a project. After, the initial start to our project, it was necessary to make an adjustment from our original project proposal due to clarification of details impacting the desired outcome (i.e. minimal requirements). We also learned to verify column formatting to exclude spaces and other special characters to ensure a smooth transition when loading data to the database. Additionally, we learned the importance of knowing multiple ways of dropping unwanted and null data. Lastly, we learned the importance of focusing on the steps to database creation rather than possible future analysis of the datasets. 

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Credits](#credits)
- [License](#license)

## Installation

1. Clone the repository in your Git Bash terminal using the following text: git clone git@github.com:truthprice/Sports-Salaries.git
2. The CSVs used can be found in the 'Resources' folder, but they can also be obtained from the following sites:
	1. <https://data.world/sportsvizsunday/2021-february-nfl-salary-cap/workspace/file?filename=Feb+2020+SportsVizSunday.xlsx>
	2. <https://data.world/datadavis/nba-salaries/workspace/file?filename=players.csv>
	3. <https://data.world/datadavis/nba-salaries/workspace/file?filename=salaries_1985to2018.csv>
	4. <https://www.kaggle.com/datasets/andrewdecker/hitters-salary-adjusted-to-inflation>
	5. <https://www.kaggle.com/datasets/andrewdecker/pitcher-salary-adjusted-to-inflation>
3. Create a 'Sports_Salaries' database in pgAdmin4. The following three tables will be created within the database upon running the jupyter notebook code:
	1. A 'football' table that contains the "index", "Years", "Franchise", "Player", "Pos", "Cap_Type", "Base_Salary", "Signing_Bonus", "Workout_Bonus", "Dead_Cap", "Cap_Hit", "Cap_Percent" columns. 
	2. A 'basketball' table that contains the "index", "name", "player_id", "salary", "season_start", "team", "birthDate", "birthPlace", "career_AST", "career_FG_Percent", "career_FG3_Percent", "career_FT_Percent", "career_G", "career_PER", "career_PTS", "career_TRB", "career_WS", "career_eFG_Percent", "college", "draft_pick", "draft_round", "draft_team", "draft_year", "height", "highSchool", "position", "shoots", "weight" columns.
	3. A 'baseball' table that conatins the "index", "playerID", "Unnamed_0_hitter", "yearID_hitter", "salary_hitter", "ADJ_Salary_hitter", "GS_hitter", "InnOuts_hitter", "PO_hitter", "A_hitter", "E_hitter", "DP_hitter", "teamID_hitter", "lgID_hitter", "G_hitter", "AB", "R_hitter", "H_hitter", "2B", "3B", "HR_hitter", "RBI", "SB", "CS", "BB_hitter", "SO_hitter", "IBB_hitter", "HBP_hitter", "SH_hitter", "SF_hitter", "GIDP_hitter", "Unnamed_0_pitcher", "yearID_pitcher", "salary_pitcher", "ADJ_Salary_pitcher", "InnOuts_pitcher", "PO_pitcher", "A_pitcher", "E_pitcher", "DP_pitcher", "teamID_pitcher", "lgID_pitcher", "W", "L", "G_pitcher", "GS_pitcher", "CG", "SHO", "SV", "IPouts", "H_pitcher", "ER", "HR_pitcher", "BB_pitcher", "SO_pitcher", "BAOpp", "ERA", "IBB_pitcher", "WP", "HBP_pitcher", "BK", "BFP", "GF", "R_pitcher", "SH_pitcher", "SF_pitcher", "GIDP_pitcher" columns.
4. Make sure you have the following libraries installed:
	1. [pandas](https://pandas.pydata.org/docs/getting_started/install.html)
	2. [sqlalchemy](https://docs.sqlalchemy.org/14/intro.html)
	3. [psycopg2](https://www.psycopg.org/docs/install.html)
5. **Extraction**
	- We put each CSV into a Pandas DataFrame.
	- **Note:** 'NFL_Salaries1' and 'NFL_Salaries2' are the football datasets. 'players' and 'salaries_1985to2018' are the basketball datasets. 'Hitters_Adjusted_Salary' and 'Ptichers_Adjusted_Salary' are the baseball datasets.  
6. **Transform**
	- We removed _only_ the columns we did not need from each dataset.
	- We renamed the columns for each dataset to match the tables created in the database.
	- Handle (i.e. dropping) any null values and data marked with "-" as null values.
	- Set the index to the previously created primary key. **Note:** We had to reset for the football dataframe
7. **Load**
	- We created a connection to the database.
	- We checked for a successful connection to the database, and confirmed that the tables had been created.
	- We appended the DataFrames to tables.


## Usage

Run the code in the jupyter notebook. From pgAdmin4, run queries for each table to ensure that data was properly loaded into the database. 

## Credits

[Truth Price](https://github.com/truthprice)  
[Jeff Frazier](https://github.com/jfraz027)  
<https://www.quickdatabasediagrams.com/>  
<https://stackoverflow.com/>

## License

MIT License

Copyright (c) [2022] [Truth Price, Jeff Frazier]

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

---
