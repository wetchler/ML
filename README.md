# ML
Teaching resource for GDSO pre-workshop 2019

### Other lessons this week
1. (Monday) - [GitHub and git](https://github.com/geoffbacon/collaboration) (Instructor: Geoff)
1. (Tuesday) - [Jupyter notebooks](https://github.com/charlesfrye/DSW2018-tutorials/tree/master/JupyterNotebookForGreatGood) (Instructor: Charles)
1. (Wednesday) - [PANDAS](https://github.com/wetchler/pandas) (Instructor: Everett)
1. (Thursday) - Data visualization (link forthcoming) (Instructor: Liang)
1. (Friday) - [Stats and machine learning (this tutorial)](https://github.com/wetchler/ML) (Instructor: Everett)

### Machine Learning is a BIG topic

We're not going to take you from zero to full-speed here today. We'll orient you to some of the basics, and show you how to do already-familiar things (e.g. linear regression) in Python.

### **If you learn nothing else today...

...learn to hang out on the scikit-learn website -- they have LOTS of good tutorials [here](https://scikit-learn.org/stable/documentation.html) (start with their [Quick Start](https://scikit-learn.org/stable/tutorial/basic/tutorial.html))

All that said...

### Overview of today

1. Review the "data science" pipeline
1. Build, interpret, and score a basic linear regression model
1. Show how to use the same process for logistic regression and random forests.

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

### Lies, damned lies, and statistics

Machine learning, like statistical models, can be (and often are) used improperly to generate bogus results. Often by the kindest, best-intended people who were just trying to do honest science. So, be careful. All models have assumptions, all code has bugs, so be sure to 1) work in teams (to check each other) and 2) work with an experienced person who can shine a light on things you didn't know that you didn't know.

### Further links
* I meantioned [scikit-learn tutorials](https://scikit-learn.org/stable/documentation.html) already.
* [Kaggle](www.kaggle.com) is a good website to hone your machine learning / data science chops. You can join a competition OR simply read the notebooks that others write. READING OTHERS' CODE IS ONE OF THE BEST WAYS TO LEARN
