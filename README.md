# cookiecutter-data-science

cookiecutter-data-science contains the boilerplate you need to start a Data Science project.

Project Goals
* Provide project templates to quickstart Data Science research & development projects
* Stop the use of filenames such as YYYYMMDD_data_exploration_v1_new_old_new_v34_final_new.sql

## Install guide

Get cookiecutter (first time only)
```bash
$ pip install cookiecutter
```

Now run it against this repo
```bash
$ cookiecutter https://github.com/jvawdrey/cookiecutter-data-science.git
```
You will be prompted to answer a set of questions which will be used to fill out the boilerplate. Note - Hitting enter will keep the defaults displayed.

```text
Cloning into 'cookiecutter-data-science'...
remote: Counting objects: 24, done.
remote: Compressing objects: 100% (15/15), done.
remote: Total 24 (delta 9), reused 23 (delta 8), pack-reused 0
Unpacking objects: 100% (24/24), done.
Checking connectivity... done.
full_name [Matthew Upson]:
email [gdsdatascience@digital.cabinet-office.gov.uk]:
client [GDS]:
project_name [My Data Science Project]:
project_slug [my-data-science-project]:
project_description [Data Science cookiecutter contains all the boilerplate you need to create a Data Science project.]:
created_date [2015-11-17]:
```

Enter project
```bash
$ cd <project name>
```

Create git repo for version control
```bash
# initialize project
$ git init

# add all files
$ git add -A

# first commit
$ git commit -m "Initial commit"
```

## Repo layout

* **/data:** Utility project data such as mapping tables
* **/docs:** Project documents including excel files
* **/img:** Visualizations generated for project
* **/python:** Python code for project
  * **/python/notebooks:** Python notebook code
* **/prod:** "Operational ready code"
* **/prod/tests:**  "Tests for prod code"
* **/r:** R code for project
* **/sql:** SQL scripts
* **/tmp:** Temp files (Note - Files in this directory are ignored from Git repo)

## File descriptions

* **/data:**
  * *filename: description*
* **/docs:**
  * *filename: description*
* **/img:**
  * *Note - Relevant images are documented in related powerpoint presentation in
    the '/docs' directory*
* **/python:**
  * *filename: description*
* **/r:**
  * data-exploration.R: This code contains data exploration queries used
    to understand available data for cleaning and feature generation.
* **/sql:**
  * data-exploration.sql: This file contains data exploration queries used to
    audit and understand available data in addition to determining correct data
    preparation logic
  * data-preparation.sql:  This script contains table generation queries
    used to prepare available data for feature generation.
  * feature-generation.sql: This script creates features (independent
    variables) for testing as inputs into the models.
  * feature-selection.sql: This script contains a set of queries which
    calculate summary statistics, correlations etc. to be used for feature
    selection.
  * model-development.sql: This script is used to build (train) the model
  * model-scoring.sql: This script is used to apply model to new data (scoring)
  * model-update.sql: This script is used to update (retrain) model

## Contact

* Better Use of Data Team (gdsdatascience@digital.cabinet-office.gov.uk)
