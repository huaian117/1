# Wytham Woods: 3D model

This repository hosts the Wytham Woods 3D scene.

![alt text](http://www2.geog.ucl.ac.uk/~uceskca/trees.png?width=660&height=628&cropmode=none)

## Overview

The Wytham Woods 3D model represents a one hectare model for a deciduous forest in Wytham, UK. The model contains 559 individual trees. We matched the TLS data with traditional census data to determine the species of each individual tree and allocate species-specific radiometric properties.
Full details of the model generation can be found in Calders et. al (2018).

The 3D information is stored in *obj* files and can readily be used in the *librat* radiative transfer model (see https://github.com/philwilkes/librat_in_jupyter/). Wood and leaf material is stored in separate *obj* files, the spectral information is stored in *dat* files.

## Authors

* **Kim Calders** (kim.calders@ugent.be)
* **Niall Origo** (niall.origo@npl.co.uk)
* **Mathias Disney**
* **Joanne Nightingale**
* **Chang Liu**

## License

This project is licensed under the [Attribution-NonCommercial 4.0 International (CC BY-NC 4.0) License](https://creativecommons.org/licenses/by-nc/4.0/). Please cite Calders et al. (2018) when using this 3D scene. 

## Reference
Calders, K., Origo, N., Burt, A., Disney, M. Nightingale, J., Raumonen, P., Akerblom, M, Malhi, Y. and Lewis, P. (2018) Virtual forest for radiative transfer modelling: realistic stand reconstruction from terrestrial LiDAR. Remote Sensing, 10(6):1-15

## Acknowledgements
The research leading to these results was funded through the Metrology for Earth Observation and Climate project (MetEOC-2), grant number ENV55 within the European Metrology Research Programme (EMRP). The EMRP is jointly funded by the EMRP participating countries within EURAMET and the European Union.

## Updates
Version 5 (on master) fixes an error where the LAI was twice as large as it should be (created in version 3). There were other errors that were fixed in version 3 related to parameterisation of the leaf addition code such that a merge back to that would not be useful.
Version 4 (on version4) fixes an error where the DEM wasn't positioned correctly.
Version 3 (on version3) includes updates to the number of leaves (version2 had half as many leaves as intended) and updated spectra. The latter has been created by using the measured leaf reflectances to invert the PROSPECT model and return the reflectance and transmittance. This is not an ideal method but it is the best I can do without transmittance data. The prospect parameters can also be found in the `materials/leafspec` directory.
