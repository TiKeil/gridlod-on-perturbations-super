# gridlod-on-perturbations-super

```
# This repository is part of the project for "Numerical upscaling of perturbed diffsuion problems":
#   https://github.com/gridlod-community/gridlod-on-perturbations-super.git
# Copyright holder: Tim Keil, Fredrik Hellman 
# License: BSD 2-Clause License (http://opensource.org/licenses/BSD-2-Clause)
```

This repository provides code for the experiments of the paper "Numerical upscaling of perturbed diffusion problems" by Fredrik Hellman, Tim Keil and Axel Målqvist. The super repository consists of three modules. `gridlod` has been developed by Fredrik Hellman and Tim Keil and consists of code for PGLOD. `MasterthesisLOD` has been developed by Tim Keil for implementing code for arbitrary perturbed problems. `gridlod-on-perturbations` contains domain mappings and algorithms that are used and established in the paper.  

## Setup

This setup works with a Ubuntu system and Mac with minimal requirements. Python and suitesparse are required. For further information on required packages please see the README file of each submodule that we use. 
First of all, initialize all submodules via

```
git submodule update --init --recursive
```

Now, build and activate a python3 virtual environment with 

```
virtualenv -p python3 venv3
. venv3/bin/activate
```

and execute the following commands 

```
echo $PWD/gridlod/ > $(python -c 'from distutils.sysconfig import get_python_lib; print(get_python_lib())')/gridlod.pth
echo $PWD/MasterthesisLOD/ > $(python -c 'from distutils.sysconfig import get_python_lib; print(get_python_lib())')/MasterthesisLOD.pth
echo $PWD/gridlod_on_perturbations/ > $(python -c 'from distutils.sysconfig import get_python_lib; print(get_python_lib())')/gridlod_on_perturbations.pth
```
Now you can use every file from all the submodules in the virtualenv. Install all the required python packages for gridlod and go to 

```
cd gridlod-on-perturbations/2d_applications/HeKeMa2019/
``` 

to run the experiments that are presented in the paper.


``` 
python ex1_local_defects.py
``` 

If you only want to see the results, you just have to go to gridlod-on-perturbations/2d_applications/data/HeKeMa2019/ and run the plot file. All data from the experiments are available and stored in the repository. 
For any question or problems, please contact us via 'tim.keil@wwu.de' 
