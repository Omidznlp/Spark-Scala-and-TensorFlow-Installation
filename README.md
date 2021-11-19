# Spark-and-Scala-Installation-on-Jupyter-Notebook-for-Machine-Learning
The repository helps to install Spark and Scala on Jupyter notebook in Ubuntu 18.04

1. pip3 install virtualenv
2. virtualenv -p python3.6 venv
3. source venv/bin/activate
4. pip3 install jupyter notebook
6. pip3 install pyspark
7. append the following lines to ~/.bashrc file
export SPARK_HOME=/home/<username>/venv/lib/python3.6/site-packages/pyspark/
export PYSPARK_DRIVER_PYTHON=jupyter
export PYSPARK_DRIVER_PYTHON_OPTS='notebook'
8. source ~/.bashrc
9. pip3 install spylon-kernel
10. python3.6 -m spylon_kernel install --user
11. pyspark 
12. create a new notebook and select the spylon-kernel forlanguage

