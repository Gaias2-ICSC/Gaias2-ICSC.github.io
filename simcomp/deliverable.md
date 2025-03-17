# Deliverable B

The main goal of Activity B is to verify that CORSIKA7 and CORSIKA8 simulations provide similar outputs. It should be recalled that at the moment, CORSIKA8 is not yet at a stable release, and as such should not be yet used in a real analysis scenario. It is in any case relevant also to estimate possible uncertainties behind the datasets used to train and test the Generative AIs produced in the GAIAS2 project.

## Literature

Comparisons between CORSIKA7 and CORSIKA8 have been provided by the authors of CORSIKA8 as the code is being developed. Such comparisons are partly available in conference proceedings. The most complete of such collections has been published in the ICRC2021 proceedings, grouped together <a href="https://arxiv.org/pdf/2112.11761">here</a>. Additional comparisons have been made public at the ICRC2023 conference, as for example shown in <a href="https://arxiv.org/abs/2308.05475">these proceedings</a>. The current recommendation from the CORSIKA8 developers is to avoid using the code for mass productions in real physics cases, as the code is not yet as complete as CORSIKA7. However, a good agreement is found for the simulation of the most relevant parts of the cosmic ray air shower.

## Current comparisons

A summary of comparisons between simulations with CORSIKA7 and CORSIKA8 obtained with the GAIAS2 productions described in the <a href="../benchsim">simulation benchmarks</a> and in the <a href="../compsim">simulation comparison</a> pages are available on the dedicated <a href="https://github.com/Gaias2-ICSC/compsim">github</a> project. Here, the codes used to obtain distributions out of the simulated datasets are stored, together with some explanatory plots.

A global agreement is found in the distributions of particles on ground and their distributions.