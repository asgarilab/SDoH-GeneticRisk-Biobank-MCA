# SDoH-GeneticRisk-Biobank-MCA
Code accompanying the following manuscript:

**Title:** Integrating social determinants of health and genetic risk in disease risk models

**Authors:** Abhijith Biji<sup>1,2</sup>, Kathleen Ferar<sup>1,2</sup>, Vikas Pejaver<sup>1,2</sup>, Eimear E. Kenny<sup>1,2</sup>, Bian Liu<sup>3</sup>, Samira Asgari<sup>1,2 *</sup>

**Affiliations:** 
<sup>1</sup> Institute for Genomic Health, Icahn School of Medicine at Mount Sinai, New York, NY
<sup>2</sup> Department of Genetics and Genomic Sciences, Icahn School of Medicine at Mount Sinai, New York, NY
<sup>3</sup> Department of Population Health Science and Policy, Icahn School of Medicine at Mount Sinai, New York, NY, USA

**Corresponding author:** samira.asgari@mssm.edu

**Abstract**
Complex diseases are shaped by heritable factors and non-genetic environmental, behavioral, and social determinants of health, but these are rarely modeled together. The growing availability of large-scale, multimodal biobanks creates new opportunities to integrate diverse data types into more accurate disease risk models. Here, we apply Multiple Correspondence Analysis (MCA) to over 100 environmental, behavioral, and social variables from the All of Us biobank (N = 413,457 individuals) to generate lowdimensional embeddings that quantify non-genetic risk for six common chronic conditions: asthma, chronic kidney disease, coronary heart disease, hypercholesterolemia, prostate and breast cancer. These embeddings recovered known risk factors such as economic status and smoking, but also pointed to novel ones such as loneliness and spirituality. Including MCA axes in addition to demographics and polygenic scores (PGS) consistently improved disease risk prediction, with ΔAUC ranging from 0.007 to 0.027. For four of six diseases, the gains in model predictive power from MCA embeddings surpassed those attributable to PGS. Genetic and non-genetic risks combined additively with little evidence of interaction effects (ΔAUC ≤ 0.001) and the variant effect sizes were highly stable when embeddings were included in genetic association models (r > 0.98). In summary, we introduce a scalable, interpretable framework that summarizes survey-based environmental, behavioral, and social factors without prior assumptions about disease-specific variables. Our results demonstrate that these non-genetic contexts improve prediction but show limited evidence of interaction with genome-wide polygenic disease risk. Our results underscore the importance of incorporating social, behavioral, and environmental factors, into clinical models of disease risk.

Preprint link: [https://www.medrxiv.org/content/10.64898/2026.02.15.26346336v1](https://www.medrxiv.org/content/10.1101/2025.09.29.25336903v1.full)

## Description of files:

1. **a_extract_age_sex_phecodes.ipynb** : Obtain age, sex, DOB and EHR information. Use PheWAS package to get phecodes from ICD codes.
2. **b_plink_array_QC_metrics.ipynb** : Using plink array data on _All of Us_, get important metrics on quality of genotyped data.
3. **c_plink_array_QC_metrics_PLOT.ipynb** : Plot the plink array metrics to choose thresholds for QC.
4. **d_plink_array_QC.ipynb** : QC plink array data for Step 1 of GWAS and PCA.
5. **e_PCA_for_GWAS.ipynb** : Perform principal component analysis on QC'd plink array.
6. **f_GRM_for_GWAS.ipynb** : Construct genetic relatedness matrix (GRM) using QC'd plink array.
7. **g_extract_surveys_and_get_mca.ipynb** : Extract survey data and perform MCA.
8. **h_analysis_of_survey_data_and_regressions.ipynb** : Analyze the survey data obtained from earlier step, perform regressions (Fig 1, 2, 3 from paper).
9. **i_GWAS.ipynb** : GWAS with and without MCA for asthma, chronic kidney disease, coronary heart disease, hypercholesterolemia, prostate and breast cancer.
10. **j_GWAS_plots.ipynb** : Plots after performing GWAS (Fig 4 from paper)
