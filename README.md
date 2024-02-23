# Optimization-Industrial-Process

Repo to show and example of end-to-end industrial project



### Abstract
The idea is solve a optimization of a industrial process using gurobi and machine learning models. 
The industrial process is divided into 3 small subprocess where the output of one subprocess is the input of another subprocess.
Each output of subprocess could be modeladed as a Machine Learning Model

The objetive is that the output of the final subprocess (output of the process) needs to be controled into a range of optimal operation changing the values of differents features in the differents subprocess. Also, in addition to have the output of the process in control it needs to be it with the minimal costs

### Consideration
The data and some names are privated so it not uploaded to this repo

### Folder
- **0_data**: folder where the datalake data (almost raw data) is downloaded from a datalake in bigquert (GCP)

- **basic_process_data**: folder where the data getting form the datalake is transformed in a version of data that a data scientist can manipulate (pivot data, delete hidden duplicates, etc)


- TERMINAR - .... -