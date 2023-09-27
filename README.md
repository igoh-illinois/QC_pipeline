+Code by:      Cris Vera
+Group:        IGOH Theme, IGB, University of Illinois
+Date:         06-24-2019
+Contact:      jcvera@illinois.edu

## Description: 
Runs the Whitaker lab WGS pipeline through initial QC and alignment steps. Establishes a directory hiearchy for output and downstream pipelines.

```
Main Options-Switches:
	-d  Option: specify input directory with sample files. Required.
	-e  Option: specify output directory. Required.
	-p  Option: specify project name. Required.
	-t  Option: specify number of threads to use (when possible). Default=8.
	-z  Option: raw reads are gzipped. Default=0.
	-u  Option: run assembly step. Defualt=0.
		 0: no assembly
		 1: Unicycler assembly, use raw reads with correction
		 2: Unicycler assembly, use trim reads with no correction
		 3: Spades assembly, use raw reads with correction
		 4: Spades assembly, use trim reads with no correction
	-m  Option: run ariba MLST. Default=0.
		 0: no Ariba
		 1: Ariba MLST
		 2: Ariba MLST, Magares, and VFDB
	-k  Option: specify sequencing library name. Default=Unknown.
		 0: Unknown
		 1: Nextera_XT_DNA_Library_Prep_Kit
		 2: TruSeq_RNA_Library_Prep_Kit
		 3: TruSeq_Stranded_mRNA_LT_Kit
		 4: TruSeq_Stranded_Total_RNA_LT_Kit
		 5: TruSeq_Small_RNA_Library_Prep_Kit
		 6: TruSeq_Chip_Library_Prep_Kit
		 7: TruSeq_DNA_Library_Prep_Kit
		 8: NEBNext_Multiplex_Small_RNA_Library_Prep_Kit
		 9: Clonetech_SMARTer_Ultra_Low_Input_RNA_Kit
		10: SureSelect_XT_Mouse_All_Exome
		11: SureSelect_XT_Human_All_Exon_V5-UTR
		12: iGenomx_Riptide_DNA_HT-RLP
		13: Kappa_DNA_HTP_Prep_Kit
		14: Kappa_PCR-free_DNA_HTP_Prep_Kit
		15: Nextera_Flex_DNA_Library_Prep_Kit
	-R  Option: specify reference genome/assembly. Default=1.
		1: CF_1_A12_F10-like (10)
		2: CF_1_A12_H10_vir (10)
		3: PA14-RJW_PhageTS1-Ref (11)
		4: PA14-RW_DMS3 (11)
		5: Paeruginosa_CompleteRef_PA14-RW (10)
		6: Paeruginosa_CompleteRef_PA_A12 (10)
		7: Paeruginosa_CompleteRef_PA_pl44B5 (10)
		8: Paeruginosa_CompleteRef_PA_pl68B3 (10)
		9: Paeruginosa_CoreGenome1 (10)
		10: Paeruginosa_RefSeq_PA01 (10)
		11: salmonella_enterica (10)


Usage:
Run_MainPipeline_IGOH_QConly.pl -d [Input Sample Directory] -e [Output Directory] -p [Project Name] -t [Threads] -z [Gzipped] -m [Ariba] -R [Reference] -u [Assembly] -k [Library Kit]
```
