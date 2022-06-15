# Pectus Finance challenge - Survey data analysis

### How it is structured

This challenge was approached as an exploration effort using Jupyter Notebooks due to time constraints, so there is no "main" function/file to start the application, but the following notebooks order is advisable due to the Markdown explanation present on each notebook, as well as the creation of intermediary Parquet files during the exploration:

1. [data_1.ipynb](./data_1.ipynb)
2. [data_2.ipynb](./data_2.ipynb)
3. [data_3.ipynb](./data_3.ipynb)
4. [analysis.ipynb](./analyses.ipynb) -- This needs to be the last due to the Parquet files dependency.

### How to set up the environment

It was used PySpark and SparkSQL to manipulate data similar as a regular database, and because of that some external dependency is needed before actually running the notebooks (besides actually installing Jupyter):

1. Install Apache Spark, the version used was 3.2.1, downloadable [here](https://www.apache.org/dyn/closer.lua/spark/spark-3.2.1/spark-3.2.1-bin-hadoop2.7.tgz)
2. Set **SPARK_HOME** environment variable to the path of the unzipped Spark folder.
3. [If on Windows] Download the following [winutils.exe package](https://github.com/steveloughran/winutils/tree/master/hadoop-2.7.1), and set the **HADOOP_HOME** environment variable to its path.

The dependency of this project was managed using [Poetry](https://python-poetry.org/), but it is not a hard requirement to run these notebooks, as the project is only dependent on **pyspark==3.2.1** and **findspark==2.0.1** packages.

### Some design decisions

- Like mentioned, the project is structured as a collection of notebooks, but this was just because of the timeframe (see [WISHLIST.md](./WISHLIST.md) for a production-ready checklist for this project)
- It was separated on different notebooks due to the extensive need of exploration and analysis of corner cases.
- The cleaned data was persisted in Apache Parquet format to improve performance on the final notebook [analysis.ipynb](./analyses.ipynb)
- The decisions regarding every transformation, query and assumption is written as Markdown cells in all notebooks. Again, prefer to read them in order to fully understand because similar logics were not repeated on every notebook.

### Feedback/Notes

This a really nice challenge, in regards of the difficulty itself and for the possible improvements, such as consuming APIs or using more robust libraries or packages to, for example, analyze text and extract more data.
