

# Assignment: Value Iteration and Q-values Implementation on Grid World

## Assignment Objective

The objective of this assignment is to learn:

- Understanding of a given RL problem parameters.
- The implementation of the environment.
- The implementation of Value iteration and Q-values.



## Assignment Description

Implement value iteration and Q-values methods on the Grid World problem.

### 1. Build the Environment

- Number of states: 12 (each grid represents a state).
- Number of actions: 4 (Up, Down, Left, Right).
- Rewards:
  - Grid 3: +1
  - Grid 7: -1
  - Grid 5: Wall (no entry).
- Parameters:
  - Discount factor (Gamma): 0.9
  - Noise: 0.2
  - Number of iterations: 100

### 2. For Every Iteration Print the Grid Values

Example of the output:
```
| -0.01 | -0.01 | 0.782 | +1   |
| -0.01 | WALL  | -0.01 | -1   |
| -0.01 | -0.01 | -0.01 | -0.01|
```

### 3. Extract and Print the Policy After Convergence or Completion of Iterations

Example of the output:
```
| Right | Right | Right | +1   |
| Up    | WALL  | Up    | -1   |
| Up    | Right | Up    | Down |
```

### Tip

For building the environment, you can use a 3x4 2D array where each state is represented by the index of that array (state 1 => [0][0], state 2 => [0][1], and so on). For the actions, you could define:
```python
Actions = [(1, 0), (0, -1), (-1, 0), (0, 1)] # Down, Left, Up, Right
```
The next state when taking action `a` can be obtained by adding the current state indexes and the action values. For example, if we are in state [0][1] and go down (1,0), the new state will be [0+1][1+0] -> [1][1].

### Hint

Any trial will be appreciated, so please try your best.
