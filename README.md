# Polygenic Risk Score Prediction Using Machine Learning 🧬

Tanzania Vernon

-This project uses machine learning to simulate and optimize Polygenic Risk Scores (PRS) using data from the 1000 Genomes Project.

##Absract
Identifying individuals at elevated risk for disease is a central challenge in genomics. This project applies machine learning to predict disease risk by constructing polygenic risk scores (PRS) from real genetic data sourced from the 1000 Genomes Project. To simulate a polygenic trait, I extracted unique biallelic SNPs from chromosome 1 and assigned each SNP a simulated effect size (β) drawn from a normal distribution. 

Polygenic risk scores were calculated for each individual as the weighted sum of SNP dosages multiplied by these β values. Indiiduals in the top 25% of PRS were labeled as high risk, while the remaining 75% were labeled low risk. This binary classification served as the target variable for training a logistic regression model using SNP genotype data as features. 

The model successfully learned to distinguished high-risk individuals in a purely simulated context, demonstrating the feasibility of using realistic genomic structure to test PRS-based prediction pipelines. By working in a controlled environment with simulated outcomes, I created a flexible framework for experimenting with PS construction, modeling choices, and future extensions using real-world phenotypic labels. 



## Key Features 
- SNP selection an PRS simulation
- Logistic regression modeling
- Performance comparison across multiple SNP set sizes


## Presentaion Slides 

Slides for Project Proposal:(https://docs.google.com/presentation/d/11kkzmFFXPyeSW2X9j4ECWjZ5Iz4L7Jbn54CR8RepZfQ/edit#slide=id.g34d23677ba6_1_40)

Slides for Literature Review: (https://docs.google.com/presentation/d/1fGYBkSskf08zTaSUiWpJyl9JyOsz5Yd--yFTtZCO8Q0/edit?usp=sharing)

Slides for Results: 

Final Project slides: (https://docs.google.com/presentation/d/1K9pWVvPT-lRhS-XT_D8wQJkyqFWiWlKgR_F1na6paNY/edit#slide=id.g3527f96c201_0_2)
