Dirichlet
=========

A Python package to estimate the Dirichlet distribution, calculate maximum
likelihood, and test for independence from a variable based on fitting nested
Dirichlet distribution hypotheses.

Most of this package is a port of Thomas P. Minka's wonderful
[Fastfit][fastfit] MATLAB code. Much thanks to him for that and his clear
paper ["Estimating a Dirichlet distribution"][estimating].

[estimating]: http://research.microsoft.com/en-us/um/people/minka/papers/dirichlet/
[fastfit]: http://research.microsoft.com/en-us/um/people/minka/software/fastfit/

Dirichlet Test
--------------

This likelihood ratio test for independence will determine whether two
Dirichlet-distributed data sets are likely to be from the same distribution
or from two different ones, much like a chi-square or G-test for independence,
but with Dirichlet models.

Simplex Plots
-------------

The `dirichlet.simplex` module creates scatter, contour, and filled contour 2-simplex plots.

Caveats
-------

Note that this package at the moment doesn't support sparse data vectors due to the
numerical fitting algorithm that uses the gamma function. Possibly some sort of
[additive smoothing](https://en.wikipedia.org/wiki/Additive_smoothing) would
make this package work in your context, but that will depend on your application.

Installation
------------

    pip install git+https://github.com/ericsuh/dirichlet.git

Note: this has only been tested with Python 2.7+ and Python 3.6+. Other versions
may work, but they haven't been tested.

The v0.8.0 series will be the last version to support Python 2.7, since the latest
versions of all of the dependencies have dropped support for Python 2. v0.8.0
should be compatible with the last versions of each of `scipy`, `numpy`, and
`matplotlib` that support Python 2.