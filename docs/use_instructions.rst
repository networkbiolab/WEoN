Instructions to use WEoN FlyT
=============================

This document contains the principal instructions in order to use the Cytoscape
app **WEoN FlyT (Weighted Epigenetic Networks: Fly Tool)**. 

0. **Open WEoN FlyT**

   Within Cytoscape, go to: Apps >> WEoN FlyT - Weighted Epigenomic Network: Fly Tool. This will display the user interface as shown in the figure.

1. **Interface**

The WEoN FlyT interface is a simple selector screen that serves as input screen. In the backend, WEoN FlyT run under Perl scripts, therefore parsing correctly the genomic data and calling orderly the scripts to filter out unlikely ocurring regulations.

.. image:: images/interface.png
	:align: center

.. note::
	Mac users has reported that the network definition selector did not shown correctly, but this selector is still here, you only need to click in this ``blank space`` and the menu will be displayed to select other reference network


.. .. note::
.. .. 	We will improve the annotation of histone marks associating each mark to an
.. .. 	experimentally validated effect on specific DNA sequences like promoters. For
.. .. 	the current release of WEoN, the 3rd column don't interfere with the filtering
.. .. 	process.

2. **Required data**

In order to use WEoN FlyT you need to provide at least three required parameters as listed as follod:

- Network Definition: This field correspond to the base network in order to apply filters to generate the final Gene Regulatory Network. We provide three References, which were constructed within a differente cutoff of 1500, 2000, and 5000 nucleotides from the Transcription Start Site of the Drosophila melanogaster genome.

- Expression File: WEoN FlyT use RNA-seq data to filter out absent transcription factors and miRNAs from the Reference Gene Regulatory Network (GRN). So in this parameter you need to provide a two-column file separated by tabulations, where the first column is the gene name while the second is the expression in any unit, like counts, RPKM, or FPKM. WEoN FlyT use an internal dictionary to match gene names from the Reference Network and the Expression File. Data must be a single experiment or the average value of the experimental replication.

- Result Folder: A folder where final output will be placed.

3. **Optional data**

If you have data from DNase, Histone modificationes and/or methylation experiments, you can use it to get a more specific Gene Regulation Network. 

So, for the ``DNase file`` and ``Methylation file`` fields, you need to select a four-columns files separated by tabulations. Each column correspond, in order, to the chromosome, the initial coordinate, the ending coordinate, and the score for the mapped feature. Both files has an associated ``Score`` block which the user can use a threshold value where all lower scores in the fouth column of the original file are dismissed. Default is zero, which means that all mapped features in the ``DNase`` and ``Methylation`` files will be used in the filtering process.

Respect to the ``Histone Mark Path Files`` button, once you click it a new window will appear as shown in the next image

.. image:: images/marks.png
	:align: center
	
So in this new window you can select files for the corresponding Post-traductional modification in Histone tails. Each file must be a three columns files separated by a tabulation, where each column correspond to the chromosome, the initial coordinate and the ending coordinate.

4. **Execute filtering**

After all the data is loaded, please click on ``Run WEoN FlyT`` and when all processes are done the network will be loaded into cytoscape. It is important to note that when the job is finished, you need to click on ``Create View`` button to display the time/tissue specific GRN in Cytoscape.

.. note::
	It's important to remark that this proces can take a very long time depending on your machine characteristics and files provided to WEoN FlyT (with more information/data, more time will take to compute all the information). Please be patinet


4. **Output Files**

Additionally, a set of files are created after executing WEoN FlyT and are located in the folder selected as output in the main window of the app. These files are described as follow:

- output_filter_PTMs.txt: A file which display information about chomosome, id of the coding gene for the transcription factor (TF), starting coordinate of the transcription factor binding site (TFBS), ending coordinate of the TFBS, name of the postraductional histonemark (PTM), starting coordinate of the PTM, ending coordinate of the PTM, open or closed chromatine (represented as + or -) and place where the PTM was found (into the promotor, P, or gene,G)

- output_connect.txt: A file where the first columns is the conection in the Gene Regulatory Network (GRN) and the second has info about PTM and the number of times that these PTM was found and affecting the conection

- output_connection_analysis.txt: A file with all PTM affecting the binding of the TF

- output_regulator_express.tsv: A file with conections from expressing regulators to gene

- output_regulator_no_express.tsv: A file with conections from non-expressing regulators to gene

- output_mirna_express.tsv: A file with conections from expressing miRNA to gene

- output_mirna_no_express.tsv: A file with conections from non-expressing miRNA to gene

- out_TFBS_network.tsv: A copy of the reference GRN preciusly used

- specific_GRN.tsv: A file that merge output_regulator_express.tsv and output_mirna_express.ts

- scored_GRN.tsv: Same as specific_GRN.tsv, but this file include information about the score of the conection. This score is calculated based on a set of filters (based on Expression, DNase, PTM and Methylation), indicating the existense of evidence about the interaction. Importantly to note that minimum score is 1 and maximum is 5 (only if all type of experiment were provided by the user)

.. note::
	If in the future you want to display the network in cytoscape, please use **specific_GRN.tsv** or **scored_GRN.tsv**


.. note::
	Feel free to contact directly throught the `Github repository <https://github.com/networkbiolab/WEoN>`_
	or to Dr. Alberto Martin's `e-mail <amartin@umayor.cl>`_.

