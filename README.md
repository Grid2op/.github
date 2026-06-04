# Grid2op

Grid2Op provides a simulation environment for running fast and reproducible "experiments" on power grids. Such experiments could include running large scale powerflows, training or evaluating "smart controller" (heuristic based, optimization based, machine-learning based or a combination of any) in realistic settings (*eg* with operational constraints). It can also be used to model sequential decision making in power system. 

# Eco system

The grid2op ecosystem is split into two. There are the "core" packages, well maintained, well tested and documented. With them comes the "companions" packages. Their role is to make the use of core package easier, better integrated with other tools or to promote the use of certain core packages in a specific settings.

> You are using grid2op for some "experiments" and want to share more broadly your work ? Do not hesitate to reach out to use by oppening a discussion and we will see how your work could be integrated in the eco system.

The current roadmap for the eco system can be found here [ROADMAP](https://github.com/Grid2op/.github/blob/main/ROADMAP.md)

## Core packages

As of now, there are 2 core packages:

- [grid2op](https://github.com/Grid2op/grid2op) is the core package. It is pure python, available on pypi and rather flexible. It allows lots of customization and provide default implementation for most of its component
- [lightsim2grid](https://github.com/Grid2op/lightsim2grid) is a grid2op "backend" that is a port of Pandapower in c++ and is optimized for speed and usability in grid2op

## Example / companion packages

This is anon exhaustive list of current companion packages:

- [pypowsybl2grid](https://github.com/Grid2op/pypowsybl2grid) is another grid2op "backend", currently under heavy development. It aims at bringing all the power of the powsybl framework (including its capacity to simulate in great detail a powergrid) into the grid2op ecosystem
- [chronix2grid](https://github.com/Grid2op/chronix2grid) is the package that we use to generate "time series" that are themselves used in grid2op environment. They provide load and generation for each time step of the grid during the entire episode.
- [l2rpn-baselines](https://github.com/Grid2op/l2rpn-baselines) is pacakge that aims at providing code example to get started in the training of agent able to control a powergrid for some reinforcement learning framework.
- [grid2game](https://github.com/Grid2op/grid2game) is a graphical user interface that allows real human to "play" the grid2op and to act as a grid2op agent.
- [grid2viz](https://github.com/Grid2op/grid2viz) is another graphical user interface that allows people to inspect how a grid2op agent has performed when evaluated on a given set of scenarios. It also allows to easily compare an agent with a baseline.
- [LearningToAlert](https://github.com/Grid2op/LearningToAlert) provides an algorithm to "solve" part of the grid2op actions (sending alert at the right time to a possible human operator)
- [grid2op-milp-agent](https://github.com/Grid2op/grid2op-milp-agent) is an example of a grid2op agent that is based on linear optimisation and is able to perform topological actions.

# Other packages

Other contributors are also developing code that could be hosted here. For example, the l2rpn top performers aften publish on github their approach. See https://l2rpn-baselines.readthedocs.io/en/latest/external_contributions.html for an updated list.

 The ecosystem is also made of packages hosted elsewhere, for example:

 - a graphical user interface developed by NVIDIA: https://github.com/NVIDIA/energy-sdk-l2rpn
 - some good solutions to the L2RPN competitions:
   - https://github.com/lajavaness/l2rpn-2023-ljn-agent
   - https://github.com/enlite-ai/maze-l2rpn-2022-submission
   - etc. 
