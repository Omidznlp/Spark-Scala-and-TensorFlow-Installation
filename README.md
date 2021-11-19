# Spark-and-Scala-Installation-on-Jupyter-Notebook-for-Machine-Learning
The repository helps to install Spark and Scala on Jupyter notebook in Ubuntu 18.04

## Check Current Directory
```
$ pwd
/home/omid/
```
![image](https://user-images.githubusercontent.com/87664653/142626395-9be03569-5869-4db5-a6bf-33fcf83439c2.png)
## prerequirments  
### Install pip3
```
sudo apt-get update
sudo apt-get -y install python3-pip
```
## Install virtual environment
```
1. pip3 install virtualenv
```
## Create virtual environment 

Create virtual environment (e.g venv folder) in the current directory
```
2. virtualenv -p python3.6 venv
```
## Activate virutal environment
```
4. source venv/bin/activate
```
![image](https://user-images.githubusercontent.com/87664653/142626953-4565452b-434d-4f6c-8ecb-abf59f1d5ac3.png)

## Install jupyter notebook
```
6. pip3 install jupyter notebook
```
## Install java 
Check Java with the java --version command. If it is not installed, install it with the following command:
```
$  java --version
```
```
7. sudo apt-get install openjdk-11-jdk
```
## Install pyspark
```
8. pip3 install pyspark
```
## Configure bash profile
9. Append the following lines to end of ~/.bashrc file
```
export SPARK_HOME=<current_directoty>/venv/lib/python3.6/site-packages/pyspark/
export PYSPARK_DRIVER_PYTHON=jupyter
export PYSPARK_DRIVER_PYTHON_OPTS='notebook'
```
### Note 
In the fist line of the above lines, please put the name of your current directory instead of "current_directory" in the above lines which you had already created your venv folder inside that. For example, my current directory is /home/omid , Therefore : 
```
export SPARK_HOME=/home/omid/venv/lib/python3.6/site-packages/pyspark/
export PYSPARK_DRIVER_PYTHON=jupyter
export PYSPARK_DRIVER_PYTHON_OPTS='notebook'
```
## Update bash profile
```
10. source ~/.bashrc
```
## Install spylon for Programming Scala on Jupyter 
```
12. pip3 install spylon-kernel
13. python3.6 -m spylon_kernel install --user
```
## Run pyspark or jupyter notebook
```
14. pyspark 

```
or 

```
$ jupyter notebook
```
After a few seconds, Jupyter will launch in your browser.
## Create a notebook and select spylon-kernel
15. create a new notebook on the and select the spylon-kernel

![image](https://user-images.githubusercontent.com/87664653/142623665-02eb4dc8-2847-4d9b-aad0-a2303020a4a5.png)

Enjoy it!!!
