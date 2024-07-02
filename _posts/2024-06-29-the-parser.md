---
title: Deep in the Parser
---

# Deep in the Parser

# Current Work

As discussed in my previous blog post, I am now working on developing the OpenBabelParser concurrently with its tests. I have had some issues with pytest not working, but was able to overcome this with some assistance from Hugo and Cedric. 

Unfortunately, OpenBabel doesn't seem to support a handful of the attributes taken when creating an MDAnalysis Atom, including:  altlocs, occupancies and tempfactors. I am still actively searching for this attributes, especially considering that OpenBabel accepts PDB files. I will be including this as a question when I write to the active OpenBabel maintainers (yet to be done). 
I am behind where I would like to be at this point in the project, as my personal life has been quite busy. However, I have settled and come into a quieter period finally, so I am keen to get more work done on this converter.

# What is done
* Obtain all relevant attributes from atoms in OBMols

# Working on
* Develop unit testing for standard and edge cases
* Convert these attributes to their relevant MDAnalysis Atom attribute, taking care with units

# Next Steps
* Maintain bond integrity to ensure Atoms are placed in appropriate AtomGroups, Residues and Segments
* Ensure robustness to OBMol atoms with different features, as OpenBabel supports formats that do not contain critical information like explicit hydrogens.
