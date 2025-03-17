# Simulation benchmarks

CORSIKA is the state-of-the-art software for the simulation of cosmic ray air showers. As such, it can be used to create several benchmarks to evaluate the performance of other competing programs, both from the resource usage and from the physics output point of view.

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

Following the strategy employed in the CONCORDIA project (WP3 of the ESCAPE initiative), singularity containers with CORSIKA7 have been prepared, together with a set of scripts to run them on a batch system (slurm). All the codes and the container recipes are available on <a href="https://github.com/Gaias2-ICSC/corsikasim/"> github </a>.

### Preliminary benchmark

The results from the preliminary set of benchmark simulations setup are available <a href="benchsim/testprod"> here </a>.

### Deliverable A


