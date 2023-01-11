# The the FLYE assembler

[FLYE](https://github.com/fenderglass/Flye/blob/flye/docs/USAGE.md) is one of many genome assemblers, but is very efficient for assembling bacterial genomes. You are going to use this to process your fastq data files into 1 or more contigs representing the E. coli genome.

## Before the assembly: base calling

We have already base called your sequences. This means that the variable current measurements as the sequence passes through the nanopore have been interpreted as a sequence of nucleotides. These nucleotide sequences have been stored in `.fastq` format files.

## Before the assembly: Quality Control

The sequences called from the Nanopore have been quality controlled to remove very short sequences and sequences with low quallity sequence.

## Before the assembly: identifying your files

You will need to be in the correct working directory, and know the location and names of the data files you wish to assemble. Your sequences are your data, you need to be able to describe them. A useful approch is to run [seqkit stats](https://bioinf.shenwei.me/seqkit/usage/#stats)

`seqkit stats path/*.fastq.gz > samples-fastq-seqkitstats.tsv`

This command tells the program seqkit to run the submodule "stats" and report on the file specified, then write (`>`) the output to the `.tsv` file specified.

## Running Flye

test your installation of Flye

`flye -help`

You should get Flye help written out.

### Developing your assembly command

Read the help, and read the [Flye documentation](https://github.com/fenderglass/Flye/blob/flye/docs/USAGE.md).

Now assemble your command to assemble the data. You will have to tell Flye what format your data is, where the files are and what they are called, where to write the output and how many threads to use in running the program.

Once you have written your command check it with one of us.
