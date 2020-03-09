Installation
============

First, be aware that WEoN FlyT runs a PERL script that filter out regulations unlikely occurring from a Reference GRN. Please follow the specific instructions for your platform `here <https://www.perl.org/get.html>`_.

.. Also, the app backend is in transition to python, so please also follow intructions to get python3 `here <https://www.python.org/about/gettingstarted/>`_.

**Requeriments**

- Java: Instructions to install Java depends on your operating system. Windows and MacOS users should download Java 8 from `Download_Java`_ and follow the installer instructions. For Unix users, Java could be installed from the repository packages `openjdk-8-jdk` and `openjdk-8-jre` (e.g. `apt-get install openjdk-8-jdk openjdk-8-jre`).

- Cytoscape: Download the Cytoscape software from `Download_Cytoscape`_. The webpage will automatically determine your operating system and prompt a download button.

- Perl: Similarly to Java, Windows users should install a Perl interpreter. Please download from `Download_Perl`_ and follow the instructions. For MacOS and Unix operating systems, Perl can be already installed; if not, the user can install it from the repository.

**Getting WEoN FlyT**

You can Download WEoN FlyT from **Figshare** cliking in the **download button** as shown in the image.

.. image:: images/download.png
	:align: center

As WEoN FlyT can be used in several operating systems (Linux, Windows and mac) you need to download you current version as listed as follow.

- WEoN FlyT for Linux `download here <https://figshare.com/articles/WEoN_FlyT_for_Linux/11956758>`_ 

- WEoN FlyT for Windows `download here <https://figshare.com/articles/WEoN_FlyT_for_windows/11958972>`_ 

- WEoN FlyT for Mac `download here <https://figshare.com/articles/WEoN_FlyT_for_mac/11958942>`_ 



**Installation**

long with example data. Then, within Cytoscape, go to: Apps >> App Manager >> Install from File...


Once you have downloaded and uncompress WEoN, and the requirements are met, you can install WEoN as follow

- Windows 10: double click on `install.bat` file and follow instructions. Or manually copy the uncompressed directory with data into any directory (e.g. `C:\\users\\your_user\\Desktop`) and WEoN.jar into the `C:\\Users\\your_user\\CytoscapeConfiguration\\3\apps\\installed` directory.

- Unix (Ubuntu): double click on `install.jar` and follow instructions. Or manually copy the uncompressed directory with data into any directory (e.g `/home/your_user/Desktop`) and WEoN.jar into `/home/your_user/CytoscapeConfiguration/3/apps/installed`

- MacOS: Copy the uncompressed directory with data into `/Users/your_user` and WEoN.jar into `/Users/your_user/CytoscapeConfiguration/3/apps/installed`

.. Additionally, please run ``script.sh`` or copy the PERL scripts to  ``/home/$USER/CytoscapeConfiguration/3/apps/installed`` (\*UNIX), while similar paths exist in MacOS and Windows OS. Please be aware you need a PERL interpreter to execute WEoN backend.


.. note::
	**Need Help?**
	If you run into any problems with installation, please leave an issue in the
	official `Github repository <https://github.com/networkbiolab/WEoN>`_.

.. refs
.. _Download_Cytoscape: https://cytoscape.org/download.html
.. _Download_Java: https://www.java.com/es/download/manual.jsp
.. _Download_Perl: http://strawberryperl.com/
