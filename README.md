# A Survey of Reinforcement Learning algorithms
In this project I've explored how different RL algorithms performed in various environments. Let's be specific about what these algorithms and the environments are.

### Environments
As anyone working in RL knows, the defacto method of working with environments is through OpenAI's [gym](https://www.gymlibrary.dev/) package. So, I too have chosen to work via this package.
#### 1. HalfCheetah
The [half cheetah environment](https://www.gymlibrary.dev/environments/mujoco/half_cheetah/) is part of the MuJoCo environments provided as
part of the built-in environments of the gym library. This is originally based on the work by
Wawrzy ́nski (2009) from the chapter A Cat-Like Robot Real-Time Learning to Run in the
book Adaptive and Natural Computing Algorithms.

![half_cheetah](https://user-images.githubusercontent.com/24986098/190415392-df795136-a55c-415f-8b34-e55a850c04d3.png)

It is a 2D stick model which has 8 joints and 9 links connecting them, which also has two
paws. The aim is to apply torque on the joints so that the cheetah run forward as fast as
possible and the reward is based on the distance moved forward which will be negative in case
the cheetah moves backward. The torque won’t be applied on the head and the torso joints.

The action space is a continuous space defined by 6 degrees of freedom each taking values
between -1 and +1. And the observation space consists of positional and velocity values for
each of the cheetah body parts, represented by a vector of length 17.

#### 2. NLPGym
[NLPGym environment](https://github.com/rajcscw/nlp-gym) is a toolkit developed by Ramamurthy et al. (2020) which aims to
bridge the gap between applications in the fields of NLP and RL. This environment does not
come as part of the built-in environments from the gym library. Instead it has to be installed
separately as it is a third-party environment. But, the developers have followed the gym
library’s API, which essentially makes sure that the usage of the environment remains similar
to the other environments.

This toolkit provides a set of interactive environments commonly needed in Natural language
processing tasks such as Sequence tagging, Sequence classification, and Question answering.
Each of these tasks have differing action space and observation spaces, with each problem
cast as a Markov Decision Process (MDP).

### RL Algorithms
* Q-learning & Deep Q-Network (DQN)
* Trust Region Policy Optimization (TRPO)
* Deep Determinstic Policy Gradient (DDPG)

### Technologies Used
* Tensorflow
* OpenAI gym
* Stable-Baselines3

### Results (so far)
**Cartpole balancing** and **Lunar Lander** are two of the introductory environments for teaching about Reinforcement Learning. Both of these were solved by the DQN algorithm as of now.
