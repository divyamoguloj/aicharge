![AI-charge](/strang.png)

#AI-charge
AI-based fast ab initio gene prediction

Final project for the Building AI https://buildingai.elementsofai.com/ course

## Summary

AI-charge is an AI based solution that quickly populates ("charges") a newly assembled reference genome with gene predictions that can then be further curated and annotated.


## Background

Building a reference genome of a species from the sequencing reads is called genome assembly. After the assemby is done the next part is to find locations of genes in the genome. Although tools exist, AI-based solutions in this space are still very scarce. aicharge aims also to be a fast and easy-to use solutions despite the size of the reference genome.

AI-charge solves the genome annotation problem, i.e. finding all locations of all genes in a reference genome, given nothing but the assembled genome sequence that consists of sequences of A, T, C, & G.

This author has worked as a bioinformatician building eukaryote genomes. Training your gene prediction tool after the assembly stage is a really hard work with the present tools. E.g. the authors of another popular ab initio gene prediction tool AUGUSTUS (Stanke & Waack 2003, Stanke et al. 2006) have announced that they will do the training for you in exchange for money. aicharge aims to take all this cumbersomeness away.

Admittedly, AI-charge is not the first software tool to solve this problem but it will be the easiest to use.

## How is it used?

Assuming our genome assembly is in a (non-multifasta) file called "genome.fasta":
```

def aicharge(starts):
   #TODO: start codon processing logic (aicharge complete logic)
   pass
   
def main():
   input_genome = open("genome.fasta", "r")
   fasta = readlines(input_genome)
   input_genome.close()
   
   for line in fasta:
      #fasta header check:
      if line[0] == ">":
         print("AI-charging %s" % line)
      else:
         #Find start codons (=coding for amino acid methionine) in sequence:
         starts = line.find("ATG")
         print("Found start codons at base indices: ", starts)
         aicharge(starts)
         

   TODO: Output logic (gff3)

main()
```

Output will be a General Feature Format version 3 (gff3) file that specifies the locations of the gene models (annotations) in the input genome.


## Data sources and AI methods

Input data: Genome assembly in singleline (=non-multifasta) FASTA format
Training logic: Train and test data from known cDNA databases, specify at input wheter prokaryote (bacterium) or eukaryote (micro-organism, plant, animal etc.) genome.
TODO: Find most suitable AI method for this or set the program logic to try multiple and then present accuracy / precision results to the user.

## Challenges

AI-charge finds gene models (annotations) ab initio in an input genome assembly. In animal genomes this will sum up to 10,000 - 100,000 gene models in total. The results should be manually curated using e.g. Apollo (Dunn et al. 2011) or otherwise verified before publication.

## What next?

AI-charge could be a "hive" of AI's allowing it to connect to other aicharge instances on the web, exchange data and learn from and teach the other instances. We need absolutely best performance implementation for aicharge as especially animal genome annotation requires huge computational resources.


## Acknowledgments

* Dunn et al. 2019: Apollo: Democratizing genome annotation. PLoS Comput Biol. 15(2): e1006790. https://dx.doi.org/10.1371%2Fjournal.pcbi.1006790
* Stanke & Waack, 2003: Gene prediction with a hidden Markov model and a new intron submodel. Bioinformatics, Volume 19, Issue suppl_2, Pages ii215–ii225, https://doi.org/10.1093/bioinformatics/btg1080
* Stanke et al. 2006: Gene prediction in eukaryotes with a generalized hidden Markov model that uses hints from external sources. BMC Bioinformatics volume 7, Article number: 62
