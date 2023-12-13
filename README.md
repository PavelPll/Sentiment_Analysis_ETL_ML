# The project Sentiment Analysis

Get/Extract the data from the internet --> Transform the data --> Load data into MongoDB database
## Extraction
* The file src/Extract/**Extract_single.ipynb** (as well as its **.py** version) extracts the comments (author, score, ...) for certain categories (from categorie i to categorie j) of Software from this [website](https://www.capterra.fr/directory). The output see in data_csv/i_j.csv file. 
* The file src/Extract/**Extract_multiple.py** parallelizes the extraction process on multiple CPUs. It runs Extract_single.py in a parallel. Each CPU is taking care only of certain categories.
## Transform
* The file src/Transform/**Transform.ipynb** concatenates all single extraction (see in data_csv/i_j.csv) to the final dataframe frame (data_csv/capterra.csv).


> [!NOTE]
> For technical side how to run the code please see the file ./How_to_run.txt.
