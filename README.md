# aicharge
AI-based fast ab initio gene prediction

Final project for the Building AI course

## Summary

aicharge is an AI based solution that quickly populates ("charges") a newly assembled reference genome with gene predictions that can then be further curated and annotated.


## Background

Building a reference genome of a species from the sequencing reads is called genome assembly. After the assemby is done the next part is to find locations of genes in the genome. Although tools exist, AI-based solutions in this space are still very scarce. aicharge aims also to be a fast and easy-to use solutions despite the size of the reference genome.

aicharge solves the genome annotation problem, i.e. finding all locations of all genes in a reference genome, given nothing but the assembled genome sequence of (A, T, C G).

This author has worked as a bioinformatician building eukaryote genomes. Training your gene prediction tool after the assembly stage is really cumbersome work with the present tools. The authors of another popular open source gene prediction tool AUGUSTUS have announced that they will do the training for you in exchange for money. aicharge aims to take all this cumbersomeness away.

## How is it used?

Describe the process of using the solution. In what kind situations is the solution needed (environment, time, etc.)? Who are the users, what kinds of needs should be taken into account?


This is how you create code examples:
```
def main():
   countries = ['Denmark', 'Finland', 'Iceland', 'Norway', 'Sweden']
   pop = [5615000, 5439000, 324000, 5080000, 9609000]   # not actually needed in this exercise...
   fishers = [1891, 2652, 3800, 11611, 1757]

   totPop = sum(pop)
   totFish = sum(fishers)

   # write your solution here

   for i in range(len(countries)):
      print("%s %.2f%%" % (countries[i], 100.0))    # current just prints 100%

main()
```


## Data sources and AI methods
Where does your data come from? Do you collect it yourself or do you use data collected by someone else?
If you need to use links, here's an example:
[Twitter API](https://developer.twitter.com/en/docs)

| Syntax      | Description |
| ----------- | ----------- |
| Header      | Title       |
| Paragraph   | Text        |

## Challenges

What does your project _not_ solve? Which limitations and ethical considerations should be taken into account when deploying a solution like this?

## What next?

How could your project grow and become something even more? What kind of skills, what kind of assistance would you  need to move on? 


## Acknowledgments

* Stanke & Waack, 2003: Gene prediction with a hidden Markov model and a new intron submodel. Bioinformatics, Volume 19, Issue suppl_2, 27 September 2003, Pages ii215–ii225, https://doi.org/10.1093/bioinformatics/btg1080
