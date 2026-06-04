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

Grid2Op is a simulation environment for fast, reproducible experiments on power grids. Use it to run large-scale powerflows, to train or evaluate "smart controllers" (heuristic, optimization-based, machine-learning, or any combination) under realistic operational constraints, or to model sequential decision-making in power systems.

# Ecosystem

The Grid2op ecosystem has two parts: **core packages**, which are well maintained, tested, and documented, and **companion packages**, which make the core packages easier to use, integrate them with other tools, or apply them to specific settings.

> Using Grid2op for your own experiments and want to share your work? Open a discussion and we'll look at how it could fit into the ecosystem.

The current roadmap is available here: [ROADMAP](https://github.com/Grid2op/.github/blob/main/ROADMAP.md).

## Core packages

There are currently two core packages:

- [grid2op](https://github.com/Grid2op/grid2op) — the core package. Pure Python, available on PyPI, and highly flexible: it allows extensive customization and ships default implementations for most of its components.
- [lightsim2grid](https://github.com/Grid2op/lightsim2grid) — a fast Grid2op "backend" / "computation engine". It implements the power-flow solvers in C++, optimized for speed and ease of use within Grid2op.

## Companion packages

A non-exhaustive list of current companion packages:

- [pypowsybl2grid](https://github.com/Grid2op/pypowsybl2grid) — another Grid2op backend, under active development. It brings the full power of the PowSyBl framework, including its detailed power-grid simulation, into the ecosystem.
- [chronix2grid](https://github.com/Grid2op/chronix2grid) — generates the time series used in Grid2op environments, providing load and generation values for every time step of an episode.
- [l2rpn-baselines](https://github.com/Grid2op/l2rpn-baselines) — code examples to get started training agents that control a power grid, for several reinforcement-learning frameworks.
- [grid2game](https://github.com/Grid2op/grid2game) — a graphical interface that lets a human "play" Grid2op and act as an agent.
- [grid2viz](https://github.com/Grid2op/grid2viz) — a graphical interface for inspecting how a Grid2op agent performed across a set of scenarios, and for comparing an agent against a baseline.
- [LearningToAlert](https://github.com/Grid2op/LearningToAlert) — an algorithm for one part of the Grid2op action space: sending alerts to a human operator at the right moment.
- [grid2op-milp-agent](https://github.com/Grid2op/grid2op-milp-agent) — an example Grid2op agent based on linear optimization that performs topological actions.

# Other packages

Other contributors develop code that could be hosted here. For example, top L2RPN performers often publish their approaches on GitHub — see the [updated list of external contributions](https://l2rpn-baselines.readthedocs.io/en/latest/external_contributions.html).

The ecosystem also includes packages hosted elsewhere, such as:

- a graphical interface developed by NVIDIA: https://github.com/NVIDIA/energy-sdk-l2rpn
- strong solutions to the L2RPN competitions, for example:
  - https://github.com/lajavaness/l2rpn-2023-ljn-agent
  - https://github.com/enlite-ai/maze-l2rpn-2022-submission
- a "computation engine" based on "dynamics" simulation and the gridpack framework see https://github.com/GridOPTICS/GridPACK/tree/grid2op_integration
