# HPCG
run HPL
cd /home/liux7/HPCG/hpl-2.3/bin
mpirun -np 4 ./xhpl > HPLresult.txt

run HPCG
cd /home/liux7/HPCG/hpcg/setup/build/bin
mpirun -np 8 ./xhpcg > HPCGresult.txt

