# Deep Learning with TensorFlow

This repo contains notebooks and related code for [TensorFlow Tutorial](https://www.tensorflow.org/tutorials/).

* **Part 1:** Introduction to PyTorch and using tensors
* **Part 2:** Building fully-connected neural networks with PyTorch
* **Part 3:** How to train a fully-connected network with backpropagation on MNIST
* **Part 4:** Exercise - train a neural network on Fashion-MNIST
* **Part 5:** Using a trained network for making predictions and validating networks
* **Part 6:** How to save and load trained models
* **Part 7:** Load image data with torchvision, also data augmentation
* **Part 8:** Use transfer learning to train a state-of-the-art image classifier for dogs and cats

# Instructions

To setup our project environment to run the code in this repository, follow the instructions below.

1. Install Git
	- Linux: https://www.atlassian.com/git/tutorials/install-git#linux
	- Mac: https://www.atlassian.com/git/tutorials/install-git#mac-os-x
	- Windows: https://www.atlassian.com/git/tutorials/install-git#windows
		- [Download for Windows](https://drive.google.com/file/d/1FIElyMq4C1M0sVyEAtJ61jb8NRFowPtI/view?usp=sharing)

2. Install Anaconda

	**Download** the latest version of `miniconda` that matches your system.

	**NOTE**: There have been reports of issues creating an environment using miniconda `v4.3.13`. If it gives you issues try versions `4.3.11` or `4.2.12` from [here](https://repo.continuum.io/miniconda/).

	|        | Linux | Mac | Windows |
	|--------|-------|-----|---------|
	| 64-bit | [64-bit (bash installer)][lin64] | [64-bit (bash installer)][mac64] | [64-bit (exe installer)][win64]
	| 32-bit | [32-bit (bash installer)][lin32] |  | [32-bit (exe installer)][win32]

	[win64]: https://repo.continuum.io/miniconda/Miniconda3-latest-Windows-x86_64.exe
	[win32]: https://repo.continuum.io/miniconda/Miniconda3-latest-Windows-x86.exe
	[mac64]: https://repo.continuum.io/miniconda/Miniconda3-latest-MacOSX-x86_64.sh
	[lin64]: https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86_64.sh
	[lin32]: https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86.sh

	**Install** [miniconda](http://conda.pydata.org/miniconda.html) on your machine. Detailed instructions:


- Anaconda for Windows 설치시 주의사항
	* 설치시 'Advanced Options' 단계에서 'Add Anaconda to my PATH environment variable' 옵션을 체크합니다.(Windows의 Default Command Prompt에서 Anaconda 명령어를 사용하기 위함입니다.)
			![](assets/images/readme_1_anaconda_installation_advanced_option_add_path.png)

3.	Clone this repository
	- [Reference #1 : Intorduction to Git for Data Science](https://www.datacamp.com/courses/introduction-to-git-for-data-science)
	- [Reference #2 : Git the simple guide](https://rogerdudler.github.io/git-guide/index.ko.html)

	```
	git clone https://github.com/parksurk/DLND_Exercises.git
	cd DLND_Exercises
	```

4. Create (and activate) a new environment, named `dlnd` with Python 3.6. If prompted to proceed with the install `(Proceed [y]/n)` type y.

	- __Linux__ or __Mac__:
	```
	conda create -n dlnd python=3.6
	source activate dlnd
	```
	- __Windows__:
	```
	conda create --name dlnd python=3.6
	activate dlnd
	```

	At this point your command line should look something like: `(dlnd) <User>:DLND_Exercises <user>$`. The `(dlnd)` indicates that your environment has been activated, and you can proceed with further package installations.

5. Install PyTorch and torchvision; this should install the latest version of PyTorch.

	- __Linux__ or __Mac__:
	```
	pip install tensorflow
	```
	- __Windows__:
	```
	pip install tensorflow
	```

6. Install a few required pip packages, which are specified in the requirements text file (including OpenCV).
	```
	cd DL_TF20
	pip install -r requirements.txt
	```

7. Create an [IPython kernel](http://ipython.readthedocs.io/en/stable/install/kernel_install.html) for the `dlnd` environment.  
	```
	python -m ipykernel install --user --name dlnd --display-name "dlnd"
	```

8. Run Jupyter notebook

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

# Additional JDK Installation for Konlpy

1. OS와 비트 수가 일치하고, 버젼이 1.7 이상인 자바가 설치되어 있나요? 만일 그렇지 않다면 JDK를 설치 합니다. 자바와 OS의 비트 수가 꼭 일치하도록 해주세요.
http://www.oracle.com/technetwork/java/javase/downloads/index.html

2. JAVA_HOME을 설정 합니다
http://docs.oracle.com/cd/E19182-01/820-7851/inst_cli_jdk_javahome_t/index.html

# Additional Dataset for Hands-on for CJ OliveYoung
- https://cjoliveyoung.cjdrive.cj.net/public/98iVt-w
- https://cjoliveyoung.cjdrive.cj.net/public/YrKhn-w
- 2개의 zip파일을 unzip 후 {실습 프로젝트 경로}/DLND_Exercises/DL_TF20/dataset 하위에 위치 하도록 합니다.
- 아래와 같은 디렉토리 구성이 되어야 합니다.
	- DLND_Exercises/DL_TF20/dataset/cifar
		- labels.txt
		- test
		- train
	- DLND_Exercises/DL_TF20/dataset/mnist_png
		- testing
		- training
