# Maze Navigator Agent
***Solving Problems by Searching*** is a fundamental concept in the field of Artificial Intelligence that  involves finding a sequence of actions or steps that leads from an initial state to a goal state. This approach is widely used in various domains such as robotics, game playing, pathfinding, and automated planning. In this project, I developed a maze generator that creates a unique maze on each run, along with an agent that finds its way from the starting point to the target using both informed and uninformed search algorithms.


![Image of a person in the middle of a maze](https://github.com/PeymanKh/Maze-solver-Agent/assets/118134658/0b002b9d-99ea-462e-990e-399989c062b8)

## Table of Contents
- [1. Rational Agent](#agent)
- [2. Environment](#environment)
- [3. Search Problem](#search)
- [4. Search Algorithms](#algorithms)




<a name="agent"></a>
## 1. Rational Agent 
Different people approach AI with different goals in mind. Here the main question is do you want to model humans or try to achieve the optimal results? 
According to what we call the standard model, AI is concerned mainly with rational agent which takes the best possible action in a situation. A rational agent is any entity that can perceive its environment through sensors and acts upon that environment using actuators. The key characteristic of a rational agent is its ability to make decisions or choose actions that maximize its chances of achieving a certain goal or set of goals. Rationality, in this context, means that given a set of perceptions and a knowledge base, the agent will perform an action that is expected to bring about the best outcome according to a specific performance measure. This measure can vary depending on the agent's objectives, such as maximizing utility, minimizing cost, or achieving a particular state.
Rational agents can be simple or complex, ranging from automated thermostats to sophisticated robotic systems.

<a name="environment"></a>
## 2. Environment
The entire universe could be considered as the environment, but practically speaking, it's only the part of the universe around the agent that can influence or be influenced by the agent's actions. Environments can be physical, like a robot navigating a room, or virtual, like a software agent operating within a computer system. They can also vary in terms of their properties such as being predictable or unpredictable. The complexity of an agent's behavior and its decision-making process are often directly related to the complexity of its environment. Understanding the environment is crucial for designing an agent that can effectively achieve its goals within that context.


<a name="search"></a>
## 3. Search Problem
A search problem can be defined formally as follows:
1. State Space: A set of all possible states of the problem.
2. Initial State: The starting point of the problem, where the search begins.
3. Goal state(s): The state or states that represent a solution to the problem.
4. Actions: The actions available to the agent. Given a state "s", ACTIONS(s) returns a finite set of actions that can be executed in "s".
5. Transition Model: Describes what each action does. RESULT(s, a) returns the state that results from doing action "a" in state "s".
6. Search Algorithm: The method used to explore the state space. It systematically checks states, expanding them to discover new states until the goal is reached.


<a name="algorithms"></a>
## 3. Search Algorithms
A search algorithm takes a search problem as input and returns either a solution, or indication of failure. In this project, I utilized search tree over the state space graph. Each node in this tree represents a cell in the maze, and the connections between nodes (edges) represent the possible moves. The root of the tree represents the problem's initial state.

![(1, 1)](https://github.com/PeymanKh/Maze_Navigator_Agent/assets/118134658/98fbb387-0ca7-466d-96ca-6ff5ccabbf20)

Throughout the project's development, two distinct strategies were applied to systematically expand from the current state towards discovering new states until the goal was achieved. 
The first strategy is **Uninformed Search** also known as blind search. In these strategy, the agent do not have additional information about states beyond the current state. I utilized two algorithms which search through the state space using this strategy:
* 1- Breadth-First Search (BFS): This algorithm explores the state space level by level, expanding all states at a given depth before moving to the next level. It guarantees finding the shortest path in terms of the number of steps.
* 2- Depth-First Search (DFS): This algorithm explores as far as possible along each branch before backtracking. It's memory-efficient but doesn't guarantee the shortest path.
![DFS & BFS](https://github.com/PeymanKh/Maze_Navigator_Agent/assets/118134658/3dee7b5e-9ade-49e7-8643-e24a9a7a480a)

The second strategy is **Informed Search** also known as heuristic search. Within this approach, the agent utilizes additional knowledge about the state space to efficiently find the solution. Unlike uninformed search strategies that explore the search space without any direction, informed strategies use heuristics to guide the search process towards the goal more quickly. A* (A_star) is a  widely used informed search algorithm estimates the cost of reaching the goal with heuristic function.
- g(n):  The cost of the path from the start node to node n.
- h(n): The heuristic estimate of the cost from n to the closest goal node. This is where A* integrates knowledge about the problem domain.
- f(n) = g(n) + h(n): The total estimated cost of the cheapest solution through n. A* uses this function to prioritize which node to explore next.



