## Protein antibody interface design_platform

This notebook describes an interface design experiment where we will analyse 3D crystal structures of SAR-COV2 spike protein bound with ACE2 enzyme (pdb - 6m0j) and antibody P5A-3CD, rescpectively. We will design an experiment where we will try to mentain or imporve the binding affinity of Spike protein with ACE2 enzyme while abrogating binding with P5A-3C8 antibody. We will analyse the interfaces in these two crystal structures and find out the key amino acid residues at the interfaces that are involved in non-covalent interaction in these two structures. We will then query PDBE (www.pdbe.og) and Uniprot (www.uniprot.org) databases to find out available information about those residues. We will analyse the information available from 3D structures and protein databases, and use these information to create a platform where we can perform an interface design experiment.

This notebook divides in three part. First part of this notebook deals with the analysis of the interfacee, second part shows an in-silico mutagenesis platform and thrid part is an evaluation platform. To run this notebook, we need nglview (for visualisation), pymol (for in-slico mutagenesis), prodigy (A tool from Bonvon lab to calculate binding affinity) and openmm (Open source tool for molecular dynamics). Two conda environments are needed to run this notebook because of conflict in dependencies between Pymol and Prodigy package. I have used an open source Pymol library, which I believe causing the dependency issue. I beleieve using the proprietary python library from Schrodinger will solve this problem.

# Steps for the design platform
- Step -1: Analysis of the protein protein interface
○ Visual analysis of the interface
○ Querying PDBe database to gather information of interface in a PDB entry
○ Querying Uniprot database to identify the key functional residues present at the interface
- Step -2: Mutation platform
○ Perform point mutation one by one on each of those key residues that have information about mutagenesis
○ Another approach will be to mutate all residues that are present in the interface
- Step - 3: Evaluation - Binding affinity prediction and MD simulation
○ Predict or calculate Binding affinity of all the mutated structures
○ Finally we can perform MD simulation and/or docking studies on specific (high scored) structures to model the structural changes in a reliable way





