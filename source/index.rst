#############################
The spectra-cluster toolsuite
#############################

Welcome
=======

The spectra-cluster toolsuite provides tools to facilitate the usage of
spectrum clustering for MS/MS based proteomics data analysis.

It is centered around our spectra-cluster algorithm which is used to build
the `PRIDE Archive`_ resource (`Griss et al., Nat. Methods 2016`_).

.. _PRIDE Archive: https://www.ebi.ac.uk/pride/cluster
.. _Griss et al., Nat. Methods 2016: http://rdcu.be/i1Sa

Tutorials
=========

  * :doc:`/tutorials/clustering_basics`: Exaplanation of how to prepare your
    data for clustering and run the spectra-cluster-gui tool.

Clustering MS/MS data
=====================

The spectra-cluster toolsuite currently contains three tools to cluster
MS/MS based proteomics data:

  * `spectra-cluster-gui`_: Graphical user interface
  * `spectra-cluster-cli`_: Command line version
  * `spectra-cluster-hadoop`_: Hadoop version

All of these tools use the `spectra-cluster Java API`_ to perform the actual
clustering and should produce comparable results.

.. _spectra-cluster-gui: https://github.com/spectra-cluster/spectra-cluster-gui
.. _spectra-cluster-cli: https://github.com/spectra-cluster/spectra-cluster-cli
.. _spectra-cluster-hadoop: https://github.com/spectra-cluster/spectra-cluster-hadoop
.. _spectra-cluster Java API: https://github.com/spectra-cluster/spectra-cluster


Analysing clustering results
============================

The spectra-cluster toolsuite uses the **.clustering** file format
to store MS/MS clustering results. 

The spectra-cluster toolsuite contains a collection of tools that are able
to process this format:

The `clustering-file-converter`_ can extract consensus spectra in a variety for formats.
Most importantly it also supports the MSP format and can thereby be used to create
spectral libraries from clustering results.

The `spectra-cluster-py`_ project contains a collection of tools to analyse clustering
results. A detailed descritption of all the available tools can be found at
https://spectra-cluster-py.readthedocs.io

.. _clustering-file-converter: https://github.com/spectra-cluster/clustering-file-converter

Developing own tools
====================

The spectra-cluster toolsuite provides several ready-to-use APIs that support the
development of MS/MS clustering algorithms as well as own analaysis tools.

  * `clustering-file-reader`_: Java API to read the .clustering format
  * `spectra-cluster-py`_: Tools to analyse .clustering files as well as
    a Python API to process .clustering files

.. _clustering-file-reader: https://github.com/spectra-cluster/clustering-file-reader
.. _spectra-cluster-py: https://github.com/spectra-cluster/spectra-cluster-py

The `spectra-cluster Java API`_ contains the core clustering functionality used by the
implementations of the spectra-cluster algorithm. To test the effect of a, for example,
different spectrum similarity method it is only necessary to implement a single interface.
This new code will then be fully compatible with all existing tools (for example the
`spectra-cluster-cli`_ command-line interface) which allows the user to immediately test the
new implementation.

.. _spectra-cluster Java API: https://github.com/spectra-cluster/spectra-cluster

.. toctree::
   :maxdepth: 2
   :hidden:

   self
   tutorials/index

.. * :ref:`genindex`
.. * :ref:`modindex`
.. * :ref:`search`

