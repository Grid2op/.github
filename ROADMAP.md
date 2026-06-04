# Grid2Op Ecosystem Roadmap

The Grid2Op ecosystem provides an open, modular platform for research and
development in power system operations. It is built around a core simulation
framework and a growing set of companion packages, backends, and integrations.

This document describes the overall direction of the ecosystem. It is intended
as a compass for the maintainers of each package when writing their own
roadmaps, and as an invitation to example package contributors to align their
work with these shared goals.

---

## Core principles

The following principles reflect the current focus of the ecosystem. They are
intended to guide development and prioritisation today, and may evolve as the
ecosystem matures and its community grows.

### Speed

Simulation should never be the bottleneck for research. Whether running a
single agent in a notebook or training across thousands of parallel
environments, the ecosystem should make efficient use of available hardware.

*In practice this means, for example: avoiding unnecessary data copies between
the backend and the rest of the framework, and adding multiprocessing support
to batch simulations in compiled backends.*

### Realism

The problems Grid2Op exposes should reflect the complexity of real power
systems, close enough that methods developed here are meaningful to
practitioners. This means progressively closing the gap between what the
platform models and what operators actually deal with.

*In practice this means, for example: modelling new types of elements such as
transformers, demand-side management, and deferrable loads. On the backend
side, this means higher-fidelity power flow solvers — the ongoing integration
with PowSyBl is a concrete step in this direction, and Power Grid Model is a
natural candidate for future collaboration.*

### Research-friendliness

The ecosystem should be easy to extend, experiment with, and build upon.
A researcher should be able to plug in a new idea — a custom backend, reward
function, action space, or training framework — without having to understand
the entire codebase. This principle covers both the modularity of the
architecture and its usability within the wider research tooling ecosystem.

*In practice this means, for example: improving internal modularity so that
components like redispatching routines or protection models can be swapped or
extended independently, and ensuring smooth integration with widely used
frameworks such as Gymnasium. More broadly, Grid2Op sits at a natural
intersection with other open source AI and energy projects — GridFM, as a
foundation model framework for power grids, is one example of a project where
both communities could mutually benefit.*

---

## Cross-cutting commitments

These apply to every repository in the ecosystem at all times, regardless of
release cycle or roadmap priorities:

- **Security issues are always the top priority** and are addressed before any
  feature work.
- **Bug fixes take precedence over new features.**

---

## Package roadmaps

Each core package maintains its own roadmap that maps concrete work to the
principles above:

- [grid2op](https://github.com/Grid2Op/grid2op/blob/master/ROADMAP.md)
- [lightsim2grid](https://github.com/Grid2Op/lightsim2grid/blob/master/ROADMAP.md)

---

## Example packages

The Grid2Op ecosystem welcomes experimental and companion packages — baselines,
data generators, research paper code, and beyond. These packages are not
required to follow this roadmap. However, contributors are warmly invited to
consider these principles when planning their development: a package that is
fast, realistic, and easy to integrate tends to be more useful to the community
and more likely to have a lasting impact.

---

*Last updated: May 2026*