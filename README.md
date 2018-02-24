# How to set up a wallet & connect to 
# blockchain via neo python package & Docker

1. First download python 3.5.4
Check what version of python you have by typing: 

$ python --version

2. If not then install 3.5.4 via brew

Type in terminal:

$ brew install pyenv
$ pyenv install 3.5.4

To export path -
Type in terminal:

$ export PYENV_ROOT=~/.pyenv   
$ export PATH=$PYENV_ROOT/shims:$PATH
$ pyenv local 3.5.4

To see what version of python you are running on type:

$ python --version

3. Next install docker to hook up to the blockchain

Install docker with brew command:

$ brew install docker

To pull down docker image:

$ docker pull cityofzion/neo-privatenet

To run :

$ docker run --rm -d --name neo-privatenet -p 20333-20336:20333-20336/tcp -p 30333-30336:30333-30336/tcp cityofzion/neo-privatenet

4. Next download ne-python package

To download, first clone repo on following git page into any directory of your choosing:

$ git clone https://github.com/CityOfZion/neo-python.git
 
Make sure you have the right python version 

$ python --version

If not then run 

$ pyenv local 3.5.4

To avoid "file not found #include "leveldb/db.h" " error run:

$ brew isntall leveldb

Then run:

$ pip install -r requirements.txt


