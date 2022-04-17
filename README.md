# State-change Relation Extraction Dataset (StaRE)

This is the state-change relation extraction dataset of paper "Enhanced Distant Supervision with State-Change Information for Relation Extraction" in LREC 2022.

## Data

This git repo requires access to the LDC2011T07 (English Gigaword Fifth Edition) dataset, and we provide manual annotations for our usecase. In addition, we provide indices of the data and script so that the actual data can be retrieved from Gigaword corpus.

You can run the `./get_original.py ` to get the actual sentences, tokens and subject-object names in sentences by giving the dataset directory as input path. 

You can run:

`conda create --name myenv`

`conda activate myenv`

`conda install pip`

`pip install --r ./requirements.txt`

`python ./get_original.py <path_to_gigaword_unzipped_directory> <path_where_you_want_to_save_the_data>`


In `./data`, there are 5 folders :
1) `train` contains all the training data with the format - train_windowsize_relationtype.txt which contains all the positives referring to a particular relation. It also contains a train_negatives files which contains 10k fixed negatives which are to be used in addition to the positives for training each sceanrio.
2) `val` contains all the static validation data for each relation type.
3) `test` contains all the static test data for each relation type.
4) `dynamic_val` contains all the dynamic validation data for each relation type.
5) `dynamic_test` contains all the dynamic test data for each relation type.


## _Relationtype_ in dynamic:

1) 0.txt represents P26@start
2) 1.txt represents P26@end
3) 3.txt represents P35@start
4) 7.txt represents P54@start
5) 5.txt represents P463@start

## _Relationtype_ in static:

1) Merging 0.txt and 1.txt represents P26 
2) 3.txt represents P35
3) 7.txt represents P54
4) 5.txt represents P463


## License
The code is released under the under terms of the Apache-2.0 License.
