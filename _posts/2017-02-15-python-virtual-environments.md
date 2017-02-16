---
title: Python Virtual Environments
---

# Why do we need Virtual Environment?
To keep dependencies isolated from one project to another. In one project we
can use a package v1.X and in other we can use v2.X. Not just project
dependencies we can even have different python versions in each project
using virtual environments

There are tools which allow us to create virtual environments.
`virtualenv` is popular one.

`pip install virtualenv`

### Settingup virtual environment for python2.7

```
$ virtualenv <path_to_store_your_virtual_environment>

# activating virtual environment
$ source <path_to_virtual_evnironment/bin/activate>

# check version of the python
$ python --version # Python 2.7.11

# deactivating
$ deactivate
```

### Settingup virtual environment for python3
```
$ virtualenv -p python3 <path_to_store_your_virtual_environment>

# activate and check the python version
$ python --version # Python 3.5.1
```

With `virtualenv` we have to manage all the virtual environment folders ourself 
and everytime to activate we need to provide the entire path. There is a
nice little wrapper `virtualenvwrapper` around `virtualenv` which
simplifies the creation, activating and managing python virtual
environments.

`pip install virtualenvwrapper`

With `virtualenvwrapper` you can configure where to put all your python virtual environments. Default location is `~/.virtualenvs`, to change this configure the environment variable `WORKON_HOME`.

After installing `virtualenvwrapper` you need to source it to use magic commands or place the following line in `~/.bashrc`.

`source /usr/local/bin/virtualenvwrapper.sh`

### Creating virtual envs using virtualenvwrapper
```
# this creates virtual env in ~/.virtualenvs
directory and activates it by default
$ mkvirtualenv env1

# to deactivate
$ deactivate


# to activate
$ workon env1 # we don't have to specify location of the virtualenv.
```

Along with the magic commands `virtualenvwrapper` also provides
`preactivate`, `predeactivate`, `postactivate` and `postdeactivate`
scripts to perform actions before, after activating and deactivating
virtual environments.

One use case I use these start scripts is to set environment variables
for a project. I set environment variables in `postactivate` script and
unset them in `postdeactivate` script.

Location of these startup scripts: `~/.virtualenvs/env1/bin`. Here
`env1` is your name of the virtual environment.


## References
[virtualenvwrapper](https://virtualenvwrapper.readthedocs.io/en/latest/){:target="_blank"}

[virtualenv](https://virtualenv.pypa.io/en/stable/){:target="_blank"}

