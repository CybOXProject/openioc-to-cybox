OpenIOC to CybOX Translator
===========================

Generate CybOX XML from OpenIOC XML

**Version**: 0.21 BETA

    Copyright (c) 2013 - The MITRE Corporation
    All rights reserved. See LICENSE.txt for more details.

    BY USING THIS PROGRAM, YOU SIGNIFY YOUR ACCEPTANCE OF THE TERMS AND CONDITIONS
    OF USE.  IF YOU DO NOT AGREE TO THESE TERMS, DO NOT USE THIS PROGRAM.


Compatible with:
* [CybOX 2.0.1](http://cybox.mitre.org/language/version2.0.1/)
* [OpenIOC 1.0](http://schemas.mandiant.com/2010/ioc/ioc.xsd)


Installation
------------

Download and extract the included files into your directory of choice. 
OpenIOC-to-CybOX requires Python 2.X. It was developed using Python 2.7, and may work under Python 2.6. It is not compatible with Python 3.

### Dependencies 

* [python-cybox](https://pypi.python.org/pypi/cybox) - A Python library for CybOX

You can install the dependencies using pip:

    $ pip install cybox

**NOTE**: Installing LXML (which python-cybox depends on) on Ubuntu requrires the
python-dev, libxml2-dev, and libxslt1-dev packages to be installed. 
Follow the link for instructions on installing python-cybox and LXML on Windows


Usage
-----

    python openioc_to_cybox.py <flags> -i <openioc xml file> -o <cybox xml file>

    Available Flags:
      -e: Embedded Observable Output Mode. Creates a single root Observable with nested 
          Observable Composition and Observables.   If this mode is not specified, the script 
          will create a single Observable at the root level for each Indicator Item and then 
          add a separate Observable with the Boolean logic that composes the indicator, via 
          Observable_Compositions.
      -v: Verbose output mode. Lists any skipped indicator items and also prints traceback for errors.



More information
----------------

* CybOX - http://cybox.mitre.org/
* OpenIOC - http://www.openioc.org/
