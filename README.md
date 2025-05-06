# Polygenic Risk Score Prediction Using Machine Learning 🧬

Tanzania Vernon

-This project uses machine learning to simulate and optimize Polygenic Risk Scores (PRS) using data from the 1000 Genomes Project.

## Absract
Identifying individuals at elevated risk for disease is a central challenge in genomics. This project applies machine learning to predict disease risk by constructing polygenic risk scores (PRS) from real genetic data sourced from the 1000 Genomes Project. To simulate a polygenic trait, I extracted unique biallelic SNPs from chromosome 1 and assigned each SNP a simulated effect size (β) drawn from a normal distribution. 

Polygenic risk scores were calculated for each individual as the weighted sum of SNP dosages multiplied by these β values. Individuals in the top 25% of PRS were labeled as high risk, while the remaining 75% were labeled low risk. This binary classification served as the target variable for training a logistic regression model using SNP genotype data as features. 

The model successfully learned to distinguished high-risk individuals in a purely simulated context, demonstrating the feasibility of using realistic genomic structure to test PRS-based prediction pipelines. By working in a controlled environment with simulated outcomes, I created a flexible framework for experimenting with PS construction, modeling choices, and future extensions using real-world phenotypic labels. 



## Dataset 
I used real genomic data from the 1000 Genomes Project, a landmark international collaboration that has cataloged human genetic vaiation across global populations. The full dataset includes whole-genome sequencing data from 2,504 individuals reprresenting 26 populations worldwide. 

For this project, we focused on Chromosome 1, extracting biallelic single nucleotide polymorphisms (SNPs) from the publicly available VCF (Variant Call Format) files. SNP dosage data was derived from individuals genotypes, representing the number of alternate alleles (0, 1, or 2) per variant site. 

The choromosome-scale SNP matrix served as the input for simulating disease risk through polygenic risk score (PRS) modleing. The use of real genomic architecture ensures realistic linkage disequilibrium patterns and allel frequency distribution while allowng full control over phenotype simulation. 

The dataset is available here: 
https://www.internationalgenome.org/data

## Methodology 

I developed a polygenic risk scoring pipeline using genomic data and a simulated disease model. I preproceesed the data, simulated risk, and train a predictive model by doing the following: 

1. SNP Extraction
   I extracted uniqu biallelic SNPs from the Chromosome 1 VCF file, representing high-quality, autosomal variants.

2. Effect Size Simulation
   To simulate a complex polygenic trait, I assigned each SNP a synthetic effect size (β value) randomly drawn from a     standard normal distribution. These values represent the simulated contribution of each SNP to disease risk.
3. PRS Calculation
   For each individual, I computed a polygenic risk scor as the sum of :

                       **PRS<sub>i</sub>** = Σ (SNP<sub>ij</sub> × β<sub>j</sub>)
