# AA Tournament
## Anastasia Tiganescu, FAF-231

### Part 1 - Basic Nydegger
The Nydegger strategy follows a structured approach to interactions, starting with a Tit-for-Tat strategy for the first
three rounds. In the initial rounds, the strategy cooperates (1) on the first move, and then it simply mirrors the opponent’s
previous move for the second and third moves, in the typical Tit-for-Tat manner. However, there is an exception: if Nydegger 
is the only one to cooperate on the first move and the only one to defect on the second move, it will defect (0) on the third
move.

After the first three moves, the strategy switches to a more complex decision rule based on the outcomes of the last three 
moves. For each of these moves, Nydegger assigns points: 1 point for its own defection, and 2 points for the opponent’s 
defection. The points for the three most recent moves are then weighted according to their chronological order: 16 for the
most recent move, 4 for the second most recent, and 1 for the third most recent. These weighted points are summed to produce
a value, A.

Based on the value of A, Nydegger will make its decision. If A matches any of the following values: 1, 6, 7, 17, 22, 23, 26,
29, 30, 31, 33, 38, 39, 45, 49, 54, 55, 58, 61, it will defect (0). In all other cases, the strategy will cooperate (1).

### Part 2 — Improved Nydegger
In the second part of the tournament, additional features are added to optimize performance.

Initially, if it encounters opponents who have not yet played any rounds, it prioritizes them. In this way,
Nydegger plays with each opponent at least 3 times so it makes a more rational decision afterward. Otherwise, it evaluates all available opponents
by calculating two factors: the average payoff achieved in past interactions with them and their overall cooperation rate. To favor more cooperative
players, the cooperation rate is given a significant weight in the final score used to rank opponents. Nydegger then chooses to interact with the
opponent who offers the best combination of past rewards and cooperative behavior. Additionally, it avoids opponents who have already participated in
200 rounds or more, ensuring it focuses on fresher, potentially more favorable interactions.