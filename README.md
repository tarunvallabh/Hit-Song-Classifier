# Hit Song Predictor

This project aims to predict song popularity using machine learning models. The models are trained on a dataset that includes audio features, metadata, and genre information. The main goal is to classify songs as non-hits, post-2000 hits, or pre-2000 hits.

## Directory Structure
```
root
│ README.md
│ Music_Predictor_Report.pdf
│
├───data
│ artists.csv
│ dict_artists.json
│ tracks.csv
│
├───dataset
│ transformer_df.pkl
│
├───src
│ notebook_1.ipynb
│ notebook_2.ipynb
```

### File Descriptions

- **README.md**: This file. Contains a description of the project, the directory structure, and relevant information.
- **data/artists.csv**: Contains artist-related information such as artist name and popularity.
- **data/dict_artists.json**: A JSON file mapping each song to its respective genres.
- **data/tracks.csv**: The main dataset containing song information.
- **dataset/transformer_df.pkl**: Pickle file containing the transformed data used in all the models.
- **notebooks/notebook_1.ipynb**: (843 lines) Jupyter notebook for initial data exploration and visualization, preprocessing, and model setup, evaluation, and tuning for XGBoost, KNN (all features), and Random Forest. The dataframe (once processed) is saved as a pickle file to avoid rerunning the sentence transformer, which takes over 4 hours.
- **notebooks/notebook_2.ipynb**: (370 lines) Jupyter notebook that continues evaluating the models and comparing their performance. This notebook focuses on neural networks and also tested KNN with reduced features towards the end.
- **src/main.py**: (100 lines) The main script to run the entire workflow including data preprocessing, model training, and evaluation.
- **src/data_preprocessing.py**: (150 lines) Contains functions for loading data, handling missing values, and applying SMOTE.
- **src/model_training.py**: (200 lines) Contains code for training the Random Forest, XGBoost, KNN, and Neural Network models.
- **src/evaluation.py**: (120 lines) Contains functions for evaluating the models, generating classification reports, and plotting confusion matrices.

### Code Not Written by Me
- None of the data files were written by me. All the code in the Jupyter Notebook was written by me. 

### Data Files

- **data/tracks.csv**: Contains song information including audio features, release date, and popularity metrics.
- **data/artists.csv**: Contains artist-related information such as artist name and popularity.
- **data/dict_artists.json**: A JSON file mapping each song to its respective genres.

### Packages Used

- pandas
- numpy
- scikit-learn
- imbalanced-learn
- xgboost
- tensorflow
- keras
- matplotlib
- seaborn
- sentence-transformers

### Other Relevant Information

- Ensure that you have all the necessary Python packages installed.
- To run the project, please run both `notebook_1.ipynb` and `notebook_2.ipynb` which will process the data, train the models, and evaluate their performance.
- The notebooks provide a step-by-step process of data exploration and model evaluation. They are useful for understanding the workflow and results.
