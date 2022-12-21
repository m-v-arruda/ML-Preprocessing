# ML-Preprocessing

The development of data preprocessing is based on the work of Chandrasekaran et al. (2019). The authors introduce a machine-learning-based scheme to predict the electronic structure of a material or a molecule, given just its atomic configuration (Chandrasekaran et al., 2019). Therefore the work here described is reproduction work.

The input used in the model is from VASP, specifically CHGCAR file, so first we need to pre-process the CHGCAR file. The preprocessing is a process of preparing the raw data and making it suitable for a machine learning model. It is the first and crucial step while creating a machine learning model, because it is not always the case that we come across clean and formatted data. So, it is mandatory to clean it and put it in a formatted way.

The CHGCAR file stores the charge density and the Projector-Augmented-Wave (PAW) one-center occupancies and can be used for restarting VASP calculations. This file consists of the following blocks: structure, charge density and augmentation occupancies. For the script that is in development the CHGCAR is interpreted as a .txt file. The script reads the document line by line as follows: First Line (Universal Lattice Scaling Factor), Lattice Vectors, Elements and Number of Atoms, Direct (Atoms Positions) and the Electronic Density Dimensions and Electronic Density 3D Matrix.
