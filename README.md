<img src="multiqc/templates/default/assets/img/MultiQC_logo.png" width="300" title="MultiQC">

### Aggregate bioinformatics results across many samples into a single report.

##### Find [documentation](http://multiqc.info/docs/0.2/README.md) and [example reports](http://multiqc.info/examples/rna-seq/multiqc_report.html) at [http://multiqc.info](http://multiqc.info)

[![PyPI Version](https://img.shields.io/pypi/v/multiqc.svg?style=flat-square)](https://pypi.python.org/pypi/multiqc/)
[![Conda Version](https://anaconda.org/bioconda/multiqc/badges/version.svg)](https://anaconda.org/bioconda/multiqc)
[![Build Status](https://img.shields.io/travis/ewels/MultiQC.svg?style=flat-square)](https://travis-ci.org/ewels/MultiQC)

-----

MultiQC is a tool to create a single report with interactive plots
for multiple bioinformatics analyses across many samples.

MultiQC is written in Python (tested with v2.7 / v3.4 / v3.5). It is
available on the [Python Package Index](https://pypi.python.org/pypi/multiqc/)
and through conda using [Bioconda](http://bioconda.github.io/).

Reports are generated by scanning given directories for recognised log files.
These are parsed and a single HTML report is generated summarising the statistics
for all logs found. MultiQC reports can describe multiple analysis steps and
large numbers of samples within a single plot, and multiple analysis tools making
it ideal for routine fast quality control.

Currently, supported tools include:

* Quality control & pre-processing
  * [FastQC](http://www.bioinformatics.babraham.ac.uk/projects/fastqc/)
  * [FastQ Screen](http://www.bioinformatics.babraham.ac.uk/projects/fastq_screen/)
  * [Cutadapt](https://code.google.com/p/cutadapt/)
  * [Trimmomatic](http://www.usadellab.org/cms/?page=trimmomatic)
  * [Skewer](https://github.com/relipmoc/skewer)
* Read aligners / quantifiers
  * [Salmon](http://combine-lab.github.io/salmon/)
  * [STAR](https://github.com/alexdobin/STAR)
  * [Tophat](https://ccb.jhu.edu/software/tophat/)
  * [Bowtie](http://bowtie-bio.sourceforge.net)
  * [Bowtie 2](http://bowtie-bio.sourceforge.net/bowtie2/)
  * [Bismark](http://www.bioinformatics.babraham.ac.uk/projects/bismark/)
  * [HiCUP](http://www.bioinformatics.babraham.ac.uk/projects/hicup/)
* Post-alignment tools
  * [RSeQC](http://rseqc.sourceforge.net/) (`bam_stat`, `gene_body_coverage`, `inner_distance`, `junction_annotation`, `junction_saturation`, `read_distribution`, `read_duplication`, `read_gc`)
  * [Subread featureCounts](http://bioinf.wehi.edu.au/featureCounts/)
  * [Samblaster](https://github.com/GregoryFaust/samblaster)
  * [Samtools stats](http://www.htslib.org)
  * [Picard](http://broadinstitute.github.io/picard/) (`MarkDuplicates`, `InsertSizeMetrics`, `GcBiasMetrics`, `HsMetrics`, `OxoGMetrics`)
  * [Preseq](http://smithlabresearch.org/software/preseq/)
  * [methylQA](http://methylqa.sourceforge.net/)
  * [Qualimap](http://qualimap.bioinfo.cipf.es/) (`BamQC`, `RNASeq`)
  * [SnpEff](http://snpeff.sourceforge.net/)

More modules are being written all of the time. Please suggest any ideas as a new
[issue](https://github.com/ewels/MultiQC/issues) _(include an example log
file if possible)_.

## Installation

You can install MultiQC from [PyPI](https://pypi.python.org/pypi/multiqc/)
using `pip` as follows:

```
pip install multiqc
```

If you would like the development version instead, the command is:

```
pip install git+https://github.com/ewels/MultiQC.git
```

Alternatively, you can install using [Conda](http://anaconda.org/)
from the [bioconda channel](https://bioconda.github.io/):
```
conda install -c bioconda multiqc
```

## Usage
Once installed, you can use MultiQC by navigating to your analysis directory
(or a parent directory) and running the tool:

```
multiqc .
```

That's it! MultiQC will scan the specified directory ('.' is the current dir)
and produce a report detailing whatever it finds.

The report is created in `multiqc_report.html` by default. Tab-delimited data
files are also created in `multiqc_data/`, containing extra information.
These can be easily inspected using Excel (use `--data-format` to get `yaml`
or `json` instead).

For more detailed instructions, run `multiqc -h` or see the
[documentation](http://multiqc.info/docs/#running-multiqc).

## Contributions & Support

Contributions and suggestions for new features are welcome, as are bug reports!
Please create a new [issue](https://github.com/ewels/MultiQC/issues) for any
of these, including example reports where possible. MultiQC has extensive
[documentation](http://multiqc.info/docs) describing how to write new modules,
plugins and templates.

If in doubt, feel free to get in touch with the author:
[@ewels](https://github.com/ewels) (phil.ewels@scilifelab.se)

### Contributors
Many thanks to those who have helped out with with project so far:
* Project lead and main author: [@ewels](https://github.com/ewels)
* Early code refactoring help: [@moonso](https://github.com/moonso)
* Early version of Qualimap module: [@guillermo-carrasco](https://github.com/guillermo-carrasco)
* Skewer and Samblaster modules: [@dakl](https://github.com/dakl)
* Samtools stats module: [@lpantano](https://github.com/lpantano)
* Tweaks / core help: [@robinandeer](https://github.com/robinandeer) and [@avilella](https://github.com/avilella)

