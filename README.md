# MDP REPRESENTATION
## AIM:
The aim of this MDP is to model the decision-making process of a person while coding, considering two levels of concentration - full concentration and half concentration, and to maximize productivity.

## PROBLEM STATEMENT:
### Problem Description
In this scenario, we assume a model called lift.There are three states :Empty floor,Treasure floor,Ground floor and two actions : up(1) and down(0).If the model reach the state called treasure floor,it can get the reward of 1.Otherwise,it will get 0.By the actions of up and down, the model will navigate among the three states.

## State Space:
Empty floor, Ground floor,Treasure floor.

## Sample State:
Treasure floor.

## Action Space:
Up(1) and Down(0).
## Sample Action:
Up(1)
## Reward Function:
1->If the goal is reached
0->Otherwise

## Graphical Representation:
![Screenshot (572)](https://github.com/kumaranricky/mdp-representation/assets/75243072/e503a45f-75a3-45f7-9af8-cb4c8bfa7952)


# Python Representation
```python
MDP = {
    "Treasure floor": {
         0 : [(0.8, "GF", 0, False),(0.2, "TF", 1, True)],
        1 : [(0.8, "TF", 1, True),(0.2, "GF", 0, False)]
    },
    "Ground floor": {
        0 : [(0.8, "EF", 0, False),(0.2, "GF", 0, False)],
        1 : [(0.8, "TF", 1, True),(0.2, "GF", 0, False)]
    },
    "Empty floor": {
         0 : [(0.8, "EF", 0, False),(0.2, "GF", 0, False)],
        1 : [(0.8, "GF", 0, False),(0.2, "EF", 0.0, False)]
    }
}
```
## OUTPUT:
![Screenshot (571)](https://github.com/kumaranricky/mdp-representation/assets/75243072/e620fc70-2b83-4fe2-8ca1-50defadcd6c4)


## RESULT:
The result of solving this MDP would be an optimal policy that tells the person which action to take in each state to maximize their productivity while coding.
