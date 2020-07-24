# miRNA 软件背景

### 1.1 FilTar 2020
using RNA-Seq data to improve microRNA target prediction accuracy in animals
Thomas Bradley 1,2 and Simon Moxon, Bioinformatics, 36(8), 2020, 2410–2416
 
     (i) provide sample specific 3'-UTR reannotation; extending or truncating default
     annotations based on RNA-Seq read evidence and 
 
     (ii) filter putative miRNA target predictions by transcript expression level,
     thus removing putative interactions where the target transcript is not expressed
     in the tissue or cell line of interest.

---


    特点：mRNA 因APA（alternative cleavage and polyadenylation）的3'UTR具有时空差异，
    利用样本中的mRNA做实时分析，已有的软件都是采用已有的固定的3'UTR库
    HISAT2 (v2.1.0) (Kim et al., 2015),align ，会产生新的转录本
    Salmon(Patro et al., 2017) RNA-seq quantification tool
    APAtrap (Ye et al., 2018), the 3’-UTR reannotation tool，
 
 原文表述
 
>   Most algorithms, in addition to considerations of seed complementarity, and the location of the target site within the transcript, also consider features such as
> the conservation of the miRNA target site in closely related species,
> the thermodynamic stability of the miRNA–mRNA duplex, and the
> structural accessibility of putative target sites to the miRNA–RISC
> complex, as variables which are also thought to influence miRNA
> targeting and subsequent transcript repression (Ritchie and Rasko,
> 2014).

