# Duck Demo App

[Duck](https://github.com/FREVA-CLINT/duck) is a demo web-application for the *CLINT* project.
It provides an AI-enhanced service to infill missing values in climate datasets.

The current demo gives the possibility to infill near-surface air temperature anomalies in the [HadCRUT4](https://www.metoffice.gov.uk/hadobs/hadcrut4/) and [HadCRUT5](https://www.metoffice.gov.uk/hadobs/hadcrut5/) datasets.

## Install duck with conda

We need `mamba` to install the requirements.
Use your existing `mamba` or install it from here:
https://github.com/conda-forge/miniforge

Get the source:
```
git clone https://github.com/FREVA-CLINT/duck.git
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
