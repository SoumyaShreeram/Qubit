## Guide to Install QuTiP on Windows

This guide walks you through installing QuTiP and using it with nteract or Jupyter desktop. 
The general guide for installing QuTip is also available [here](http://qutip.org/docs/4.1/installation.html). 

### **Step 1:** Download [Conda](https://docs.conda.io/projects/conda/en/latest/) and nteract (the order matters!):


1. In order to handle library dependencies outside of the Python packages, the Conda packaging tool needs to be downloaded. 

	<div id="demobox", style="background-color: #cfc ; padding: 10px; border: 1px solid green;">
	Download Miniconda 64-bit (exe installer) for Windows from <a href="https://docs.conda.io/en/latest/miniconda.html">here</a>.
	</div>

	**Note**: Allowing the situation of running QuTip alongside pip; this installation guide recommends Miniconda instead of Anaconda.


2. Go to the start menu and type *Anaconda prompt*. Here you can check the version of conda installed by typing `conda --version`. All the steps below use *Anaconda prompt*.

	Now, install the required kernels to run nteract

	`conda install ipykernel`

	`python -m ipykernel install --user`

3. Download nteract from [here](https://nteract.io/) and run the installation.

---

### **Step 2:** Installing QuTiP in a [Conda environment (env)](http://qutip.org/docs/4.1/installation.html#building-your-conda-environment)

1. Create Conda env for QuTiP called `qutip-env`

	`conda create -n qutip-env python=3`

2. Activate this environment

	`conda activate qutip-env`

3. Install the minimum required packages

	`conda install numpy scipy cython nose matplotlib ipykernel`	

4. Add the conda forge channels

	`conda config --append channels conda-forge`

5. Install QuTiP

	`conda install qutip`	

6. Let python know about the environment name 

	`python -m ipykernel install --user --name qutip-env --display-name "Python (qutip-env)"`

7. You are good to get started! Type in Anaconda prompt:

	`"c:\Program Files\nteract\nteract.exe"` 

	<div id="demobox", style="background-color: #cfc ; padding: 10px; border: 1px solid green;">
	<b>Note</b>: Since this guide is assuming that python is not downloaded on the OS, you would need to start interact through Anaconda prompt. If you have python installed prior, it would be possible to run <i>qutip-env</i> on nteract by opening nteract from the start menu. If you want to run QuTiP on nteract from the start menu go to <b>step 4</b>.
	</div>

8. In nteract make sure to run select *Python (qutip-env)* in the runtime option of the menu bar before running code in your notebook. 


### **Step 3:** Installing kernels for a general Python 3 environment using Conda (Optional)

1. Create a general kernel for all python packages

	`conda create -n Python3 python=3 ipykernel`

	`source activate Python3`

	`python -m ipykernel install --user`	

2. Download any other packages and you can run python 3 in this environment. For more information on making ipython kernels available accross different kernel refer to [this](https://ipython.readthedocs.io/en/stable/install/kernel_install.html) webpage.