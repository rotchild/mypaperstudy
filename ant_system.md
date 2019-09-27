# AS outline

## introduce

there are two main steps for AS algorithm.The first step is initial parameters,the second is top update the ant's steps

## details

for the first step, some crutial parameters should be mentioned,they are described as follow:

- NC, the cycle counter,additionally,we define the **cycle** as a complete trip for an ant over the whole towns

- towns, the nodes where ants should travel

- pheromone_matrix,the **pheromone** dentsity of ant i lay on town j

- L_short,the shortest path for the whole ants
  
- p, where 1-p means the evaporate

as the second part,update function is for every ant who are traveling the towns.The function decide which town to go next. And the main idea of it is choice probability relative to two parameters:**visibility** and **pheromone**,the formula is as follow:

$prob_{i,j}=\frac{pheromone_{i,j}^\alpha*\eta^\beta_{i,j}}{\sum_{k\in S,k\neq p}pheromeno_{k,j}^{\alpha}*\eta^\beta_{k,j}}$

where S is the set of probably choice for the next town j for ant i
