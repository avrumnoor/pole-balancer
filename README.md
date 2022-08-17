# Pole Balancer

![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white) ![SciPy](https://img.shields.io/badge/SciPy-%230C55A5.svg?style=for-the-badge&logo=scipy&logoColor=%white)

![PyCharm](https://img.shields.io/badge/pycharm-143?style=for-the-badge&logo=pycharm&logoColor=black&color=black&labelColor=green)

## About Pole Balancer

Pole Balancer is a Python program that uses reinforcement learning (RL) to automatically design a policy for the classic controls problem of a cart balancing a pole. Through Markov decision processes framework, we can perform reinforcement learning without having any explicit knowledge of the physics of the underlying system, in our case, the pole on the cart.

## Requirements
- Ubuntu 18.04+, macOS 10.15+ and Windows 10+ (64-bit)
- At least 5GB of memory
- Anaconda/Miniconda
- Python 3.9 or above
- A Python IDE (Jupyter/PyCharm)

## Getting Started

Install the following Python packages:
- matplotlib
- numpy
- scipy
- pillow

Run 
`python polebalancer.py`

***

## Model

A thin pole is hinged to a cart. The cart moves laterally on a smooth table surface. The program fails if either the angle of the pole deviates by more than a particular amount from the vertical position (i.e., if the pole falls over), or if the cart’s position goes out of bounds (i.e., if it falls off the end of the table). 

![Pole being balanced](./images/sample_demo.gif) 

## Program Objective

Balance the pole with these constraints, by appropriately having the cart accelerate left and right.

## Algorithm
- [ ] Estimate a model (i.e., transition probabilities and rewards) for the underlying MDP.
- [ ] Obtain a value function by solving Bellman’s equations for this estimataion to obtain a value function.
- [ ] Act greedily with respect to this value function.
- [ ] Initially, each state has estimated reward zero, and the estimated transition probabilities are uniform.
- [ ]  As the program goes along taking actions, it will gather observations on transitions and rewards, which it can use to get a better estimate of the MDP model.
- [ ]  Store the state transitions and reward observations each time, and update the model and value function/policy only periodically. 
- [ ]  Each time a failure occurs, re-estimate the transition probabilities and rewards as the average of the observed values (if any). 
- [ ]  Repeat previous steps until convergence (once several consecutive attempts (defined by the parameter `NO LEARNING THRESHOLD`) to solve Bellman’s equation all converge in the first iteration since this implies that the estimated model has stopped changing significantly).

## Author

Avrum Noor

<a href="https://www.buymeacoffee.com/avrumnoor" target="_blank"><img src="https://cdn.buymeacoffee.com/buttons/v2/default-blue.png" alt="Buy Me A Coffee" style="height: 41px !important;width: 174px !important;box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;-webkit-box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;"></a> 

[![LinkedIn](https://img.shields.io/badge/linkedin-%230077B5.svg?style=social&logo=linkedin)](https://www.linkedin.com/in/avrumnoor/) ![Twitter](https://img.shields.io/twitter/follow/avrumnoor?style=social) ![Followers](https://img.shields.io/github/followers/avrumnoor?style=flat-square) ![Stars](https://img.shields.io/badge/stars-104-blue?style=flat-square)


## Acknowledgements

[Anand Avati](https://avati.github.io/)
Stanford Machine Learning Coursework 
