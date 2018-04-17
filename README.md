# Binder Tutorial

# Repository/Working directory

First, a directory for the project should be created and turned into a Git repository, or a git repository could be created on GitHub and cloned to the local machine.

```
git clone https://github.com/sVujke/{repo_name}.git
```

# Setting up the environment

Now, an environment should be created, this time we will do it with Anaconda. 

```
conda create -n binder_env python=3.6
```

This will create an environment arbitrarilly named as binder_env, with a python 3.6 interpreter. Before installing the packages, we need to activate the environment!

```
activate binder_env (Windows)
source activate binder_env (macOS or Linux)
```

In this example, two libraries have been added:


```
conda install pandas
conda install tensorflow
```

**NOTE!** In order for the jupyter notebook to recognize the environment, we need to install ipykernel

```
conda install ipykernel
```

We need to add pur environment as a kernel, which will enable jupyter notebook to recognize our environment and it's interpreter.


```
 python -m ipykernel install --user --name binder_env --display-name "Py - binder"
```

After this, we will be able to import packages into our notebooks! 

# Exporting the environment

As we need to keep track of our dependencies, we need to export a list of packages from our environment: 

```
conda env export > environment.yml
```

After this, we should commit and push our changes.
