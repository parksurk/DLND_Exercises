Deep Learning with PyTorch
==========================

This repo contains notebooks and related code for Udacity's Deep Learning with PyTorch lesson. This lesson(Part 1~8) appears in Udacity [AI Programming with Python Nanodegree program](https://www.udacity.com/course/ai-programming-python-nanodegree--nd089).

-	**Part 1:** Introduction to PyTorch and using tensors
-	**Part 2:** Building fully-connected neural networks with PyTorch
-	**Part 3:** How to train a fully-connected network with backpropagation on MNIST
-	**Part 4:** Exercise - train a neural network on Fashion-MNIST
-	**Part 5:** Using a trained network for making predictions and validating networks
-	**Part 6:** How to save and load trained models
-	**Part 7:** Load image data with torchvision, also data augmentation
-	**Part 8:** Use transfer learning to train a state-of-the-art image classifier for dogs and cats
-	**Part 9:** Using dataset loader - torchvision.imageFolder
-	**Part 10:** Using dataset loader - custom dataset
-	**Part 11:** Using dataset loader - torchvision.transforms
-	**Part 12:** Using Tensorboard in PyTorch
-	**Part 13:** Using Learning Rate Schedule
-	**Part 14:** Saving and loading model

Configure and Manage Your Environment with Anaconda
===================================================

Per the Anaconda [docs](http://conda.pydata.org/docs):

> Conda is an open source package management system and environment management system for installing multiple versions of software packages and their dependencies and switching easily between them. It works on Linux, OS X and Windows, and was created for Python programs but can package and distribute any software.

Overview
--------

Using Anaconda consists of the following:

1.	Install [`miniconda`](http://conda.pydata.org/miniconda.html) on your computer, by selecting the latest Python version for your operating system. If you already have `conda` or `miniconda` installed, you should be able to skip this step and move on to step 2.
2.	Create and activate * a new `conda` [environment](http://conda.pydata.org/docs/using/envs.html).

\* Each time you wish to work on any exercises, activate your `conda` environment!

---

1.	Installation ---------------

**Download** the latest version of `miniconda` that matches your system.

**NOTE**: There have been reports of issues creating an environment using miniconda `v4.3.13`. If it gives you issues try versions `4.3.11` or `4.2.12` from [here](https://repo.continuum.io/miniconda/).

|        | Linux                                                                                            | Mac                                                                                               | Windows                                                                                            |
|--------|--------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| 64-bit | [64-bit (bash installer)](https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86_64.sh) | [64-bit (pkg installer)](https://repo.continuum.io/miniconda/Miniconda3-latest-MacOSX-x86_64.pkg) | [64-bit (exe installer)](https://repo.continuum.io/miniconda/Miniconda3-latest-Windows-x86_64.exe) |
| 32-bit | [32-bit (bash installer)](https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86.sh)    |                                                                                                   | [32-bit (exe installer)](https://repo.continuum.io/miniconda/Miniconda3-latest-Windows-x86_64.exe) |

**Install** [miniconda](http://conda.pydata.org/miniconda.html) on your machine. Detailed instructions:

-	**Linux:** http://conda.pydata.org/docs/install/quick.html#linux-miniconda-install
-	**Mac:** http://conda.pydata.org/docs/install/quick.html#os-x-miniconda-install
-	**Windows:** http://conda.pydata.org/docs/install/quick.html#windows-miniconda-install

-	Create and Activate the Environment
	-----------------------------------

For Windows users, these following commands need to be executed from the **Anaconda prompt** as opposed to a Windows terminal window. For Mac, a normal terminal window will work.

#### Git and version control

These instructions also assume you have `git` installed for working with Github from a terminal window, but if you do not, you can download that first with the command:

```
conda install git
```

If you'd like to learn more about version control and using `git` from the command line, take a look at our [free course: Version Control with Git](https://www.udacity.com/course/version-control-with-git--ud123).

**Now, we're ready to create our local environment!**

1.	Clone the repository, and navigate to the downloaded folder. This may take a minute or two to clone due to the included image data.

```
git clone https://github.com/parksurk/DLND_Exercises.git
cd DLND_Exercises
```

1.	Create (and activate) a new environment, named `dlnd` with Python 3.6. If prompted to proceed with the install `(Proceed [y]/n)` type y.

	-	**Linux** or **Mac**:

	```
	    conda create -n dlnd python=3.6
	    source activate dlnd
	```

	-	**Windows**:

	```
	    conda create --name dlnd python=3.6
	    activate dlnd
	```

	At this point your command line should look something like: `(dlnd) <User>:DLND_Exercises <user>$`. The `(dlnd)` indicates that your environment has been activated, and you can proceed with further package installations.

2.	Install PyTorch and torchvision; this should install the latest version of PyTorch.

	-	Please, refer to the PyTorch Installation Guide : https://pytorch.org/get-started/locally/

	-	**Linux** or **Mac**:`
		conda install pytorch torchvision -c pytorch
		`

	-	**Windows**:\` conda install pytorch-cpu -c pytorch pip install torchvision\`

3.	Install a few required pip packages, which are specified in the requirements text file (including OpenCV).

```
cd DL_PyTorch
pip install -r requirements.txt
```

1.	Create an [IPython kernel](http://ipython.readthedocs.io/en/stable/install/kernel_install.html) for the `dlnd` environment.  

```
python -m ipykernel install --user --name dlnd --display-name "dlnd"
```

1.	Run Jupyter notebook

Now all of the `dlnd` libraries are available to you. Assuming you're environment is still activated, you can navigate to the Exercises repo and start looking at the notebooks:

```
cd DLND_Exercises
jupyter notebook
```

To exit the environment when you have completed your work session, simply close the terminal window.

### Notes on environment creation and deletion

**Verify** that the `dlnd` environment was created in your environments:

```
conda info --envs
```

**Cleanup** downloaded libraries (remove tarballs, zip files, etc):

```
conda clean -tp
```

**Uninstall** the environment (if you want); you can remove it by name:

```
conda env remove -n dlnd
```
