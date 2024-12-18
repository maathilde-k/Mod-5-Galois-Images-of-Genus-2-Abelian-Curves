# Computing Mod-5 Galois Images of Torsion on Abelian Surfaces

This repository contains code for computing the mod-5 image of the Galois Representation of torsion for the Jacobian of a genus 2 hyperelliptic curve.
The algorithm is described in the paper "Computing Mod-5 Galois Images of Torsion on Abelian Surfaces" by Andy Zhu, Mathilde Kermorgant, and Aidan Hennessey.
All code provided is written in Magma.
Note that the primary implementation relies on Andrew Sutherland's [Smalljac](https://math.mit.edu/~drew/smalljac.html) and this may require separate configuration.
An alternative (but much slower) method is provided which does require Smalljac.
To be consistent with the labeling in LMFDB, we use the same subgroup lattice. This is constructed in the file GSp.m, which was written by Andrew Sutherland.

The primary algorithm is contained in imager.m, while other computational results referenced in our paper have code to verify located in paper-lemmas.

## Acknowledgements

We are grateful to Isabel Vogt and Sachi Hashimoto for their guidance and support throughout this project.
