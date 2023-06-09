# Phylogenetics Group Project

## 4.2.3: Phylogenetics Group Practical

Time to test out what you've learnt on a new dataset! 

The dataset you'll be working on can be found in `/shared-team/Phylogenetic_data/BA2_subsampled.fasta`

This dataset consists of sequences from the BA2 SARS-CoV-2 lineage.

Create a new directory, download the dataset to it.

___

### Task 1

Try to use the skills you've learnt to answer the following questions:

1. How many sequences are in this dataset?
2. What is the best fitting model? What do the parameters mean?
3. What initial observations can you make from the tree topology? Which sequence(s) show the most divergence?
4. What do the bootstrap values tell us about this tree?
5. What format are the sequence IDs in? What information can we extract from them?

___

### Task 2

Create a publication ready image of the maximum likelihood tree of these sequences, with tips coloured by region and only bootstrap values of at least 70 shown. Present this in a word document with an appropriate figure legend. 

___

### Task 3

Extract the dates from the sequence IDs and make a txt file with the date for each ID, similar to what we've done before.

Import the tree and dates into Tempest.
Hint: The date format may be different to last time!

1. Does this dataset show a temporal signal? What evidence do you have for/against this? Why do you think this could be?
2. What is the estimated date of the MRCA? 
3. What is the estimated evolutionary rate? 
4. Which sequences show greater divergence than expected? Which show less divergence? 
5. Can we trust these values we've answered here? 
6. What could we try to fix these issues? 

___

### Task 4

The steps we've been doing to create and visualise trees can be combined into a bash script! 

To prevent things being overwritten, create a new directory and copy the `BA2_subsampled.fasta` that we started with into this. 

Can you write a bash script that aligns and creates a tree for this file? E.g. combining mafft and iqtree?

___

### Task 5

We can even add R scripts into bash scripts! 

Write an R script that extracts metadata about the region of the sequences (e.g. the code you wrote for task 2 here) and then makes and saves a tree with tips coloured by region. 

Check this R script runs and produces the expected figure. 

To prevent things being overwritten, create a new directory and copy the `BA2_subsampled.fasta` that we started with into this. 

Edit your R script to make sure the file paths reflect this new directory. The files it's calling on won't exist yet, but they will soon!

Save the R script. 

Edit your bash script from before to now process the fasta file in this directory, and add to this your R script! 

You can add R scripts to bash scripts by writing in your bash script:

```
/usr/lib/R/bin/Rscript PATH_TO_RSCRIPT
```

Replacing the PATH_TO_RSCRIPT with the full path to your R Script. 

Try running this on your fasta file. If it works and runs to completion, this should generate your `.png` figure automatically! 

___
