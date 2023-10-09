# Tasks

### Test e-utils

#### 25%

Getting e-utils working on the discovery cluster was  a bit of a pain. There's a module on the cluster available called edirect, but it's from 2018. I should ask if they can make a newer version available, but I don't know if I need it.

It needs a package available called lwp::protocol::https. It turns out I can get this on bash by creating a conda environment and installing perl-lwp-protocol-https through the bioconda channel. Then I activate that environment and can run it. So if I turn this into a script, having a conda environment in the main directory will be important, and I'll need to activate that environment in the script.

The following is an e-util command to fetch data from the bioproject database, id PRJNA982836, and get the abstract of it.

`$ efetch -db bioproject -id PRJNA982836 -format abstract`

The output includes the title, bioProject accession name (PRJNA982836) and ID within the database (982836):

1. Vedolizumab efficacy is associated with decreased intracolonic dendritic cells, not memory T cells [P430]
   Organism: Homo sapiens (Taxonomy ID 9606)
   BioProject Accession: PRJNA982836
   ID: 982836

There's a bioconda package for sra (sra-tools).
for connecting using ftp, you can do

```
$ ftp
ftp:> open ftp.ncbi.nlm.gov

```



The sra-tools bioconda package doesn't seem to be able to be used on the discovery cluster. There's some network issue. That said, there's a module on the discovery cluster calle sratoolkit that I can use for this.

If there's a list of 'SRR' accession #s stored in a local variable `$ACCESSION`

type `$ prefetch $ACCESSION` and it should download each one one at a time. In the event of the program being stopped, it can pick back up where it left off.

The result of this command will give a bunch of folders with .sra files in them. To convert them to fastq files, run `$ fasterq-dump --split-files $ACCESSION`.


### test

Test snakemake

#### 0%

### Create a pid folder creation rule

#### 0%
