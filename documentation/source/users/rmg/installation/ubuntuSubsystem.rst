.. _ubuntuSubsystem:

*****************************************************
Installing RMG in the Ubuntu Subsystem on Windows 10
*****************************************************

Installing the Ubuntu Subsystem
===================================

1. Follow the instructions provided by Microsoft to install the Ubuntu subsystem, available `here
<https://docs.microsoft.com/en-us/windows/wsl/install-win10>`_. The basic steps include enabling the Windows Linux
subsystem from a powershell **run as an administrator**, and downloading the latest LTS version of Ubuntu
*from the Windows store*. We highly recommend Ubuntu over the other Linux distros, as Ubuntu is used by many of the
RMG developers.

2. Once the Ubuntu subsystem is installed, open an Ubuntu terminal. Open a web browser in Windows and go to the
`Anaconda Python Platform Downloads Page <https://www.anaconda.com/download/#linux>`_. Go to the tab for the
**Linux Installer**, and **right click** on the download icon for Python 2.7 to copy the link location. Paste this link
into the Ubuntu terminal immediately after the ``wget`` command, so that your terminal looks like the following: ::

    wget https://repo.continuum.io/archive/Anaconda2-2018.12-Linux-x86_64.sh

Your exact link will look similar to the one above, but may be a more recent version of the installer. Execute this
command in the terminal to begin downloading the installer.

3. Once the Anaconda installer has downloaded, execute the following commands in the Ubuntu terminal, changing the name
of ``Anaconda2-2018.12-Linux-x86_64.sh`` to match the name of the script you downloaded. ::

    chmod 744 Anaconda2-2018.12-Linux-x86_64.sh
    ./Anaconda2-2018.12-Linux-x86_64.sh

Install the anaconda2 folder inside your home directory (it should be the default location when it asks for a location
to install). **When prompted to append Anaconda to your PATH, select or type Yes**. You do NOT need to install Microsoft
VSCode.

4. Execute the following commands to make sure that all of the required packages in Ubuntu are also installed: ::

    sudo apt install gcc
    sudo apt install g++
    sudo apt install make
    sudo apt-get install libxrender1

5. Follow the instructions for either the binary or source installation for the Linux Operating system.
