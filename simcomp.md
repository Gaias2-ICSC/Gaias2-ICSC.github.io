# Simulation comparisons

The current standard for CORSIKA simulations is version 7 of the software. This code has been used in the last decade to simulate cosmic ray air showers in many different experiments. The code is currently being entirely rewritten in C++, towards version 8 of the software (available <a href="https://gitlab.iap.kit.edu/AirShowerPhysics/corsika">here</a>).

Following the advice of CORSIKA8 developers, as the code is still in a beta version, the mass productions reported in the <a href="../benchsim" >simulation benchmarks</a> have been run using CORSIKA7. These simulations will be used for the training and validation of the Generative AIs to be developed within GAIAS2. However it can be valuable to check the agreement between the two versions of the code.

### CORSIKA8 preparation

A CORSIKA8 container has been first prepared. Differently from CORSIKA7, only one compilation of the code is necessary, since all physics inputs are available together, and the simulation setup can be personalised at runtime directly as an option for the CORSIKA8 executable. The container definition is available on <a href="https://github.com/Gaias2-ICSC/corsikasim/tree/main/corsika8_containers">github</a>.

It should be noted that the container prepared here is not the official container released with the current CORSIKA8 beta, as incompatibilities have been found in the installation procedure there.

### CORSIKA8 running

The CORSIKA8 executable can be directly run from the container

`singularity exec corsika8.sif /corsika-build/applications/c8_air_shower`

followed by the required options (such as the energy range, the hadronic model of interest, the primary cosmic ray, etc.).

`singularity exec corsika8.sif /corsika-build/applications/c8_air_shower --help`

returns the full list of possible arguments.

### CORSIKA8 productions

A simplified setup has been used for the CORSIKA8 productions, with monocromatic generation of protons of 1, 10 and 100 PeV along the vertical direction. 2000 events have been produced in each simulation setup. Also in this case, as for the CORSIKA7 productions, all simulations have been run on the local servers at the G. Romano Laboratory of the Department of Physics of the University of Salerno.

### Deliverable B

The second deliverable of the GAIAS2 project consists of sanity checks of CORSIKA8 productions in comparison with the standard CORSIKA7 productions. The results are provided in the <a href="simcomp/deliverable">deliverable</a> of this activity.