# Optimization-Industrial-Process

Repo to show and example of end-to-end industrial project. ---> USING FREE GUBORI LICENCE <---



### Abstract
The idea is solve a optimization of a industrial process using gurobi and machine learning models. 
The industrial process is divided into 3 small subprocess where the output of one subprocess is the input of another subprocess.
Each output of subprocess could be modeladed as a Machine Learning Model

The objetive is that the output of the final subprocess (output of the process) needs to be controled into a range of optimal operation changing the values of differents features in the differents subprocess. Also, in addition to have the output of the process in control it needs to be it with the minimal costs

### List models
The list of models trained and used in optimization models are divided into:
- d0eop_microkappa
- d1_brillo
- p_blancura


### Consideration
1. The data and some names are privated so it not uploaded to this repo
2. The optimization codes are parametrized to read input parameters but the codes are not optimal and it needs to be written in a better way
3. These codes can work using gurobi free licence
4. In the next repo I use gurobi licence training best models and included updates and improves into machine learning modesl, optimization engine and streamlit app. Link repo: https://github.com/joseortegalabra/Optimization-Industrial-Process-Advanced


### Folder
- **0_templates**: folder that contains a templates. Template how to load a licence gurobi using differents ways and a template notebook with the first lines of codes that can be used in all the folders (see that the folder artifacts, config, etc there are located in the root path and the notebooks are in folders) 

- **1_data**: folder where the datalake data (almost raw data) is downloaded from a datalake in bigquert (GCP)

- **2_basic_process_data**: folder where the data getting form the datalake is transformed in a version of data that a data scientist can manipulate (pivot data, delete hidden duplicates, etc)

- **3_eda**: folder that contains codes for simple EDA for each model tranined (correlations) and select the features to use to train the models

- **4_modeling_ml**: train the ml models with models suported by gurobi

- **5_offline_evaluation_ml**: evaluate ml models

- **6_optimization**: join the ml models with the optimization model. The constraints are:
    - the 3 ml models deffined as constraints
    - delta of decision variables. Delta of decision variables that are features machine learning models. Delta between the base value and the optimal value because there are physical constraints that these features can't increment too much

- **7_app_streamlit**: app in streamlit to test the resolution of gurobi ml

- **artifacts**: folder that contains artifacts as data, ml models, etc

- **config**: folder that contains configuration file. For example, list of features, classification of the features, operational limits, upper and lower bound of decision variables in optimization, etc