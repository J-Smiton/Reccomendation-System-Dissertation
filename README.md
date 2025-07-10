# Reccomendation-System-Dissertation
AI System to Suggest Signings for Football Clubs

This project uses MATLAB to create a recommendation system for clubs, to help guide them with signings in the transfer market. 
The system takes in-depth metrics from the majority of the 24/25 season from both teams and players, and creates profiles for both and compares whether the team and player would be a good fit. The data used includes every player from Europe’s top 5 leagues, and thus will only suggest signings between European clubs. The suggestions are based on the median of the relevant team and player’s stats and gives a top 20 suggestions for the selected club, by the selected position. 
If the selected club is considered to have less ‘signing power’ in the transfer market, they will also be suggested market opportunities in the form of fringe players. The players are given a suggestion score (0-1) and ranked on that. The results are listed and opened in Excel.
There is also a user interface built into the system, where the user of the system must choose the league first from the initial dashboard, then select a club and position. The system calculates the final score on cosine similarity, and is done through the use of content-based filtering.

This Word document also gives context and instructions on different aspects of the system. 
Key of tricky metrics:
Rk – rank
Min – minutes
CrdY – Yellow cards
CrdR – Red cards
GA – Goals and assists
PK- Penalty kicks
xG – Expected goals
xAG – Expected assists
NPxG+xAG - Non-penalty expected goals plus expected assists
SoT/90 – Shots on target per 90 minutes
SoT% - Shot on target percent
G/Sh – Goals per shot
G-xG – Goals minus expected goals
Cmp% - Pass completion%
PrgC – Progressive carries
PrgP – Progressive Passes
TotDist – Total distance 
PrgDist – Progressive distance
TB – Through balls
Crs – Crosses
Recov – Ball recoveries
Rec – Passes received
Tkl – tackles
Def3rd – tackles in defensive 3rd
Clr – Clearances 
Err – Errors
Fls – Fouls
GA90 – Goals against per 90 minutes
CS% - Clean sheet%
PKA – Penalty kicks against
PKsv – Penalty kicks saved
/90PSxG-GA/90 – Post shot xG-goals allowed per 90 minutes (higher numbers = better)
GKCmp% - Goalkeeper pass completion%
Launch% - %Accuracy of 40+ yard passes
Stp% - Crosses stopped%
OPA/90 – Defensive actions outside the area per 90

Context for using the system. The system must be run manually before UI use:
ClubName = input('Enter club name:', 's')
%Manual entering for when UI not in use
%ClubName = GetClubName()
%Take ClubName from UI dropdown
And input a club before using UI
After used manually once,
%ClubName = input('Enter club name:', 's')
%Manual entering for when UI not in use
ClubName = GetClubName()
%Take ClubName from UI dropdown
And clubname will be interpreted from the UI dropdown.

System will error if a positional results table is open, as it doesn’t have permission to edit the file.

Notable results:
Tijjani Reijnders #1 suggestion for Manchester City (Mid)
Morgan Gibbs-White #3 suggestion for Spurs (Mid)
Joao Pedro #5 suggestion for Chelsea (Att)
Jeremie Frimpong #5 suggestion for Liverpool (Def)
Milos Kerkez #7 suggestion for Liverpool (Def)

First in the dissertation (DMU)
