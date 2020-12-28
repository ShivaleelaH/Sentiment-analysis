# Sentiment-analysis

This folder consists of all the notebooks and the relevant python files.

1. Transformer.py: The file contains the implementation of Transformer model class.

2. utils.py: This file contains all the utility methods used such as pad_or_truncate which gives you either performs zero padding on a vector or truncates a vector based on the max_length specified. We use other methods from this file such as preprocess_for batch, pad_and_sort_batch etc.

3. Data_Preprocess.ipynb: This notebook deals with the preprocessing of data and saves the data into hdf file formats for further use. 
IMPORTANT: In order to run this notebook, create folders and upload the following files in the same structure:
	a. utils.py
	b. For IMDB dataset: upload 'imdb_master.csv'
	c. For Yelp dataset: upload 'yelp_train.csv' and 'yelp_test.csv'
	d. Create the following folder to save the hdf files in the same structure:
		- dataset (All .h5 files to be used in Train_Models.ipynb would be created withing this folder according to the dataset used.)
			-IMDB 
			-Yelp

4. Train_Models.ipynb: The notebook deals with the training of transformer model and evaluating it on either IMDB or Yelp dataset. It also helps you visualise the attention mechanism of the transformer using colormaps and saves them as html files.
IMPORTANT: In order to run this notebook, create folders and upload the following files in the same structure:
	a. Transformer.py
	b. utils.py
	c. dataset (Upload all the files and folder within this folder before running the code.)
		- IMDB 
			- X_train.h5
			- X_val.h5
			- X_test.h5
			- y_train.h5
			- y_val.h5
			- y_test.h5
			- word2num_series.h5
			- test.csv
		- Yelp
			- X_train.h5
			- X_val.h5
			- X_test.h5
			- y_train.h5
			- y_val.h5
			- y_test.h5
			- word2num_series.h5
			- y_test.csv
	d. word2vector (Upload all the files and folder within this folder before running the code.)
		- glove.twitter.27B.200d.txt
	e. output (Create the folders output -> model_save in order to save the model parameters in terms of .pth files which can be used to reload the model for evaluation.)
		- model_save (If you already have .pth files just upload them within this folder)
			- Transformer_on_IMDB_l1_h1.pth
			- Transformer_on_IMDB_l1_h2.pth
			- Transformer_on_IMDB_l1_h4.pth
			- Transformer_on_IMDB_l1_h8.pth
			- Transformer_on_IMDB_l2_h1.pth
			- Transformer_on_IMDB_l2_h2.pth
			- Transformer_on_IMDB_l2_h4.pth
			- Transformer_on_IMDB_l2_h8.pth
			- Transformer_on_IMDB_l3_h1.pth
			- Transformer_on_IMDB_l3_h2.pth
			- Transformer_on_IMDB_l3_h4.pth
			- Transformer_on_IMDB_l3_h8.pth
			- Transformer_on_Yelp_l1_h1.pth
			- Transformer_on_Yelp_l1_h2.pth
			- Transformer_on_Yelp_l1_h4.pth
			- Transformer_on_Yelp_l1_h8.pth
			- Transformer_on_Yelp_l2_h1.pth
			- Transformer_on_Yelp_l2_h2.pth
			- Transformer_on_Yelp_l2_h4.pth
			- Transformer_on_Yelp_l2_h8.pth
			- Transformer_on_Yelp_l3_h1.pth
			- Transformer_on_Yelp_l3_h2.pth
			- Transformer_on_Yelp_l3_h4.pth
			- Transformer_on_Yelp_l3_h8.pth
5. Baseline_models.ipynb: The file contains the implementation of off-the-shelf baseline models for sentiment analysis of IMDB and Yelp dataset.
IMPORTANT: In order to run this notebook, upload the following files:
	a. glove.twitter.27B.200d.txt
	b. For IMDB dataset: IMDB_Dataset.csv
	c. For Yelp dataset: yelp_train.csv and yelp_test.csv    
