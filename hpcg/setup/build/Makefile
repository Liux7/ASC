# -*- Makefile -*-

arch = Linux_MPI
setup_file = setup/Make.$(arch)

include $(setup_file)


HPCG_DEPS = src/CG.o \
	    src/CG_ref.o \
	    src/TestCG.o \
	    src/ComputeResidual.o \
	    src/ExchangeHalo.o \
	    src/GenerateGeometry.o \
	    src/GenerateProblem.o \
	    src/GenerateProblem_ref.o \
	    src/CheckProblem.o \
	    src/MixedBaseCounter.o \
	    src/OptimizeProblem.o \
	    src/ReadHpcgDat.o \
	    src/ReportResults.o \
	    src/SetupHalo.o \
	    src/SetupHalo_ref.o \
	    src/TestSymmetry.o \
	    src/TestNorms.o \
	    src/WriteProblem.o \
	    src/YAML_Doc.o \
	    src/YAML_Element.o \
	    src/ComputeDotProduct.o \
	    src/ComputeDotProduct_ref.o \
	    src/mytimer.o \
	    src/ComputeOptimalShapeXYZ.o \
	    src/ComputeSPMV.o \
	    src/ComputeSPMV_ref.o \
	    src/ComputeSYMGS.o \
	    src/ComputeSYMGS_ref.o \
	    src/ComputeWAXPBY.o \
	    src/ComputeWAXPBY_ref.o \
	    src/ComputeMG_ref.o \
	    src/ComputeMG.o \
	    src/ComputeProlongation_ref.o \
	    src/ComputeRestriction_ref.o \
	    src/CheckAspectRatio.o \
	    src/OutputFile.o \
	    src/GenerateCoarseProblem.o \
	    src/init.o \
	    src/finalize.o

# These header files are included in many source files, so we recompile every file if one or more of these header is modified.
PRIMARY_HEADERS = /home/liux7/HPCG/hpcg/src/Geometry.hpp /home/liux7/HPCG/hpcg/src/SparseMatrix.hpp /home/liux7/HPCG/hpcg/src/Vector.hpp /home/liux7/HPCG/hpcg/src/CGData.hpp \
                  /home/liux7/HPCG/hpcg/src/MGData.hpp /home/liux7/HPCG/hpcg/src/hpcg.hpp

all: bin/xhpcg

bin/xhpcg: src/main.o $(HPCG_DEPS)
	$(LINKER) $(LINKFLAGS) src/main.o $(HPCG_DEPS) $(HPCG_LIBS) -o bin/xhpcg

