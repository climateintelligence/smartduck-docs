# Deploy a building block as Climate Service

## Example: Duck Demo App

Duck is a demo web-application for the *CLINT* project.

Smartduck is a demo web-application of AI-enhanced Climate Science.
It is based on the [Phoenix](https://pyramid-phoenix.readthedocs.io/en/latest/) web-application from the [Birdhouse](http://bird-house.github.io/) collection and makes use of the [PyWPS](https://pywps.org/) Python package, which is an implementation of the [Web Processing Service](https://www.ogc.org/standards/wps) standard from the [Open Geospatial Consortium](https://www.ogc.org/).

Smartduck uses [CRAI](https://github.com/FREVA-CLINT/climatereconstructionAI/tree/clint), a state-of-the-art deep learning based inpainting technology to infill missing values in climate datasets[^1].

The current demo gives the possibility to infill near-surface air temperature anomalies in the [HadCRUT4](https://www.metoffice.gov.uk/hadobs/hadcrut4/) and [HadCRUT5](https://www.metoffice.gov.uk/hadobs/hadcrut5/) datasets. The input and output netCDF files are handled through an intuitive user interface.

[^1]: [Kadow, C. *et al.*, *Nature Geoscience* 13, 408–413 (2020)](http://dx.doi.org/10.1038/s41561-020-0582-5)


The current demo gives the possibility to infill near-surface air temperature anomalies in the [HadCRUT4](https://www.metoffice.gov.uk/hadobs/hadcrut4/) and [HadCRUT5](https://www.metoffice.gov.uk/hadobs/hadcrut5/) datasets.

## Install duck with conda

We need `mamba` to install the requirements.
Use your existing `mamba` or install it from here:
https://github.com/conda-forge/miniforge

Get the source:
```
git clone https://github.com/climateintelligence/duck.git
cd duck
```

Create the conda environment for duck:
```
mamba env create
```

Activate the duck environment:
```
conda activate duck
```

Install duck in this environment:
```
pip install -e .
```

Start your duck as a web service:
```
duck start -d
```

See it is responding by sending a WPS `GetCapabilities` request:

http://localhost:5000?service=WPS&request=GetCapabilities

You can stop the service with:
```
duck stop
```
