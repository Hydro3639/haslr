# HASLR: fast hybrid assembly of long reads

HASLR is a tool for rapid genome assembly of long sequencing reads. HASLR is a hybrid tool which means it requires long reads generated by Third Generation Sequencing technologies (such as PacBio or Oxford Nanopore) together with Next Generation Sequencing reads (such as Illumina) from the same sample. HASLR is capable of assembling large genomes on a single computing node. Our experiments show that it can assemble a CHM1 human dataset in less than 10 hours using 64 CPU threads.

## Installation

### Requirements
- GCC ≥ 4.8.5
- zlib

### Building from source
```
git clone https://github.com/vpc-ccg/haslr.git
cd haslr
make
```

### Dependencies
HASLR depends on the following tools which will be installed automatically:
- [SPOA](https://github.com/rvaser/spoa) - For consensus calling of long reads
- [Minia](https://github.com/GATB/minia) - For assembling short reads
- [minimap2](https://github.com/lh3/minimap2) - For aligning short read contigs onto long reads
- [fastutils](https://github.com/haghshenas/fastutils) - For FASTA/Q manipulation

## Bugs
Please report the bugs through HASLR's issue tracker at [https://github.com/vpc-ccg/haslr/issues](https://github.com/vpc-ccg/haslr/issues).

## Copyright and License
This software is released under GNU General Public License (v3.0)
- SPOA is released under MIT license
- Minia is released under AGPL license 
- minimap2 is released under MIT license
- fastutils is released under GPL license 

## Author
[Ehsan Haghshenas](https://github.com/haghshenas) (ehaghshe AT sfu DOT ca)
