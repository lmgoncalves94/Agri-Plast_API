Case study
==========

.. note::

   The following tutorial is intended to be run entirely with Python 3.

.. _obtaining_the_files:

Obtaining the files
-------------------

In the case you haven't created the working directory, run the following:

``On Windows:``

.. code-block:: python
   
  import subprocess
  subprocess.run('wsl bash -c "mkdir /mnt/c/Agri-Plast"', shell=True, check=True)

``On Linux/Mac:``

.. code-block:: python

  import subprocess
  subprocess.run('mkdir ~/Agri-Plast', shell=True, check=True)

In this case study we'll be focusing on the following dataset:
`https://dmportal.biodata.pt/dataset.xhtml?persistentId=doi:10.34636/DMPortal/Q3YLV4 <https://dmportal.biodata.pt/dataset.xhtml?persistentId=doi:10.34636/DMPortal/Q3YLV4>`_
Take note of the doi:

.. code-block:: console

  doi:10.34636/DMPortal/Q3YLV4

Run the following to obtain the metadata file:

``On Windows:``

.. code-block:: python
   
  import subprocess
  doi = "doi:10.34636/DMPortal/Q3YLV4"
  subprocess.run(f'wsl bash -c "curl -L \\"https://dmportal.biodata.pt/api/datasets/:persistentId/?persistentId={doi}\\" -o /mnt/c/Agri-Plast/dataset.metadata"', shell=True, check=True)

``On Linux/Mac:``

.. code-block:: python

  import subprocess
  doi = "doi:10.34636/DMPortal/Q3YLV4"
  subprocess.run("TBA")

Searching for the ID following ´´"dataFile":{"id":´´ the following IDs are identified: ´´1231´´ and ´´1232´´. Run the following to obtain both files:

