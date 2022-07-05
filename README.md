# ICMApp
The Python files needed to post-process the ICMA simulations for interfacial thermal transport analysis.

The ICMA method is one of the computational methods in the field of nanoscale thermal transport to study the heat transfer across solid-solid interfaces. 

This repository provides a source to the post-processing files that might be needed to analyze the finished simulations.

Things to possibly talk about:
ICMA simulations and what each folder will contain at the end of the simulation: force.txt, velocity.txt
Using these force and velocity files, Q.txt files will be generated for total G analysis.
If modal analysis is needed Qn.txt is generated, which includes the heat flow as a function of simulation time for all the modes in the system.
The Qn.txt file will be post-processed to give us the cordata.txt, which include the correlation data for all the vibrational modes in the system.
the process will be repeated for different ensembles, and they will be stored in different folders (v1, v2, ...) at each temperature.
The ICMApp package will be utilized at this stage to give the temperature dependent modal contributions and conductance values following the below two main steps:
1. Due to the large file sizes for cordata.txt, it will be first splitted into smaller files...
2. The actual post-processing step using ICMApp will be applied to the correlation splitted files to give the modal contributions and temperature-dependent interfacial conductance values.
