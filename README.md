# GenomeSyn
We developed GenomeSyn as a new tool for constructing and visualizing genome synteny, its novel design and implementation can serve as a necessary complement to the study of genomic synteny and structural variation and its visualization tools.

An online service of GenomeSyn at: http://cbi.gxu.edu.cn/GenomeSyn/. 

![fig1](https://user-images.githubusercontent.com/84839565/147895831-1c6e7f17-9c85-4478-89df-2beccb78586a.png)

## Install container

build the container after downloading the recipe with a git pull like so

```
git pull https://github.com/jmsong2/GenomeSyn
cd GenomeSyn
singularity build genomesyn.sif recipe
```

# Quick start

	eg. GenomeSyn -g1 ../data/rice_MH63.fa -g2 ../data/rice_ZS97.fa

	eg. GenomeSyn -t 3 -g1 ../data/rice_MH63.fa -g2 ../data/rice_ZS97.fa -cf1
		../data/rice_MH63vsZS97.delta.filter.coords

	eg. GenomeSyn -t 3 -g1 ../data/rice_MH63.fa -g2 ../data/rice_ZS97.fa -cf1
	../data/rice_MH63vsZS97.delta.filter.coords -cen1
	../data/rice_MH63_centromere.bed -cen2 ../data/rice_ZS97_centromere.bed
	-tel1 ../data/rice_MH63_telomere.bed -tel2 ../data/rice_ZS97_telomere.bed
	-TE1 ../data/rice_MH63_repeat.bed -TE2 ../data/rice_ZS97_repeat.bed -PAV1
	../data/rice_MH63_PAV.bed -PAV2 ../data/rice_ZS97_PAV.bed -NLR1
	../data/rice_MH63_NLR.bed -NLR2 ../data/rice_ZS97_NLR.bed -r MH63 -q ZS97
	-GD1 ../data/rice_MH63_nonTEgene.gff3 -GD2
	../data/rice_ZS97_nonTEgene.gff3 -GC1 ../data/rice_MH63_GC_10000.bed -GC2
	../data/rice_ZS97_GC_10000.bed -GC_win 100000 -TE_min 40

	eg. GenomeSyn -t 3 -n3 12 -g1 ../data/rice_MH63.fa -g2
	../data/rice_ZS97.fa -g3 ../data/rice_R498.fasta -cf1
	../data/rice_MH63vsZS97.delta.filter.coords -cf2
	../data/rice_MH63vsR498.delta.filter.coords -cen1
	../data/rice_MH63_centromere.bed -cen2 ../data/rice_ZS97_centromere.bed
	-cen3 ../data/rice_R498_centromere.bed -tel1
	../data/rice_MH63_telomere.bed -tel2 ../data/rice_ZS97_telomere.bed -tel3
	../data/rice_R498_telomere.bed -TE2 ../data/rice_ZS97_repeat.bed -PAV1
	../data/rice_MH63_PAV.bed -PAV2 ../data/rice_ZS97_PAV.bed -NLR1
	../data/rice_MH63_NLR.bed -NLR2 ../data/rice_ZS97_NLR.bed -r MH63 -q1 ZS97
	-q2 R498 -GD1 ../data/rice_MH63_nonTEgene.gff3 -GD2
	../data/rice_ZS97_nonTEgene.gff3 -GD3 ../data/rice_R498_IGDBv3_coreset.gff
	-GC2 ../data/rice_ZS97_GC_10000.bed -GC_win 100000 -TE_min 40
