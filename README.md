# The project Sentiment Analysis

Get/Extract the data from the internet --> Transform the data --> Load data into MongoDB
## Extraction
* The file **Extract_single.ipynb** (as well as its **.py** version) extracts the comments (author, score, ...) for certain categories of Software using this [website](https://www.capterra.fr/directory).  
* The file **Extract_multiple.py** paralelizes the extraction process (Extract_single.py) on multiple CPUs (each CPU is taking care only of certain categories). 


> [!NOTE]
> For technical side how to run the code please see the file ./How_to_run.txt.
