---
title: "Introduction to Ensembl and BioMart"
teaching: 9
exercises: 1
questions:
- What is Ensembl?
- What is BioMart?
- How are Ensembl and Biomart different?
objectives:
- Introduce the Ensembl project.
- Explain the Biomart project and its functions.
keypoints:
- Ensembl is a joint project between EMBL-EBI and the Wellcome Trust Sanger Institute to
  develop a software system which produces and maintains automatic annotation on selected
  eukaryotic genomes
- BioMart is a community-driven project to provide unified access to distributed research
  data to facilitate the scientific discovery process.
- Biomarts are available for many biological databases, including Ensembl.
figures:
  fig1:
    title: Genomes completed
    file: ../fig/genome_completed.png
  fig2: 
    title: Biomart overview
    file: ../fig/biomart_overview.png
---

## About the Ensembl project

[Ensembl][ensembl] is a joint project between [European Bioinformatics Institute][ebi]
(EMBI-EBI), an outstation of the European Molecular Biology Laboratory (EMBL), and
the [Wellcome Trust Sanger Institute][wtsi] (WTSI). Both institutes are located on the
Wellcome Trust Genome Campus in Hinxton, south of the city of Cambridge, United Kingdom.

Ensembl is one of the world's primary resources for genomic research, a
resource through which scientists can access the human genome as well as
the genomes of other model organisms. Because of the complexity of the
genome and the many different ways in which scientists want to use it,
Ensembl has to provide many levels of access with a high degree of flexibility.
Through the Ensembl website a wet-lab researcher with a simple web browser
can for example perform BLAST searches against chromosomal DNA,
download a genomic sequence or search for all members of a given protein
family. But Ensembl is also a software and database system that
can be installed locally to serve the needs of a genomic centre or a
bioinformatics division in a pharmaceutical company enabling complex data
mining of the genome or large-scale sequence annotation.

With the rapid development of next generation sequencing technologies, we are experiencing
a exponential growth of sequencing data. This raw data can be very valuable when provided
with proper annotation.

![genome_completed](../fig/genome_completed.png)

(taken from [Greg Zynda's blog](http://gregoryzynda.com/ncbi/genome/python/2014/03/31/ncbi-genome.html))

In response to the acceleration of the public effort to sequence the human genome, the Ensembl project was started in 1999.

> ## Three main goals of Ensembl
> 
> 1. Provide a scalable way to storing and retrieving genomic data.
> 2. Automatically annotate the genome and integrate with other available biological data.
> 3. Provide a website for genome display for public use.
{: .callout}

Ensembl provides access to genomic information with a number of visualisation tools,
including the Ensembl genome browser. The Ensembl website allows users to directly
download data, whether it is the DNA sequence of a genomic contig in which you are trying
to identify novel genes, or positions of SNPs in a gene you are working on. An updated
version of the website is released bimonthly. Old versions are accessible on
the [Ensemble Archives][archives] website, dating back two years. Apart from that
the [Ensembl pre-release][pre] website provides displays of genomes that are still in the
process of being annotated. There is also an ftp site to download large amounts of data
from the Ensembl database, as well as the data-mining tool BioMart, that allows rapid
retrieval of information from the databases, and BLAST/BLAT sequence searching and
alignment.

> ## Ways of retrieving Ensembl data
> 
> 1. The data export button on the Ensembl browser interface.
> 2. RESTful access.
> 3. Programming through the Perl API.
> 4. Direct database access.
{: .callout}


## What is BioMart

[BioMart][biomart] is a project to provide easy collaborative data access for researchers.
Many of the problems researchers experience every day include challenges in getting the
right data, linking data between systems of different identifiers, and adding related
attributes to existing data. Biomart addresses these problems with a consistent database
model and a simple, easy to use query system.


Biomart incldues an easy-to-use web-based tool that allows extraction of data from linked
databases without any programming knowledge or understanding of the underlying database
structure. Biomarts are available for many different data sources, including Ensembl.
While Ensembl and Biomart are different projects (there are biomart data sources other
than Ensembl), Ensembl provides a consistent Biomart interface to all its data, so we will
often refer to the Ensembl Biomart as Biomart.

### Biomart interface

The Ensembl Biomart interface is shown below, but all biomart interfaces look similar.
*Data sets*, *filters* and *attributes* can be selected in the right panel. A summary of your
current choices is also displayed in the left panel, so you can count and preview results
before downloading.


![biomart_overview](../fig/biomart_overview.png)

> ## Ways of retrieving data using BioMart
> 1. A web interface such as on the Ensembl or Biomart home pages.
> 2. BiomaRt R packages.
> 3. Programming through the Perl API.
> 4. RESTful access
> 5. Direct database access.
{: .callout}

We will walk through how to use BioMart in the next session.


> ## Exercise 1 
> 
> How would you explain the relationship between Ensembl and Biomart?
> 
> >
> > ## Solution
> > Biomart is a data cross-referencing and query tool for different kinds of biological
> > data. Ensembl is a genome annotation project and browser. Ensembl provides different
> > ways of accessing data from a genome browser; Biomart is one of those ways. Many other
> > Biomarts, not part of Ensembl, are available from sites like [Biomart][biomart].
> {: .solution}
{: .challenge}

[ensembl]: http://asia.ensembl.org/index.html
[ebi]: http://www.ebi.ac.uk/
[biomart]: http://www.biomart.org
[wtsi]: http://www.sanger.ac.uk/
[archives]: http://asia.ensembl.org/info/website/archives/index.html
[pre]: http://pre.ensembl.org/index.html
