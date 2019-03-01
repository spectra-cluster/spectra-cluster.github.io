===========================
Clustering tools / software
===========================

The spectra-cluster toolsuite currently contains four tools to cluster
MS/MS based proteomics data:

  * `Proteome Discoverer node`_: Proteome Discoverer node of the spectra-cluster algorithm
  * `spectra-cluster-cli`_: Command line version
  * `spectra-cluster-gui`_: Graphical user interface
  * `spectra-cluster-hadoop`_: Hadoop version

All of these tools use the `spectra-cluster Java API`_ to perform the actual
clustering and should produce comparable results.

Our own development focuses on the `spectra-cluster-cli`_ tool. Therefore, this tool is always at
the latest development stage.

.. _spectra-cluster-gui: https://github.com/spectra-cluster/spectra-cluster-gui
.. _spectra-cluster-cli: https://github.com/spectra-cluster/spectra-cluster-cli
.. _spectra-cluster-hadoop: https://github.com/spectra-cluster/spectra-cluster-hadoop
.. _spectra-cluster Java API: https://github.com/spectra-cluster/spectra-cluster

Developing own algorithms
=========================

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

