I was inspired by Joshua Bull's video "A Mathematician's Guide to the World Cup" posted on the Oxford Mathematics YouTube channel. Joshua Bull is a mathematical modeller and the winner of the 2020 Fantasy Football competition with over 8 million entrants. In his video, he shows an idea to build a model to predict the World Cup winner. Joshua focuses on xG (expected goals) but recognizes that the approach may be biased and proposes to extend the model with the Elo rating from World Football Elo Ratings.

The World Football Elo Ratings are based on the Elo rating system created by Dr. Arpad Elo. This system, used by FIDE (the international chess federation), ranks chess players. Eloratings.net applies the Elo rating system to international football, taking into account the type of match, home team advantage, and goal difference in the result. After about 30 matches, the ratings tend to reflect a team's true strength compared to its opponents. Ratings for teams with fewer than 30 matches should be considered provisional.

The ratings are based on the following formulas:

Rn = Ro + K × (W - We)

Rn is the new rating, Ro is the old (pre-match) rating.

K is the weight constant for the tournament played:
•	60 for World Cup finals;
•	50 for continental championship finals and major intercontinental tournaments;
•	40 for World Cup and continental qualifiers and major tournaments;
•	30 for all other tournaments;
•	20 for friendly matches.

K is then adjusted for the goal difference in the game. It is increased by half if a game is won by two goals, by 3/4 if a game is won by three goals, and by 3/4 + (N-3)/8 if the game is won by four or more goals, where N is the goal difference.

W is the result of the game (1 for a win, 0.5 for a draw, and 0 for a loss).
We is the expected result (win expectancy), either from the chart or the following formula:
We = 1 / (10(-dr/400) + 1)
dr equals the difference in ratings plus 100 points for a team playing at home.

Sample Winning Expectancies

Difference in Ratings //	Higher Rated	//Lower Rated
0	0.500	0.500
10	0.514	0.486
20	0.529	0.471
30	0.543	0.457
40	0.557	0.443
50	0.571	0.429
60	0.585	0.415
70	0.599	0.401
80	0.613	0.387
90	0.627	0.373


My idea was to assess the reliability of Elo ratings for the group stage in the World Cup and identify any biases associated with them. I was curious to see if it was possible to predict surprises like for example Japan vs Geramany.

I have gathered predictions from EloRating.net and then compared them with the results available on sports portals.

Source:
1. https://www.eloratings.net/about
2. https://www.youtube.com/watch?v=KjISuZ5o06Q
