# Spark-and-Scala-Installation-on-Jupyter-Notebook-for-Machine-Learning
The repository helps to install Spark and Scala on Jupyter notebook in Ubuntu 18.04

## Check Current Directory
```
$ pwd
/home/omid/
```
## Install virtual environment
```
1. pip3 install virtualenv
```
## Create virtual environment
```
2. virtualenv -p python3.6 venv
```
## Activate virutal environment
```
4. source venv/bin/activate
```
## Install jupyter notebook
```
6. pip3 install jupyter notebook
```
## Install java
```
7.sudo apt-get install openjdk-11-jdk
```
## Install pyspark
```
8. pip3 install pyspark
```
## Configure bash profile
9. append the following lines to end of ~/.bashrc file
```
export SPARK_HOME=/home/<username>/venv/lib/python3.6/site-packages/pyspark/
export PYSPARK_DRIVER_PYTHON=jupyter
export PYSPARK_DRIVER_PYTHON_OPTS='notebook'
```
## Update bash file
```
10. source ~/.bashrc
```
## Install spylon for activating Scala
```
12. pip3 install spylon-kernel
13. python3.6 -m spylon_kernel install --user
```
## Run pyspark
```
14. pyspark 
```
## Create a notebook and select scala
'''
16. create a new notebook on the and select the spylon-kernel for language
'''

![Screenshot from 2021-11-13 11-22-51](https://user-images.githubusercontent.com/87664653/142623180-d4245bb9-f62a-4777-b713-872f7db48e50.png)
