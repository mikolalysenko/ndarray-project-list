ndarray-project-list
====================
This is a high level list of projects involving ndarrays that still need to get done organized by topics


# Core functionality

### Better sparse array support

Already kind of possible using ndarray-hash and ndarray-segment, but we need more sparse formats and better routines for working with them and converting between them

### RLE support for cwise

cwise should be able to exploit run length encoded and sparse matrices.  This is very important for voxel.js

### Tensor algebra compiler

Similar to cwise, would be nice if we could use code generation to get fast generic tensor operations on ndarrays.  This would let us generate modules for arbitrary expressions in Einstein summation and possibly other situations

### High level macro language?

A common pattern with ndarrays is to use lazy just-in-time code generation that generates an optimized routine based on pattern matching types.  It would be nice if we could encode this somehow into JavaScript using some sort of meta language/module so that it would be easier to explain and modify these sorts of routines.  More work would be necessary to figure out how this could be done though

### Debugging tools


# Linear algebra tools

Currently little progress in this area so far.  If someone wants to take up the banner and lead onward, here is a list of projects:

### Matrix-vector multiply

* Should take into account striding, use JIT code generation

* Sparse products should be blazing fast, need to figure out the best solution for how to handle this.

### Matrix-matrix product

* Same deal as above.  For tricky non-aligned case use divide-and-conquer.

* Question:  Is Strassen-type iteration worth it?

* Question:  Should sparse matrix products be supported?

### Matrix inverse


### Solvers (sparse and dense)

### Linear least squares

### Condition number

### Eigendecomposition (sparse and dense)

* Sparse stuff should be done with Lanczos algorithm/arnoldi method

### SVD (sparse and dense)

### Psuedoinverse

### Matrix logarithms and exponents

* Maybe not necessary to use ndarrays here

### Other factorizations

* Cholesky
* LU
* etc.

### Ports of native solvers?

Possibly using emscripten


# Graphics

### ndarray optimized isosurface extractor

Can use dual contouring/surface nets.  Should work for arbitrary dimensions

### Better volume rendering tools

### Curve/surface rasterization

Basically a dimension independent voxelize

## Plotting

Maybe connect with d3.js somehow?

### Curve plots

### Contour plots

### Headless/node only plotting


# Data formats and interoperability

### Extend save-pixels and read-pixels to support more file formats

### MATLAB interoperability

### SciPy interoperability

### CSV

### Voxel formats

* Minecraft schematics
* ...?

# Your project here
