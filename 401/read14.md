# Matplotlib tutorial

- matplotlib is probably the single most used Python package for 2D-graphics. It provides both a very quick way to visualize data from Python and publication-quality figures in many formats. We are going to explore matplotlib in interactive mode covering most common cases.

### IPython and the pylab mode:
- IPython is an enhanced interactive Python shell that has lots of interesting features including named inputs and outputs, access to shell commands, improved debugging and much more.

### pyplot:
- pyplot provides a convenient interface to the matplotlib object-oriented plotting library. It is modeled closely after Matlab(TM).

### Simple plot:
- In this section, we want to draw the cosine and sine functions on the same plot. Starting from the default settings, we'll enrich the figure step by step to make it nicer.

- The first step is to get the data for the sine and cosine functions:

import numpy as np

- X = np.linspace(-np.pi, np.pi, 256, endpoint=True)
C, S = np.cos(X), np.sin(X)

- To run the example, you can download each of the examples and run it using:
- $ python exercice_1.py

### Using defaults:
- Matplotlib comes with a set of default settings that allow customizing all kinds of properties. 
![](https://github.com/rougier/matplotlib-tutorial/raw/master/figures/exercice_1.png)

### Instantiating defaults:

- In the script below, we've instantiated (and commented) all the figure settings that influence the appearance of the plot.
![](https://github.com/rougier/matplotlib-tutorial/raw/master/figures/exercice_2.png)


