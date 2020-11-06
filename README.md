# selection_scikit-allel_py

Python pipeline to perform PBS and Tajima D and plot/tabulate the results. 

It contains two notebooks one for the analysis and one for the plot and table. 

The files used are the VCF phased genomes of 1KGP and can be downloaded from [here](ftp://ftp.1000genomes.ebi.ac.uk/vol1/ftp/release/20130502/). I downloaded them in the folder called ```data``` using the following script: 

```
mkdir data

cd data

for c in (1..22)
do wget  ftp://ftp.1000genomes.ebi.ac.uk/vol1/ftp/release/20130502/ALL.chr${c}.phase3_shapeit2_mvncall_integrated_v5a.20130502.genotypes.vcf.gz
done
```

The example perform PBS to investigate signals of positive selection in Southern European populations (TSI and IBS) vs CHB using as outgroup YRI.
A delta Tajima D is also computed only on TSI population using as outgroup YRI


For faster results download the PBSTajD_acrossChrom.ipynb as python script and you can run it in a cluster within a conda environment. You can apply also the analysis to one chromosome or few chromosome with little adjustments of the scripts.
