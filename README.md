# Discrete Mathematics classes

Class notebooks for Imperial College ELEC50006 by Dan Goodman.

My recommended way of running code is to use Google Colab with a Google account (links below). Other good options are running locally with Jupyter notebook server or VSCode (instructions below for Python) or [Replit](https://replit.com/).

## Week by week

### Week 1. Intro and Fibonacci.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/goodman-imperial/discrete-maths-classes/blob/main/week_1_class.ipynb) [![GitHub](https://badgen.net/badge/icon/github?icon=github&label)](week_1_class.ipynb)

### Week 2. Complexity Notation

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/goodman-imperial/discrete-maths-classes/blob/main/week_2_class.ipynb) [![GitHub](https://badgen.net/badge/icon/github?icon=github&label)](week_2_class.ipynb)

### Week 3. Divide and Conquer

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/goodman-imperial/discrete-maths-classes/blob/main/week-3-class.ipynb) [![GitHub](https://badgen.net/badge/icon/github?icon=github&label)](week-3-class.ipynb)

### Week 4. Divide and Conquer 2

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/goodman-imperial/discrete-maths-classes/blob/main/week-4-class.ipynb) [![GitHub](https://badgen.net/badge/icon/github?icon=github&label)](week-4-class.ipynb)

### Week 5. Dynamic Programming

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/goodman-imperial/discrete-maths-classes/blob/main/week-5-class.ipynb) [![GitHub](https://badgen.net/badge/icon/github?icon=github&label)](week-5-class.ipynb)

### Week 6. Greedy Algorithms

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/goodman-imperial/discrete-maths-classes/blob/main/week-6-class.ipynb) [![GitHub](https://badgen.net/badge/icon/github?icon=github&label)](week-6-class.ipynb)

### Week 7. Graphs

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/goodman-imperial/discrete-maths-classes/blob/main/week-7-class.ipynb) [![GitHub](https://badgen.net/badge/icon/github?icon=github&label)](week-7-class.ipynb)

### Week 8. Various topics

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/goodman-imperial/discrete-maths-classes/blob/main/week-8-class.ipynb) [![GitHub](https://badgen.net/badge/icon/github?icon=github&label)](week-8-class.ipynb)

## Installing Python locally

If you're comfortable with Python, you can install and run Python locally. My recommended technique is as follows:

Firstly, install [Miniconda](https://docs.conda.io/en/latest/miniconda.html) for Python 3.

Next, set up Conda to use ``conda-forge`` for binary distributions, by running this at the terminal.

```
conda config --add channels conda-forge 
conda config --set channel_priority strict
```

Create a virtual environment:

```
conda create --name dmclass python=3 jupyter matplotlib numpy scipy
```

## Running local Jupyter notebook server

Now activate the environment and run the Jupyter server in the directory where you downloaded the notebooks or cloned the repository.

```
conda activate dmclass
jupyter notebook
```

## Running via VSCode

Install Python as above and [follow the instructions here](https://code.visualstudio.com/docs/datascience/jupyter-notebooks).
