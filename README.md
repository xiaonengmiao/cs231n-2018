# cs231n-2018

This repository contains my completed assignment to the CS231n Spring 2017 course from Stanford University. So far I have finished all three of them. The course page: [http://cs231n.github.io/](http://cs231n.github.io/)

## Useful links

- [Assignment 1](http://cs231n.github.io/assignments2017/assignment1/)
- [Assignment 2](http://cs231n.github.io/assignments2017/assignment2/)
- [Assignment 3](http://cs231n.github.io/assignments2017/assignment3/)

## Setup

You can work on the assignment in one of two ways: locally on your own machine, or on a virtual machine on Google Cloud.

### Working remotely on Google Cloud (Recommended)

**Note:** after following these instructions, make sure you go to **Working on the assignment** below (you can skip the **Working locally** section).

As part of this course, you can use Google Cloud for your assignments. We recommend this route for anyone who is having trouble with installation set-up, or if you would like to use better CPU/GPU resources than you may have locally. 

Please see the Google Cloud GPU set-up tutorial [here](http://cs231n.github.io/gce-tutorial-gpus/) for instructions. 

We strongly, strongly recommend using Google Cloud with GPU support for the last part of this assignment (the TensorFlow or PyTorch notebooks), since your training will go much, much faster. :)

### Working locally
Here's how you install the necessary dependencies:

**(OPTIONAL) Installing GPU drivers:**
If you choose to work locally, you are at no disadvantage for the first 3 parts of the assignment. For the last part, which is in TensorFlow or PyTorch, however, having a GPU will be a significant advantage. We recommend using a Google Cloud Instance with a GPU, at least for this part. If you have your own NVIDIA GPU, however, and wish to use that, that's fine -- you'll need to install the drivers for your GPU, install CUDA, install cuDNN, and then install either [TensorFlow](https://www.tensorflow.org/install/) or [PyTorch](http://pytorch.org/). You could theoretically do the entire assignment with no GPUs, though this will make training much slower in the last part. 

**Installing Python 3.5+:**
To use python3, make sure to install version 3.5 or 3.6 on your local machine. If you are on Mac OS X, you can do this using [Homebrew](https://brew.sh) with `brew install python3`. You can find instructions for Ubuntu [here](https://www.digitalocean.com/community/tutorials/how-to-install-python-3-and-set-up-a-local-programming-environment-on-ubuntu-16-04).

**Virtual environment:**
If you decide to work locally, we recommend using [virtual environment](http://docs.python-guide.org/en/latest/dev/virtualenvs/) for the project. If you choose not to use a virtual environment, it is up to you to make sure that all dependencies for the code are installed globally on your machine. To set up a virtual environment, run the following:

```bash
cd assignment1
sudo pip install virtualenv      # This may already be installed
virtualenv -p python3 .env       # Create a virtual environment (python3)
source .env/bin/activate         # Activate the virtual environment
pip install -r requirements.txt  # Install dependencies
# Note that this does NOT install TensorFlow or PyTorch, 
# which you need to do yourself.

# Work on the assignment for a while ...
# ... and when you're done:
deactivate                       # Exit the virtual environment
```

Note that every time you want to work on the assignment, you should run `source .env/bin/activate` (from within your `assignment2` folder) to re-activate the virtual environment, and `deactivate` again whenever you are done.

### Download data:
Once you have the starter code (regardless of which method you choose above), you will need to download the datasets needed for the assignments.
For example, you need to run the following from the `assignment1` directory:

```bash
cd cs231n/datasets
./get_datasets.sh
```

### Start IPython:
After you have downloaded the correponding datasets, you should start the IPython notebook server from the
`assignment` directory, with the `jupyter notebook` command. (See the [Google Cloud Tutorial](http://cs231n.github.io/gce-tutorial/) for any additional steps you may need to do for setting this up, if you are working remotely)

If you are unfamiliar with IPython, you can also refer to our
[IPython tutorial](/ipython-tutorial).
