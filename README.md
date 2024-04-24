# Google-Girl-Hackathon-2024
The problem statement for the Silicon Track of Google Girl Hackathon 2024 revolves around optimizing the design of a Network on Chip for a System on chip architecture consisting of CPU, IO Peripherals and system memory.The challenge is to optimize the chip in such a way that it minimizes latency,maximizes bandwidth and improves area and power efficiency. 
# Why is the project useful
Optimizing an NOC design can further lead to improving efficiency of embedded systems, IoT devices, electronic gadgets and more. The use of RL agorithms make it more flexible and adaptible to dynamic environments ensuring that NOC is working under various workload and traffic conditions

# Approach
We can approach using Reinforcement learning. The algorithm that can be best suited is the Deep Deterministic Policy Gradient (DDPG) which is an actor-critic reinforcement learning algorithm. It is designed for continuous state and action spaces.By defining a custom environment for the problem, state space, action space and reward structures are specified.Pythia’s PL agent architecture is used to customize and fit the requirements. It supports the DDPG algorithm.
The algorithm uses two neural networks, one for the actor and one for the critic. The actor policy is updated according to the sampled policy gradient. The actor is a policy network, which provides mapping sequences. The critic network estimates the communication cost of these mapping sequences. The learning is stored in samples for training. Training the critic network and actor update are necessary steps to minimise the errors and maximise the accuracy. Then the values must be updated improving the policy. The algorithm iterates and adjusts parameters such as buffer size, arbiter weights and throttling frequency. When trained within the environment, NOC learns to dynamically adapt to various traffic conditions

# Prerequisites:
Before setting up the Pythia environment, ensure you have the following prerequisites installed:
Python (version 3.6 or higher)
TensorFlow (version 2.0 or higher)
PyTorch (version 1.6 or higher)
NumPy
Pandas
Matplotlib

# Pythia framework
Pythia, which formulates the prefetcher as a reinforcement learning agent. For every demand request, Pythia observes multiple different types of program context information to make a prefetch decision. For every prefetch decision, Pythia receives a numerical reward that evaluates prefetch quality under the current memory bandwidth usage. Pythia uses this reward to reinforce the correlation between program context information and prefetch decision to generate highly accurate, timely, and system-aware prefetch requests in the future.
Pythia is implemented in ChampSim simulator.
Pythia can be used for training RL agents using DDPG algorith, and evaluating the performance.

This has the detailed information on using Pythia

@inproceedings{bera2021,
  author = {Bera, Rahul and Kanellopoulos, Konstantinos and Nori, Anant V. and Shahroodi, Taha and Subramoney, Sreenivas and Mutlu, Onur},
  title = {{Pythia: A Customizable Hardware Prefetching Framework Using Online Reinforcement Learning}},
  booktitle = {Proceedings of the 54th Annual IEEE/ACM International Symposium on Microarchitecture},
  year = {2021}
}

# Run the  DDPG algorithm code
It invlolves adding all the libaries, setting up the RL frameowrk using Pythia. 
Then the algorithm paramters are initialized and functions are called. Training is monitored and evaluated and compared to see if they are close to the benchmark after which iterations lead to optimization.Experiment with different configurations, such as reward functions and state representations, to optimize the agent's behavior further.

# Other details
Make sure that the environment simulates workload and traffic patterns, buffer sizes and arbiters accurately. Accurate buffer sizes, arbiter designs are necessary for area optimization.Efficient routing algorithms are also necessary to ensure optimum data paths.
