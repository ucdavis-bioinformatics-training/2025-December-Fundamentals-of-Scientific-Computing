Apptainer
============

Apptainer (previously called Singularity) is a program that basically packages everything a piece of software needs into one isolated, self-contained environment. Software that has many dependencies and needs specific versions of libraries can (hopefully) be packaged into something Apptainer can use. You need to look at the software installation instructions to see if this is possible.

Let's install Apptainer and then create an Apptainer file for a gene prediction program called [Braker](https://github.com/Gaius-Augustus/BRAKER).

First, install Apptainer into a conda environment. We need to add some channels:

	conda config --add channels bioconda
	conda config --add channels conda-forge

Search for Apptainer:

	conda search apptainer

Install Apptainer:

	conda create -y -n apptainer-1.4.5 apptainer=1.4.5

Activate the environment:

	conda activate apptainer-1.4.5

Now we are ready to create our Apptainer file. In the Braker documentation, take a look at the [Container section](https://github.com/Gaius-Augustus/BRAKER?tab=readme-ov-file#container). Here they show us how to create our own Apptainer file, except they use Singularity. However, the commands are the same.

	apptainer build braker3.sif docker://teambraker/braker3:latest

This should take no more than 10 minutes to run.

Once it is finished, you can run the software through Apptainer like so:

	apptainer exec braker3.sif braker.pl

Some software might provide an apptainer file directly, in which case you don't need to build it (obviously).