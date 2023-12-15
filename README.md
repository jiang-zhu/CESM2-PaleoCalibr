# CESM2-PaleoCalibr: The Paleoclimate-Calibrated CESM2.1.x

We implemented two changes in the standard CESM2.1.x to fix the unrealistically high ECS and cold simulation of the Last Glacial Maximum. The fixes include:
* removing a limiter on the cloud ice number in microphysics to improve the physical consistency of mixed-phase clouds
* shortening the microphysical timestep (substepping in MG2) to improve the numerical performance, i.e. a converging solution in the cloud feedback.

CESM2-PaleoCalibr has been validated with the ~2° CAM6 with a compset of 1850_CAM60_CLM50%BGC-CROP_CICE_POP2_MOSART_CISM2%NOEVOLVE_WW3. It should also improve simulations with other configurations (i.e., the ~1° CAM6) but it is unclear how much substepping is needed. Substepping of 8 increases model cost by ~20%.

**Data availability**
* [Derecho](https://arc.ucar.edu/knowledge_base/74317833): /glade/campaign/cgd/ppc/jiangzhu
* ESGF: Source ID: CESM2-FV2 and CESM2; Variant Label: r1i2p2f1; Version: 20220915. Or, you could use this link: https://esgf-node.llnl.gov/search/cmip6?min_version=20220915&institution_id=NCAR&project=CMIP6

References
* Zhu, J., Otto-Bliesner, B. L., Brady, E. C., Gettelman, A., Bacmeister, J. T., Neale, R. B., Poulsen, C. J., Shaw, J. K., McGraw, Z. S., & Kay, J. E. (2022). LGM paleoclimate constraints inform cloud parameterizations and equilibrium climate sensitivity in CESM2. Journal of Advances in Modeling Earth Systems, 14(4), e2021MS002776. https://doi.org/10.1029/2021MS002776
* Zhu, J., Otto-Bliesner, B. L., Brady, E. C., Poulsen, C. J., Tierney, J. E., Lofverstrom, M., & DiNezio, P. (2021). Assessment of equilibrium climate sensitivity of the Community Earth System Model version 2 through simulation of the Last Glacial Maximum. Geophysical Research Letters, n/a(n/a), e2020GL091220. https://doi.org/10.1029/2020GL091220
