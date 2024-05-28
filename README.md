# MPCS 53120 Final Project - Music Popularity Predictor

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
- **src/notebook_1.ipynb**: (843 lines) Jupyter notebook for initial data exploration and visualization, preprocessing, and model setup, evaluation, and tuning for XGBoost, KNN (all features), and Random Forest. The dataframe (once processed) is saved as a pickle file to avoid rerunning the sentence transformer, which takes over 4 hours.
- **src/notebook_2.ipynb**: (370 lines) Jupyter notebook that continues evaluating the models and comparing their performance. This notebook focuses on neural networks and also tested KNN with reduced features towards the end.


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
Due to large file storage issues with GitHub, the data and dataset directories are not included in this repository. Instead, there is a subdirectory with a file called download_info that contains a link to a Google Drive where the data and dataset folders are stored. Please follow these steps to set up the project:
- Download the data from the Google Drive link provided in download_info.
- Place the downloaded data and dataset folders in the root directory as specified in the directory structure above.
- Ensure that you have all the necessary Python packages installed.
- To run the project, please execute both notebook_1.ipynb and notebook_2.ipynb, which will process the data, train the models, and evaluate their performance. The notebooks are useful for understanding the workflow and results.
  
Note: If you change the directory structure, please update the respective paths in the notebooks to reflect these changes before re-running them.
