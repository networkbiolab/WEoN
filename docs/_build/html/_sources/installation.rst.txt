Installation
============

First, be aware that WEoN runs a PERL script that filter out regulations unlikely occurring
from a gold standard GRN. Please follow the specific instructions for your
platform `here <https://www.perl.org/get.html>`_. Also, the app backend is in
transition to python, so please also follow intructions to get python3
`here <https://www.python.org/about/gettingstarted/>`_.

There are two different ways to obtain WEoN:

1. **Download from the Figshare repository (Recommended).** WEoN can be downloaded
   from `Figshare repository <https://figshare.com/articles/WEoN_install_zip/7913912>`_
   along with example data. Then, within Cytoscape, go to: Apps >> App Manager >> Install from File...

   *OR*

2. **Download from the Github repository.** If you are familiar
   with git, the `Github repository <https://github.com/networkbiolab/WEoN>`_ can be cloned
   and the respective jar file installed from within Cytoscape: Apps >> App Manager >> Install from File...

Additionally, please run ``script.sh`` or copy the PERL scripts to
``/home/$USER/CytoscapeConfiguration/3/apps/installed``
(\*UNIX), while similar paths exist in MacOS and Windows OS.
Please be aware you need a PERL interpreter to execute WEoN backend.

.. note::
	**Downloading from the Cytoscape App Store.** We'll upload WEoN to the Cytoscape
	`App Store <https://apps.cytoscape.org/>`_ soon, where it could be downloaded. However,
	example data could only be obtained from the Figshare repository due to size limitations.

.. note::
	**Need Help?**
	If you run into any problems with installation, please leave an issue in the
	official `Github repository <https://github.com/networkbiolab/WEoN>`_.
