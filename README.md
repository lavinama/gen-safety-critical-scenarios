# gen-safety-critical-scenarios
Generation of safety-critical scenarios that are used to to improve the safety of autonomous vehicles.

This is an example of a scenario generated by the rl agents (the AV vehicle in ![green](https://via.placeholder.com/15/c5f015/c5f015.png) and the adversarial rl-agents in ![blue](https://via.placeholder.com/15/1589F0/1589F0.png)). We can see that the scenario generated is dangerous but at the same time realistic. Finding this perfect balance was the great challenge of this project.

https://user-images.githubusercontent.com/70475094/197851556-7571ffab-531e-4115-aecc-58e477361f2d.mp4


There are two main parts to this project:
### 1. The simulation software: [`highway-env`](https://github.com/lavinama/highway-env)

This is a 2D simulation software where different types of agents interact mimicking the behaviour of vehicles in a road environment. The problem is that this simulation software did not accound for adversarial agents, agent's who don't follow the rules of the road. Example of these agents in real life are for example intoxicated drivers. Hence, we needed to create this special scenario in the simulation software. This is under the [`adv-highway-env`](https://github.com/lavinama/highway-env/tree/adv-highway-env) branch 

### 2. The reinforcement learning agents: [`rl-agents`](https://github.com/lavinama/rl-agents/tree/madqn)

The repository [`rl-agents`](https://github.com/lavinama/rl-agents/tree/madqn) is similar to the one created by @eleurent (https://github.com/eleurent/rl-agents). However, it has two changes. First, under the branch `madqn` it includes an implementation of the MADQN algorithm. Second, it allows has lfs enabled allowing me to push the models to the repository which can be found in the directory `rl-agents/project/*`. It also includes the shell scripts that are required in order to train the agents under the directory `rl-agents/shell_scripts/*`.
