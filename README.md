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

Might be nice to have inspectors/logging tools for investigating ndarrays.  Maybe have some options for bounds checking that can be turned on.

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

* Dense version is kind of easy

* Sparse is pretty hard, could try to port some native code with emscripten

### Iterative solvers (sparse and dense)

* Mainly useful with sparse matrices, already have some arly work

### Linear least squares

* Again, pretty straightforward.  Same concept as above

### Condition number

### Eigendecomposition (sparse and dense)

* Sparse stuff should be done with Lanczos algorithm/arnoldi method

### SVD (sparse and dense)

* Dense somewhat easy

* Sparse requires hard work

### Psuedoinverse

* Should be easy given svd, maybe don't even need separate module

### Matrix logarithms and exponents

* Maybe not necessary to use ndarrays here

### Other factorizations

* Cholesky
* LU
* etc.

### Ports of native solvers?

Possibly using emscripten

# Optimization

## Convex

### Linear programming solver

* Must have, could probably implement a couple of different algorithms

### Quadratic programming solver

* Also must have.  The current quadprog on npm works, but is a kind of crappy port of some R code and is very slow.  A better version is clearly needed.

### Network flow

* Could try out a couple of methods, bfs, push-relabel, etc.

### Minimum cut

* Side effect of network flow

## Nonconvex

### Bindings to native libraries

* CPLEX
* CERES
* UMFPACK
* ..?

### BFGS

### Nelder-Mead

### Quasi-Newton


# Graphics

### ndarray optimized isosurface extractor

Can use dual contouring/surface nets.  Should work for arbitrary dimensions.  This is already mostly there, but will take a bit more work to get it to work on general ndarrays.  Would also be nice to exploit sparsity when possible.

### Better volume rendering tools

Have raymarch, but it needs a lot more work.  Should also try to figure out how to make this more modular.

### Curve/surface rasterization

Basically a dimension independent voxelize

## Plotting

Maybe connect with d3.js somehow?

### Curve plots

### Contour plots

### Headless/node only plotting

* Maybe pipe plots to streams or render to ndarrays?

# Data formats and interoperability

### Extend save-pixels and read-pixels to support more file formats

### MATLAB interoperability

### SciPy interoperability

### CSV

### Voxel formats

* Minecraft schematics
* ...?

# Your project here
