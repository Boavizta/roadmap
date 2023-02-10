# Boavizta's roadmap

Let's create commons to make the environmental impact assessment of digital products, services and systems more reliable, easier and more open.

## General roadmap


## Products

* 💾 [Boavizta repository](#boavizta-repository)
* [Datavizta](#datavizta)
* 🛠️ [Boaviztapi](#boaviztapi)
* [Boagent](#boagent)
* 🛰️ [Cloud-scanner](#cloud-scanner)
* 🔌 [Energizta](#energizta)
* [Eco-benchmark](#eco-benchmark)
* [Cloud-bill](#cloud-bill)


## Boavizta repository

### Objective

### Technical stack

**Language :** Python, CSV

### Main features

### Milestones

### Lead dev

@airloren

### Links

**github :** https://github.com/Boavizta/environmental-footprint-data/blob/main/tools/spiders/README.md


## Datavizta

### Objective

### Technical stack

**Language :** TypeScript, CSS, HTML

**Framework :** Svelte

### Main features

### Milestones

### Lead dev
TBD

### Links

**github :** https://github.com/Boavizta/boavizta-front


## BoaviztAPI

### Objective

Give access to BOAVIZTA reference data and methodologies throught a RESTful API

### Technical stack

**Language :** Python 

**Framework :** FastAPI

### Main features

* Evaluation of manufacture impacts
* Evaluation of usage impacts
* Multiple impacts types (gwp, adp, pe)
* Multiple components (CPU, RAM, SSD, ...)
* Multiple devices (Server, Cloud, more to come)
* Auto-completion of missing values
* Modelization of components, server and cloud energy consumption

### Milestones

* V0.2 : 
  * Code refactoring
  * Model the energy consumption of CPU, RAM, Server & cloud instances
  * Complete CPU data from name
  * Rust & python SDK

* V0.3 : 
  * Add the impacts of IoT devices
  * Add multiple source of impacts factors (electicity map, research paper, ...)
  * Add new component (GPU, HDD)
  * Automate the collection of of components\', devices\' and cloud instances\' characteristics 

* V0.4 : 
  * Model the electrical consumption from Energizta

* V1 : 
  * Test covorage of 95%
  * Code quality process

### Lead dev
@da-ekchajzer

### Links

**github :** https://github.com/Boavizta/boaviztapi

**documentation :** https://doc.dev.api.boavizta.org/

**demo api :** https://dev.api.boavizta.org/docs


## Boagent

### Objective

### Technical stack

**Language :** python

### Main features

### Milestones

### Lead dev
@bpetit

### Links

**github :** https://github.com/Boavizta/boagent


## Cloud-scanner

### Objective

Cloud-scanner returns environmental impacts of your AWS Instances usage.

> Main  objective is to give  a **more realistic view of impacts** compared to what is natively returned in the dashboards of cloud providers, who often rely on carbon compensation mechanism or unclear methodology to display what we consider unrealistically low impacts.

Cloud scanner combines real time usage data from your AWS account with Boavizta API to offer a global view of your impacts. It will later be enriched to cover other cloud providers.

### Technical stack

**Language :** Rust + AWS SDK

### Main features

Generate real time metrics (json or prometheus) that can be displayed in dashboards.

Fine granularity: provide filtering (on tags) to ease attribution to a service or application.

Cloud-scanner can be used:

* from command line 💻 (for a quick one-shot assessment)
* as a server application (for continuous monitoring)⚡

See full documentation: [Introduction - Boavizta cloud scanner 📡](https://boavizta.github.io/cloud-scanner/)

### Milestones

* December 2022: first public release targeting AWS EC2 instances.
* 2023:
  * **Communicate** on the tool (short video demo + article + Social Media posts)
  * Call to contributions:
    * Gather feedback by testing it in in multiple real world accounts
    * Improve doc
    * Compare results with outputs from Cloud Carbon Footprint
  * Follow evolutions of Boavizta API (error margin a.s.o.)
  * Add support for serverless (lambda) estimations
  * Add a custom dashboard (using the new sveltejs components)
  * Add support for OVH instances
  * Add support for Azure
  * Tech debt: use a better serverless plugin + change API SDK generation tool.
  * Implement a module for terraform to help estimate future impacts prior to deployment (Maybe this means a separate dedicated projet).

See also:

* [Issues · Boavizta/cloud-scanner](https://github.com/Boavizta/cloud-scanner/issues)
* [Milestones - Boavizta/cloud-scanner](https://github.com/Boavizta/cloud-scanner/milestones)

### Lead dev

@demeringo

### Links

* **github :** https://github.com/Boavizta/cloud-scanner
* **documentation:** https://boavizta.github.io/cloud-scanner/


## Energizta

### Objective

### Technical stack

**Language :** Bash, Python

### Main features

### Milestones

### Lead dev
TBD

### Links

**github :** https://github.com/Boavizta/Energizta


## Eco-benchmark

### Objective

### Technical stack

Language : ALL

### Main features

### Milestones

### Lead dev

@youenchene & @jdrouet

### Links

github : https://github.com/Boavizta/ecobenchmark-applicationweb-backend


## Cloud-bill

### Objective

### Technical stack

**Language :** python

### Main features

Estimate impacts of a cloud account using billing or reports informations.

### Milestones

Initiated  mid 2022 during Boavizta hackatons.

⚠ On hold, no recent developments.

### Lead dev
TBD 

### Links

**github :** https://github.com/Boavizta/cloud-bill
