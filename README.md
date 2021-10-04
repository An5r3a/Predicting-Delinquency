### Delinquency Model

This is the markdown version of the jupyter notebook for easy read online.
Please find the Case_study_delinquency.ipynb for the executable code.
And Case Study.pdf for the report.

## Case Study

The objective of this case study is to create a delinquency model which can predict in terms of probabilities for each loan transaction, whether a consumer will be delinquent on his mortgage repayments in the next month. 
Delinquency is a condition that arises when an activity or situation does not occur at its schedule or expected date; that is, it occurs later than expected. 

Environment specification
This notebook should be run under python with all necessary Data Science packages, Anaconda environment is recommended.
Please install the following packages

```
pip install treeinterpreter
pip install datatable
pip install h2o
pip install collections
```

If an error occurs with h2o api, try changing the project name

```
aml = H2OAutoML(max_runtime_secs = 30, #change this if you are in a rush hehehe
                max_models = 25,  
                seed = 42, 
                project_name='classification_2',
                sort_metric = "AUC")
```

## Read data from file

Change the path to read the csv files provided

```
path = '/Python/case_study_data/'
data01 = pd.read_csv(path + 'data01.csv', sep =',', header = 0)
data02 = pd.read_csv(path + 'data02.csv', sep =',', header = 0)
data03 = pd.read_csv(path + 'data03.csv', sep =',', header = 0)
data04 = pd.read_csv(path + 'data04.csv', sep =',', header = 0)
```
