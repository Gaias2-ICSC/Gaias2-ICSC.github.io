# Deliverable A

Using the same CORSIKA7 containers that have been tested in the first test productions, described <a href = "testprod">here</a>, the first deliverable of the GAIAS2 consists of a set of high-statistics simulations of proton cosmic rays.

10 energy ranges have been made available:

1. 1 - 10 TeV
2. 10 - 100 TeV
3. 100 TeV - 1 PeV
4. 1 PeV - 10 PeV
5. 10 PeV - 20 PeV
6. 20 PeV - 30 PeV
7. 30 PeV - 50 PeV
8. 50 PeV - 100 PeV
9. 100 PeV - 200 PeV
10. 200 PeV - 300 PeV

for each generation setup (URQMD or GEISHA of the low-energy hadronic model, EPOS or SYBILL for the high-energy hadronic model, in all the 4 possible combinations).

The event generation is performed according to a power-law spectrum with spectral index -1, to allow for the generation of a flat distribution in the logarithm of the cosmic ray energy. 50,000 events have been generated in each decade in energy. To do so, generation has been split into different numbers of jobs for each range of interest.

These simulations have been performed on local servers in the G. Romano Laboratory at the Department of Physics of the University of Salerno. In total, 30 TB of disk space are used to store them. Approximately 500k HSPEC06 hours have been consumed. 

All codes and containers employed for the generation of the CORSIKA events is available on <a href = "https://github.com/Gaias2-ICSC/corsikasim">github</a>.

