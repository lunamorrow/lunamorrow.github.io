# Adjustments

While I officially started GSoC a couple weeks ago, I have only just finished my exams for this university semester. I am really keen to sink my teeth into this project and start putting in the hours now. I have had two meetings so far with my three mentors, Hugo, Cedric and Xu Hong. We have made some adjustments both to how this project will work and what the end result will be. The OpenBabel Converter will now be a MDAKit which we hope to integrate into the main code base in the future. There has been some adjustments to the three classes, where the OpenBabelReader will read trajectory positions, to make a Universe alongside the OpenBabelParser which will read atoms. 
The converter will still function as originally proposed to convert a Universe to an OpenBabel OBMol. I will be reaching out to any remaining active OpenBabel maintainers shortly too, for input into this project. Additionally, I have been granted a 22 week extension for this project while I balance university and work commitments.


# Next Steps

I will be commencing on the the OpenBabelParser this week and develop it concurrently with tests. This will be followed by the OpenBabelReader, and finally the OpenBabelConverter.

Priorities for the OpenBabelParser:
* Obtain all relevant attributes from atoms in OBMols
* Convert these attributes to their relevant MDAnalysis Atom attribute, taking care with units
* Maintain bond integrity to ensure Atoms are placed in appropriate AtomGroups, Residues and Segments
* Develop unit testing for standard cases
* Ensure robustness to OBMol atoms with different features, as OpenBabel supports formats that do not contain critical information like explicit hydrogens.
