# Submission for UMA EDA

## Outline

In this we have two notebooks

1. Data scraping
    - This contains all the code for pulling data from the spotify API, this uses the spotipy package which exists as a wrapper for the spotify API.
2. EDA
    - This is a quick EDA for the data pulled. Here we look at two main questions:
        1. Does universal own typically 30% of a playlist
        2. Does universal have more popular songs?

Conclusions:
    1. No, it tends to be closer to about 7-21% however this can wildly vary
    2. Yes, if a song is owned by Universal it tends to be more popular.

## Setup

### python
0. have python installed, and it must be 3.7, if you don't have it, you can compile it from source with the following instructions
```
sudo apt-get install build-essential checkinstall
sudo apt-get install libreadline-gplv2-dev libncursesw5-dev libssl-dev \
    libsqlite3-dev tk-dev libgdbm-dev libc6-dev libbz2-dev libffi-dev zlib1g-dev
cd /usr/src
sudo wget https://www.python.org/ftp/python/3.7.3/python-3.7.3.tgz
sudo tar xzf python-3.7.3.tgz
cd python-3.7.3
sudo ./configure --enable-optimizations
sudo make altinstall
```

if you do it, then replace all further instances of python with python3.7


1. creating the virtual enviroment, i put it in the work folder to keep everything seperate.
```
python -m venv venv/
source venv/bin/activate
pip install jupyterlab ipython
```


2. jupyterlab/jupyter-notebook tends to be a bit weird about virtualenvironments, so we have to create a new ipython kernel for this virtual enviroment. here projectname can be replaced with whatever you want
```
ipython kernel install --user --name=projectname
```

3. install requirements.txt
```
pip install -r requirements.txt
```

4. you should be ready to go
to run, use either jupyter-notebook or jupyter-lab, i prefer jupyter-lab since you have a lot more options within it
```
jupyterlab
```

