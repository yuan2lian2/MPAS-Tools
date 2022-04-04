# MPAS Tools

[![Build Status](https://dev.azure.com/MPAS-Dev/MPAS-Tools%20testing/_apis/build/status/MPAS-Dev.MPAS-Tools?branchName=master)](https://dev.azure.com/MPAS-Dev/MPAS-Tools%20testing/_build/latest?definitionId=4&branchName=master)

This repository houses all MPAS related tools. These include compiled tools,
and scripts with a variety of purposes. Tools should be sorted into larger
directories based on their purpose. Under each of these directories, a tool
should live in it's own directory.

## Documentation

The latest documentation for the conda package `mpas-tools` can be found here:

[http://mpas-dev.github.io/MPAS-Tools/stable/](http://mpas-dev.github.io/MPAS-Tools/stable/)

Many tools are not in the conda package, and documentation (sometimes fairly
limited) is available at the beginning of each script.

## YL: Installation of mpas_tools to site-packages using conda_packages
1. brew install proj
2. brew install geos
3. pip install cartopy
4. pip install imageio
5. install jigsawpy https://github.com/dengwirda/jigsaw-python.git

	+ a. python setup.py build_external
	+ b. python setup.py install

6. install mpas_tools https://github.com/MPAS-Dev/MPAS-Tools.git

	+ a. cd conda_package
	+ b. python setup.py install

## YL: modifications for 2D mesh generation
add option to rotate periodic_hex from yz plane to xz plane (xz_plane=1 at prompt)

To generate xz plane mesh (using included namelist as an example):

	$ cd mesh_tools/periodic_hex
	$ make
	$ ./periodic_grid (xz_plane=1 at prompt)
