# Birdhouse

[Birdhouse](http://bird-house.github.io/) tools enable you to build your
own customised [Web Processing Service](http://opengeospatial.org/standards/wps)
application in support of web-based geospatial (climate) data analysis.
Birdhouse offers you:

* A [Cookiecutter template](https://github.com/bird-house/cookiecutter-birdhouse) to create your own [PyWPS](http://pywps.org/) compute service.
* A web-based application, [Phoenix](https://github.com/bird-house/pyramid-phoenix), and ...
* ... a Python library, [Birdy](https://github.com/bird-house/birdy), suitable for [Jupyter notebooks](https://jupyter.org/) to interact with WPS compute services.

## Example: duck app

We show here an example how to build your processing service application, *duck*, using the cookiecutter template.

Install cookiecutter:
```
$ conda install -c conda-forge cookiecutter cruft
```

Run the cookiecutter with the birdhouse template:
```
$ cruft create https://github.com/bird-house/cookiecutter-birdhouse.git
```

Once cookiecutter clones the template, you will be asked a series of questions related to your project:
```
full_name [Full Name]: Alice Kingsleigh
email [your@email]: alice@wonderland.org
github_username [bird-house]: clint
project_name [Babybird]: duck
project_slug [duck]:
project_repo_name [duck]:
project_readthedocs_name [duck]:
project_short_description [A Web Processing Service for Climate Data Analysis.]: A Demo Web Service for Clint.
version [0.1.0]:
Select open_source_license:
1 - Apache Software License 2.0
2 - MIT license
3 - BSD license
4 - ISC license
5 - GNU General Public License v3
6 - Not open source
Choose from 1, 2, 3, 4, 5, 6 [1]: 1
http_port [5000]:
use_pytest [y]: y
create_author_file [y]: y
```

We have created a *duck* app for the *CLINT* project using this template.
We describe this app in the next section.
