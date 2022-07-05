Guideline

the following sections are describing how to transfer scientific methods into technical services which are deployable in climate resilience information systems.

## Background

Climate datasets rapidly grow in volume and complexity and creating climate products requires high bandwidth, massive storage and large compute resources. For some regions, low bandwidth constitutes a real obstacle to developing climate services. Data volume also hinders reproducibility because very few institutions have the means to archive original data sets over the long term. Moreover, typical climate products often aggregate multiple sources of information, yet mechanisms to systematically track and document the provenance of all these data are only emerging. So although there is a general consensus that climate information should follow the **FAIR Principles** :cite:`Wilkinson2016,mons2017`, that is be *findable, accessible, interoperable, and reusable*, a number of obstacles hinder progress. The following principles can help set up efficient climate services information systems, and show how the four FAIR Principles not only apply to data, but also to analytical processes.

## FAIR principles

For climate resilience information systems

### Findable
Findable is the basic requirement for data and product usage and already an difficult obstacle with time intensive work for the data provider ensuring find-able data. On the production level finding algorithms requires open source software with intensive documentation.

**Finding data:**

Finding data requires a structured data repository and if possible an assigning of a globally unique and eternally persistent identifier (like a DOI or Handle), describing the data with rich metadata, and making sure it is find-able through discovery portals of search clients. It is recommended to establish data repository collecting and managing core input and output data enabling coordinated provisioning and sharing of data focusing on sustainable storage and management of core data collections. Depending on data importance a certified long-term archive can be managed. The identification of core data collections to be managed in centralized repositories might be realized with e.g the Research Data Management Organiser (RDMO) tool. https://rdmorganiser.github.io/

**Finding algorithms:**

In free and open source for geospatial (FOSS4G) developments workflows, independent developer groups are collaborating in a win-win situation and ensuring a high-quality software product :cite:`Bahamdain2015`. Public repositories enabling a work efficient participating and knowledge sharing approach :cite:`Bejoy2010`. A high certainty and quality of scientific evidence is needed for information in a juridical context to regulate the conflict between economic development and environmental protection :cite:`Brown2019`. Therefor backend solutions to provide climate information for decision makers, need to be as much as possible 'error free'. The challenge of high-quality software solutions is illustrated with Linus's law that "given enough eyeballs, all bugs are shallow". :cite:`Raymond2001`.

###Accessible
**Access to data:**

For data users, the prevailing *modus operandi* has traditionally been to download raw data locally to conduct analyses. As data volume grows, bandwidth and local storage capacity limits the type of science that individual scientists can perform.

**Access to algorithms:**

A high certainty and quality of scientific evidence is needed for information in a juridical context to regulate the conflict between economic development and environmental protection :cite:`Brown2019`. Therefor backend solutions to provide climate information for decision makers, need to be as much as possible 'error free'. The challenge of high-quality software solutions is illustrated with Linus's law that "given enough eyeballs, all bugs are shallow". :cite:`Raymond2001`. In free and open source for geospatial (FOSS4G) developments workflows, independent developer groups are collaborating in a win-win situation and ensuring a high-quality software product :cite:`Bahamdain2015`. Public repositories enabling a work efficient participating and knowledge sharing approach :cite:`Bejoy2010`.

###Interoperable

Following the UNGGIM recommendations (2020) about 'Implementation and adoption of standards for the global geospatial information community' climate data should be organized following this UNGIM recommendations.  (http://ggim.un.org/meetings/GGIM-committee/10th-Session/documents/E-C.20-2020-33-Add_1-Implementation-and-Adoption-of-Standards-21Jul2020.pdf)
Interoperabillity needs to be respected on two levels:

**Interoperable data :**

following the conventions regarding metadata.

**Interoperable structures:**

The OGC standardisation also enables communication between climate services information systems services.

###Reusable

Reusabillity is a major aspect to avoid duplication of work and to foster the dynamique of providing high quality products.

**Reusable data:**

The data should maintain its initial richness. The description of essential, recommended, and optional metadata elements should be machine processable and verifiable, use should be easy and data should be citable to sustain data sharing and recognize the value of data. Result output data from one service can be post-processed by another service where other component are provided.

**Reusable algorithms:**

Contrary to running analysis code on a local machine, it is recommended to use remote services have no direct control on the software they are running. The server's maintainer essentially decides when software and services are upgraded, meaning that within the time a scientist performs initial exploration and produces the final version of a figure for a paper, remote-services might have slightly changed or have been retired.

**Reproducabillity:**

This implies that reproducabillity results might not be easily reproducible if earlier versions of services are not available anymore. This puts an additional burden on scientists to carefully monitor the version of all the remote services used in the analysis to be able to explain discrepancies between results. Similar issues occur with data versions. If a scientist used version 1 for an analysis, there is no guarantee the source data will be archived over the long term if it has been superseded by version 2. In practice, climate services use ensembles of simulations, meaning that typical climate products aggregate hundreds or thousands of files, whose versions should ideally be tracked up until the final graphic or table. This capability to uniquely identify simulation files, errata and updates is available in CMIP6 :cite:`Stockhause2017,Weigel2013`, but it is the responsibility of climate service providers to embed this information into the products they develop.

## Climate building blocks

The [Birdhouse](http://bird-house.github.io/) organisation is a collection on OGC Standards based tools which enables you to build your own customised Climate Resilience information System.

## Create your own climate building block


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
conda install -c conda-forge cookiecutter cruft
```

Run the cookiecutter with the birdhouse template:
```
cruft create https://github.com/bird-house/cookiecutter-birdhouse.git
```

Once cookiecutter clones the template, you will be asked a series of questions related to your project:
```console
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
