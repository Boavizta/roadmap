# Boavizta's open source projects roadmap

Let's create commons to make the environmental impact assessment of digital products, services and systems more reliable, easier and more open.

## Products

* [Datavizta](#datavizta)
* 🛠️ [Boaviztapi](#boaviztapi)
* [Boagent](#boagent)
* 🛰️ [Cloud-scanner](#cloud-scanner)
* 🔌 [Energizta](#energizta)
* 📉 [Eco-benchmark](#eco-benchmark)
* 💾 [Boavizta repository](#boavizta-repository)
* [Cloud-bill](#cloud-bill)

----

## Datavizta

### Objective

Explore Boavizta's data and methods through a pedagogical frontend.

### Technical stack

**Language :** TypeScript, CSS, HTML

**Framework :** Svelte

### Main features

This educational frontend intends to achieve several complementary objectives:

- Being able to search easily for carbon impact factors for digital equipment in [Boavizta environmental footprint open database](https://github.com/Boavizta/environmental-footprint-data)
- Being able to visualize the impacts repartition by stages of the life cycle of equipment by differentiating the use phase (scope 2) from the manufacturing, transport and end-of-life phases (scope 3)
- Being able to assess the impacts of extending the life of the product or using it in one geographical area rather than another.

### Milestones

### Lead dev

@airloren

### Links

**demo :** https://dataviz.boavizta.org
**github :** https://github.com/Boavizta/datavizta

----

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
  * Add multiple source of impacts factors (electricity map, research paper, ...)
  * Add new component (GPU, HDD)
  * Automate the collection of of components\', devices\' and cloud instances\' characteristics 

* V0.4 : 
  * Model the electrical consumption from Energizta

* V1 : 
  * Test coverage of 95%
  * Code quality process

### Lead dev
@da-ekchajzer

### Links

**github :** https://github.com/Boavizta/boaviztapi

**documentation :** https://doc.dev.api.boavizta.org/

**demo api :** https://dev.api.boavizta.org/docs

----

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

----

## Cloud-scanner

### Objective

Cloud-scanner returns environmental impacts of your AWS Instances usage.

> Main  objective is to give  a **more realistic view of impacts** compared to what is natively returned in the dashboards of cloud providers, who often rely on carbon compensation mechanism or unclear methodology to display what we consider unrealistically low impacts.

Cloud scanner combines real time usage data from your AWS account with Boavizta API to offer a global view of your impacts. It will later be enriched to cover other cloud providers.

### Main features

Generate real time metrics (json or prometheus) that can be displayed in dashboards.

Fine granularity: provide filtering (on tags) to ease attribution to a service or application.

Cloud-scanner can be used:

* from command line 💻 (for a quick one-shot assessment)
* as a server application (for continuous monitoring)⚡

See full documentation: [Introduction - Boavizta cloud scanner 📡](https://boavizta.github.io/cloud-scanner/)

### Roadmap (updated January 2025)

1. Support automating inventory of additional providers
2. Provide estimations related to object storage (like aws S3)
3. FAAS / Serverless (like AWS lambda or Azure functions)
4. Additional managed services (like DB as a service)
5. Impacts of GPUs, which is key to assess AI/ML workload

See also:

* [Issues · Boavizta/cloud-scanner](https://github.com/Boavizta/cloud-scanner/issues)
* [Milestones - Boavizta/cloud-scanner](https://github.com/Boavizta/cloud-scanner/milestones)

### Technical stack

**Language :** Rust + AWS SDK

### Lead devs

[@demeringo](https://github.com/demeringo) & [@jnioche](https://github.com/jnioche)

### Links

* **github:** https://github.com/Boavizta/cloud-scanner
* **Project overview:** https://demeringo.github.io/cloud-scanner-intro/
* **documentation:** https://boavizta.github.io/cloud-scanner/

----

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

----

## Eco-benchmark (Backend)

### Objective

Highlight the main way to achieve a sustainable design on a BackEnd API.

For tech leaders and developers.

### Technical stack

#### Measurement infrastructure 

Language : Ansible, Javascript

#### Services

Language : All

### Main features

#### Measurement infrastructure 

- Measure automation

#### Services

- go-pgx
- jvm-kotlin-spring
- node-express-sequelize
- php-symfony-apache-dev
- rust-actix-native
- rust-sqlx-native
- rust-axum-native

### Milestones

* January 2022
  * Measurement infrastructure 
    * Automated test to validate service behavior.
    * Preload database
  * Services
    * php-symfony-apache-prod
    * php-symfony-apache-nginx
    * ruby-on-rails

* Next
  * Measurement infrastructure 
    * Connection pool harmonization.
  * Services
    * Python use case
  * Design variant  
    * grpc protocole 


### Lead dev

@youenchene & @jdrouet

### Links

github : https://github.com/Boavizta/ecobenchmark-applicationweb-backend

How to Contribute : https://github.com/Boavizta/ecobenchmark-applicationweb-backend/blob/main/CONTRIBUTING.md

----

## Boavizta repository

### Objective

This data repository is maintained by [Boavizta](https://www.boavizta.org) and is complementary to Boavizta's environmental footprint evaluation methodology (as implemented in [Boaviztapi](#boaviztapi)). It aims to reference as much data as possible to help organizations to evaluate the environmental footprint of their information systems, applications and digital services.

> [!WARNING]
> Boavizta database is quite exclusively derived from PCF (Product Carbon Footprint) sheets provided by the manufacturers. Methodologies used by manufacturers are not transparent and have very large margins of error and the purpose of making these data available is mainly to give ideas of orders of magnitude and to compare different models from the same manufacturer.
>
> Therefore **WE RECOMMAND NOT USING THESE DATA TO MAKE ACCURATE IMPACTS EVALUATIONS** or to compare the impacts of devices from different manufacturers.

### Technical stack

**Language :** Python, CSV

### Main features

### Milestones

⚠ Development on this project are frozen.

### Lead dev

@airloren

### Links

**github :** https://github.com/Boavizta/environmental-footprint-data/blob/main/tools/spiders/README.md

----

## Cloud-bill

### Objective

Estimate impacts of a cloud usage of a cloud account using billing or reports informations.

### Technical stack

**Language :** python

### Main features


### Milestones

⚠ On hold, no recent developments.

Initiated  mid 2022 during Boavizta hackathons.

### Lead dev
TBD 

### Links

**github :** https://github.com/Boavizta/cloud-bill
