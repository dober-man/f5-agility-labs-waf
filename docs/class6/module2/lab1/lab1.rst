Lab 2.1: Installation of f5's WAF Tester
-------------------------------------------

Expected time to complete **10 minutes**

**Installation**

	This tool runs on a linux based host and requires Python 2.7+.  

To install Python:
1. Log into the Ubuntu jumphost, client01 (usernamba/password f5student/f5DEMOs4u!).

Ubuntu/Kali:

.. code-block:: bash

        sudo apt-get install -y python-pip


2. Once Python is installed, install the tool using the following command:

.. code-block:: bash

        pip install git+https://github.com/f5devcentral/f5-waf-tester.git

.. toctree::
   :maxdepth: 1
   :glob:

   lab1/lab1
   lab2/lab2
   lab3/lab3
   lab4/lab4