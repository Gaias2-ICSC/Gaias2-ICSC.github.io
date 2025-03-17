# Simulation benchmarks

CORSIKA is the state-of-the-art software for the simulation of cosmic ray air showers.

## Benchmark configuration

### Primary cosmic rays

The yield in particles out of the interaction of a primary cosmic rays depends on its mass. Even though most cosmic rays are protons, the composition of the cosmic ray flux changes significantly all through the spectrum, and thus different primary species must be considered. 5 species are usually chosen to allow for a characterisation on the primary CR spectrum:

- Protons
- Helium
- Carbon
- Silicon
- Iron

For the benchmark configuration, we limited the simulations to protons.

### Hadronic interaction models

For a given primary, the production of particles in the cosmic ray air shower depend on the hadronic interaction of the primary and of the products of its first interaction. The low-energy hadronic interaction models of choice are

- GEISHA
- URQMD

while for the high-energy hadronic interactions the following models are chosen

- SYBILL 2.3c
- EPOS-LHC

### Other options

#### Energy range

4 sets of energy ranges are tested:

- Low-energy (L): 1 - 100 TeV
- Mid-energy (M): 100 TeV - 10 PeV
- High-energy (H): 10 - 100 PeV
- Ultra-High-energy (UH): 100 PeV - 1 EeV

The energy spectrum of choice is a power law, with spectral index -1 

#### Zenith range

2 sets of zenith ranges (0: vertical, 90: horizontal) are tested:

- Vertical (V): 0 - 60 degrees 
- Horizontal (H): 60 - 90 degrees

Generation is flat in the cosine of the zenith angle

#### Performance checks

The results of the performance checks are available on <a href="https://github.com/Gaias2-ICSC/corsikasim/tree/main/perf"> git </a>