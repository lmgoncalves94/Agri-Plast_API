Obtaining the data
==================

.. note::

   The following tutorial is intended to be run entirely with Python 3.

.. _installing_wsl:

Installing WSL
--------------

To run the following tutorial on Windows 10/11, you need a Linux environment. The easiest way to achieve this is by using the Windows Subsystem for Linux (WSL). To install it, follow the steps below:

1. Go to Control Panel
2. Change View By to "Category"
3. Go to Programs
4. Go to Turn Windows features on or off
5. Check Windows Subsystem For Linux and click Ok
6. Restart your computer
7. Go to Microsoft Store
8. Search for "Ubuntu"
9. Click on the first search result
10. Click on Get or Install
11. Open Ubuntu
12. Wait for installation and choose username and password
13. Done!

.. _creating_dir:

Creating working directory
--------------------------

Running the following commands will create an Agri-Plast directory on C:/ and /home/user/ directories on Windows or Linux, respectively:

``On Windows:``

.. code-block:: python
   
   import subprocess
   subprocess.run('wsl bash -c "mkdir /mnt/c/Agri-Plast"', shell=True, check=True)

``On Linux/Mac:``

.. code-block:: python
   
   print("TBA")

.. _download_metadata:

Downloading metadata file
-------------------------

In this tutorial, we will be firstly focusing on the following dataset:
`https://dmportal.biodata.pt/dataset.xhtml?persistentId=doi:10.34636/DMPortal/AWYIXC <https://dmportal.biodata.pt/dataset.xhtml?persistentId=doi:10.34636/DMPortal/AWYIXC>`_

From this link we should take note of the doi:

.. code-block:: console
   
   doi:10.34636/DMPortal/AWYIXC

And replace on the the ``doi`` variable on the following command:

``On Windows:``

.. code-block:: python
   
   import subprocess
   doi = "doi:10.34636/DMPortal/AWYIXC"
   subprocess.run(f'wsl bash -c "curl -L \\"https://dmportal.biodata.pt/api/datasets/:persistentId/?persistentId={doi}\\" -o /mnt/c/Agri-Plast/dataset.metadata"', shell=True, check=True)

``On Linux/Mac:``

.. code-block:: python
   
   import subprocess
   doi = "doi:10.34636/DMPortal/AWYIXC"
   print("TBA")












