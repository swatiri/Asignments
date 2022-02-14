## What is it?

Snakemake is a scalable workflow management system used to create reprodicible data analyses by hooking into the pyhthon interpreter. 
A workflow is a systsem designed to execute a series of computational or data manipulation steps.
Snakemake is unique in that, it offers a defination languagewhich is an extension of Pyhton. 
it intergrates with the *Conda* package manager and the *Singularity* container engine
It is a generral purpose workflow system for any discipline including Bionformatics
Snakemake is inspired by the GNU Make paradigm which is a tool that controls the generation of excecutables and other non-source files of a program
from the progrmas source files.

## Why use snakemake?
1. SImpler to learn especially if you are familar with Python
2. It interoperartes with any intstalled tools or available web service with well defined inputs and output file formats.

## Set up

To install mamba

`conda install mamba -n base -c conda-forge`
 
Installing snakemake

 `conda activate base`
 
`mamba create -c conda-forge -c bioconda -n snakemake snakemake`

After succesfull  downloading and installation the command below displays  usage 
 
 `snakemake --help`
 
 ### Working with snakemake
 
Create an empty workflow in the current directory

`touch Snakefile`
`snakemake -n`

Create a rule following the snakemake syntax e.g: to map sequences to the reference genome create a rule file that looks like this

rule map_reads:
  input:
      "data/genome.fa",
      "data/samples/A.fastq"
  output:
      "results/mapped/A.bam"
  conda:
      "envs/mapping.yaml"
  shell:
      "bwa mem {input} | samtools view -b - > {output}"
Run your workflow
snakemake --use-conda results/mapped/A.bam --cores 1




