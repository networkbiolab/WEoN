Installation
============

First, be aware that WEoN runs a PERL script that filter out regulations unlikely occurring from a Reference GRN. Please follow the specific instructions for your platform `here <https://www.perl.org/get.html>`_.

.. Also, the app backend is in transition to python, so please also follow intructions to get python3 `here <https://www.python.org/about/gettingstarted/>`_.

**Requeriments**

- Java: Instructions to install Java depends on your operating system. Windows and MacOS users should download Java 8 from `Download_Java`_ and follow the installer instructions. For Unix users, Java could be installed from the repository packages `openjdk-8-jdk` and `openjdk-8-jre` (e.g. `apt-get install openjdk-8-jdk openjdk-8-jre`).

- Cytoscape: Download the Cytoscape software from `Download_Cytoscape`_. The webpage will automatically determine your operating system and prompt a download button.

- Perl: Similarly to Java, Windows users should install a Perl interpreter. Please download from `Download_Perl`_ and follow the instructions. For MacOS and Unix operating systems, Perl can be already installed; if not, user can install it from the repository.

**Download WEoN**
There are two different ways to obtain WEoN:

1. **Download from the Figshare repository (With data, Recommended).** WEoN can be downloaded from `Figshare repository <https://figshare.com/articles/WEoN_install_zip/7913912>`_ along with example data. Then, within Cytoscape, go to: Apps >> App Manager >> Install from File...

.. image:: images/Download.png
    :align: center

   *OR*

2. **Download from the Github repository (Without data).** If you are familiar
   with git, the `Github repository <https://github.com/networkbiolab/WEoN>`_ can be cloned and the respective jar file installed from within Cytoscape: Apps >> App Manager >> Install from File...

**Installation**

Once you have downloaded and uncompress WEoN, and the requirements are met, you can install WEoN as follow

- Windows 10: double click on `install.bat` file and follow instructions. Or manually copy the uncompressed directory with data into any directory (e.g. `C:\users\your_user\Desktop`) and WEoN.jar into the `C:\Users\your_user\CytoscapeConfiguration\3\apps\installed` directory.

- Unix (Ubuntu): double click on `install.jar` and follow instructions. Or manually copy the uncompressed directory with data into any directory (e.g `/home/your_user/Desktop`) and WEoN.jar into `/home/your_user/CytoscapeConfiguration/3/apps/installed`

- MacOS: Copy the uncompressed directory with data into `/Users/your_user` and WEoN.jar into `/Users/your_user/CytoscapeConfiguration/3/apps/installed`

.. Additionally, please run ``script.sh`` or copy the PERL scripts to  ``/home/$USER/CytoscapeConfiguration/3/apps/installed`` (\*UNIX), while similar paths exist in MacOS and Windows OS. Please be aware you need a PERL interpreter to execute WEoN backend.

.. note::
	**Downloading from the Cytoscape App Store.** We'll upload WEoN to the Cytoscape
	`App Store <https://apps.cytoscape.org/>`_ soon, where it could be downloaded. However, example data could only be obtained from the Figshare repository due to file size limitations.

.. note::
	**Need Help?**
	If you run into any problems with installation, please leave an issue in the
	official `Github repository <https://github.com/networkbiolab/WEoN>`_.

.. refs
.. _Download_Cytoscape: https://cytoscape.org/download.html
.. _Download_Java: https://www.java.com/es/download/manual.jsp
.. _Download_Perl: http://strawberryperl.com/
