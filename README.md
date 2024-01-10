# How (<em>not</em>) to hash into class groups of imaginary quadratic fields?

This repository contains the open-source code of the following pre-print paper:

Title: How (<em>not</em>) to hash into class groups of imaginary quadratic fields?

Currently available at the following links:
* IACR [eprint link](https://eprint.iacr.org/2024/034.pdf).
* Researchgate [link](https://www.researchgate.net/publication/377241277_How_not_to_hash_into_class_groups_of_imaginary_quadratic_fields).

 The Python3 code investigates two main questions:
* How (<em>not</em>) to hash into class groups of imaginary quadratic fields?
* How to hash into class groups of imaginary quadratic fields?

  It mostly contains a Jupyter Notebook with the following measurements, illustrations, and visualizations.

## Insecure hash-to-class group functions

### SageMath's random form solution
We show that selecting a random binary quadratic form and reducing it in a certain interval results in a codomain with a skewed, power-law distribution. We also show, that if a VDF was deployed with this hash function, then the deployment would be completely insecure.
### Uniformly random b
It might be tempting to sample a uniformly random coefficient "b" and then choose the coefficient "a" of the reduced form accordingly. We show that the distribution of coefficient "b" is not uniform. Hence, this strategy cannot yield a uniform codomain in a class group.
## Secure hash-to-class group functions
We propose and implement two families of hash functions with a class group codomain.
### CSIDH hash
This hash function is reminiscent of the key generation algorithm of CSIDH. The main idea is that one precomputes a set of generating ideals with small prime norms and then composes these ideals according to another hash function output. 
### Wesolowski hash
Wesolowski's original construction samples a uniformly random prime and generates a corresponding "b" coefficient. This function has two major downsides: 1) it must generate large primes, and 2) it is not surjective. We propose an extension to this function that deals with these issues.
