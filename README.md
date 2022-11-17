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

It combines real time usage data from your AWS account with Boavizta API to offer a global view of your impacts on a given region.

### Technical stack

**Language :** Rust

### Main features

Cloud-scanner can be used:

* from command line 💻
* as a serverless application deployed with AWS lambda ⚡

Cloud-scanner can be automated to produce metrics at regular interval and monitor your impacts in a dashboard.

See full documentation: [Introduction - Boavizta cloud scanner 📡](https://boavizta.github.io/cloud-scanner/)

### Milestones

* December 2022: first public release targeting AWS EC2 instances.
* 2023
  * Compare results with outputs from Cloud Cardbon Footprint
  * expand list of instances
  * support serverless estimations
  * Azure

See also:

* [Issues · Boavizta/cloud-scanner](https://github.com/Boavizta/cloud-scanner/issues)
* [Milestones - Boavizta/cloud-scanner](https://github.com/Boavizta/cloud-scanner/milestones)

### Lead dev
@demeringo

### Links

**github :** https://github.com/Boavizta/cloud-scanner


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
