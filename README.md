# Spark and Scala Installation for Supervised Learning and TensorFlow for Deep Learning on Jupyter Notebook
The repository helps to install Spark, Scala and TensorFlow on Jupyter notebook in Ubuntu 18.04

## Spark and Scala Installation 
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
export SPARK_HOME=<venv_directoty>/venv/lib/python3.6/site-packages/pyspark/
export PYSPARK_DRIVER_PYTHON=jupyter
export PYSPARK_DRIVER_PYTHON_OPTS='notebook'
```
### Note 
In the first line above, please put the name of your directory instead of <venv_directoty>, where you have already created your venv folder inside it. For example, my venv_directory is /home/omid which I have used to create my virtual environment inside it. 
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

Please give an star if it works well for you ;))

Enjoy it!!! 

## Additional Options
If you want to change the default configuration of your Jupyter notebook, insert the below command to create configuration file.
```
$ jupyter notebook --generate-config
```
![image](https://user-images.githubusercontent.com/87664653/142846219-567bc776-361d-4263-a242-b2f1d16bac87.png)

As It's shown, configuration file was created in /home/<user_name>/.jupyter/jupyter_notebook_config.py .

Example: for me is /home/omid/.jupyter/jupyter_notebook_config.py . Now it can be edited if you want to change some default configuration: 
```
$ nano /home/omid/.jupyter/jupyter_notebook_config.py
```
![image](https://user-images.githubusercontent.com/87664653/142846608-961d6aef-32fa-4eee-98e2-a05f61166bff.png)

## TensorFlow Installation 

If you haven't already created a virtual environment and installed a Jupyter notebook, do so now by following the 6 steps in the previous section and then following the instructions below:

Install latest stable release with CPU and CPU support

```
pip3 install --upgrade tensorflow
```
For more information: https://www.tensorflow.org/install/pip

After that, you can use Python 3 to program Deep Learning.
