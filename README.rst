##################################################
Veggiecron Server: a healthier alternative to cron
##################################################

.. class:: no-web

    Veggiecron (inspired by the unix crontab and `celery <http://www.celeryproject.org/>`_) is a **Python server for scheduling jobs via REST API**. Standing on the shoulders of such giants as `asyncio <https://docs.python.org/dev/library/asyncio.html>`_ and `tornado <http://www.tornadoweb.org/en/stable/>`_, veggiecron is able to run thousands of jobs a minute.


    .. image:: http://i.imgur.com/yJm3tLz.gif
        :alt: live preview gif
        :width: 100%
        :align: center

========
Contents
========
.. contents::


============
Installation
============

Veggiecron will not be available via pip until we reach the version 1.0 `milestone <https://github.com/jacobbridges/veggiecron-server/milestone/1>`_ For those brave enough to run the "pre-v1" product, follow these instructions:

.. code-block:: bash

   # Ensure you have Python 3.5+
   $ python --version

   # Clone the repo
   $ git clone https://github.com/jacobbridges/veggiecron-server.git && cd veggiecron-server

   # (OPTIONAL) Create a virtual environment to run the project
   $ virtualenv venv -p python3.5
   $ ./venv/bin/activate

   # Install the dependencies
   pip install -r requirements.txt

=====
Usage
=====

-------------
Configuration
-------------

High-level configurations can be found in the ``config.yaml`` file. Descriptions of each config are in the following table:

========  =====================================================================
Config    Description
========  =====================================================================
app.env   Application environment. Defaults to "development".
app.name  If you don't like "veggiecron-server".
app.key   Application key used to hash passwords. Be sure to generate your own!
host      Host to run the server on.
port      Port to run the server on.
db_file   Name of the SQLite3 database file.
========  =====================================================================
