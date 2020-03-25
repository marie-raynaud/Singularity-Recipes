## HotRec Project Containers

###  1.1 Create a Singularity container `Base_msprime.sif` in Singularity Image Format (SIF) as root: 

`sudo singularity build Base_msprime.sif Base_msprime_Recipe-v0.1.2.def`

*Contains:* `R-v3.5.3`, `snakemake-v5.10.0`, `python-v3.7.4`, `msprime-v0.7.4`, `tskit-v0.2.3`, and other packages 



###  1.2 Create a writable Singularity container `Simul_LDhelmet.sif` as root from the existing container `Base_msprime.sif` in Singularity Image Format (SIF) 

`sudo singularity build --writable Simul_LDhelmet.sif LDhelmet_Singularity_Recipe.def`


