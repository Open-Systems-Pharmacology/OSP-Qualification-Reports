# Pediatric Qualification Package: CYP2C8 Ontogeny





| Version                         | 1.2-OSP10.0                                                  |
| ------------------------------- | ------------------------------------------------------------ |
| Qualification Plan Release      | https://github.com/Open-Systems-Pharmacology/Pediatric_Qualification_Package_CYP2C8_Ontogeny/releases/tag/v1.2 |
| OSP Version                     | 10.0                                                         |
| Qualification Framework Version | 2.3                                                          |





This qualification report is filed at:

https://github.com/Open-Systems-Pharmacology/OSP-Qualification-Reports
# Table of Contents
  * [1 Introduction to Pediatric Translation](#1-introduction-to-pediatric-translation)
  * [2 Pediatric translation qualification](#2-pediatric-translation-qualification)
    * [2.1 Montelukast PK Ratio tables and Figures](#21-montelukast-pk-ratio-tables-and-figures)
    * [2.2 Montelukast Concentration-Time profiles in Children](#22-montelukast-concentration-time-profiles-in-children)
  * [3 References](#3-references)
# 1 Introduction to Pediatric Translation
The presented qualification report evaluates the predictive performance of the OSP suite to predict cytochrome P450 2C8 (CYP2C8)-mediated drug clearance in children.

Therefore, PBPK models of specific *in vivo* probe substances covering children aged below 6 months up to adolescents were built and evaluated. All models are whole-body PBPK models, allowing for pediatric translation in organs expressing CYP2C8. The qualification report demonstrates the level of confidence of the OSP suite with regard to reliable PBPK predictions of age-related CYP2C8-mediated drug clearance during model-informed drug development. The presented PBPK models as well as the respective qualification plan and qualification report are provided open-source and transparently documented (https://github.com/Open-Systems-Pharmacology/Pediatric_Qualification_Package_CYP2C8_Ontogeny). 


## Translation of Adult PBPK to Children

Using a developed and validated (adult) PBPK model for an *in vivo* probe substance, a pediatric PBPK model can be established for children at different ages by translating physiology, clearance processes (as parameterized in the adult model) and age-dependent protein binding including the variability therein.[[Maharaj 2013](#3-references)] 

The PBPK models are developed with clinical data of healthy adult subjects obtained from the literature, covering available dosing ranges for e.g. intravenous as well as oral administration, to capture both systemic clearance as well gut-wall metabolic clearance processes. For orally administered drugs, the same formulations that are used in children should ideally be included in the model for adults. Plasma concentrations following multiple-dose application, mass balance information and other clinical measurements need to be included for model development, if available. During model translation from adults to children for a specific substance, uncertainties in data-quality caused by impact of disease or the target study population, inaccurate in vitro assay-techniques regarding mass balance, as well as study differences may cause not being able to adequately predict the PK in children for all reported studies. 

Prediction performance of the PBPK model for these probe substances in children are then shown by means of e.g. predicted versus observed area under the plasma concentration (AUC)-ratio plots, of which the results support an adequate prediction of the ontogeny function for the application of PBPK model translation of adult PBPK to children.

For qualification purpose, during the translation of adult PBPK to children the following assumptions and considerations were made: 

- when translating an adult model to children, it was assumed that the metabolism and excretion pathways are qualitatively the same in children and in adults.
- no further changes to input parameters other than those for the physiology and protein binding. All other parameters (e.g. lipophilicity, intestinal permeability, solubility) were kept unchanged.

## Anthropometric and Physiological Information 

Regarding the age-dependencies of the relevant anthropometric (height, weight) and physiological parameters (e.g. blood flows, organ volumes, binding protein concentrations, hematocrit, cardiac output) in children was gathered from the literature and has been previously published. [[Edginton 2006](#3-references)] The information was incorporated into PK-Sim® and was used as default values for the simulations in children.

The CYP2C8 ontogeny function is reported by Upreti et al. [[Upreti 2015](#3-references)] and was integrated into PK-Sim. The ontogeny of CYP2C8 reaches 15% of adult activity at birth, peaks at 260% of adult activity around the age of 14 months and reaches adult activity by the age of 5 to 6 years. The applied ontogeny and variability of other active processes that are integrated into PK-Sim® for translation to children, are described in the publicly available ‘PK-Sim® Ontogeny Database Version 7.3' [[Ontogeny Database](#3-references)]  or otherwise referenced for the specific process.

### Qualification of **CYP2C8 enzyme ontogeny**

To qualify the OSP suite for the pediatric translation of the pharmacokinetics of new drugs that are metabolized by CYP2C8, the following probe substance was included:

- Montelukast [[Montelukast-Model](#3-references)]

The adult PBPK model report and the corresponding PK-Sim project file are filed at: https://github.com/Open-Systems-Pharmacology/OSP-PBPK-Model-Library/


# 2 Pediatric translation qualification
## Evaluation of Pediatric translation

All pediatric translations are pure retrospective predictions, no pediatric pharmacokinetic studies were used to inform model parameters. All parameters necessary to model the pediatric populations, such as demographics (age, weight, height), as well as dosing formulation information were taken from the respective pediatrics studies from literature in order to evaluate their predictive performance. 

The models were evaluated by ratio plots of area under the plasma concentration-time curve (AUC), or clearance (CL) values resulting from our predictions to the values observed during clinical studies, and by comparison of concentration-time profiles if available. As a quantitative measure of the descriptive and predictive performance of each model, the geometric mean fold error was calculated according to Eq. 1:



Eq. 1: GMFE=10^((Σ|log10(pred PK parameter∕obs PK parameter)|)∕n)



with GMFE = geometric mean fold error of all AUC or CL predictions of the respective model, pred PK parameter = predicted AUC or CL, obs PK parameter = observed AUC or CL, and n = number of observed values.

The ratios of predicted over observed mean AUC or CL values from all compound were also plotted across all age groups in the figure below. As illustrated, most of the prediction were within the 0.5 to 2.0 range (2-fold error). 

In the next sections the demographics as well as the evaluation results of the predictive performance of the specific compound PBPK models in children can be found.  


![003_plotPKRatioAUC.png](images/002_2_Pediatric_translation_qualification/003_plotPKRatioAUC.png)

GMFE (AUC) = 1.403890 

|AUC                   |Number|Ratio [%]|
|---------------------:|-----:|--------:|
|Points total          |56    |-        |
|Points within 1.5 fold|36    |64.2857  |
|Points within 2-fold  |50    |89.2857  |

|Study ID    |Age [y] |BodyWeight [kg]|Predicted AUC [ng*h/ml]|Observed AUC [ng*h/ml]|Pred/Obs AUC Ratio|
|-----------:|-------:|--------------:|----------------------:|---------------------:|-----------------:|
|Kearns 2008 |0.083333|4.0417         |20846.5415             |30336.98              |0.68717           |
|Kearns 2008 |0.083333|4.0417         |20846.5415             |29350.14              |0.71027           |
|Kearns 2008 |0.083333|4.0417         |20846.5415             |19481.8               |1.0701            |
|Kearns 2008 |0.083333|4.0417         |20846.5415             |15271.04              |1.3651            |
|Kearns 2008 |0.083333|4.0417         |20846.5415             |14152.63              |1.473             |
|Kearns 2008 |0.16667 |4.5833         |10046.0244             |19490.31              |0.51544           |
|Kearns 2008 |0.16667 |4.5833         |10046.0244             |17384.8               |0.57786           |
|Kearns 2008 |0.16667 |4.5833         |10046.0244             |16069.03              |0.62518           |
|Kearns 2008 |0.16667 |4.5833         |10046.0244             |14555.88              |0.69017           |
|Kearns 2008 |0.16667 |4.5833         |10046.0244             |12845.36              |0.78207           |
|Kearns 2008 |0.16667 |4.5833         |10046.0244             |10016.44              |1.003             |
|Kearns 2008 |0.25    |5.125          |8802.0518              |10024.69              |0.87804           |
|Kearns 2008 |0.25    |5.125          |8802.0518              |8774.445              |1.0031            |
|Kearns 2008 |0.25    |5.125          |8802.0518              |6998.658              |1.2577            |
|Kearns 2008 |0.25    |5.125          |8802.0518              |5419.723              |1.6241            |
|Kearns 2008 |0.25    |5.125          |8802.0518              |5024.989              |1.7517            |
|Kearns 2008 |0.25    |5.125          |8802.0518              |3709.209              |2.373             |
|Kearns 2008 |0.33333 |5.6667         |8681.5629              |9835.066              |0.88272           |
|Kearns 2008 |0.33333 |5.6667         |8681.5629              |6941.125              |1.2507            |
|Kearns 2008 |0.41667 |6.2083         |8698.6969              |10369.89              |0.83884           |
|Kearns 2008 |0.41667 |6.2083         |8698.6969              |9843.322              |0.88372           |
|Kearns 2008 |0.41667 |6.2083         |8698.6969              |6488.084              |1.3407            |
|Kearns 2008 |0.41667 |6.2083         |8698.6969              |3791.252              |2.2944            |
|Kearns 2008 |0.41667 |6.2083         |8698.6969              |3462.049              |2.5126            |
|Kearns 2008 |0.5     |6.75           |9614.077               |6167.911              |1.5587            |
|Kearns 2008 |0.58333 |7.2917         |9805.1205              |11833.5               |0.82859           |
|Kearns 2008 |0.66667 |7.8333         |9987.4783              |10986.76              |0.90905           |
|Kearns 2008 |0.66667 |7.8333         |9987.4783              |10394.92              |0.9608            |
|Kearns 2008 |0.66667 |7.8333         |9987.4783              |8289.154              |1.2049            |
|Kearns 2008 |0.75    |8.375          |10137.9282             |10534.24              |0.96238           |
|Kearns 2008 |0.75    |8.375          |10137.9282             |4612.969              |2.1977            |
|Kearns 2008 |0.83333 |8.9167         |10286.7337             |3897.288              |2.6395            |
|Kearns 2008 |0.91667 |9.4583         |10426.5702             |15879.4               |0.65661           |
|Kearns 2008 |0.91667 |9.4583         |10426.5702             |13116.26              |0.79493           |
|Kearns 2008 |0.91667 |9.4583         |10426.5702             |5155.535              |2.0224            |
|Kearns 2008 |1       |10             |10563.8641             |18848.16              |0.56047           |
|Kearns 2008 |1       |10             |10563.8641             |7334.827              |1.4402            |
|Kearns 2008 |1       |10             |10563.8641             |5690.103              |1.8565            |
|Kearns 2008 |1.1667  |10.375         |10779.5082             |6167.137              |1.7479            |
|Kearns 2008 |1.4167  |10.9375        |11130.8787             |11060.03              |1.0064            |
|Kearns 2008 |1.5833  |11.3125        |11324.8416             |15221.25              |0.74402           |
|Kearns 2008 |1.5833  |11.3125        |11324.8416             |8642.352              |1.3104            |
|Kearns 2008 |1.5833  |11.3125        |11324.8416             |7392.36               |1.532             |
|Kearns 2008 |1.5833  |11.3125        |11324.8416             |5945.002              |1.9049            |
|Kearns 2008 |1.6667  |11.5           |11424.6012             |14374.25              |0.7948            |
|Kearns 2008 |1.6667  |11.5           |11424.6012             |11940.31              |0.95681           |
|Kearns 2008 |1.6667  |11.5           |11424.6012             |11414                 |1.0009            |
|Kearns 2008 |1.6667  |11.5           |11424.6012             |10558.23              |1.0821            |
|Kearns 2008 |1.75    |11.6875        |11520.1464             |12013.84              |0.95891           |
|Kearns 2008 |1.75    |11.6875        |11520.1464             |9250.706              |1.2453            |
|Friesen 2004|11.9    |40.55          |4428.263               |4387.2                |1.0094            |
|Knorr 1999  |7       |26             |3480.9842              |2929                  |1.1885            |
|Knorr 2001  |4       |17             |3382.7539              |2721                  |1.2432            |
|Knorr 2006  |0.33333 |6.8            |5964.2785              |3644.3                |1.6366            |
|Miyoga 2004 |1.5     |9              |4454.6408              |3629.2                |1.2274            |
|Miyoga 2004 |0.75    |9              |4819.056               |2470.9                |1.9503            |

## 2.1 Montelukast PK Ratio tables and Figures
### Montelukast model

Montelukast PBPK predictions in children were evaluated using pharmacokinetic (PK) data reported in the following studies: 

- Knorr B, Holland S, Rogers JD, Nguyen HH, Reiss TF. Montelukast adult (10-mg film-coated tablet) and pediatric (5-mg chewable tablet) dose selections. J Allergy Clin Immunol. 2000 Sep;106(3 Suppl):S171-8.[[Knorr 2000](#3-references)]
- Friesen CA, Kearns GL, Andre L, Neustrom M, Roberts CC, Abdel-Rahman SM. Clinical efficacy and pharmacokinetics of montelukast in dyspeptic children with duodenal eosinophilia. J Pediatr Gastroenterol Nutr. 2004 Mar;38(3):343-51. [[Friesen 2004](#3-references)]
- Kearns GL, Lu S, Maganti L, Li XS, Migoya E, Ahmed T, Knorr B, Reiss TF. Pharmacokinetics and safety of montelukast oral granules in children 1 to 3 months of age with bronchiolitis. J Clin Pharmacol. 2008 Apr;48(4):502-11. doi: 10.1177/0091270008314251. Epub 2008 Feb 22. [[Kearns 2008](#3-references)]
- Knorr B, Nguyen HH, Kearns GL, Villaran C, Boza ML, Reiss TF, Rogers JD, Zhang J, Larson P, Spielberg S. Montelukast dose selection in children ages 2 to 5 years: comparison of population pharmacokinetics between children and adults. J Clin Pharmacol. 2001 Jun;41(6):612-9. [[Knorr 2001](#3-references)]
- Knorr B, Larson P, Nguyen HH, Holland S, Reiss TF, Chervinsky P, Blake K, van Nispen CH, Noonan G, Freeman A, Haesen R, Michiels N, Rogers JD, Amin RD, Zhao J, Xu X, Seidenberg BC, Gertz BJ, Spielberg S. Montelukast dose selection in 6- to 14-year-olds: comparison of single-dose pharmacokinetics in children and adults. J Clin Pharmacol. 1999 Aug;39(8):786-93. [[Knorr 1999](#3-references)]
- Knorr B, Maganti L, Ramakrishnan R, Tozzi CA, Migoya E, Kearns G. Pharmacokinetics and safety of montelukast in children aged 3 to 6 months. J Clin Pharmacol. 2006 Jun;46(6):620-7. [[Knorr 2006](#3-references)]
- Migoya E1, Kearns GL, Hartford A, Zhao J, van Adelsberg J, Tozzi CA, Knorr B, Deutsch P. Pharmacokinetics of montelukast in asthmatic patients 6 to 24 months old. J Clin Pharmacol. 2004 May;44(5):487-94. [[Migoya 2004](#3-references)]

The pediatric PBPK model predicted the clearance values of montelukast observed in pediatric studies reasonably across all available age groups, ranging from 1 month to 11.9 years old. The ratios of mean predicted over observed area under the observed plasma concentrations (AUC) are illustrated in the table below as well as in the predicted versus observed AUC ratio plot, showing that most predictions in children were within 2-fold error of observed values.


![001_plotPKRatioAUC.png](images/002_2_Pediatric_translation_qualification/001_2_1_Montelukast_PK_Ratio_tables_and_Figures/001_plotPKRatioAUC.png)

GMFE (AUC) = 1.403890 

|AUC                   |Number|Ratio [%]|
|---------------------:|-----:|--------:|
|Points total          |56    |-        |
|Points within 1.5 fold|36    |64.2857  |
|Points within 2-fold  |50    |89.2857  |

|Study ID    |Age [y] |BodyWeight [kg]|Predicted AUC [ng*h/ml]|Observed AUC [ng*h/ml]|Pred/Obs AUC Ratio|
|-----------:|-------:|--------------:|----------------------:|---------------------:|-----------------:|
|Kearns 2008 |0.083333|4.0417         |20846.5415             |30336.98              |0.68717           |
|Kearns 2008 |0.083333|4.0417         |20846.5415             |29350.14              |0.71027           |
|Kearns 2008 |0.083333|4.0417         |20846.5415             |19481.8               |1.0701            |
|Kearns 2008 |0.083333|4.0417         |20846.5415             |15271.04              |1.3651            |
|Kearns 2008 |0.083333|4.0417         |20846.5415             |14152.63              |1.473             |
|Kearns 2008 |0.16667 |4.5833         |10046.0244             |19490.31              |0.51544           |
|Kearns 2008 |0.16667 |4.5833         |10046.0244             |17384.8               |0.57786           |
|Kearns 2008 |0.16667 |4.5833         |10046.0244             |16069.03              |0.62518           |
|Kearns 2008 |0.16667 |4.5833         |10046.0244             |14555.88              |0.69017           |
|Kearns 2008 |0.16667 |4.5833         |10046.0244             |12845.36              |0.78207           |
|Kearns 2008 |0.16667 |4.5833         |10046.0244             |10016.44              |1.003             |
|Kearns 2008 |0.25    |5.125          |8802.0518              |10024.69              |0.87804           |
|Kearns 2008 |0.25    |5.125          |8802.0518              |8774.445              |1.0031            |
|Kearns 2008 |0.25    |5.125          |8802.0518              |6998.658              |1.2577            |
|Kearns 2008 |0.25    |5.125          |8802.0518              |5419.723              |1.6241            |
|Kearns 2008 |0.25    |5.125          |8802.0518              |5024.989              |1.7517            |
|Kearns 2008 |0.25    |5.125          |8802.0518              |3709.209              |2.373             |
|Kearns 2008 |0.33333 |5.6667         |8681.5629              |9835.066              |0.88272           |
|Kearns 2008 |0.33333 |5.6667         |8681.5629              |6941.125              |1.2507            |
|Kearns 2008 |0.41667 |6.2083         |8698.6969              |10369.89              |0.83884           |
|Kearns 2008 |0.41667 |6.2083         |8698.6969              |9843.322              |0.88372           |
|Kearns 2008 |0.41667 |6.2083         |8698.6969              |6488.084              |1.3407            |
|Kearns 2008 |0.41667 |6.2083         |8698.6969              |3791.252              |2.2944            |
|Kearns 2008 |0.41667 |6.2083         |8698.6969              |3462.049              |2.5126            |
|Kearns 2008 |0.5     |6.75           |9614.077               |6167.911              |1.5587            |
|Kearns 2008 |0.58333 |7.2917         |9805.1205              |11833.5               |0.82859           |
|Kearns 2008 |0.66667 |7.8333         |9987.4783              |10986.76              |0.90905           |
|Kearns 2008 |0.66667 |7.8333         |9987.4783              |10394.92              |0.9608            |
|Kearns 2008 |0.66667 |7.8333         |9987.4783              |8289.154              |1.2049            |
|Kearns 2008 |0.75    |8.375          |10137.9282             |10534.24              |0.96238           |
|Kearns 2008 |0.75    |8.375          |10137.9282             |4612.969              |2.1977            |
|Kearns 2008 |0.83333 |8.9167         |10286.7337             |3897.288              |2.6395            |
|Kearns 2008 |0.91667 |9.4583         |10426.5702             |15879.4               |0.65661           |
|Kearns 2008 |0.91667 |9.4583         |10426.5702             |13116.26              |0.79493           |
|Kearns 2008 |0.91667 |9.4583         |10426.5702             |5155.535              |2.0224            |
|Kearns 2008 |1       |10             |10563.8641             |18848.16              |0.56047           |
|Kearns 2008 |1       |10             |10563.8641             |7334.827              |1.4402            |
|Kearns 2008 |1       |10             |10563.8641             |5690.103              |1.8565            |
|Kearns 2008 |1.1667  |10.375         |10779.5082             |6167.137              |1.7479            |
|Kearns 2008 |1.4167  |10.9375        |11130.8787             |11060.03              |1.0064            |
|Kearns 2008 |1.5833  |11.3125        |11324.8416             |15221.25              |0.74402           |
|Kearns 2008 |1.5833  |11.3125        |11324.8416             |8642.352              |1.3104            |
|Kearns 2008 |1.5833  |11.3125        |11324.8416             |7392.36               |1.532             |
|Kearns 2008 |1.5833  |11.3125        |11324.8416             |5945.002              |1.9049            |
|Kearns 2008 |1.6667  |11.5           |11424.6012             |14374.25              |0.7948            |
|Kearns 2008 |1.6667  |11.5           |11424.6012             |11940.31              |0.95681           |
|Kearns 2008 |1.6667  |11.5           |11424.6012             |11414                 |1.0009            |
|Kearns 2008 |1.6667  |11.5           |11424.6012             |10558.23              |1.0821            |
|Kearns 2008 |1.75    |11.6875        |11520.1464             |12013.84              |0.95891           |
|Kearns 2008 |1.75    |11.6875        |11520.1464             |9250.706              |1.2453            |
|Friesen 2004|11.9    |40.55          |4428.263               |4387.2                |1.0094            |
|Knorr 1999  |7       |26             |3480.9842              |2929                  |1.1885            |
|Knorr 2001  |4       |17             |3382.7539              |2721                  |1.2432            |
|Knorr 2006  |0.33333 |6.8            |5964.2785              |3644.3                |1.6366            |
|Miyoga 2004 |1.5     |9              |4454.6408              |3629.2                |1.2274            |
|Miyoga 2004 |0.75    |9              |4819.056               |2470.9                |1.9503            |

## 2.2 Montelukast Concentration-Time profiles in Children
#### Concentration-Time Profiles

Predicted versus observed plasma concentration-time profiles are listed below. Only simulations where observed data was available for comparison are shown.  Depending if the observed data were individual data or aggregated data, individual predictions or population predictions including variability are shown, respectively.
![001_plotPopulationTimeProfile.png](images/002_2_Pediatric_translation_qualification/002_2_2_Montelukast_Concentration-Time_profiles_in_Children/001_plotPopulationTimeProfile.png)

![002_plotPopulationTimeProfile.png](images/002_2_Pediatric_translation_qualification/002_2_2_Montelukast_Concentration-Time_profiles_in_Children/002_plotPopulationTimeProfile.png)

# 3 References
**Edginton 2006** Edginton AN, Schmitt W, Willmann S. Development and evaluation of a generic physiologically based pharmacokinetic model for children. Clin Pharmacokinet. 2006;45(10):1013-34.

**Friesen 2004** Friesen CA, Kearns GL, Andre L, Neustrom M, Roberts CC, Abdel-Rahman SM. Clinical efficacy and pharmacokinetics of montelukast in dyspeptic children with duodenal eosinophilia. J Pediatr Gastroenterol Nutr. 2004 Mar;38(3):343-51. 

**Kearns 2008** Kearns GL, Lu S, Maganti L, Li XS, Migoya E, Ahmed T, Knorr B, Reiss TF. Pharmacokinetics and safety of montelukast oral granules in children 1 to 3 months of age with bronchiolitis. J Clin Pharmacol. 2008 Apr;48(4):502-11. doi: 10.1177/0091270008314251. Epub 2008 Feb 22.

**Knorr 1999** Knorr B, Larson P, Nguyen HH, Holland S, Reiss TF, Chervinsky P, Blake K, van Nispen CH, Noonan G, Freeman A, Haesen R, Michiels N, Rogers JD, Amin RD, Zhao J, Xu X, Seidenberg BC, Gertz BJ, Spielberg S. Montelukast dose selection in 6- to 14-year-olds: comparison of single-dose pharmacokinetics in children and adults. J Clin Pharmacol. 1999 Aug;39(8):786-93. 

**Knorr 2000** Knorr B, Holland S, Rogers JD, Nguyen HH, Reiss TF. Montelukast adult (10-mg film-coated tablet) and pediatric (5-mg chewable tablet) dose selections. J Allergy Clin Immunol. 2000 Sep;106(3 Suppl):S171-8.

**Knorr 2001** Knorr B, Nguyen HH, Kearns GL, Villaran C, Boza ML, Reiss TF, Rogers JD, Zhang J, Larson P, Spielberg S. Montelukast dose selection in children ages 2 to 5 years: comparison of population pharmacokinetics between children and adults. J Clin Pharmacol. 2001 Jun;41(6):612-9. 

**Knorr 2006** Knorr B, Maganti L, Ramakrishnan R, Tozzi CA, Migoya E, Kearns G. Pharmacokinetics and safety of montelukast in children aged 3 to 6 months. J Clin Pharmacol. 2006 Jun;46(6):620-7. 

**Maharaj 2013** Maharaj AR, Barrett JS, Edginton AN. A workflow example of PBPK modeling to support pediatric research and development: case study with lorazepam. The AAPS journal. 2013;15(2): 455-464.

**Migoya 2004** Migoya E1, Kearns GL, Hartford A, Zhao J, van Adelsberg J, Tozzi CA, Knorr B, Deutsch P. Pharmacokinetics of montelukast in asthmatic patients 6 to 24 months old. J Clin Pharmacol. 2004 May;44(5):487-94.

**Montelukast-Model** Montelukast-Model, Whole-body PBPK model of Montelukast. (https://github.com/Open-Systems-Pharmacology/Montelukast-Model)

**Ontogeny Database** OSPSuite.Documentation/PK-Sim Ontogeny Database Version 7.3.pdf (https://github.com/Open-Systems-Pharmacology/OSPSuite.Documentation/blob/38cf71b384cfc25cfa0ce4d2f3addfd32757e13b/PK-Sim%20Ontogeny%20Database%20Version%207.3.pdf)

**Upreti 2015** Upreti VV, Wahlstrom JL. Meta-analysis of hepatic cytochrome P450 ontogeny to underwrite the prediction of pediatric pharmacokinetics using physiologically based pharmacokinetic modeling. J Clin Pharmacol. 2016 Mar;56(3):266-83. doi: 10.1002/jcph.585. Epub 2015 Oct 9.
