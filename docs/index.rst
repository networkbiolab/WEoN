Welcome to WEoN FlyT documentation!
===================================

The Weighted Epigenomic Network: Fly Tool (WEoN-FlyT) is a `Cytoscape`_ app that incorporates a filtering method to determine context-specific gene regulatory networks (GRNs). The method employs diverse data to filter out regulatory connections between genes. The tool uses histone modifications through Chromatin Inmunoprecipitation followed by DNA sequencing (ChIP-seq), gene expression through RNA-seq, and chromatin accesibility through DNase-seq data to perform analysis of a GRN. A serie of heuristic filters removes experimentally determined and computational inferred regulations (such as Transcription factors and regulatory RNAs) from a GRN considered as a Reference Network (e.g. a GRN with all known connections, regardless the developmental stage or cell type). The corresponding context-specific GRN considers weighted information, and the generated network can be further analyzed within the `Cytoscape`_ software.

Please write directly to us (`Leandro Murgas`_, `Alberto JM Martin`_) or post an issue at the `Github repository`_ if you encounter any problem.

.. toctree::
   :maxdepth: 3

   installation
   use_instructions

Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`

.. refs
.. _Cytoscape: https://cytoscape.org/
.. _Leandro Murgas: leandro.murgas@mayor.cl
.. _Alberto JM Martin: alberto.martin@umayor.cl
.. _Github repository: https://github.com/networkbiolab/WEoN/issues
