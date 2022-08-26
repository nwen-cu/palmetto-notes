# 1. Load MPI and OpenMP Module
```sh
module load mpich/3.3.2-gcc/8.3.1-cuda10_2
module load openmpi/4.0.5-gcc/8.4.1-ucx
module load mumps/5.3.3-gcc/8.3.1-mpi-double-cuda10_2
```

# 2. Pull Source Code of Elmer FEM
``````sh
cd buildspace/
git clone https://github.com/ElmerCSC/elmerfem.git
cd elmerfem/
``````

# 3. Prepare Build Source

``````sh
cmake -S. -B~/buildspace/elmerbuild -DWITH_OpenMP:BOOLEAN=TRUE -DWITH_MPI:BOOLEAN=TRUE -DWITH_Mumps:BOOLEAN=TRUE
``````

# 4. Build Libraries

``````
cd ../elmerbuild
make 
``````

