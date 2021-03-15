Introduction
============


.. image:: https://readthedocs.org/projects/circuitpython-uschedule/badge/?version=latest
    :target: https://circuitpython-uschedule.readthedocs.io/
    :alt: Documentation Status


.. image:: https://img.shields.io/discord/327254708534116352.svg
    :target: https://adafru.it/discord
    :alt: Discord


.. image:: https://github.com/cognitivegears/CircuitPython_uschedule/workflows/Build%20CI/badge.svg
    :target: https://github.com/cognitivegears/CircuitPython_uschedule/actions
    :alt: Build Status


.. image:: https://img.shields.io/badge/code%20style-black-000000.svg
    :target: https://github.com/psf/black
    :alt: Code Style: Black

Reduced version of the schedule library for CircuitPython

This library is a reduced version of the Python `schedule
library <https://pypi.org/project/schedule/>`_. Credit to `Dan Bader
(dbader) <https://dbader.org/>`_ for
this excellent library.


Dependencies
=============
This driver depends on:

* `Adafruit CircuitPython <https://github.com/adafruit/circuitpython>`_

Please ensure all dependencies are available on the CircuitPython filesystem.
This is easily achieved by downloading
`the Adafruit library and driver bundle <https://circuitpython.org/libraries>`_
or individual libraries can be installed using
`circup <https://github.com/adafruit/circup>`_.Installing from PyPI
=====================


On supported GNU/Linux systems like the Raspberry Pi, you can install the driver locally `from
PyPI <https://pypi.org/project/adafruit-circuitpython-uschedule/>`_.
To install for current user:

.. code-block:: shell

    pip3 install adafruit-circuitpython-uschedule

To install system-wide (this may be required in some cases):

.. code-block:: shell

    sudo pip3 install adafruit-circuitpython-uschedule

To install in a virtual environment in your current project:

.. code-block:: shell

    mkdir project-name && cd project-name
    python3 -m venv .env
    source .env/bin/activate
    pip3 install adafruit-circuitpython-uschedule



Usage Example
=============

.. code-block:: python

    import time
    import uschedule as schedule

    def greet():
        print("Hello, world!")

    schedule.every(10).seconds.do(greet)

    while True:
        schedule.run_pending()
        time.sleep(1)
    python3 -m venv .env



Contributing
============

Contributions are welcome! Please read our `Code of Conduct
<https://github.com/cognitivegears/CircuitPython_uschedule/blob/main/CODE_OF_CONDUCT.md>`_
before contributing to help this project stay welcoming.

Documentation
=============

For information on building library documentation, please check out
`this guide <https://learn.adafruit.com/creating-and-sharing-a-circuitpython-library/sharing-our-docs-on-readthedocs#sphinx-5-1>`_.
