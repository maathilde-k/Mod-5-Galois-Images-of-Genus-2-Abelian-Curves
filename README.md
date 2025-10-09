# Computing mod-5 Galois images of torsion on abelian surfaces

This repository contains code for computing the mod-5 image of the Galois Representation of torsion for the Jacobian of a genus 2 hyperelliptic curve.
The algorithm is described in the paper "Computing mod-5 Galois images of torsion on abelian surfaces" by Andy Zhu, Mathilde Kermorgant, and Aidan Hennessey.
All code provided is written in Magma.
Note that the primary implementation relies on Andrew Sutherland's [Smalljac](https://math.mit.edu/~drew/smalljac.html) and this may require separate configuration.
To be consistent with the labeling in LMFDB, we use the same subgroup lattice. This is constructed in the file GSp.m, which was written by Andrew Sutherland.

The primary algorithm is contained in imager.m, while other computational results referenced in our paper have code to verify located in paper-lemmas.

## Running the code

To run a particular curve, use the following block:
```magma
Attach("Imager.magma");
// create the dictionary
dict := InvariantDictionary(L);

// LMFDB curve 431250.a.431250.1
R<x> := PolynomialRing(Rationals());
C := HyperellipticCurve(R![-1, 5, 1, -5, 0, 1], R![0, 1]);

// Use the imaging function
ImageByFroblist(L, dict, C);
```

## Preprint

The preprint can be found on arXiv: https://arxiv.org/abs/2510.06423

## Acknowledgements

We are grateful to Isabel Vogt and Sachi Hashimoto for their guidance and support throughout this project.
