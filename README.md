# HPCG
run HPL ref:https://www.cnblogs.com/zhyantao/p/10614238.html
	cd /home/liux7/HPCG/hpl-2.3/bin/Linux_PII_CBLAS
	mpirun -np 4 ./xhpl > HPLresult.txt

run HPCG ref:https://www.cnblogs.com/lijiaji/p/14283958.html
	cd /home/liux7/HPCG/hpcg/setup/build/bin
	mpirun -np 8 ./xhpcg > HPCGresult.txt

