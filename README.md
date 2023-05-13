# Optimised Numerical Methods for the Computation of Particles in Fusion Hotspots and Particle Interactions in Magnetized Liner Inertial Fusion (MagLIF)

## Description

## Barnes Hut Simulation
The Barnes Hut Model is a method for calculating the gravitational force between charged particles. It is a tree-based algorithm that uses a quadtree or octree to calculate the force between particles. The algorithm is described in the paper [A hierarchical O(N log N) force-calculation algorithm](https://www.doi.org/10.1038/324446a0) by Barnes and Hut.

While summing the forces between every particle is an O(N^2) operation, the Barnes Hut Model uses the octree to reduce the number of particles that need to be considered when calculating the force between particles. [The algorithm](http://arborjs.org/docs/barnes-hut) for calculating the force between particles is as follows:
1. If the current node is an external node (and it is not body b), calculate the force exerted by the current node on b, and add this amount to b’s net force.
2. Otherwise, calculate the ratio s/d, where s is the width of the region represented by the internal node, and d is the distance between the body and the node’s center-of-mass. 
3. If s/d < θ, treat this internal node as a single body, and calculate the force it exerts on body b, and add this amount to b’s net force.
4. Otherwise, run the procedure recursively on each of the current node’s children.

The Barnes Hut Model is an O(N log N) algorithm. The value of θ is a parameter that affects the degree of approximation. The smaller the value of θ, the more accurate the simulation is. However, the smaller the value of θ, the longer the simulation takes to run.

## Projects from previous years

### NUSH (2022)

### [check hilary's school] (2021)
