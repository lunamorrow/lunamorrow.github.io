---
title: End of the Parser Era
---

# End of the Parser Era

# Current Work

After a solid 6+ weeks of working on the OpenBabelParser, I am happy to annouce that it is done! 

During the implimentation of this class I hit quite a few roadblocks, namely that the CI was not working and having to convert support from OpenBabel 2.x to OpenBabel 3.x. I was able to rectify the CI with assistance from Hugo and Irfan and quite a lot of trial and error. 

Conversion to OpenBabel 3.x support was more challenging unfortunately. I had to create a fresh Python environment on my workstation and installing OpenBabel 3.1.1 proved to be difficult as the typical commands such as `mamba install -c conda-forge openbabel` were not working. This was because I had version 4.10.3 of conda and the newest version is 24.5.0... 
Once that was sorted I was able to run my tests again with pytest, and to my dismay, many of the OpenBabel 2.x methods I was using to access attributes had been depreciated. Accessing chiralities in particular was not replaced with an equivalent method, so this attribute cannot be converted across currently. I am in discussion with OpenBabel devs to try to find a better method to access chirality so that this attribute can be maintained.

I did get in contact with the OB devs about the missing PDB attributes and only some of them are recorded, and are quite buried with no easy access method. I have been requested to submit a PR with OpenBabel to rectify this (thus enabling me to access these variables), but this will be going on the backburner for once I finish the majority of this project.

The parser has been implimented with a handful of unit tests, which I will be circling back to extend after the OpenBabelReader is completed.

# What is done
* Obtain all relevant attributes from atoms in OBMols
* Develop unit testing for OpenBabelParser
* Convert these attributes to their relevant MDAnalysis Atom attribute, taking care with units (OpenBabelParser)
* CI is functional
* Support for OpenBabel 3.x instead of OpenBabel 2.x

# Working on
* OpenBabelReader - convert positions/trajectory; this class will work alongside the OpenBabelParser to create a Universe from an OBMol
* Tests for OpenBabelReader

# Next Steps (in order)
* Develop further tests with different file/molecule types for OpenBabelParser and OpenBabelReader.
* Documentation (including examples) for OpenBabelParser and OpenBabelReader.
* OpenBabel converter to work in the reverse direction - including tests and documentation.
* Cut a release and deploy on conda-forge.
