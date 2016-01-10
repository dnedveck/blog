---
layout: post
title: "Lab 11/23 -- ANOVA and alpha div"
date: 2015-11-23
categories: 
---

[Slides are live](https://docs.google.com/presentation/d/1l9UDqPMwdpiBzaWgXQLglOq-IS7I2Eo9Kcq3YgdCwQs/edit?usp=sharing)

## ANOVA

there were some issues with 3A, especially with an error generated during the normalization step. Derek couldn't solve it, Yikes. 


For number 7, you're going to have to run a script to get the alpha diversity from your rarefied OTU table. 

I made a `.sh` script to make it easier to run ..

Make a directory to do our work in:

	mkdir alpha_div

cd into it and make a script to run, and set it to be executable

	cd alpha_div
	touch alphadiv.sh
	chmod u+x alphadiv.sh

Then open it up in nano and make it have the following contents

	module load qiime/1.7.0

	alpha_diversity.py \ 
		    -i ~/otu_picking/output/otu_table_d8000.biom \
		    -o ./alpha_div_out.txt \
		    -m PD_whole_tree,shannon,simpson,observed_species \
		    -t /home/biol2002/shared/97_otus.tree

then log into lab, and run it. 


## Alpha diveristy

Due by the time I start grading it (sometime Monday 11/30) -- your choice if you work on it over break, or finish it by Wednesday.


