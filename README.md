Modulefiles for use and testing of my Python packages
on GA's Iris computational cluster.

Details regarding Iris can be found
[here](https://diii-d.gat.com/diii-d/Iris), while
particulars of modules and modulefiles can be found
[here](https://diii-d.gat.com/diii-d/Iris#Environment_modules).

Use:
----
Currently, this repository contains modulefiles for
two of my github repositories:

* [random_data](https://github.com/emd/random_data), and
* [mitpci](https://github.com/emd/mitpci).

The modulefiles are named after their corresponding packages, and
they should require *minimal* modification for your own use on Iris.
At the top of each module file, there is a TCL variable named

    <package>_root

You will need to change this to the top-level directory of
`<package>` on your account (the top-level directory is the
directory created when pulling from the github repo).
That's it! You shouldn't need to change anything else in
the modulefile. The `random_data` and `mitpci` modules can
then be loaded, unloaded, etc., as is discussed in the
above-linked Iris documentation.
