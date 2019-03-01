============================
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

.. note::

  The `Proteome Discoverer Node`_ can directly export the clustering results in a standard 
  results table that can subsequently be easily loaded into R or MS Excel.

.. _clustering-file-converter: https://github.com/spectra-cluster/clustering-file-converter


