# Ionosphere Signals Discrimination - Goose Bay, Labrador #

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/jofaval/ionosphere/blob/master/notebook.ipynb)

## Table of contents

1. [📁 Data](#-data)
1. [📓 Description](#-description)
1. [✔️ Objective](#-objective)
1. [🧱 Tech stack](#-tech-stack)
1. [💹 Algorithms](#-algorithms)
1. [📊 Visualization](#-visualization)
1. [🤓 Conclusions](#-conclusions)
1. [©️ Credits](#-credits)

## 📁 Data
[↑ Back to the table](#table-of-contents)

The data is available at the official archive link:\
[https://archive.ics.uci.edu/ml/datasets/ionosphere](https://archive.ics.uci.edu/ml/datasets/ionosphere)

## 📓 Description
[↑ Back to the table](#table-of-contents)

**Abstract**: Classification of radar returns from the ionosphere

This radar data was collected by a system in Goose Bay, Labrador. This system consists of a phased array of 16 high-frequency antennas with a total transmitted power on the order of 6.4 kilowatts. See the paper for more details. The targets were free electrons in the ionosphere. "Good" radar returns are those showing evidence of some type of structure in the ionosphere. "Bad" returns are those that do not; their signals pass through the ionosphere. 

## ✔️ Objective
[↑ Back to the table](#table-of-contents)

To discriminate between good and bad ionosphere signals. Received signals were processed using an autocorrelation function whose arguments are the time of a pulse and the pulse number. There were 17 pulse numbers for the Goose Bay system. Instances in this databse are described by 2 attributes per pulse number, corresponding to the complex values returned by the function resulting from the complex electromagnetic signal.

TL;DR; A binary classification task.

## 🧱 Tech stack
[↑ Back to the table](#table-of-contents)

Python, that's it! R is a programming language that, as for the moment being, I have no experience with, even though it's powerful and broadly used, but I'd dare to say that no more than Python.

And one of the strongest points, if not the most, about Python, are it's libraries, so... the libraries I've used are:

- Pandas, data manipulation with an ease of use and exploration data analysis.
- Numpy, a really strong linear algebra library, used in the project for it's statistics utilities, SciPy may be an alternative, but I have no experience at all with it.
- Matplotlib and Seaborn, both fantastic libraries for data visualization, and they complement each other.
- Scikit-Learn, the library used for Machine Learning and statistics models: Linear Regression, SVR, Lasso, Ridge, etc.

## 💹 Algorithms
[↑ Back to the table](#table-of-contents)

I've used XGBoost and a really simple neural network using Tensorflow.

- XGBoost, a powerful algorithm based on gradient boosted regularization.
- Neural networks, a scalable architecture that is said to be able to learn almost anything.

My reasoning as to why I chose those two, XGBoost is really useful and quite easy to get started in. While neural networks seem a better fit for signal recognition, and I wanted to try that out with a simple architecture.

Surprisingly, they weren't too far off from each other, but XGBoost did perform better.

## 📊 Visualization
[↑ Back to the table](#table-of-contents)

The dataset is composed of signals, so the only, and appropiate visualization, that's worth featuring, are the signals representations themselves. As to better comprehend and evaluate the problem and it's model performances.

Another visualization worth noticing it's the pattern similarity comparison. I tried to create a plot that would kind of represent the two types of signals and overlap them, as to better identify any noticable difference. If there were to be almost no difference, the task would have been much harder, luckily, that was not the case.

## 🤓 Conclusions
[↑ Back to the table](#table-of-contents)

Whenever possible, even on a perfect, ready-to-work dataset, read the abstract, the paper, whatever information it is that you may have at hand, it truly helps understand the evaluation of the results and it's tuning.

I'm starting to realize that, even though it's important, understanding what you're tackling, and correctly visualizing the problem, it's one of the most important tasks, if not the most, and comprehending what you're doing, even if we, nowadays, have algorithms that are really powerful and easy to implement, can help a lot as to understand what's going on, or what's not going on if it should.

## ©️ Credits
[↑ Back to the table](#table-of-contents)

```
Donor:

Vince Sigillito (vgs '@' aplcen.apl.jhu.edu)

Source:

Space Physics Group
Applied Physics Laboratory
Johns Hopkins University
Johns Hopkins Road
Laurel, MD 20723

Donated in 1989-01-01
```

But more information can be found at the [official datateset's paper](http://archive.ics.uci.edu/ml/datasets/connectionist+bench+(sonar,+mines+vs.+rocks)).