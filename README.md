# gridlod-on-perturbations-super

This repository aims to provide code for experiments with gridlod-on-perturbations

## Setup

First of all, initialize all submodules via

```
git submodule update --init --recursive
```

Now, build and activate a python3 virtual environment and do the following commands 

```
echo $PWD > $(python -c 'from distutils.sysconfig import get_python_lib; print(get_python_lib())')/gridlod.pth
echo $PWD/MasterthesisLOD/ > $(python -c 'from distutils.sysconfig import get_python_lib; print(get_python_lib())')/MasterthesisLOD.pth
echo $PWD/gridlod_on_perturbations/ > $(python -c 'from distutils.sysconfig import get_python_lib; print(get_python_lib())')/gridlod_on_perturbations.pth
```
Now you can use every file from all the submodules in the virtualenv.


