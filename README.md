Download Link: https://assignmentchef.com/product/solved-cse5331-project2-mongodb-soccer-project
<br>
In this project, you will learn to use MongoDB as an example of a document-oriented NOSQL system, and see how data is stored and queried in such a system. You will also learn about the difference between storing data in a flat (relational) format versus in a document (complex object) JSON format.

The input to your program will be several data files in flat relational format for the WORLD CUP 2018 database example (see attached approximate ER and relational schemas). The files contain data records about information regarding the 2018 soccer world cup tournament.




<strong><u>Project 2, Part 1:</u></strong>

Install Mongo DB on your computer. Load the data files into Mongo DB as flat files: TEAM, GAME, PLAYER, STARTING_LINEUP, GOALS.

Turn in documentation to show that you installed Mongo DB and created the flat file document collections corresponding to the above tables.

<strong><u>Project 2, Part 2:</u></strong>




You will need to design two document (complex object) schemas corresponding to this data. The first one is required, while the second one is optional for extra credit (20 points extra over 100):

<ol>

 <li>The TEAM_SCORES document will include the following data about each team: Team (that is, the team name), and a collection of the team match (GAME) scores. Each match score in the collection will include: the date of the match, the name of the city and stadium where the match was played, repeat of the team’s name, the team score in the match, the name of the opposing team, and the score of the opposing team.</li>

 <li>The PLAYER_DATA document will include the following data about each player: the player name (Pname), the player’s team name (Team), the player number (PNo) and position (Position), and a collection of games that the player has started – for each game (match) the player has started, include the MatchDate, City, Stadium Name, and opposing team name. Also include for each player a collection of goals that the player has scored (if any) – for each goal scored, include the GoalType, Time, MatchDate, City, Stadium Name, and opposing team name.</li>

</ol>

Instructions on how to download and install MongoDB on your computer are on Canvas and also at crystal.uta.edu/~elmasri/db2 under <u>Projects</u>.

We will have the following data files for the world cup database:

TEAM(TeamID, Team, Continent, League, Population)

(* Team is the Team Name, which is the name of one of the participating countries *)

STADIUM(SID, SName, SCity, SCapacity)

(* SName and SCity are the name and city of each stadium *)

PLAYER(Team,TeamID,PNo,Position,PName,Birth Date,Shirt Name,Club,Height,Weight)

(* PLAYER corresponds to the data in the “rosters” data file – Pno corresponds to PlayerID,

and PName corresponds to FIFA Popular Name in the rosters file *)

GAME(GameID,MatchType,MatchDate,SID,TeamID1,TeamID2,Team1_Score,Team2_Score)

(* GAME corresponds to the data in the “matches” data file *)

STARTING_LINEUPS(GameID,TeamID,PNo)

GOALS(GameID,TeamID,PNo,Time,Penalty)

OWN_GOALS(GameID,TeamID,PNo,Time,For_TeamID)







Your tasks for the project are as follows:

<ol>

 <li>Write programs or use Mongo DB tools to extract the data needed for the complex document types (TEAM_SCORES (required) and PLAYER_DATA (optional)), and load these documents into the MongoDB system. Notice that the data from each document will be the result of a join on more than one flat file. You will need to convert the flat-file data loaded in Project 2, Part 1 to convert into the nested format into JSON for loading on MongoDB</li>

 <li>Write some MongoDB queries to retrieve some of the stored documents. (For example, retrieve all team scores for the team “Japan”).</li>

</ol>