clean:
	rm -f src/*.o bin/xhpcg

.PHONY: all clean

src/main.o: /home/liux7/HPCG/hpcg/src/main.cpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/home/liux7/HPCG/hpcg/src $< -o $@

src/CG.o: /home/liux7/HPCG/hpcg/src/CG.cpp /home/liux7/HPCG/hpcg/src/CG.hpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/home/liux7/HPCG/hpcg/src $< -o $@

src/CG_ref.o: /home/liux7/HPCG/hpcg/src/CG_ref.cpp /home/liux7/HPCG/hpcg/src/CG_ref.hpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/home/liux7/HPCG/hpcg/src $< -o $@

src/TestCG.o: /home/liux7/HPCG/hpcg/src/TestCG.cpp /home/liux7/HPCG/hpcg/src/TestCG.hpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/home/liux7/HPCG/hpcg/src $< -o $@

src/ComputeResidual.o: /home/liux7/HPCG/hpcg/src/ComputeResidual.cpp /home/liux7/HPCG/hpcg/src/ComputeResidual.hpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/home/liux7/HPCG/hpcg/src $< -o $@

src/ExchangeHalo.o: /home/liux7/HPCG/hpcg/src/ExchangeHalo.cpp /home/liux7/HPCG/hpcg/src/ExchangeHalo.hpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/home/liux7/HPCG/hpcg/src $< -o $@

src/GenerateGeometry.o: /home/liux7/HPCG/hpcg/src/GenerateGeometry.cpp /home/liux7/HPCG/hpcg/src/GenerateGeometry.hpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/home/liux7/HPCG/hpcg/src $< -o $@

src/GenerateProblem.o: /home/liux7/HPCG/hpcg/src/GenerateProblem.cpp /home/liux7/HPCG/hpcg/src/GenerateProblem.hpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/home/liux7/HPCG/hpcg/src $< -o $@

src/GenerateProblem_ref.o: /home/liux7/HPCG/hpcg/src/GenerateProblem_ref.cpp /home/liux7/HPCG/hpcg/src/GenerateProblem_ref.hpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/home/liux7/HPCG/hpcg/src $< -o $@

src/CheckProblem.o: /home/liux7/HPCG/hpcg/src/CheckProblem.cpp /home/liux7/HPCG/hpcg/src/CheckProblem.hpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/home/liux7/HPCG/hpcg/src $< -o $@

src/MixedBaseCounter.o: /home/liux7/HPCG/hpcg/src/MixedBaseCounter.cpp /home/liux7/HPCG/hpcg/src/MixedBaseCounter.hpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/home/liux7/HPCG/hpcg/src $< -o $@

src/OptimizeProblem.o: /home/liux7/HPCG/hpcg/src/OptimizeProblem.cpp /home/liux7/HPCG/hpcg/src/OptimizeProblem.hpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/home/liux7/HPCG/hpcg/src $< -o $@

src/ReadHpcgDat.o: /home/liux7/HPCG/hpcg/src/ReadHpcgDat.cpp /home/liux7/HPCG/hpcg/src/ReadHpcgDat.hpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/home/liux7/HPCG/hpcg/src $< -o $@

src/ReportResults.o: /home/liux7/HPCG/hpcg/src/ReportResults.cpp /home/liux7/HPCG/hpcg/src/ReportResults.hpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/home/liux7/HPCG/hpcg/src $< -o $@

src/SetupHalo.o: /home/liux7/HPCG/hpcg/src/SetupHalo.cpp /home/liux7/HPCG/hpcg/src/SetupHalo.hpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/home/liux7/HPCG/hpcg/src $< -o $@

src/SetupHalo_ref.o: /home/liux7/HPCG/hpcg/src/SetupHalo_ref.cpp /home/liux7/HPCG/hpcg/src/SetupHalo_ref.hpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/home/liux7/HPCG/hpcg/src $< -o $@

src/TestSymmetry.o: /home/liux7/HPCG/hpcg/src/TestSymmetry.cpp /home/liux7/HPCG/hpcg/src/TestSymmetry.hpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/home/liux7/HPCG/hpcg/src $< -o $@

src/TestNorms.o: /home/liux7/HPCG/hpcg/src/TestNorms.cpp /home/liux7/HPCG/hpcg/src/TestNorms.hpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/home/liux7/HPCG/hpcg/src $< -o $@

src/WriteProblem.o: /home/liux7/HPCG/hpcg/src/WriteProblem.cpp /home/liux7/HPCG/hpcg/src/WriteProblem.hpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/home/liux7/HPCG/hpcg/src $< -o $@

src/YAML_Doc.o: /home/liux7/HPCG/hpcg/src/YAML_Doc.cpp /home/liux7/HPCG/hpcg/src/YAML_Doc.hpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/home/liux7/HPCG/hpcg/src $< -o $@

src/YAML_Element.o: /home/liux7/HPCG/hpcg/src/YAML_Element.cpp /home/liux7/HPCG/hpcg/src/YAML_Element.hpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/home/liux7/HPCG/hpcg/src $< -o $@

src/ComputeDotProduct.o: /home/liux7/HPCG/hpcg/src/ComputeDotProduct.cpp /home/liux7/HPCG/hpcg/src/ComputeDotProduct.hpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/home/liux7/HPCG/hpcg/src $< -o $@

src/ComputeDotProduct_ref.o: /home/liux7/HPCG/hpcg/src/ComputeDotProduct_ref.cpp /home/liux7/HPCG/hpcg/src/ComputeDotProduct_ref.hpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/home/liux7/HPCG/hpcg/src $< -o $@

src/finalize.o: /home/liux7/HPCG/hpcg/src/finalize.cpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/home/liux7/HPCG/hpcg/src $< -o $@

src/init.o: /home/liux7/HPCG/hpcg/src/init.cpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/home/liux7/HPCG/hpcg/src $< -o $@

src/mytimer.o: /home/liux7/HPCG/hpcg/src/mytimer.cpp /home/liux7/HPCG/hpcg/src/mytimer.hpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/home/liux7/HPCG/hpcg/src $< -o $@

src/ComputeOptimalShapeXYZ.o: /home/liux7/HPCG/hpcg/src/ComputeOptimalShapeXYZ.cpp /home/liux7/HPCG/hpcg/src/ComputeOptimalShapeXYZ.hpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/home/liux7/HPCG/hpcg/src $< -o $@

src/ComputeSPMV.o: /home/liux7/HPCG/hpcg/src/ComputeSPMV.cpp /home/liux7/HPCG/hpcg/src/ComputeSPMV.hpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/home/liux7/HPCG/hpcg/src $< -o $@

src/ComputeSPMV_ref.o: /home/liux7/HPCG/hpcg/src/ComputeSPMV_ref.cpp /home/liux7/HPCG/hpcg/src/ComputeSPMV_ref.hpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/home/liux7/HPCG/hpcg/src $< -o $@

src/ComputeSYMGS.o: /home/liux7/HPCG/hpcg/src/ComputeSYMGS.cpp /home/liux7/HPCG/hpcg/src/ComputeSYMGS.hpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/home/liux7/HPCG/hpcg/src $< -o $@

src/ComputeSYMGS_ref.o: /home/liux7/HPCG/hpcg/src/ComputeSYMGS_ref.cpp /home/liux7/HPCG/hpcg/src/ComputeSYMGS_ref.hpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/home/liux7/HPCG/hpcg/src $< -o $@

src/ComputeWAXPBY.o: /home/liux7/HPCG/hpcg/src/ComputeWAXPBY.cpp /home/liux7/HPCG/hpcg/src/ComputeWAXPBY.hpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/home/liux7/HPCG/hpcg/src $< -o $@

src/ComputeWAXPBY_ref.o: /home/liux7/HPCG/hpcg/src/ComputeWAXPBY_ref.cpp /home/liux7/HPCG/hpcg/src/ComputeWAXPBY_ref.hpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/home/liux7/HPCG/hpcg/src $< -o $@

src/ComputeMG_ref.o: /home/liux7/HPCG/hpcg/src/ComputeMG_ref.cpp /home/liux7/HPCG/hpcg/src/ComputeMG_ref.hpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/home/liux7/HPCG/hpcg/src $< -o $@

src/ComputeMG.o: /home/liux7/HPCG/hpcg/src/ComputeMG.cpp /home/liux7/HPCG/hpcg/src/ComputeMG.hpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/home/liux7/HPCG/hpcg/src $< -o $@

src/ComputeProlongation_ref.o: /home/liux7/HPCG/hpcg/src/ComputeProlongation_ref.cpp /home/liux7/HPCG/hpcg/src/ComputeProlongation_ref.hpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/home/liux7/HPCG/hpcg/src $< -o $@

src/ComputeRestriction_ref.o: /home/liux7/HPCG/hpcg/src/ComputeRestriction_ref.cpp /home/liux7/HPCG/hpcg/src/ComputeRestriction_ref.hpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/home/liux7/HPCG/hpcg/src $< -o $@

src/GenerateCoarseProblem.o: /home/liux7/HPCG/hpcg/src/GenerateCoarseProblem.cpp /home/liux7/HPCG/hpcg/src/GenerateCoarseProblem.hpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/home/liux7/HPCG/hpcg/src $< -o $@

src/CheckAspectRatio.o: /home/liux7/HPCG/hpcg/src/CheckAspectRatio.cpp /home/liux7/HPCG/hpcg/src/CheckAspectRatio.hpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/home/liux7/HPCG/hpcg/src $< -o $@

src/OutputFile.o: /home/liux7/HPCG/hpcg/src/OutputFile.cpp /home/liux7/HPCG/hpcg/src/OutputFile.hpp $(PRIMARY_HEADERS)
	$(CXX) -c $(CXXFLAGS) -I/home/liux7/HPCG/hpcg/src $< -o $@

