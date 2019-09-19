# Score-prediction
 you how bad is taking run rate as a single factor to predict the final score in an limited overs cricket match.  In ODI and T-20 cricket, many factors play a key role in deciding what the final score will be.  Let’s look at some of the key factors:

    Number of wickets left
    Number of balls left
    On how much scores are the current batsman batting?
    How much the team had scored in last 5 overs?
    How much the team had lost wickets in last 5 overs?
    The nature of the pitch
    How strong is the batting and bowling team?

I will use some of these factors to predict score using machine learning algorithms. We use regression analysis in machine learning to predict the final score of an ODI or T-20 match.
Preparing the dataset

I have not scrapped the web pages to prepare the dataset. I have downloaded the dataset from cricsheet. The site gives us ball by ball details of matches. I then wrote a custom code to only include some of the features which I will be using.

The dataset contains ball by ball coverage of:

    1188 ODI matches: data/odi.csv
    1474 T-20 matches: data/t20.csv
    617 IPL matches: data/ipl.csv

Each dataset consists of following columns(features):

    mid: Each match is given a unique number
    date: When the match happened
    venue: Stadium where match is being played
    bat_team: Batting team name
    bowl_team: Bowling team name
    batsman: Batsman name who faced that ball
    bowler: Bowler who bowled that ball
    runs: Total runs scored by team at that instance
    wickets: Total wickets fallen at that instance
    overs: Total overs bowled at that instance
    runs_last_5: Total runs scored in last 5 overs
    wickets_last_5: Total wickets that fell in last 5 overs
    striker: max(runs scored by striker, runs scored by non-striker)
    non-striker: min(runs scored by striker, runs scored by non-striker)
    total: Total runs scored by batting team after first innings
