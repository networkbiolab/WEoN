Instructions to use WEoN
========================

This document contains the principal instructions in order to use the Cytoscape
app WEoN (Weighted Epigenetic Networks). To open WEoN, go to Cytoscape Apps menu,
then click on WEoN to open it.

We currently applied the method to *Droshophila melanogaster* due to a specific
epigenetic code referred to the experimentally determined impact of post-
traslational modifications on histones.

1. **Interface**

   The WEoN interface is a simple selector screen that serves as input screen for
   the backend PERL scripts, therefore parsing correctly the genomic data and
   calling orderly the scripts to filter out unlikely ocurring regulations.

.. image:: images/interface.png
	:align: center

2. **Required data**

   WEoN use RNA-seq data to filter out absent transcription factors and miRNAs
   from the Gold Standard (or Reference Network). We provide three Gold Standards,
   which were constructed within a differente cutoff of 1500, 2000, and 5000
   nucleotides from the Transcription Start Site.

   Please select a two-column file separated by tabulations as an ``Expression File``.
   The first column is the gene name while the second is the expression in any
   unit, like counts, RPKM, or FPKM. WEoN use an internal dictionary to match gene
   names from the Gold Standard and the Expression File. Data must be a single
   experiment or the average value of the experimental replica.

   We provide ``expression_test.tsv`` as an example ``Expression File``. Please
   click on the corresponding ``Select File`` button and navigated to the containing
   folder. Also, provide a path (with write permission) from the ``Select Folder``
   button: click on and navigate.

.. note::
	The resulting Gene Regulatory Network will be stored at the user selected path
	from the ``Select Folder`` button. Although, the GRN will be loaded automatically
	when WEoN finish the filtering processes, the user can reuse the GRN.

3. **Optional data**

   ``DNase file`` and ``Methylation file`` are four-columns files separated by
   tabulations. Each column correspond, in order, to the chromosome where was mapped
   the sequence, the initial coordinate, the ending coordinate, and the score for
   the mapped feature. Both files has an associated ``Score`` block which the user
   can use a threshold value where all lower scores are dismissed. Default is zero,
   meaning all mapped features in the ``DNase`` and ``Methylation`` files will
   be used in the filtering process.

   The ``Histone Mark Path Files`` allows the introduction of a single file that
   determine the absolute path to ChIP-seq experiments for each histone post-
   tranlational modification. The file is a four-column text as follow:

   .. code-block:: bash

		mark		state	annotation	location
		H3K27me3	-		promoter	/absolute/path/to/example_data/H3K27me3_0-4hr.bed
		H3K27ac		+		promoter	...
		H3K36me2	+		promoter	...
		H3K36me3	+		promoter	...
		H3K4me1		+		promoter	...
		H3K4me2		+		promoter	...
		H3K4me3		+		promoter	...
		H3K79me2	+		promoter	...
		H3K9ac		+		promoter	...
		H3K9me2		+		promoter	...
		H3K9me3		+		promoter	...
		H3S10ph		+		promoter	...
		H4K16ac		+		promoter	...
		H4K20me3	-		promoter	...

.. note::
	We will improve the annotation of histone marks associating each mark to an
	experimentally validated effect on specific DNA sequences like promoters. For
	the current release of WEoN, the 3rd column don't interfere with the filtering
	process.

4. **Execute filtering**

   Click on ``Run WEoN``, wait, and load the time/tissue specific GRN into Cytoscape
   clicking on ``Create View``.

.. note::
	Feel free to contact directly throught the `Github repository <https://github.com/networkbiolab/WEoN>`_
	or to Dr. Alberto Martin's `e-mail <amartin@umayor.cl>`_.