# Copulalib

This is a package/library in python to model the copulas.
This was developed as part of my PhD thesis.

This contains module for the following copula:
----------------------------------------------
* Frank
* Clayton
* Gumbel


Installing copulalib
======================

Installing copulalib is done by

    python setup.py install

with the usual Distutils options available


Usage
=========
Import required modules

    import numpy as np
    import matplotlib.pyplot as plt
    from copulalib.copulalib import Copula


Generate random (normal distributed) numbers

    x = np.random.normal(size=100)
    y = 2.5*x+ np.random.normal(size=100)

Make the instance of Copula class with x, y and clayton family

    foo = Copula(x, y, family='clayton')

Print the Kendall's rank correlation

    print(foo.tau) 

Print spearmen's correlation

    print(foo.sr)

Print pearson's correlation

    print(foo.pr)

Print the parameter (theta) of copula

    print(foo.theta)

Generate the 1000 samples (U,V) of copula
   
    X1, Y1 = foo.generate_xy(1000)

For more details see the test.py file inside module.

Changes
=============
Version 1.0.0 -- May, 2011 --- Initial release

Version 1.1.0 -- June, 2011 --- changed from function orieted to object oriented, documentation improved

version 2.0.0 -- Oct, 2022 --- Updated for Python 3, removed the dependancy on statistics library

Any questions/comments
=====================
If you have any comment/suggestion/question, 
please feel free to write me at satkumartomer@gmail.com

You may go through https://github.com/tomersk/learn-python to see the examples.

