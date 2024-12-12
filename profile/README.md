<!--
## Hi there 👋

**Here are some ideas to get you started:**

🙋‍♀️ A short introduction - what is your organization all about?
🌈 Contribution guidelines - how can the community get involved?
👩‍💻 Useful resources - where can the community find your docs? Is there anything else the community should know?
🍿 Fun facts - what does your team eat for breakfast?
🧙 Remember, you can do mighty things with the power of [Markdown](https://docs.github.com/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
-->

# Grid2op

Grid2op aims at make the use of (and the research on) "machine learning" or "artificial intelligence" for power grid operations purposed.

It can (hopefully) be used both by industry leaders and AI researchers.

# Eco system

The grid2op ecosystem is made of different packages with different goals:

- [grid2op](https://github.com/Grid2op/grid2op) is the core package. It is pure python, available on pypi and rather flexible. It allows lots of customization and provide default implementation for most of its component
- [lightsim2grid](https://github.com/Grid2op/lightsim2grid) is a grid2op "backend" that is a port of Pandapower in c++ and is optimized for speed and usability in grid2op
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
