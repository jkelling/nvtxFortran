# NVTX Wrapper module for Fortran

## Original Source and Changes

* This is the nvtx interface fortram module from an [NVIDA devblog
post](https://developer.nvidia.com/blog/customize-cuda-fortran-profiling-nvtx/).
* The original is non-compliant. A more compliant version was linked in a
[comment](https://gist.github.com/dappelha/ca99a3134ed93991158d73e7a64b207c).
* This version modifies the code again to remove direct use of "BOZ literals" in
  an array constructor, which is apparently invalid, too.
