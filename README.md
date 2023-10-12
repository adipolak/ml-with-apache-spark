Machine Learning with Apache Spark Notebooks
==========================
This project aims at teaching you the Apache Spark MLlib in python. It contains the example code and solutions to the exercises in O'Reilly upcoming book Machine Learning with Apache Spark by Adi Polak.


# Quick Start

## Want to play with these notebooks online without having to install anything?
TBD as we evaluate free platforms, if you have any recommendations, please reach out on [@AdiPolak](https://twitter.com/AdiPolak)

At the moment, you can use docker with running the following command. Memory is for providing jupyter environment with more memory, --mount is for mounting the local library, where all you work will be saved. `adipolak/ml-with-apache-spark` is an image in docker hub. -p are the port used for interacting with jupyter notebook.

```code
docker run -it --memory="28g" --memory-swap="30g"  -p 8888:8888 --mount type=bind,source=$(pwd),target=/home/jovyan adipolak/ml-with-apache-spark
```

## Just want to quickly look at some notebooks, without executing any code?
Brows it on the [Juypyter.org notebook viewer](https://nbviewer.jupyter.org/github/adipola/ml-with-apache-spark/tree/main/notebooks/)
<img src="https://nbviewer.jupyter.org/static/img/nav_logo.svg" width="90" />

## Want to run this project using a Docker image?

Clone this repo:
```code
gh repo clone adipolak/ml-with-apache-spark
```
CD into the repo
```code
cd ml-with-apache-spark
```
run:
```code
docker run -it --memory="28g" --memory-swap="30g"  -p 8888:8888 --mount type=bind,source=$(pwd),target=/home/jovyan adipolak/ml-with-apache-spark
```


# FAQ

**Which Python version should I use?**


**I get Py4JJavaError: An error occurred while calling o{some number}.parquet. (Reading Parquet file), what to do?**
From Jupyter enter the terminal and validate your Java version, given that we use Spark 3.1.1 it should be `openjdk version "11.0.11"`.
You local Java runtime should be of the same version - local Java runtime -  is the Java that installed on the machine where you are running your docker from.


**Which Apache Spark version should I use?**
The apache spark version is 3.1.1

**I don't have enough local memory; can I run it in the cloud?**
Yes! you will need a prebuilt environment that has Spark, TensorFlow, PyTorch and MLFlow like Databricks or others.
Once you have that, you can clone the repo into your new cloud environment and run the notebooks, or simply copy the notebooks themselves. 

# Contributors
I want to thank everyone who contributed to this project by providing helpful feedback, filing issues, or submitting Pull Requests. 
If you would like to contribute, please feel free to submit a pull request, or reach out on [@AdiPolak](https://twitter.com/AdiPolak).
