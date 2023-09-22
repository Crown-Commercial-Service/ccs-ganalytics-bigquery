# ccs-ganalytics-bigquery
This repository contains data models, documentation, and BigQuery scripts related to our data processing tasks. Most of the data modelled will be from the standard GA4 Schema.

**Table of Contents**
* Overview
* Setup
* Directory Structure
DBT Models
Code Snippets
Documentation
Contact
License

**Overview**
This repository will act to centralise our data models, BigQuery scripts/snippets, and associated documentation to maintain consistency and facilitate collaboration.

**Setup**
* Clone the Repository:
git clone [ADD URL HERE]

**Install DBT:**
If dbt is not installed on your system, please refer to the official installation guide (https://docs.getdbt.com/docs/introduction). If you would prefer using the cloud DBT please create a free account on DBT cloud.

**DBT Profile Configuration:**
Update your ~/.dbt/profiles.yml with the necessary BigQuery credentials:

**your_project_name:**
  target: dev
  outputs:
    dev:
      type: bigquery
      method: oauth
      project: [project_id]
      dataset: [dataset_name]
      threads: 12
      timeout_seconds: 300

Replace the above with your specific project and dataset information ^

**Directory Structure**
* models/: DBT models.
* snippets/: BigQuery code snippets.
* docs/: Documentation, including dbt specific.
* tests/: Tests for DBT models.

**DBT Models**
DBT models are located in the models/ directory. Run dbt run to build and dbt test to validate.

We still be using the following model layers:

**source**
* staging
* intermediate
* marts
  
**Code Snippets**
The snippets/ directory holds BigQuery scripts. Each script has a brief description.

**Documentation**
Refer to the docs/ directory for project documentation. For dbt model documentation, run dbt docs serve to access an interactive site detailing each model.
