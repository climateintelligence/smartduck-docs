# Welcome to Smartduck

Smartduck is a demo web-application of AI-enhanced Climate Science.
It is based on the [Phoenix](https://pyramid-phoenix.readthedocs.io/en/latest/) web-application from the [Birdhouse](http://bird-house.github.io/) collection and makes use of the [PyWPS](https://pywps.org/) Python package, which is an implementation of the [Web Processing Service](https://www.ogc.org/standards/wps) standard from the [Open Geospatial Consortium](https://www.ogc.org/).

Smartduck uses [climatereconstructionAI](https://github.com/FREVA-CLINT/climatereconstructionAI/tree/clint), a state-of-the-art deep learning based inpainting technology to infill missing values in climate datasets[^1].


The current demo gives the possibility to infill near-surface air temperature anomalies in the [HadCRUT4](https://www.metoffice.gov.uk/hadobs/hadcrut4/) and [HadCRUT5](https://www.metoffice.gov.uk/hadobs/hadcrut5/) datasets. The input and output netCDF files are handled through an intuitive user interface.

This demo web-application has been created by Carsten Ehbrecht and Étienne Plésiat in the framework of the work package 8 of the [CLINT](https://climateintelligence.eu/) H2020 project.


[^1]: [Kadow, C. *et al.*, *Nature Geoscience* 13, 408–413 (2020)](http://dx.doi.org/10.1038/s41561-020-0582-5)

```{tableofcontents}
```
