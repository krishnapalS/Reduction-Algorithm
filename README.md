# GPU Sum Reduction

An attempt at an optimized GPU sum reduction.
## Sum Reduction Algorithm : [NVIDIA doc](http://developer.download.nvidia.com/compute/cuda/1.1-Beta/x86_website/projects/reduction/doc/reduction.pdf).

## Concept
Parallel reduction algorithm typically refers to an algorithm which combines an array of elements, producing a single result. Typical problems that fall into this category are:

- summing up all elements in an array
- finding a maximum in an array

## Main Strategies
- Process as much data as possible (without affecting algorithm correctness) in shared memory.
- Use sequential addressing to get rid of bank conflicts, both on global-to-shared memory data load, and processing the shared memory data.

