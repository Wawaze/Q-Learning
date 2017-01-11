# Q_learning_demo
This is the code for the challange video "How to use Q Learning in Video Games Easily" by Siraj Raval on Youtube

##Overview

This is the associated code for [this](https://youtu.be/A5eihauRQvo) video on Youtube by Siraj Raval. This is a simple example of a type of [reinforcement learning](https://en.wikipedia.org/wiki/Reinforcement_learning)
called [Q learning](https://en.wikipedia.org/wiki/Q-learning). 


	● Rules: The agent (yellow box) has to reach one of the goals to end the game (any green or red cell).
	● Rewards: Each step gives a negative reward of -0.04. A step to a wall give additional -0.02. The red cell gives a reward of -1. The green one gives a positive reward of +1.
	● States: Each cell is a state where the agent can be.
	● Actions: There are only 4 actions. Up, Down, Right, Left.

##Modifications

Some of the things changed are:
	●Fixed to be compatible with Python 3
	
	●Added a negative reward to avoid hitting the walls and the boundaries of the grid
	
	●Made a constrain of minimum score so it will start a new episode below a limit value. This was made to discourage the agent going to path searches to far from the optimal path. The limit value need to change acording to the size of the grid.
	
	●The discount factor now increases with each successful episode to the limit of 0.8. Other functions with a slower growth at the beginning might be better. The literature suggests that a discount value to close to 1 may make it more difficult to the algorithm to converge or make it not stable
	
	●Size of each square rescalable according to the size of the grid
	
	●Placement of walls, goals and the initial position of the agent. Better convergence may be achieved by making the initial position of the agent random for each episode, but that was not made just to keep it simple while testing the code
	
	●Time step was decreased also for testing, making it show the results a bit quicker 
	

##Dependencies

-Python 
-tkinter

##Usage

Run `python Learner.py` in terminal to see the the bot in action. It'll find the optimal strategy pretty fast for a small grid

#Due Date is Thursday at noon PST January 12th 2017

##Credits

The credits for the original code wich this one is based go to [PhillipeMorere](https://github.com/PhilippeMorere).
Also credits for Siraj's video with the good and quick explanation about Q learning and the challange
