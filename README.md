Modulefiles for use and testing of my Python packages
on GA's Iris computational cluster.

Details regarding Iris can be found
[here](https://diii-d.gat.com/diii-d/Iris), while
particulars of modules and modulefiles can be found
[here](https://diii-d.gat.com/diii-d/Iris#Environment_modules).

Use:
----
Currently, this repository contains modulefiles for
four of my github repositories:

* [random_data](https://github.com/emd/random_data),
* [mitpci](https://github.com/emd/mitpci),
* [bci](https://github.com/emd/bci), and
* [magnetics](https://github.com/emd/magnetics).

In addition to my own github repositories,
there are also modulefiles for the following:

* [a color-blind proof set of distinct colors](
   https://personal.sron.nl/~pault/), and
* [least-squares fitting a set of points to an ellipse](
   https://github.com/ndvanforeest/fit_ellipse).

The modulefiles are named after their corresponding packages, and
they should require *minimal* modification for your own use on Iris.
At the top of each module file, there is a TCL variable named

    <package>_root

You will need to change this to the top-level directory of
`<package>` on your account (the top-level directory is the
directory created when pulling from the github repo).
The `mitpci` package is unique in that it depends on
`random_data`, `fit_ellipse`, `bci`, and `magnetics`;
as a result, there is an additional TCL variable named

    modulefiles_dir

You should change this to the directory containing
the modulefiles for `random_data`, `fit_ellipse`, `bci`, and `magnetics`.

That's it!
You shouldn't need to change anything else in the modulefile.
The modules can then be loaded, unloaded, etc.,
as is discussed in the above-linked Iris documentation.
