# age-related hearing loss
#### Polygenic risk score model for age-related sensorineural hearing loss
Jung, S. H., Lee, Y. C., Shivakumar, M., Kim, J, Park. Y. W., … & Kim, D. (2024) Association between genetic risk and adherence to healthy lifestyle for developing age-related hearing loss.

### Sensorineural hearing loss - 1,103,359 variants
> [FinnGen_r8_PRSCS_auto.gz](https://github.com/dokyoonkimlab/hnc-prs-phewas/blob/main/prs-model/FinnGen_r8_PRSCS_auto.gz)

---

## Description

To generate polygenic risk score (PRS), we utilized the HL-GWAS summary statistics from the FinnGen Consortium (Data Freeze R8v4) which is a large-scale public-private partnership combining digital health record data from Finnish health registries with genotyping data from Finnish Biobanks [1]. FinnGen Release 8 (https://www.finngen.fi/en) includes association data at 20,175,454 variants for 2,202 endpoints in 342,499 (190,879 females and 151,620 males) Finnish individuals. The sensorineural HL cases (H8_HL_SEN_NAS) were identified based on ICD codes (ICD-9: 3891; ICD-10: H90.3, H90.4, and H90.5). There were 28,310 cases and 302,750 controls following FinnGen phenotype definition. GWAS was performed by FinnGen using SAIGE with sex, age, 10 PCs, and genotyping batch as covariates [2]. In addition, we mapped FinnGen summary statistics from GRCh38 to GRCh37/hg19 using liftOver tool to perform PRS with UK Biobank genotyped data (GRCh37/hg19) [3]. 

We constructed PRS for HL by using a Bayesian polygenic prediction method, PRS-CS [4], which infers the posterior mean effect size of each variant using the linkage disequilibrium (LD) reference panel and GWAS summary. The 1000G Project phase 3 EUR data was used to be the external LD reference panel. The posterior SNP effect sizes in PRS-CS were inferred from GWAS summary statistics for EUR (FinnGen r8) population. The individual PRSs were computed from beta coefficients as the weighted sum of the risk alleles by applying PLINK version 1.90 with the --score command [5].

### References
1. Kurki, Mitja I., et al. "FinnGen provides genetic insights from a well-phenotyped isolated population." Nature 613.7944 (2023): 508-518.
2. Zhou, Wei, et al. "Efficiently controlling for case-control imbalance and sample relatedness in large-scale genetic association studies." Nature genetics 50.9 (2018): 1335-1341.
3. Hinrichs, Angela S., et al. "The UCSC genome browser database: update 2006." Nucleic acids research 34.suppl 1 (2006): D590-D598.
4. Ge, Tian, et al. "Polygenic prediction via Bayesian regression and continuous shrinkage priors." Nature communications 10.1 (2019): 1776.
5. Chang, Christopher C., et al. "Second-generation PLINK: rising to the challenge of larger and richer datasets." Gigascience 4.1 (2015): s13742-015.
