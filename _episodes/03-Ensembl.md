---
title: "Search and access data in Ensembl"
teaching: 1
exercises: 10
questions:
- "How can I find Ensembl data?"
- "How can I download and access Ensembl data?"
objectives:
- Learn how to explore the Ensembl genome browser.
- Use Ensembl identifiers to access and download Ensembl data from the command line
keypoints:
- Ensembl provides a variety of interfaces for accessing and downloading data.

---

# The Ensembl system

As discussed in class, [Ensembl][ensembl] is a project for genome annotation and data
access that includes one of the most widely used genome browsers in the world. The system
is entirely free and open source, and so is used for many organisms besides the three
organisms whose assemblies are supported by the [Genome Reference Consortium][grc]. 

## Finding a gene

Let's look at a particular gene.  For this example, we'll use the gene EZH2 from the
latest assembly on the Ensembl browser. 

Start by going to
[http://asia.ensembl.org/Homo_sapiens/Info/Index](http://asia.ensembl.org/Homo_sapiens/Info/Index).

> ## Exercise 1. 
> 
> Can you find the Ensembl gene identifier for EZH2?
> 
> > ## Solution
> > 
> > A search using the `EZH2` symbol brings up a link to Ensembl gene identifier
> > ENSG00000106462 for EZH2, found on the reverse strand of Chromosome 7.
> {: .solution} 
>
>   What else can we immediately notice about this gene?
>
> > ## Solution
> >
> > -  It  is a protein coding gene.
> > -  This gene has 10 transcripts (splice variants), 86 orthologues, 7 paralogues, is a
> >    member of 1 Ensembl protein family and is associated with 35 phenotypes.
> > -  Many other properties and viewable features.
> {: .solution} 
>
{: .challenge}

## Exporting data from the Ensembl interface.

If you click on the "Export data" link on the left, you can export the sequence
information for your gene in a variety of formats.

> ## Exercise 2
> 
> Export the sequence data for your gene using the Export data button. Limit your results to
> just cDNA sequences.  How many transcript sequences do you get in the fasta file? 
> 
> **Hint**: export to HTML and search for "ENST".
> 
> > ## Solution
> > 
> > For EZH2 you should see 10 fasta sequences, one for each transcript.
> {: .solution}
{: .challenge}

### Challenge: get some data using REST.

The [Ensembl REST][rest] interface support relatively complex queries over HTTP with a RESTful
interface. This means you can construct URLs to find data. The URLs have a syntax that is
readily described, so you can write a progam to construct such queries without knowing
anything more about the database.

> ## Exercise 3
> 
> Starting with the Ensembl [REST server][rest], use the Ensembl gene identifier to access
> the sequences for this gene in fasta format.
> 
> > ## Solution
> > 
> > The syntax for sequence retrieval is describe at the bottom of the [Ensembl REST][rest]
> > page. For FASTA format, the data must be request as "text/x-fasta".  You can type this on
> > your bash shell
> > 
> >     wget -q --header='Content-type:text/x-fasta' \
> >         "http://rest.ensembl.org/sequence/id/ENSG00000106462" \
> >          -O -
> > 
> {: .solution}
{: .challenge}



[ensembl]: http://asia.ensembl.org/index.html
[ebi]: http://www.ebi.ac.uk/
[biomart]: http://www.biomart.org
[wtsi]: http://www.sanger.ac.uk/
[archives]: http://asia.ensembl.org/info/website/archives/index.html
[pre]: http://pre.ensembl.org/index.html
[grc]: https://www.ncbi.nlm.nih.gov/grc
[rest]: http://rest.ensembl.org/
