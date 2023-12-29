# The project Sentiment Analysis (Containerized API)
Get/Extract the data from the internet **-->** Transform the data **-->** Load data into MongoDB database\
\
The file, **docker-compose.yml**, run the container c1, with installed Python (Jupyter notebook) and **two** MongoDB containers. The first container, c1, is used to run the code. The second container, my_mongo, is used to store the data (use my_mongo:27017 to access stored data from Python and Jupyter notebook). The third one, mongo-express, is used for MongoDB Graphic User Interface (http://localhost:8081). 
## Extraction
* The file src/Extract/**Extract_single.ipynb** (as well as its **.py** version) uses Selenium to extract the comments (author, score, ...) for certain categories (from categorie i to categorie j) of Software from this [website](https://www.capterra.fr/directory). The output see in data_csv/i_j.csv file. 
* The file src/Extract/**Extract_multiple.py** parallelizes the extraction process on multiple CPUs. It runs Extract_single.py in a parallel. Each CPU is taking care only of certain categories in order to accelerate data extraction.
## Transform
* The file src/Transform/**Transform.ipynb** concatenates all single extraction (see in data_csv/i_j.csv) to the final dataframe frame (data_csv/capterra.csv).
## Load
* The file src/Load/**MongoDB_load.py** loads capterra.csv (created in the previous Transform step) into MongoDB database and processes it.

> [!NOTE]
> For technical side how to run the code please see the file ./How_to_run.txt.
