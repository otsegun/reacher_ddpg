[//]: # (Image References)

[image1]: https://user-images.githubusercontent.com/10624937/43851024-320ba930-9aff-11e8-8493-ee547c6af349.gif "Trained Agent"
[image2]: https://user-images.githubusercontent.com/10624937/42386929-76f671f0-8106-11e8-9376-f17da2ae852e.png "Kernel"

# Continuous_Control for Reacher Agent

### Introduction

This project contains code for a trained reinforcement learning agent that solves [Reacher](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Learning-Environment-Examples.md#reacher) environment task of UnityML 

![Trained Agent][image1]

  
The environment consists a double-jointed arm that can move to target locations. A reward of +0.1 is provided for each step that the agent's hand is in the goal location. Thus, the goal of the agent is to maintain its position at the target location for as many time steps as possible.

The state space is an array of 33 elements. It contains the agent's arm position, rotation, velocity, and angular velocities, among others. Given this information, the agent has to learn how to best select actions.  The action space is an arry of 4 numbers containing torque applied to the two joints of the agent's arm.


The task is episodic, and in order to solve the environment, **the agent must get an average score of +30 over 100 consecutive episodes**.


### Getting Started

#### Dependencies
1. Create (and activate) a new environment with Python 3.6.

	- __Linux__ or __Mac__: 
	```bash
	conda create --name drlnd python=3.6
	source activate drlnd
	```
	- __Windows__: 
	```bash
	conda create --name drlnd python=3.6 
	activate drlnd
	```
2. Install Openai gym using `pip install gym`.
3. Install box2d and box2d-py: `pip install box2d`; `pip install box2d-py`. 
4. Clone the repository below and navigate to the `python/` folder.
```bash
git clone https://github.com/udacity/deep-reinforcement-learning.git
cd deep-reinforcement-learning/python
```
5. Replace the `requirements.txt` file in the `deep-reinforcement-learning/python` folder with the one provided in this repository. The difference is that pytorch has been bumped up to version 1.0.0. from version 0.4.0 in the original `deep-reinforcement-learning/python/requirements.txt` file. Then, install several dependencies with 

```bash
pip install .
```

6. Create an [IPython kernel](http://ipython.readthedocs.io/en/stable/install/kernel_install.html) for the `drlnd` environment. 

```bash
python -m ipykernel install --user --name drlnd --display-name "drlnd"
```

7. Before running code in a notebook, change the kernel to match the `drlnd` environment by using the drop-down `Kernel` menu. 

![Kernel][image2]

#### Setup Agent Environment

1. Download the environment from one of the links below.  You need only select the environment that matches your operating system:
    - Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Linux.zip)
        - Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher.app.zip)
        - Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Windows_x86.zip)
        - Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Windows_x86_64.zip)
        
        

2. Place the environment file in the `p2_continuous-control/` folder of the `deep-reinforcement-learning` folder that was cloned in the Dependencies section, and unzip (or decompress) the file.

3. Copy the `reacher_agent.py`, `actor_critic_model.py`, `checkpoint_actor.pth`, `checkpoint_critic.pth`, `Continuous_Control.ipynb` files provided in this repository into the `p2_continuous-control/` folder of the `deep-reinforcement-learning` folder that was cloned in the Dependencies section. 

4. Start a jupyter notebook in the `drlnd` environment created in the Dependencies section. Set the kernel to `drlnd` kernel created in the Dependencies section.

#### Instructions

Follow the instructions in `Continuous_Control.ipynb` to get started with training your own agent or watch an existing agent (provided  with the `checkpoint_actor.pth`, `checkpoint_critic.pth`) files perform the task!

