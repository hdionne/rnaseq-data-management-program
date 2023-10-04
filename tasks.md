# Tasks

### Test e-utils

#### 25%

Getting e-utils working on the discovery cluster was  a bit of a pain. There's a module on the cluster available called edirect, but it's from 2018. I should ask if they can make a newer version available, but I don't know if I need it.

It needs a package available called lwp::protocol::https. It turns out I can get this on bash by creating a conda environment and installing perl-lwp-protocol-https through the bioconda channel. Then I activate that environment and can run it. So if I turn this into a script, having a conda environment in the main directory will be important, and I'll need to activate that environment in the script.

### Test snakemake

#### 0%

### Create a pid folder creation rule

#### 0%
