---
layout: post
title: "Lab 11/16, finishing Taxa sum, For Loop"
date: 2015-11-16
categories:
---

[slides are live](https://docs.google.com/presentation/d/1MIDVOz6XPT3w3ykx35MkrYwYRD6EiA9PpVdmsv4fKTc/edit?usp=sharing)

## Lab content 

- finish Taxa Summary (due by end of lab)
- work on `ANOVA_in_R.doc` (due 11/18 before lab)
- cover for loops in R


## Notes


### Finishing the `taxa_sum_lev` part of the Taxa Summary

so like before, save the `taxa_sum_lev` part of the walkthrough into a separate R script and source it to bring it into the working memory.


You can pretty much copy the command they gave you in the html doc to run your stuff.

	taxa_sum <- taxa_lev_sum('otu_table_d8000.txt', 'HMP_5BS_metadata.txt',
                         minpct=0.1, minind=4, cov='BodySite', mincovpct=0,
                         TL='species', taxa='Fusobacteria')

And you can see what it looks like by using 

	str(taxa_sum)

And then I copy-pasted the plotting code

	par(mar=c(12,4,0.4,30),mgp=c(1.8,0.6,0), las=2, cex=0.7)
	par(xpd=T)
	barplot(taxa_sum$taxa_cov, col=taxa_sum$RBcolors, border=T, ylab="Relative Abundance", names.arg=taxa_sum$cov_names)
	legend(6.5, 14, taxa_sum$taxa_names, fill=rev(taxa_sum$RBcolors), border=T, ncol=1)


#### Troubleshooting notes

if you get something like `Error: figure margins too large` it means that your plotting window in Rstudio is not large enough -- just make the window bigger and try again. Also, if the plot is messed up, to start over run `dev.off()`, and then enter your commands again.

### For Loop Assignment

We started on the For loop assignment, and that is due by the beginning of class time on Wed (11/18)

**I made a walkthrough of the For Loop assignment** [here's a link to a google drive doc](https://drive.google.com/file/d/0Bxn_LX4s5eomenlUdlphVVl2NlU/view?usp=sharing)

[test link]({{ site.baseurl }}/assets/forloop.html)


