Welcome to WEoN's documentation!
===================================

WEoN (Weighted Epigenomic Network) is a `Cytoscape`_ app that incorporates a
filtering method to determine specific gene regulatory networks. The method uses
histone modifications through CHIp-on-chip seq, gene expression through
RNA-seq, and chromatin accesibility through DNase-seq to filter out known and
inferred regulations (like Transcription factors and regulatory RNAs) from a
Gene Regulatory Network (GRN) considered as a gold standard (e.g. a GRN with
all connections). The corresponding specific GRN consider weighted information
that can be further analyzed to validate the network.

.. toctree::
   :maxdepth: 3

   Installation
   Use_instructions

Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`

.. refs
.. _Cytoscape: https://cytoscape.org/
