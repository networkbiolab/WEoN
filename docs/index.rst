Welcome to WEoN's documentation!
================================

Weighted Epigenomic Network (WEoN) is a `Cytoscape`_ app that incorporates a filtering method to determine context-specific gene regulatory networks. The method employs diverse data to filter out regulatory connections between genes. WEoN uses histone modifications through Chromatin Inmunoprecipitation followed by DNA sequencing (ChIP-seq), gene expression through RNA-seq, and chromatin accesibility through DNase-seq data. A serie of heuristic filters removes known and inferred regulations (like Transcription factors and regulatory RNAs) from a Gene Regulatory Network (GRN) considered as a Reference Network (e.g. a GRN with all known connections, regardless development stage or cell type). The corresponding context-specific GRN considers weighted information, and the generated network can be further analyzed within the `Cytoscape`_ software.

Please write directly to us (`Leandro`_, `Alberto`_) or post an issue at `Issues`_ if you encounter any problem.

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
.. _Leandro: leandro.murgas@mayor.cl
.. _Alberto: alberto.martin@umayor.cl
.. _Issues: https://github.com/networkbiolab/WEoN/issues
