## Create virtual environments for python with conda
---

**How to set up a virtual environments using conda for the Anaconda Python distribution**

A virtual environment is a named, isolated, working copy of Python that that maintains its own files, directories, and paths so that you can work with specific versions of libraries or `Python` itself without affecting other Python projects. Virtual environmets make it easy to cleanly separate different projects and avoid problems with different dependencies and version requiremetns across components. The `conda` command is the preferred interface for managing intstallations and virtual environments with the *Anaconda* Python distribution. Although creating virtual environments in anaconda is very easy, however there exits some considerations and a procedure for sure!

**1. Requirements**

- Anaconda Python distribution installed

- check conda version: open a termina and type 

```bash 
conda -V

conda 4.8.3
```
- you can update the conda with comand 

```bash 
conda update conda
```
---
**2.  Create a virtual environment for your project**

- In the terminal enter the following where _envname_ is the name you want to call your environment, and replace x.x with the `Pytho` version you wish to use. (To see a list of available python versions first,

```bash 
conda inf --envs
conda env list

conda create -n envname python=x.x
```

- Press `y` to proceed. This will install the Python version and all the associated anaconda packaged libraries at “path_to_your_anaconda_location/anaconda/envs/envname”
---
**3. Activate your virtual environment**

To activate or switch into your virtual environment, simply type the following where _envname_ is the name of your environment

```bash 
source activate envname
```
- and you can install jypyter with `conda install -y jupyter`

---
**4. Install additional Python packages to a virtual environment**

To install additional packages _only_ to your new virtual environment, enter the following comand  

```bash 
conda install numpy 
conda install pytorch
conda install panda 
```

**5. Deactivate your virtual environment8***

To end a session in the current environment, enter the following. There is no need to specify the envname - which ever is currently active will be deactivated.

```bash 
source deactivate
```

**6. Delete a no longer needed virtual environment**
To delete a conda environment, enter the following, where yourenvname is the name of the environment you wish to delete

```bash 
conda remove -n envname -all
```

### Create via anaconda-navigator 

An alternative way  to create a _env_ and install IDEs (`spyder`, `jupyter`, `R`, `VS code`, ... ) is via `anaconda_navigator` directly. [see](https://docs.anaconda.com/anaconda/navigator/tutorials/manage-environments "anaconda")











