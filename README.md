# CI_TSP
Genetic Algorithms+TSP

# Approach Doubts:
- Should we save all the fitness (maybe for plots)
- Should we create a number of offspring and then select between them and the parents
  - If we do this how do we do it. We need two parents per offspring (maybe select even offspring values). If there's no crossover just keep the values? Doesn't this account too many times for the parents
- Should we just create offspring and select from there

# To do list
- [ ] IMPORTANT: fitness function currently is distance which is more like a cost function (we want to minimize it), solve this. For example in roulette it doesn't make sense because we reward big distances. 
  - [x] Maybe we could do fitness = 1/distance
- [x] Elitism
- [ ] Write about the configuration of hypereparameters we decided not to do
- [ ] Plot function
- [ ] Add hyperparameters:
  - [x] nº of iterations
  - [x] nº of prints (how often we represent the evolution on the fitness of the generations)
- [x] Add matrix of distances implementation
- [ ] Improve computing time
- [ ] Code parent selection methods
  - [x] tournament
  - [x] roulette
  - [x] rank roulette
    - in rank roulette, in order to select the weights, we considered two options: 1) Using the reciprocal of the rank as the weight 2) using the ranks in inverse order and normalize (so the 1st would get 29/norm and the last would get 1/norm). In the end we ran a little experiment and we chose the 1) 
  - [x] random
- [x] Code crossover methods
  - [x] OX1
  - [x] POS
- [x] Code mutation methods 
  - [x] Insertion
  - [x] Exchange
  - [x] IVM
- [] Add stagnation convergence (before ending the generations) WE DECIDED NOT TO DO IT, BECAUSE IT NEGLECT THE EFFECT OF GENERATIONS and COMMENT ON THE PLOTS IF IT WOULD BE USEFUL
- [ ] AT THE END
  - [ ] Check function descriptors says all the hyperparameter options
  - [ ] Talk about the optional parameters of the methods we implemented but didn't tested
  - [ ] We used the distance function and we wanted to minimize it, acting as a sort of cost function. If the objective were to be the usage of a fitness function, we could apply a monotonic descending transformation to the distance, such as $e^{-x}$

# Optional to do list:
- [ ] To test if we chose the right parameters we can repeat a certain time the experiments and perform an ANOVA on the different models (this is done in the article [3])
- [ ] We could add stagnation convergence
- [ ] Add replacement strategy

## Info for the report
* We use the **Pittsburgh view**, each individual is a full solution.
* We assume simmetrical distances (since the data we obtained was that way)
* we choose $(\mu,\lambda)$ with $\mu=\lambda$

## Selection Methods:
* Elitism
* Roulette Wheel (based on fitness)
* Roulette Wheel (based on rank)
* Niching (Doesn't seem ideal for this problem)
  
## Replacement strategies:
* Generational (offspring replace all the parents)
* Offspring replaces the worse
* Offspring replaces at random
* Offspring replaces the oldest

## Crossover Possibilities
After looking into other modern papers, we have more than enough with the crossover possibilities proposed at [1].

## 


# Bibliography:
1. *Genetic Algorithms for the Travelling Salesman Problem: A Review of Representations and Operators*, P. Larrañaga et al, (1999)
2. Github repository with a basic implementation: "https://github.com/hassanzadehmahdi/Traveling-Salesman-Problem-using-Genetic-Algorithm/"
3. *The Effect of Genetic Algorithm Parameters Tuning for Route Optimization in Travelling Salesman Problem through General Full Factorial Design Analysis* (2022)
4. We obtained the data from http://comopt.ifi.uni-heidelberg.de/software/TSPLIB95/tsp/
5. 
  

https://github.com/hassanzadehmahdi/Traveling-Salesman-Problem-using-Genetic-Algorithm/tree/main