---
name: Bcftools
url: https://samtools.github.io/bcftools/
description: >
  BCFtools is a set of utilities that manipulate variant calls in the
  Variant Call Format (VCF) and its binary counterpart BCF.
---

The Bcftools module parses results generated by
[Bcftools](https://samtools.github.io/bcftools/),
a suite of programs for interacting with variant call data.

Supported commands: `stats`

#### Collapse complementary substitutions

In non-strand-specific data, reporting the total numbers of occurences for both changes
in a comlementary pair - like `A>C` and `T>G` - might not bring any additional information.
To collapse such statistics in the substitutions plot, you can add the following section into
[your configuration](http://multiqc.info/docs/#configuring-multiqc):

```yaml
bcftools:
  collapse_complementary_changes: true
```

MultiQC will sum up all complementary changes and show only `A>*` and `C>*` substitutions
in the resulting plot.
