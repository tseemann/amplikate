[![Build Status](https://travis-ci.org/tseemann/amplikate.svg?branch=master)](https://travis-ci.org/tseemann/amplikate)
[![License: GPL v3](https://img.shields.io/badge/License-GPL%20v3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
![Don't judge me](https://img.shields.io/badge/Language-Perl_5-steelblue.svg)

:warning: This software is still in early development

# amplikate
Generic typing tool from amplicons and/or in silico PCR

## Introduction
There are numerous genotyping systems for microbes,
but they all have something in common: 
they identify small pieces of genome sequence that
are useful in some way, and use combinations of these
sequences to assign a "type", usually a single number.
The classic example of this being 
[MLST](https://en.wikipedia.org/wiki/Multilocus_sequence_typing).

Traditionally in the wet lab these sequences would
be determined by using PCR primers followed by Sanger
capillary sequencing. In the new world of WGS, we have
sequence reads (FASTQ) or assembled contigs (FASTA). 
With contigs, we can either use _in silico_ PCR, or
identify the amplicon directly, with BLAST for example.

Once we have identified all relevant amplicons,
the amplicon (allele) combinations are converted into
a genotype using a "profile table" like this:
```
TYPE AMP_1 AMP_2 AMP_3
1    1     1     1
2    2     1     1
3    3     1     2
...
324 23   178    76
```

## Quick Start

```
% amplikate --version
amplikate 0.1.2

```

## Installation

### Conda
Install [Conda](https://conda.io/docs/) or [Miniconda](https://conda.io/miniconda.html):
```
conda install -c conda-forge -c bioconda -c defaults amplikate # COMING SOON
```

### Homebrew
Install [HomeBrew](http://brew.sh/) (Mac OS X) or [LinuxBrew](http://linuxbrew.sh/) (Linux).
```
brew install brewsci/bio/amplikate # COMING SOON
```

### Source
This will install the latest version direct from Github.
You'll need to add the amplikate `bin` directory to your `$PATH`,
and also ensure all the [dependencies](#Dependencies) are installed.
```
cd $HOME
git clone https://github.com/tseemann/amplikate.git
$HOME/amplikate/bin/amplikate --help
```

## Dependencies

* `perl` >= 5.26

## License

amplikate is free software, released under the
[GPL 3.0](https://raw.githubusercontent.com/tseemann/amplikate/master/LICENSE).

## Issues

Please submit suggestions and bug reports to the
[Issue Tracker](https://github.com/tseemann/amplikate/issues)

## Author

[Torsten Seemann](https://twitter.com/torstenseemann)
