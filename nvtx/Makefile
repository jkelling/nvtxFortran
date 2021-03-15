all: nvtx.mod libnvtx.a libnvtx.so
	@echo 'Append to CMAKE flags: CMAKE_Fortran_FLAGS="-I$(shell pwd)" CMAKE_EXE_LINKER_FLAGS="-L${CUDA_ROOT}/targets/x86_64-linux/lib -lnvToolsExt -L$(shell pwd ) -lnvtx"'
	@echo 'At runtime: export LD_LIBRARY_PATH=$$LD_LIBRARY_PATH:$(shell pwd)'

%.mod: %.F90
	${FC} -c $< -fPIC

lib%.a: %.o
	ar cr $@ $^

lib%.so: %.o
	${FC} -o $@ -shared $^
