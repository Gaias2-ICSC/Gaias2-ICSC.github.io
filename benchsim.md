# Simulation benchmarks

CORSIKA is the state-of-the-art software for the simulation of cosmic ray air showers. As such, it can be considered a benchmarks to evaluate the performance of other cosmic ray simulations, both for what concerns resource usage and the physics output. Given its wide usage, version 7 of the CORSIKA software is considered the current golden standard, and will be used in this context.

## Properties of cosmic ray air showers

Cosmic ray air showers are produced in the aftermath of the interaction of primary cosmic rays with nuclei in the Earth's atmosphere. As a consequence of these interactions, short-lived particles are produced which can either decay or interact as they move through the atmosphere. A certain amount of these particles will reach the ground, constituting the target for air shower detectors which aim at studying the properties of the primary interaction.

Two main components can be identified in the air shower, which may reach the ground

- Electromagnetic: electrons, positrons, and gamma-ray photons, mainly coming from the decay of neutral mesons in the cascade of particles
- Hadronic: muons, neutrinos, and hadronic particles, mainly coming from the decay of charged mesons in the cascade of particles

### Observable quantities on the ground

Two main observable are usually defined:

- The number of electrons at the shower maximum, which is proportional to the energy of the incoming cosmic ray
- The number of muons reaching the ground, which is proportional to the energy and the mass-number of the incoming cosmic ray

## Generation of cosmic ray showers

Following the strategy employed in the CONCORDIA project (WP3 of the <a href="https://projectescape.eu/">ESCAPE</a> initiative), singularity containers with CORSIKA7 have been prepared, together with a set of scripts to run them on a batch system (slurm). All the codes and the container recipes are available on <a href="https://github.com/Gaias2-ICSC/corsikasim/">github</a>.

### Preliminary benchmark

The results from the preliminary set of benchmark simulations setup are available <a href="benchsim/testprod">here</a>.

### Deliverable A

The first deliverable of the GAIAS2 project consists of a benchmark set of cosmic ray Monte Carlo simulations on which generative AIs can be trained and tested. The details on this deliverable are reported <a href = "benchsim/deliverable">here</a>.

