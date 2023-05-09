# Movie_Resys
Movie Recommendation System Using Collaborative filtering

# Steps

Follow these steps to create the required services and run the notebook locally.

1. [Clone the repo](#1-clone-the-repo)
2. [Download all the dependencies](#2-download-all-the-dependencies)
3. [Set up Elasticsearch](#3-set-up-elasticsearch)
4. [Download Apache Spark](#4-download-apache-spark)
5. [Download the data](#5-download-the-data)
6. [Launch the notebook](#6-launch-the-notebook)
7. [Run the notebook](#7-run-the-notebook)

### 1. Clone the repo

Clone the `Movie_Resys` repository locally. In a terminal, run the following command:

```
$ git clone https://github.com/nguyenphuvinhtoan/Movie_Resys
```

### 2. Download all the dependencies
```
$ pip3 install -r /path/to/requirements.txt
```

### 3. Set up Elasticsearch

This Code Pattern currently depends on Elasticsearch 8.7.0. Go to the [downloads page](https://www.elastic.co/downloads/elasticsearch) and download the appropriate package for your system.

Change directory to the newly unzipped folder using:

```
$ cd elasticsearch-8.7.0
```

Next, start Elasticsearch (do this in a separate terminal window in order to keep it up and running):

```
$ ./bin/elasticsearch
```

### 4. Download Apache Spark
Download the Spark (Version 3.3.2) from the [downloads page](https://spark.apache.org/downloads.html). Once you have downloaded the file, unzip it:

### 5. Download the data

You will be using the [Movielens dataset](https://grouplens.org/datasets/movielens/) of ratings given by a set of users to movies, together with movie metadata. There are a few versions of the dataset. You should download the ["latest small" version](http://files.grouplens.org/datasets/movielens/ml-latest-small.zip).

_Run the following commands from the base directory of the cloned Code Pattern repository:_

```
$ cd data
$ wget http://files.grouplens.org/datasets/movielens/ml-latest-small.zip
$ unzip ml-latest-small.zip
```

### 6. Launch the notebook
```
cd elasticsearch-spark-recommender/
PYSPARK_DRIVER_PYTHON="jupyter" PYSPARK_DRIVER_PYTHON_OPTS="notebook" ../spark-3.3.2-bin-hadoop3/bin/pyspark --driver-memory 4g --driver-class-path <absolute-path-name>/Movie_Resys/elasticsearch-spark-30_2.12-8.7.0.jar
```
In that < absolute-path-name > is the path to the directory in your computer

This should open a browser window with the Code Pattern folder contents displayed. Click on the `notebooks` subfolder and then click on the `resys.ipynb` file to launch the notebook.

### 7. Run the notebook
At this step, you feel free to try our features in the project like: Find similar movies for a given movie, Find movies to recommend to a user.