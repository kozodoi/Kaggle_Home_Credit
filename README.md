# Kaggle Home Credit Default Risk

Top-4% solution to the [Home Credit Default Risk](https://www.kaggle.com/c/home-credit-default-risk) Kaggle competition on credit scoring.

![cover](https://i.postimg.cc/Y0x2LtQk/credit-cover.jpg)


## Summary

In finance, credit scoring refers to the use of statistical models to guide loan approval decisions. This project develops a binary classification model to distinguish defaulters and non-defaulters using supervised machine learning.

The project works with data from multiple sources, including credit bureau information, application data, performance on previous loans and credit card balance. I perform thorough feature engineering and aggregate data into a single high-dimensional data set. Next, I train an ensemble of LightGBM models that predict the probability of default.


## Project structure

The project has the following structure:
- `codes/`: Python notebooks with codes for data preparation, modeling and ensembling
- `data/`: input data (not included due to size constraints and can be downloaded [here](https://www.kaggle.com/c/home-credit-default-risk))
- `output/`: output figures exported from the notebooks
- `solutions/`: slides with competition solutions from other competitors
- `submissions/`: test set predictions produced by the trained models

There are three notebooks:
- `code_1_data_prep.ipynb`: processing of the raw data, feature enginering and export of the aggregated data set
- `code_2_modeling.ipynb`: training LightGBM models to predict credit risk and export of the test set predictions
- `code_3_ensemble.ipynb`: ensembling predictions from different LightGBM models trained in `code_2_modeling.ipynb`

More details are provided within the notebooks documentation.


## Working with the repo

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
