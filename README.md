# Knowledge-Transfer-Workshop

Hi Everyone!

In this GitHub, we provided the guidelines the installation of Anaconda and Jupyter-Notebook on VS Code. Please read carefully and do installation before the day workshop start, so we can avoid the technical stuff. Before we proceed to basic python and machine learning examples, we setting up the conda environment with Python and some libraries are needed in this workshop. Hope you enjoy this workshop.

# Installation-Anaconda

## System requirements

- License: Free use and redistribution under the terms of the EULA for Anaconda Individual Edition.
- Operating system: Windows 8 or newer, 64-bit macOS 10.13+, or Linux, including Ubuntu, RedHat, CentOS 7+, and others.
- If your operating system is older than what is currently supported, you can find older versions of the Anaconda installers in our [archive](https://repo.anaconda.com/archive/) that might work for you. If [using Anaconda on older operating systems](https://docs.anaconda.com/anaconda/install/index.html#old-os), here for version recommendations.
- System architecture: Windows- 64-bit x86, 32-bit x86; MacOS- 64-bit x86; Linux- 64-bit x86, 64-bit aarch64 (AWS Graviton2 / arm64), 64-bit Power8/Power9, s390x (Linux on IBM Z & LinuxONE).
- Minimum 5 GB disk space to download and install.
- At least 8GB of RAM.

## Tutorial Installation of Anaconda

This repository will aid you to install Anaconda according to your preferrence operating system (OS). Pleaes choose your Anaconda version that compatible with your OS and follow the instructions in the documentation provided to install Anaconda. Here we provided the documentations to download and install Anaconda:
* [Windows](https://docs.anaconda.com/anaconda/install/windows/)
* [Linux](https://docs.anaconda.com/anaconda/install/linux/)
* [Mac Os](https://docs.anaconda.com/anaconda/install/mac-os/)

## Setting Up the Environment of Python 3
Hooorayyy!!!! You are done the installation of Anaconda. Now open the terminal for linux and macOs and activate `base` environment of anaconda by:

![Terminal](https://user-images.githubusercontent.com/70914271/152668997-60d7a8c5-8395-4309-846c-3a2b83af2d6c.png)

```
source ~/anaconda3/bin/activate
```
For windows, search `anaconda prompt` and double click it.
![windows](https://user-images.githubusercontent.com/70914271/152669025-8f8fe0b2-fe62-40c4-b037-7b7b919bc397.jpeg)
![Screenshot (27)](https://user-images.githubusercontent.com/70914271/154524696-0894c12d-9157-4c63-937c-322e55568386.png)

Since we are activated conda `base` environment, let's start to create the environment of Anaconda with python version `3.9`. You can read up more on how Conda environments work [here](https://docs.conda.io/projects/conda/en/latest/user-guide/concepts/environments.html). Basically, they're just a separate place you can mess around without interupting or corrupting your default setup. 

```
conda create -n myEnv python=3.9
```

Here, myEnv is the conda env we designated. To enter the environment it, just type:

```
conda activate myEnv         # to enter the environment

```

The env you just setup is empty, so you need to install the packages that you want to use, even when the default Conda environment has all of them.

```
conda install ipykernel
conda install notebook
```

The Jupyter Notebooks are designed for Python, so you should have no problems. Some libraries may not be available beforehand, so you should download them, such as Matplotlib, pandas, scikit-learn, and etc. If you have already added conda-forge as a channel, the -c conda-forge is unnecessary. Adding the channel is recommended because it ensures that all of your packages use compatible versions. Here is the [conda-forge docs](https://conda-forge.org/docs/user/introduction.html#how-can-i-install-packages-from-conda-forge):

```
conda config --add channels conda-forge
conda update --all
```

For machine learning, we are required some libraries in this workshop such as:
- [`matplotlib`](https://anaconda.org/conda-forge/matplotlib)
- [`seaborn`](https://anaconda.org/anaconda/seaborn)
- [`pandas`](https://anaconda.org/anaconda/pandas)
- [`numpy`](https://anaconda.org/anaconda/numpy)
- [`tensorflow`](https://anaconda.org/conda-forge/tensorflow)
- [`scikit-learn`](https://anaconda.org/anaconda/scikit-learn)
- [`jupyter`](https://anaconda.org/conda-forge/jupyter)

You need to install all these libraries in `myEnv` environment. To install these libraries, go to command prompt or terminal, just type:

```
conda install -c conda-forge <library name>
```
For example, we want to install `matplotlib`:
```
conda install -c conda-forge matplotlib
```
![Screenshot (30)](https://user-images.githubusercontent.com/70914271/154533713-8e934767-285d-4c37-b3ed-6dd1b99f0d4f.png)

Since you are done installation the libraries, you can check and ensure all these libraries are installed. Just type:
```
conda list
```

## Jupyter-Notebook
The Notebooks will give you a brief tutorial into Python, designed for undergrads that have little to no experience in programming. These notebooks are adapated from previous ones made in Python. Just press the Binder link and let it launch. Learn, enjoy, explore!

Running on Binder requires a good internet connection, but even then it does not guarantee that the kernel would not suddenly die. So, to minimize external factors disrupting your experience to learn, it is better for you to run the Jupyter Notebooks locally on your computer. Follow the steps outlined for contributors, then launch the notebooks from the Conda environment.

To open a notebook, and start developing!
```
jupyter-notebook
```

For windows, search `anaconda navigator` and double click it.
![Screenshot (25)](https://user-images.githubusercontent.com/70914271/154525512-dc4823f8-35f4-470f-b0c6-a57ddf0a5841.png)

![Screenshot (31)](https://user-images.githubusercontent.com/70914271/154540072-265dac17-f3bd-46b8-93e5-33e89664bb01.png)

The interface will pop up and make sure check the Jupyter Notebook was installed and environment you created `myEnv` is exist. During this workshop, you need to use this environment for the basic python and hands-on. Click launch the Jupyter Notebook:
![Screenshot (32)](https://user-images.githubusercontent.com/70914271/154540494-994c35d3-13cc-472e-8c83-ee7623b2dfed.png)

The Jupyeter Notebook will pop up the interface. To create a new notebook, click the button `New` and you will see in this notebook that you will be use python 3. Please try run and print `Hello world` in this notebook.
![Screenshot (33)](https://user-images.githubusercontent.com/70914271/154542523-8cbcdcbf-348a-4a91-97e8-62951acfa0f4.png)


# Jupyter Notebooks in VS Code
Jupyter (formerly IPython Notebook) is an open-source project that lets you easily combine Markdown text and executable Python source code on one canvas called a notebook. Visual Studio Code supports working with Jupyter Notebooks natively, and through Python code files. This topic covers the native support available for Jupyter Notebooks and demonstrates how to:

* Create, open, and save Jupyter Notebooks
* Work with Jupyter code cells
* View, inspect, and filter variables using the Variable Explorer and Data Viewer
* Connect to a remote Jupyter server
* Debug a Jupyter Notebook

## Installation VS Code
Please download and install the VS Code that compatible with your operating system:

* [Linux](https://code.visualstudio.com/docs/setup/linux)



