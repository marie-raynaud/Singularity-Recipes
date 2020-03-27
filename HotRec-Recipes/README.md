## HotRec Project Containers

###  1. Create a Singularity container `Base_msprime.sif` in Singularity Image Format (SIF) as root: 

`sudo singularity build Base_msprime.sif Base_msprime_Recipe-v0.1.2.def`

*Contains:* `R-v3.5.3`, `snakemake-v5.10.0`, `python-v3.7.4`, `msprime-v0.7.4`, `tskit-v0.2.3`, and other packages 



###  2. Create a Singularity container `Simul_LDhelmet.sif` as root from the existing container `Base_msprime.sif` in Singularity Image Format (SIF): 

`sudo singularity build Simul_LDhelmet.sif LDhelmet_simulations_Recipe-v0.1.2.def`


###  3. Run the Singularity container `Simul_LDhelmet.sif` as root to perform simulations: 

`sudo singularity run -B /path-to-dir/REPLICATE_RUN_i:/RUN -B /path-to-dir/RUN_LD:/home/RUN_LD -B /path-to-dir/TMP_OUT:/home/ldhelmet/LDhelmet_v1.10/output Simul_LDhelmet.sif /home/RUN_LD/run_ld_12_conditions.sh`
