Installation
============

First, be aware that WEoN FlyT runs a PERL script that filter out regulations unlikely occurring from a Reference GRN. Please follow the specific instructions for your platform `here <https://www.perl.org/get.html>`_.

.. Also, the app backend is in transition to python, so please also follow intructions to get python3 `here <https://www.python.org/about/gettingstarted/>`_.

**Requeriments**

- Java: Instructions to install Java depends on your operating system. Windows and MacOS users should download Java 8 from `Download_Java`_ and follow the installer instructions. For Unix users, Java could be installed from the repository packages `openjdk-8-jdk` and `openjdk-8-jre` (e.g. `apt-get install openjdk-8-jdk openjdk-8-jre`).

- Cytoscape: Download the Cytoscape software from `Download_Cytoscape`_. The webpage will automatically determine your operating system and prompt a download button.

- Perl: Similarly to Java, Windows users should install a Perl interpreter. Please download from `Download_Perl`_ and follow the instructions. For MacOS and Unix operating systems, Perl can be already installed; if not, the user can install it from the repository.

**Getting WEoN FlyT**

WEoN Fly is freely available to download from **Figshare**. As WEoN FlyT can be used in several operating systems (Linux, Windows and mac) you need to download you current version a from s listed as follow.

- WEoN FlyT for Linux `download here <https://figshare.com/articles/WEoN_FlyT_for_Linux/11956758>`_ 

- WEoN FlyT for Windows `download here <https://figshare.com/articles/WEoN_FlyT_for_windows/11958972>`_ 

- WEoN FlyT for Mac `download here <https://figshare.com/articles/WEoN_FlyT_for_mac/11958942>`_ 

To download WEoN FlyT, once you are in the download page, you can get it cliking in the **download button** as shown in the image.

.. image:: images/download.png
	:align: center



**Installation**

With the corresponding file for your OS, and the requirements are met, you need to unzip it. After this process is complete you now have a folder containing another folder called WEoN_FlyT, which correspond to the core of WEoN FlyT, and WEoN_FlyT.jar file, corresponding to the cytoscape app, a visual interface that allows to Cytoscape interact with WEoN FlyT.

In order to install the prograam you need to do the following steps for the main folder and for the cytoscape app:

- **WEoN_FlyT main folder:** You need to move the WEoN_FlyT folder to /Users/your_username in **mac**, to C: in **Windows** and /home/your_username in **Linux** environments.

.. note::
	**Additional files for Windows users:**
	In some systems, copying WEoN FlyT folder must need for admin permissions, for this case we include an **installation.bat** file, which automatically will ask for these permissions and then will generate a copy of the folder in C:

- **WEoN_FlyT.jar file:** In order to install the Cytoscape app, you need to open cytoscape and then navigate to Apps menu >> App Manager >> Install from File as pointed with a red arrow in the next image.

.. image:: images/select_file.png
	:align: center

Clicking on the ``install from file`` button a new window will appear, where you need to navigate to the jar file and select it as shown in the next image 

.. image:: images/selec_file2.png
	:align: center

After selecting the jar file a new window appear as shown in the next image, so clicking the ``close`` button all the process is done. 

.. image:: images/select_file3.png
	:align: center

Now you only need to go to the Apps menu >> WEoN FlyT to start to use WEoN FlyT

.. note::
	**Need Help?**
	If you run into any problems with installation, please leave an issue in the
	official `Github repository <https://github.com/networkbiolab/WEoN>`_.

.. refs
.. _Download_Cytoscape: https://cytoscape.org/download.html
.. _Download_Java: https://www.java.com/es/download/manual.jsp
.. _Download_Perl: http://strawberryperl.com/
