### Instalation and uses of blobtools on Condor(CHTC):

--- A modular command-line solution for visualisation, quality control and taxonomic partitioning of genome datasets.

REQUIREMENTS:
 - Python 2.7
 - UNIX
 - pip

##### Installing Python on Condor
 1. First create a directory in which you will install Python 2.7. ```mkdir python```
 2. Transfer the latest version of Python 2.7 to your current working directory.
````
wget https://www.python.org/ftp/python/2.7.14/Python-2.7.14.tgz
````
 - This link may need to be updated to the latest version.
Updated 11/22/2017

 3. Untar the source code that was transfered. ```tar -xzf Python-2.7.14.tgz```
 4. Change directory to the new Python file ```cd Python-2.7.14```
 5. Compile the file to the python install file you created ``./configure --prefix=$(pwd)/../python``
 6. Make and install Python 2.7.14
 ```
 make
 make install
 ```
 
##### Ensure Proper Installation
 7. Move up a directory ```cd ..``` 
 8. Check contents of python directory, should look accordingly
```
[alice@build]$ ls python 
bin  include  lib  share
```
 9. Ensure you have a python executable ```ls python/bin```
 The output should look similar to the following:
```
2to3              idle3    pydoc3     python3.4-config   pyenv
2to3-3.4          idle3.4  pydoc3.4   python3.4m         pyenv-3.4
easy_install-3.4  pip3.4   python3    python3.4m-config  
f2py3.4           pip3     python3.4  python3-config
```

##### Install pip