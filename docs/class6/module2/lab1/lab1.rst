Lab 2.1: Installation of f5's WAF Tester
-------------------------------------------

Expected time to complete **10 minutes**

**Installation**

	This tool runs on a linux based host and requires Python 2.7+.  

To install Python:

2.1.1 - Log into the Ubuntu jumphost, client01 (username/password f5student/f5DEMOs4u!) and open a terminal.

#insert picture

Ubuntu/Kali:

.. code-block:: bash

        sudo apt-get install -y python-pip


2.1.2 - Once Python is installed, install the tool using the following command:

.. code-block:: bash

        pip install git+https://github.com/f5devcentral/f5-waf-tester.git