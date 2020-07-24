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

 但是从其模拟的结果来看：miRNA target site gain and loss (3'UTR reannotation)：
gain [mean:0.18% ]< loss [mean :1.5%]，mRNA 3'UTR 改变对影响不大

![avatar](https://oup.silverchair-cdn.com/oup/backfile/Content_public/Journal/bioinformatics/36/8/10.1093_bioinformatics_btaa007/2/btaa007f4.png?Expires=1598606494&Signature=MAWky1joWvZeNT-rmgcE85vT6ubEA2-rL5AqMGPJpKx9Uw1z6OSojAfdpT8VSDPqmPR49AK4zQbV83ECszf9iGD~QfvTXZNueGb0CBKQwbL7V1hp8hzv9B0H6OCrBX2A-24JpT7tuUJOkEnDQjzqkVOC243OCvtTvlJaGHJLZ87xEfz-4DbgIt9ZCb-Z81dS3SqyBv1qhNugXsbpnSSLHsLZtlemaIkftecTGGPsd3zBHfsAjPFYp1KfNW5miKKHjdZkCGjcoY33E1IqrO2FY21h~9GlFLhg1NUr2ph~OdVoUK3thiG9UVQKINy4kiELv4fpG1OvpgoYM-3sLK2aXA__&Key-Pair-Id=APKAIE5G5CRDK6RD3PGA)

