---
title: Documentation
---

# Documentation

# Current Work

Documentation for the forward direction of the Converter, from OpenBabel OBMol to MDAnalysis Universe, is now done! 

Documentation has been built on ReadTheDocs and is currently hosted there. The documentation has been added to the project description and README to direct users

Some further documentation, specifically ipynb examples and the 'Getting Started' page need to be completed still, but this is a lower priority over working on functionality for the reverse direction from MDAnalysis back to OpenBabel.

# What is done
* Obtain all relevant attributes from atoms in OBMols
* Develop unit testing for OpenBabelParser
* Convert these attributes to their relevant MDAnalysis Atom attribute, taking care with units (OpenBabelParser)
* CI is functional
* Support for OpenBabel 3.x instead of OpenBabel 2.x
* OpenBabelReader - convert positions/trajectory; this class will work alongside the OpenBabelParser to create a Universe from an OBMol
* Tests for OpenBabelReader
* Documentation with ReadTheDocs (including examples) for OpenBabelParser and OpenBabelReader.
* Develop further tests with different file/molecule types for OpenBabelParser and OpenBabelReader.

# Working on
* OpenBabel converter to work in the reverse direction - including tests and documentation.
* Documentation with ReadTheDocs (including examples) for OpenBabelConverter.

# Next Steps
* Cut a release and deploy on conda-forge.
* Clean up missing attributes (see earlier blog posts and Issues on GitHub).
