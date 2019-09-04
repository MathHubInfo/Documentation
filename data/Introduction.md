# Introduction

Sources:
* [OpenDreamKit D6.10](https://github.com/OpenDreamKit/OpenDreamKit/blob/master/WP6/D6.10/report-final.pdf)

## Goals

* Increased productivity for mathematicians by allowing them to focus on the mathematical datasets 
themselves while leaving issues of encoding, management, and search to dedicated systems.
* Improved reliability of published results as the research community can more easily scrutinize the underlying data.
* Collaborations via shared datasets that are currently prohibitively expensive due to the difficulty of 
understanding other researchers’ data, including collaborations across disciplines and with industry practitioners, 
who are currently excluded due to the difficulty of understanding the datasets.
* Reward mathematicians for sharing datasets (which is currently often not the case), e.g., 
by making datasets citable and their reuse known.
* More sustainable research by guaranteeing that datasets can be archived and their meaning understood in perpetuity 
(which is essential especially in mathematics).

## FAIR Data in Mathematics

There are (at least) two aspects of FAIRness that are particularly important 
for mathematical data and are not strongly stressed in the original principles. 
The first one of these is that the data need to be semantics aware. 
Computer applications and mathematically sound, interoperable services can only work 
if the mathematical meaning of the data is FAIR in all its depth. We call this "deep FAIR".

Due to the mathematical standard of rigor and the inherent complexity of mathematical data, 
deep FAIRness is both more difficult and more important for mathematics than for other scientific disciplines. 
That also means that mathematics is an ideal test case for developing the semantic aspects of the FAIR principles in general.

The second one is that the relevant principles need to apply to every datum. 
The importance of this requirement, particularly for identifiers (Findable), 
has already been pointed out in [BT](https://sites.math.washington.edu/~billey/papers/fingerprints.pdf). 
For example, while it is good that a catalogue of graphs has a globally unique and persistent identifier, 
but it is much better if in addition to that, every graph in the catalogue also has one. 
This also extends to other FAIR principles.
