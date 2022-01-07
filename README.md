# Analysing NanoAOD with uproot at IP2I 

## Installation 

You should work on one of the `lyoui*` machines, not on the `lyouicms`. 

Install miniconda: 

```bash
wget https://repo.anaconda.com/miniconda/Miniconda3-py39_4.10.3-Linux-x86_64.sh
bash Miniconda3-py39_4.10.3-Linux-x86_64.sh
```

Answer all questions, make sure everything went well, and then log out and log in again

Create your conda environment for this exercise:

```bash
conda create -n uproot python=3.9
```

Activate it: 

```bash
conda activate uproot
```

Install Coffea (and its dependencies, including uproot and awkward) and jupyter:

```bash
conda install -c conda-forge coffea jupyter 
```

## Start a jupyter notebook server

Start a server listening from everywhere on port XXXX of your lyoui machine.
Choose XXXX to be a random integer over 1000. If the port is busy, just choose another one

```
jupyter notebook --no-browser --port=8889 --ip=0.0.0.0
```

If at IP2I, follow the link printed by this command to connect to your server from your browser. 

If not, establish an ssh tunnel from your place:

On your computer, do: 

```
 ssh -L 8888:lyoui4:XXXX lyoserv
```

And keep this connection open. 
This maps port 8888 on your machine (localhost) to port XXXX on your lyoui (where the server is listening), through lyoserv.

Then, head to [http://localhost:8888](http://localhost:8888). 

On the login page, provide the token that you can find in the jupyter logs on lyoui. 

Open the notebook you'd like to run. 
