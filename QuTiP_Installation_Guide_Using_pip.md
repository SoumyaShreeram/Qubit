## Guide to Install QuTiP on Windows

This guide walks you through installing QuTiP and using it with nteract or Jupyter desktop. 
The general guide for installing QuTip is also available [here](http://qutip.org/docs/4.1/installation.html). 

### **Step 1:** Download the latest [Python](https://www.python.org/downloads/) version and nteract (the order matters!):

1. Download Python from [here](https://www.python.org/downloads/) and **select "add python to PATH"** before running the installation. 

2. Download nteract from [here](https://nteract.io/) and run the installation.

### **Step 2:** Loading general packages

1. Open windows command prompt from the start menu, and check if python has installed correctly by typing:

	`python`

	If you see version 3.x.x, you're good. 

2. Install required packages with pip

	`pip install numpy scipy cython nose matplotlib ipykernel matplotlib`

### **Step 3:** Downloading Visual Studio Build tools

1. Download and run Microsoft Build tools for Visual Studio from [here](https://visualstudio.microsoft.com/thank-you-downloading-visual-studio/?sku=BuildTools&rel=16) **or** download the latest community version from [here](https://visualstudio.microsoft.com/downloads/#build-tools-for-visual-studio-2017).

2. Under workloads, select *Build tools for Visual Studio C++* and leave remaining setting unchanged. Your download size should be ~10GB. 


### **Step 4:** Install QuTiP and run from nTeract

1. Once Step 3 is completed, go to windows command prompt and type:

	`pip install qutip`

2. Open nTeract, under Runtime --> select Python3. In the first cell type:

	`from qutip import *`

If QuTiP installed correctly, 1,2 should run without any errors. 

This guide is maintained by *Soumya Shreeram*, last updated on *06-Sept-2019*. 
