===================
Ubuntu Installation
===================

Add repository
--------------

The latest packages for Ubuntu are published in the saltstack PPA. If you have 
the ``add-apt-repository`` utility, you can add the repository and import the 
key in one step:

.. code-block:: bash

    sudo add-apt-repository ppa:saltstack/salt

Alternately, manually add the repository and import the PPA key with these commands:

.. code-block:: bash

    echo deb http://ppa.launchpad.net/saltstack/salt/ubuntu `lsb_release -sc` main | sudo tee /etc/apt/sources.list.d/saltstack.list
    wget -q -O- "http://keyserver.ubuntu.com:11371/pks/lookup?op=get&search=0x4759FA960E27C0A6" | sudo apt-key add -

After adding the repository, update the package management database:

.. code-block:: bash

    sudo apt-get update


Install packages
----------------

Install the Salt master, minion, or syndic from the repository with the apt-get 
command. These examples each install one daemon, but more than one package name 
may be given at a time:

.. code-block:: bash

    sudo apt-get install salt-master 

.. code-block:: bash

    sudo apt-get install salt-minion

.. code-block:: bash

    sudo apt-get install salt-syndic

.. _ubuntu-config:

Post-installation tasks
=======================

Now go to the :doc:`Configuring Salt</topics/configuration>` page.

