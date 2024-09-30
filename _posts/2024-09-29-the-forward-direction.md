---
title: Time to Change Directions
---

# Time to Change Directions

# Current Work

I am excited to annouce that the forward direction, from OpenBabel OBMol to MDAnalysis Universe, is now done! 

As I experienced with the OpenBabelParser, I have hit a fair few more roadblocks, mainly with a lack of API and documentation. I have a new-found love and respect for good documentation and those who create and maintain it! Conveniently, documentation will be the next task I pivot onto, to ensure that others can make use of the Converter.

The parser has now got more complete tests, as does the newly implemented reader. Unfortunately, these extended tests revealed some issues with how I was accessing and checking attributes in the OBMol or OBAtom. Namely, chainIDs, which when null in OpenBabel don't seem to equate to any None values in Python! This attribute has been removed and a new Issue made regarding its implementation later on. 

# What is done
* Obtain all relevant attributes from atoms in OBMols
* Develop unit testing for OpenBabelParser
* Convert these attributes to their relevant MDAnalysis Atom attribute, taking care with units (OpenBabelParser)
* CI is functional
* Support for OpenBabel 3.x instead of OpenBabel 2.x
* OpenBabelReader - convert positions/trajectory; this class will work alongside the OpenBabelParser to create a Universe from an OBMol
* Tests for OpenBabelReader

# Working on
* Documentation with ReadTheDocs (including examples) for OpenBabelParser and OpenBabelReader.

# Next Steps (in order)
* Develop further tests with different file/molecule types for OpenBabelParser and OpenBabelReader.
* OpenBabel converter to work in the reverse direction - including tests and documentation.
* Cut a release and deploy on conda-forge.
* Clean up missing attributes (see discussion in current work section)
