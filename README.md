# Elorating-React
A Live Elo rating demo

Manually declare the winner and the probability and rating will be automatically updated

https://github.com/kadmon47/Elorating-React

Constant K = 32

probability(p1,p2) = 1/(1+Math.pow(10,(rating1-rating2)/100))

pa = probability(r2,r1) - probability of player 1
pb = probability(r1,r2) - probability of player 1

if player 1 wins 
   r1 = Math.floor(p1Rating+k*(1-pa)) - new rating of player 1
   r2 = Math.floor(p2Rating+k*(0-pb)) - new rating of player 2

if player 2 wins 
   r1 = Math.floor(p1Rating+k*(0-pa)) - new rating of player 1
   r2 = Math.floor(p2Rating+k*(1-pb)) - new rating of player 2
