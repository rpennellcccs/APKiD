APKiD
=====

APKiD gives you information about how an APK was made. It identifies
many compilers, packers, obfuscators, and other weird stuff. It's *PEiD*
for Android.

For more information on what this tool can be used for, check out our
HITCON 2016 presentation: `Android Compiler
Fingerprinting <http://hitcon.org/2016/CMT/slide/day1-r0-e-1.pdf>`__.

Installing
==========

.. code:: bash

    git clone https://github.com/rednaga/yara-python
    cd yara-python
    python setup.py install
    pip install apkid

The *yara-python* clone and compile steps are temporarily necessary
because it installs our DEX Yara module. We're working on removing this
step.

Usage
=====

::

    usage: apkid [-h] [-j] [-t TIMEOUT] FILE [FILE ...]

    APKiD - Android Application Identifier

    positional arguments:
      FILE                  apk, dex, or dir

    optional arguments:
      -h, --help            show this help message and exit
      -j, --json            output results in JSON
      -t TIMEOUT, --timeout TIMEOUT
                            Yara scan timeout in seconds

Submitting New Packers
======================

If you come across an APK or DEX that apkid does not recognize, please
open a GitHub issue and tell us what you think it is and provide the
file hash (either MD5, SHA1, SHA256).

License
=======

This tool is available under a dual license: a commercial one suitable
for closed source projects and a GPL license that can be used in open
source software.

Depending on your needs, you must choose one of them and follow its
policies. A detail of the policies and agreements for each license type
are available in the LICENSE.COMMERCIAL and LICENSE.GPL files.

Hacking
=======

To install the package from source in editable mode (useful for
devlopment):

.. code:: bash

    pip install -e .

If the above doesn't work, due to permission errors dependant on your
local machine and where Python has been installed, try specifying the
``--user`` flag. This is likely needed if you are working on OSX:

.. code:: bash

    pip install -e . --user
