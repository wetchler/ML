# ML
Teaching resource for GDSO pre-workshop 2019

https://raw.githubusercontent.com/wetchler/ML/master/README.md

### Other lessons this week
1. (Monday) - [GitHub and git](https://github.com/geoffbacon/collaboration) (Instructor: Geoff)
1. (Tuesday) - [Jupyter notebooks](https://github.com/charlesfrye/DSW2018-tutorials/tree/master/JupyterNotebookForGreatGood) (Instructor: Charles)
1. (Wednesday) - [PANDAS](https://github.com/wetchler/pandas) (Instructor: Everett)
1. (Thursday) - [Data visualization](https://github.com/lchen23/GDSO_workshop) (Instructor: Liang)
1. ** (Friday) - [Machine Learning (this tutorial)](https://github.com/wetchler/ML) (Instructor: Everett) **

### Use CoLab (not Binder) for today if you don't have python set up locally
[USE THIS LINK](http://colab.research.google.com/github/wetchler/ML/blob/master/workbook.ipynb)

### Machine Learning is a BIG topic

We're not going to take you from zero to full-speed here today. We'll orient you to some of the basics, and show you how to do already-familiar things (e.g. linear regression) in Python.

### **If you learn nothing else today...

...learn to [hang out on the scikit-learn website](https://scikit-learn.org/stable/documentation.html) -- they have LOTS of good tutorials (start with their [Quick Start](https://scikit-learn.org/stable/tutorial/basic/tutorial.html))

All that said...

### Overview of today

1. What is Machine Learning
1. Review the "data science" pipeline
1. Build, interpret, and score a basic linear regression model
1. Understand model evaluation and cross-validation
1. Show how easy it is to extend to random forests or any other algorithm

### Machine Learning

(Very) roughly, **machine learning = prediction**. If you write a computer program that uses things you know to predict things you don't know, you're generally doing machine learning. For example:
* Someone is applying for a loan at a bank. You know their credit score, age, and income (known things). You want to know if they will repay their loan (unknown thing).
* You have a patient's medical history and recent test results (known things). You want to know if they will develop cancer later in life (unknown thing).
* You are considering implementing a new math program at a school. You have the standardized test results from a bunch of students at a bunch of schools using a bunch of different programs (known things). You want to know if instituting this program will raise standardized test scores in this school (unknown thing).

Phrases you might hear in the machine learning (ML) world:
- (Names of modelling algorithms): random forest, support vector machine, neural network, convolutional neural network, recurrent neural network, etc etc forever
- (Names of techniques): train-test split, cross-validation, k-fold, imputation, one-hot encoding, feature engineering, feature selection, hyperparameter, gradient descent, confusion matrix, ROC curve, etc etc forever

### The data science pipeline

As defined by me.

1. Initial data inspection and cleaning - `pandas` - typically, for me, this means:
   - Load the data in excel and look around
   - Load in pandas in a Jupyter notebook.
     - Figure out what the hell all the columns mean (sometimes referring to documentation where the data came from)
     - Get rid of columns and rows I realize I don't need
     - Rename columns to something easy to use
     - Join datasets together if I'm working with several (repeating the steps above for each first)
     - Look for bad / missing values and decide what to do with them (sometimes, nothing)
     - Write a cleaned-and-joined version of the data to a file for use in subsequent steps.
1. Exploratory data analysis - `seaborn`, `matplotlib`, `pandas` - we did a bit of this Wednesday, but mostly you make plots like you did Thursday with seaborn and matplotlib.
    - Plot the distribution of every column of interest.
    - Count how often each column has missing values (e.g. if a column is only there for 10% of the data, maybe I don't wanna use it?)
    - Correlate stuff with other stuff
    - Generally try to look for "interesting" things going on. This is an iterative process.
1. Modelling - `sklearn` etc - predict the main Thing of interest.
   - This is often the _least_ creative part of the process.
   - We'll learn about this in our tutorial today.
1. Presenting - `powerpoint` etc - translate your findings to your team, client, etc
   - We won't cover this here, but it's a highly overlooked step. Communicating at the right level (showing just enough technical detail to get the point across) is hard to do well.

### Lies, damned lies, and statistics

Machine learning, like statistical models, can be (and often are) used improperly to generate bogus results. Often by the kindest, best-intended people who were just trying to do honest science. So, be careful. All models have assumptions, all code has bugs, so be sure to
1. work in teams (to check each other) and
2. work with an experienced person who can shine a light on things you didn't know that you didn't know.

### Further links
* I meantioned [scikit-learn tutorials](https://scikit-learn.org/stable/documentation.html) already.
* [Kaggle](https://www.kaggle.com) is a good website to hone your machine learning / data science chops. On the surface, they host competitions, but you can also find good datasets, read others code, and generally just learn and practice. READING OTHERS' CODE IS ONE OF THE BEST WAYS TO LEARN
