# Simulation comparisons

The current standard for CORSIKA simulations is version 7 of the software. This code has been used in the last decade to simulate cosmic ray air showers in many different experiments. The code is currently being entirely rewritten in C++, towards version 8 of the software (available <a href="https://gitlab.iap.kit.edu/AirShowerPhysics/corsika"> here </a>.

Following the advice of CORSIKA8 developers, as the code is still in a beta version, the mass productions reported in the <a href="../benchsim" > simulation benchmarks </a> have been run using CORSIKA7. However it can be valuable to check the agreement between the two versions of the code.

### CORSIKA8 preparation

A CORSIKA8 container has been first prepared. Differently from CORSIKA7, only one compilation of the code is necessary, since all physics inputs are available together, and the simulation setup can be personalised at runtime directly as an option for the CORSIKA8 executable. The container definition is available on <a href="https://github.com/Gaias2-ICSC/corsikasim/tree/main/corsika8_containers"> git </a>.

### CORSIKA8 running

The CORSIKA8 executable can be directly run from the container

`singularity exec corsika8.sif /corsika-build/applications/c8_air_shower`

followed by the required options (such as the energy range, the hadronic model of interest, the primary cosmic ray, etc.)