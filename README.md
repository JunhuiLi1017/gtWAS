# gtWAS
:exclamation: This is a read-only mirror of the CRAN R package repository.  gtWAS — Genome and Transcriptome Wide Association Study
## 1. Introduction

* What is the Genome and Transcriptome Wide Association Study?

Quantitative trait loci(QTL) mapping and genome wide association analysis(GWAS) are used to find candidate molecular marker or region associated with phenotype based on linkage analysis and linkage disequilibrium. Gene expression quantitative trait loci mapping(eQTL) is used to find candidate molecular marker or region associated with gene expression. 
In this package, we applied the method in Liu W. (2011) <doi:10.1007/s00122-011-1631-7> and Gusev A. (2016) <doi:10.1038/ng.3506> to genome and transcriptome wide association study, which is aimed at revealing the association relationship between phenotype and molecular markers, expression levels, molecular markers nested within different related expression effect and expression effect nested within different related molecular marker effect. 

* What is the main features?

Genome marker effects(or Transcriptome effect) are nested within Transcriptome effects(or Genome marker effects) are perfomed as independent variable besides general methods of GWAS and TWAS. 

## 2. Statistical details in this package

* The best linear model can be obtained by stepwise regression analysis. 
* F test based on full and reduced model are performed to obtain p value or likelihood ratio statistic(LOD). 
* Thresholds can be obtained by permutation test(for LOD) and Bonferroni Correction.

## 3. Usage and Examples
	#install.package("gtWAS")
	
	library(gtWAS)
	
	data(Tdata)
	data(alldata)
	independent <- "E(B)"
	gtWAS(Tdata,alldata,independent,selection='stepwise',select="SBC",Choose="SBC",vecThr=c(0.05,0.05,0.05),correct = "Bonferroni")
	##---#---##
    ##Maybe it is not a good idea to use the same varible for the gtWAS function and gtWAS package name
	
We welcome commits from researchers who wish to improve our software, and good luck to you.
