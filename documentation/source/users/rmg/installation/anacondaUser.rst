.. _anacondaUser:

****************************************************************************
Binary Installation Using Anaconda for Unix-Based Systems: Linux and Mac OSX
****************************************************************************


* Download and install the `Anaconda Python Platform <https://www.anaconda.com/download/>`_ for Python 2.7 (make sure not to install Python 3.0+, which is incompatible with RMG).

The download will be a .sh file with a name like ``Anaconda2-2018.12-Linux-x86_64.sh``. Open a terminal in the same
directory as this file, and type the following to install Anaconda (replace the name of your .sh file below). ::

    bash Anaconda2-2018.12-Linux-x86_64.sh

**When prompted to append Anaconda to your PATH, select or type Yes**.  Install the Anaconda folder inside your home directory (typically ``/home/YourUsername/`` in Linux and ``/Users/YourUsername`` in Mac). When prompted, You do NOT need to install Microsoft VSCode (but feel free to if you are looking for a lightweight IDE).

* Install both RMG and the RMG-database binaries through the Terminal.   Dependencies will be installed automatically. It is safest to make a new Anaconda environment for RMG and its dependencies. Type the following command into the Terminal to create the new environment named 'rmg_env' containing the latest stable version of the RMG program and its database. ::

    conda create -c rmg --name rmg_env rmg rmgdatabase
    
  Whenever you wish to use it you must first activate the environment::
    
    source activate rmg_env
    
* Optional: If you wish to use the :ref:`QMTP interface <qm>` with `MOPAC <http://openmopac.net/>`_ to run quantum mechanical calculations for improved thermochemistry estimates of cyclic species, please obtain a legal license through the `MOPAC License Request Form <http://openmopac.net/form.php>`_.  Once you have it, type the following into your Terminal ::
    
    mopac password_string_here

* You may now run an RMG test job. Save the `Minimal Example Input File <https://raw.githubusercontent.com/ReactionMechanismGenerator/RMG-Py/master/examples/rmg/minimal/input.py>`_  
  to a local directory.  Use the Terminal to run your RMG job inside that folder using the following command ::

    rmg.py input.py

You may now use RMG-Py, Arkane, as well as any of the
:ref:`Standalone Modules <modules>` included in the RMG-Py package.


Updating your binary installation of RMG in Linux or Mac OSX
============================================================

If you had previously installed a binary version of the RMG package, you may
check and update your installation to the latest stable version available on Anaconda by typing the following command on the Terminal ::

    source activate rmg_env
    conda update rmg rmgdatabase -c rmg 
