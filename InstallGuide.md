# Introduction  
This is the installation instructions for getting ready for the deep learning workshop using tensorflow 2.0! 
  
There are two options I will go over for preparing to run the provided code for the workshop. 

1. The first option is to use [google colab](https://colab.research.google.com). You must have a Google account to use this cloud environment. It is free and requires no installation or changes on your local machine, so this is a good option if you don't want to install anything, or if you are concerned your laptop is too old/slow to run tensorflow. Google colab also offers free GPU time for you to use. You must be logged into you Google account to use it though. Also you must use Chrome, Firefox, or Safari as your browser (no internet explorer!) 

2. The second option is to install a local tensorflow environment on your computer, then download the course materials from github and run the notebooks. If you want to do this, I recommend you use the [Anaconda](https://www.anaconda.com/) infrastructure to easily and quickly download Python, tensorflow, and all the dependencies. I will show you how to do that with minimal impact on your computer using Windows, since that is what I use. Anaconda is available for Windows, macOS, and Linux. 

Please pick one of the options above, then follow the appropriate instructions to get setup. 

# Installation Instructions

## Method 1 - Google Colab

To use the Google colab environment, you must be logged into your google account. If you do not have a google account, you must create one. You also need to use a supported browser: Chrome, Firefox, or Safari. 

Here is a 3 minute video from Jake Vanderplas going over google colab if you have time to watch: https://www.youtube.com/watch?v=inN8seMm7UI

### Instructions for getting setup  

1. Navigate to https://colab.research.google.com/ in a supported browser. You may be prompted to login to your google account. 
2. Click on 'NEW PYTHON 3 NOTEBOOK'. 
3. This will open a fresh, new (blank) google colab notebook. Type in some basic Python code like `2 + 2`, then run the code using the 'play' button to the left of the code cell. The first time you run code, the notebook will connect to a Python runtime, which may take a few moments. 
4. Try some other basic Python code, like the following: `x = 5*30;print(x)`. You should see output, now you are up and running with Python on Google Colab! 
5. Tensorflow comes pre-installed in the colab environment, so you don't need to install it. You do need to load the module though. You also need to specify to use Version 2.X of tensorflow. I have created a notebook with all these steps and put it on github. Now I want you to import the notebook from github. It is easy to do!
6. In order to import the notebook from github:
    + first select FILE --> Open Notebook...
    + Click on the Github tab
    + type in `evan-paul-carey` into the search box. You should see a repository named `evan-paul-carey/deep-learning-workshop`. Select this repository.
    + There is a notebook in that repository called `Course_materials/notebooks/colab/Colab_Install_Test.ipynb`. Click on this notebook. 
    + To run this notebook, click 'Runtime' --> 'Run All'. Read the output from the cells, and you should see messages indicating the version of tensorflow. At the bottom cell, I create a basic tensorflow constant to prove it is loaded and functioning. 
7. You are done! Now you can sit back and marvel at how easy that was... :) 

    

## Method 2 - Install tensorflow locally (on your computer) with Anaconda

The second method you can use is to install a fully functioning Python tensorflow environment on your computer, then run it locally. Although there are other ways to do this, I will focus on using the Anaconda environment (and the associated conda package manager) to quickly and easily install all the required elements.  

### Install miniconda and build a tensorflow environment

We will use something called 'Miniconda' to install tensorflow. This is a bare bones version of the full Anaconda Python distribution, but it contains all the elements we need to build a new python environment. I am not using the full Anaconda distribution because:

*  It is large/heavy by default (includes a bunch of functionality, a lot of which we don't need)
*  It does not include tensorflow in the default environment, so you still have to build a new environment for tensorflow after you download it. 

So instead of downloading the full Anaconda distribution, I will download miniconda, then ask Miniconda to build a a python tensorflow environment. Miniconda is minimal version of Anaconda that includes Python and a few packages that support the conda package manager. 

1. Navigate to the link for miniconda, then install Miniconda3 (Python 3.x) for your OS: https://docs.conda.io/en/latest/miniconda.html 

2. Now that you have installed miniconda, launch the 'Anaconda prompt' so we can enter commands and ask Anaconda to build a new environment. On windows, I simply press the windows start button then type in 'Anaconda' to find it.  There is a lot you can do with this, here is a link to the guide on how to build environments with conda (but you can skip for now if you want to): and here is the full documentation for conda: https://conda.io/en/latest/

3. After you launch the Anaconda prompt, you should see a command prompt. The code you want to type to create a tensorflow/data science environment is this: `conda create -n py3_tf jupyter spyder tensorflow pandas seaborn`
This will create a new environment called `py3_tf`, that includes all the packages listed afterwards and their dependencies. You may need to confirm the download in the prompt, read the text and respond as directed. This will take a few minutes!

### Launch Jupyter notebooks and create a test notebook

Now you should have

1. Open Anaconda prompt again (close it and reopen it if you need to)
2. Ask conda to list the installed environments by typing `conda env list` then press enter. You should see the new environment you created for tensorflow, called `py3_tf` if you followed the instructions above. 
3. Activate the tensorflow environment by typing `activate py3_tf`. You should see the environment change from `(base)` to `(py3_tf)` in your command prompt interface
4. Now launch jupyter notebooks by typing `jupyter notebook`. This will launch the locally install jupyter notebook in the tensorflow environment. Jupyter notebooks are an html driven interface, so this will open your default web browser with the interface. The command prompt you opened will continue to run in the background, you can ignore it but you must keep it open!
5. Now you can create a new jupyter notebook from this screen. It should show you the files in your home folder. You can click on folders to navigate to them, or click the `new` button on the left to create a new folder. You also use the `new` button to create a new notebook. Create a new jupyter notebook using the `new` button. This will open a new tab with this notebook. 
6. Now we will type a few python commands into the notebook to test the functionality. 

Start with some basic Python math commands like this:

`2 + 2`
`x = 2*20`
`print(x)`

If you want to put them into different cells, use the `INSERT --> INSERT CELL BELOW` menu option. 
Now add a new cell and let's try some tensorflow commands. 

This should load tensorflow. We give the module the alias tf upon import so we can refer to it as tf in subsequent code.

`# load tensorflow`
`import tensorflow as tf`
  
`# check tensorflow version. Should be 2.x!`
`tf.__version__`

### Extras

Here is a link to the conda cheatsheet if you want to know more about the conda commands:
  
Conda cheatsheet:
https://docs.conda.io/projects/conda/en/4.6.0/_downloads/52a95608c49671267e40c689e0bc00ca/conda-cheatsheet.pdf`



If you want to try and install tensorflow in R, RStudio has a page with some directions. You can use R to run tensorflow, but I am not providing R files for this workshop at this time. This may change in the future as time permits :)  
  
https://tensorflow.rstudio.com/

