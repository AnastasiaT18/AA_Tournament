# AA_Tournament
Nydegger's strategy. It plays tit-for-tat for the first
three moves, save that if it was the only one to co-operate on the
first move and the only one to defect on the second move, it defects
on the third move. After that, its choice is determined from the 3
proceeding outcomes in the following manner. Let A be the sum formed
by counting the other's defection as 2 points and one's own as 1
point, and giving weights of 16, 4 and 1 to the proceeding three
moves in chronological order. The choice can be described as defecting only 
when A equals 1, 6, 7, 17, 22, 23, 26, 29, 30, 31, 33, 38,
39, 45, 49, 54, 55, 58, or 61.    . 