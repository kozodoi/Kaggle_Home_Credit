# Kaggle Home Credit

Files and codes with my solution to the [Kaggle Home Credit Default Risk competition](https://www.kaggle.com/c/home-credit-default-risk)


## Project summary

Credit scoring refers to the use of statistical models that guide loan approval decisions. This project considers a credit scoring task, where a binary classification model is used to distinguish defaulters and nondefaulters. 

The project works with data from multiple sources, including credit bureau information, application data, performance on previous loans and credit card balance. I perform thorough feature engineering and aggregate data into a single high-dimenional data set. Next, I train Lightgbm models that predict the probability of default.


## Project structure

The project has the follwoing structure:
- `codes/`: jupyter notebooks with codes for different project stages
- `data/`: input data
- `submissions/`: model predictions

There are three notebooks:
- `code_1_data_prep.ipynb`: data preprocessing and feature engineering
- `code_2_modeling.ipynb`: modeling credit risk with a Lightgbm model
- `code_3_ensemble.ipynb`: ensembling predictions from different models

More details are provided within the notebooks.


## Requirments

To run the project codes, you can create a new virtual environment in `conda`:

```
conda create -n py3 python=3.7
conda activate py3
```

and then install the requirements:

```
conda install -n py3 --yes --file requirements.txt
pip install lightgbm
pip install imblearn
```