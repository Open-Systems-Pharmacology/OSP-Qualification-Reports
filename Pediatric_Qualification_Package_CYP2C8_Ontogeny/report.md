# Pediatric Qualification Package: CYP2C8 Ontogeny





| Version                         | 1.1-OSP9.1                                                   |
| ------------------------------- | ------------------------------------------------------------ |
| Qualification Plan Release      | https://github.com/Open-Systems-Pharmacology/Pediatric_Qualification_Package_CYP2C8_Ontogeny/releases/tag/v1.1 |
| OSP Version                     | 9.1                                                          |
| Qualification Framework Version | 2.2                                                          |





This qualification report is filed at:

https://github.com/Open-Systems-Pharmacology/OSP-Qualification-Reports
# Table of Contents
  * [Chapter 1: Introduction to Pediatric Translation](#chapter-1-introduction-to-pediatric-translation)
  * [Chapter 2: Pediatric translation qualification](#chapter-2-pediatric-translation-qualification)
    * [Chapter 2.1: Montelukast PK Ratio tables and Figures](#chapter-21-montelukast-pk-ratio-tables-and-figures)
    * [Chapter 2.2: Montelukast Concentration-Time profiles in Children](#chapter-22-montelukast-concentration-time-profiles-in-children)
  * [Chapter 3: Adult PBPK model performance](#chapter-3-adult-pbpk-model-performance)
    * [Chapter 3.1: Montelukast Input Tables](#chapter-31-montelukast-input-tables)
    * [Chapter 3.2: Montelukast Diagnostics Plots](#chapter-32-montelukast-diagnostics-plots)
    * [Chapter 3.3: Montelukast Concentration-Time profiles in Adults](#chapter-33-montelukast-concentration-time-profiles-in-adults)
# Chapter 1: Introduction to Pediatric Translation
The presented qualification report evaluates the predictive performance of the OSP suite to predict cytochrome P450 2C8 (CYP2C8)-mediated drug clearance in children.

Therefore, PBPK models of specific *in vivo* probe substances covering children aged below 6 months up to adolescents were built and evaluated. All models are whole-body PBPK models, allowing for dynamic pediatric translation in organs expressing CYP2C8. The qualification report demonstrates the level of confidence of the OSP suite with regard to reliable PBPK predictions of age-related CYP2C8-mediated drug clearance during model-informed drug development. The presented PBPK models as well as the respective qualification plan and qualification report are provided open-source and transparently documented (https://github.com/Open-Systems-Pharmacology/Pediatric-Qualification-Package-CYP2C8). 


## Translation of Adult PBPK to Children

Using a developed and validated (adult) PBPK model for an *in vivo* probe substance, a pediatric PBPK model can be established for children by translating physiology, clearance processes (as parameterized in the adult model) and age-dependent protein binding including the variability therein.[[1](#reference)]

The PBPK models are developed with clinical data of healthy adult subjects obtained from the literature, covering available dosing ranges for e.g. intravenous as well as oral administration, to capture both systemic clearance as well gut-wall metabolic clearance processes. For orally administered drugs, the same formulations that are used in children should ideally be included in the model for adults. Plasma concentrations following multiple-dose application, mass balance information and other clinical measurements need to be included for model development, if available. During model translation from adults to children for a specific substance, uncertainties in data-quality caused by impact of disease or the target study population, inaccurate in vitro assay-techniques regarding mass balance, as well as study differences may cause not being able to adequately predict the PK in children for all reported studies. 

Prediction performance of the PBPK model for these probe substances in children are then shown by means of e.g. predicted versus observed area under the plasma concentration (AUC)-ratio plots, of which the results support an adequate prediction of the ontogeny function for the application of PBPK model translation of adult PBPK to children.

For qualification purpose, during the translation of adult PBPK to children the following assumptions and considerations were made: 

- when translating an adult model to children, it was assumed that the metabolism and excretion pathways are qualitatively the same in children and in adults.
- no further changes to input parameters other than those for the physiology and protein binding. All other parameters (e.g. lipophilicity, intestinal permeability, solubility) were kept unchanged.

## Anthropometric and Physiological Information 

Regarding the age-dependencies of the relevant anthropometric (height, weight) and physiological parameters (e.g. blood flows, organ volumes, binding protein concentrations, hematocrit, cardiac output) in children was gathered from the literature and has been previously published [[2](#reference)]. The information was incorporated into PK-Sim® and was used as default values for the simulations in children.

The CYP2C8 ontogeny function is reported by Upreti et al. [[3](#reference)] and was integrated into PK-Sim. The ontogeny of CYP2C8 reaches 15% of adult activity at birth, peaks at 260% of adult activity around the age of 14 months and reaches adult activity by the age of 5 to 6 years. The applied ontogeny and variability of other active processes that are integrated into PK-Sim® for translation to children, are described in the publicly available ‘PK-Sim® Ontogeny Database Version 7.3' [[4](#reference)] or otherwise referenced for the specific process.

### Qualification of **CYP2C8 enzyme ontogeny**

To qualify the OSP suite for the pediatric translation of the pharmacokinetics of new drugs that are metabolized by CYP2C8, the following probe substance was included:

- Montelukast [[5](#reference)]

### References

[1] [Maharaj AR, Barrett JS, Edginton AN. A workflow example of PBPK modeling to support pediatric research and development: case study with lorazepam. The AAPS journal. 2013;15(2): 455-464.](https://www.ncbi.nlm.nih.gov/pubmed/23344790)

[2] [Edginton AN, Schmitt W, Willmann S. Development and evaluation of a generic physiologically based pharmacokinetic model for children. Clin Pharmacokinet. 2006;45(10):1013-34.](https://www.ncbi.nlm.nih.gov/pubmed/16984214)

[3] [Upreti VV, Wahlstrom JL. Meta-analysis of hepatic cytochrome P450 ontogeny to underwrite the prediction of pediatric pharmacokinetics using physiologically based pharmacokinetic modeling. J Clin Pharmacol. 2016 Mar;56(3):266-83. doi: 10.1002/jcph.585. Epub 2015 Oct 9.](https://www.ncbi.nlm.nih.gov/pubmed/26139104)

[4]  [OSPSuite.Documentation/PK-Sim Ontogeny Database Version 7.3.pdf ](https://github.com/Open-Systems-Pharmacology/OSPSuite.Documentation/blob/38cf71b384cfc25cfa0ce4d2f3addfd32757e13b/PK-Sim%20Ontogeny%20Database%20Version%207.3.pdf)

[5] [Montelukast-Model, Whole-body PBPK model of Montelukast. https://github.com/Open-Systems-Pharmacology/Montelukast-Model](https://github.com/incei/Montelukast-Model)


# Chapter 2: Pediatric translation qualification
## Evaluation of Pediatric translation

All pediatric translations are pure retrospective predictions, no pediatric pharmacokinetic studies were used to inform model parameters. All parameters necessary to model the pediatric populations, such as demographics (age, weight, height), as well as dosing formulation information were taken from the respective pediatrics studies from literature in order to evaluate their predictive performance. 

The models were evaluated by ratio plots of area under the plasma concentration-time curve (AUC), or clearance (CL) values resulting from our predictions to the values observed during clinical studies, and by comparison of concentration-time profiles if available. As a quantitative measure of the descriptive and predictive performance of each model, the geometric mean fold error was calculated according to Eq. 1:



Eq. 1: GMFE=10^((Σ|log10(pred PK parameter∕obs PK parameter)|)∕n)



with GMFE = geometric mean fold error of all AUC or CL predictions of the respective model, pred PK parameter = predicted AUC or CL, obs PK parameter = observed AUC or CL, and n = number of observed values.

The ratios of predicted over observed mean AUC or CL values from all compound were also plotted across all age groups in the figure below. As illustrated, most of the prediction were within the 0.5 to 2.0 range (2-fold error). 

In the next sections the demographics as well as the evaluation results of the predictive performance of the specific compound PBPK models in children can be found.  


![003_plotPKRatioAUC.png](images/002_Chapter_2__Pediatric_translation_qualification/003_plotPKRatioAUC.png)

GMFE (AUC) = 1.403891 

|AUC                   |Number|Ratio [%]|
|---------------------:|-----:|--------:|
|Points total          |56    |-        |
|Points within 1.5 fold|36    |64.2857  |
|Points within 2-fold  |50    |89.2857  |

|Study ID    |Age [y] |BodyWeight [kg]|Predicted AUC [ng*h/ml]|Observed AUC [ng*h/ml]|Pred/Obs AUC Ratio|
|-----------:|-------:|--------------:|----------------------:|---------------------:|-----------------:|
|Kearns 2008 |0.083333|4.0417         |0.68716                |30336.98              |0.68716           |
|Kearns 2008 |0.083333|4.0417         |0.71027                |29350.14              |0.71027           |
|Kearns 2008 |0.083333|4.0417         |1.07                   |19481.8               |1.07              |
|Kearns 2008 |0.083333|4.0417         |1.3651                 |15271.04              |1.3651            |
|Kearns 2008 |0.083333|4.0417         |1.473                  |14152.63              |1.473             |
|Kearns 2008 |0.16667 |4.5833         |0.51544                |19490.31              |0.51544           |
|Kearns 2008 |0.16667 |4.5833         |0.57786                |17384.8               |0.57786           |
|Kearns 2008 |0.16667 |4.5833         |0.62518                |16069.03              |0.62518           |
|Kearns 2008 |0.16667 |4.5833         |0.69017                |14555.88              |0.69017           |
|Kearns 2008 |0.16667 |4.5833         |0.78207                |12845.36              |0.78207           |
|Kearns 2008 |0.16667 |4.5833         |1.003                  |10016.44              |1.003             |
|Kearns 2008 |0.25    |5.125          |0.87804                |10024.69              |0.87804           |
|Kearns 2008 |0.25    |5.125          |1.0031                 |8774.445              |1.0031            |
|Kearns 2008 |0.25    |5.125          |1.2577                 |6998.658              |1.2577            |
|Kearns 2008 |0.25    |5.125          |1.6241                 |5419.723              |1.6241            |
|Kearns 2008 |0.25    |5.125          |1.7517                 |5024.989              |1.7517            |
|Kearns 2008 |0.25    |5.125          |2.373                  |3709.209              |2.373             |
|Kearns 2008 |0.33333 |5.6667         |0.88272                |9835.066              |0.88272           |
|Kearns 2008 |0.33333 |5.6667         |1.2507                 |6941.125              |1.2507            |
|Kearns 2008 |0.41667 |6.2083         |0.83884                |10369.89              |0.83884           |
|Kearns 2008 |0.41667 |6.2083         |0.88372                |9843.322              |0.88372           |
|Kearns 2008 |0.41667 |6.2083         |1.3407                 |6488.084              |1.3407            |
|Kearns 2008 |0.41667 |6.2083         |2.2944                 |3791.252              |2.2944            |
|Kearns 2008 |0.41667 |6.2083         |2.5126                 |3462.049              |2.5126            |
|Kearns 2008 |0.5     |6.75           |1.5587                 |6167.911              |1.5587            |
|Kearns 2008 |0.58333 |7.2917         |0.82859                |11833.5               |0.82859           |
|Kearns 2008 |0.66667 |7.8333         |0.90905                |10986.76              |0.90905           |
|Kearns 2008 |0.66667 |7.8333         |0.9608                 |10394.92              |0.9608            |
|Kearns 2008 |0.66667 |7.8333         |1.2049                 |8289.154              |1.2049            |
|Kearns 2008 |0.75    |8.375          |0.96238                |10534.24              |0.96238           |
|Kearns 2008 |0.75    |8.375          |2.1977                 |4612.969              |2.1977            |
|Kearns 2008 |0.83333 |8.9167         |2.6395                 |3897.288              |2.6395            |
|Kearns 2008 |0.91667 |9.4583         |0.65661                |15879.4               |0.65661           |
|Kearns 2008 |0.91667 |9.4583         |0.79493                |13116.26              |0.79493           |
|Kearns 2008 |0.91667 |9.4583         |2.0224                 |5155.535              |2.0224            |
|Kearns 2008 |1       |10             |0.56047                |18848.16              |0.56047           |
|Kearns 2008 |1       |10             |1.4402                 |7334.827              |1.4402            |
|Kearns 2008 |1       |10             |1.8565                 |5690.103              |1.8565            |
|Kearns 2008 |1.1667  |10.375         |1.7479                 |6167.137              |1.7479            |
|Kearns 2008 |1.4167  |10.9375        |1.0064                 |11060.03              |1.0064            |
|Kearns 2008 |1.5833  |11.3125        |0.74402                |15221.25              |0.74402           |
|Kearns 2008 |1.5833  |11.3125        |1.3104                 |8642.352              |1.3104            |
|Kearns 2008 |1.5833  |11.3125        |1.532                  |7392.36               |1.532             |
|Kearns 2008 |1.5833  |11.3125        |1.9049                 |5945.002              |1.9049            |
|Kearns 2008 |1.6667  |11.5           |0.79479                |14374.25              |0.79479           |
|Kearns 2008 |1.6667  |11.5           |0.95681                |11940.31              |0.95681           |
|Kearns 2008 |1.6667  |11.5           |1.0009                 |11414                 |1.0009            |
|Kearns 2008 |1.6667  |11.5           |1.0821                 |10558.23              |1.0821            |
|Kearns 2008 |1.75    |11.6875        |0.95891                |12013.84              |0.95891           |
|Kearns 2008 |1.75    |11.6875        |1.2453                 |9250.706              |1.2453            |
|Friesen 2004|11.9    |40.55          |1.0094                 |4387.2                |1.0094            |
|Knorr 1999  |7       |26             |1.1885                 |2929                  |1.1885            |
|Knorr 2001  |4       |17             |1.2432                 |2721                  |1.2432            |
|Knorr 2006  |0.33333 |6.8            |1.6366                 |3644.3                |1.6366            |
|Miyoga 2004 |1.5     |9              |1.2274                 |3629.2                |1.2274            |
|Miyoga 2004 |0.75    |9              |1.9503                 |2470.9                |1.9503            |

## Chapter 2.1: Montelukast PK Ratio tables and Figures
### Montelukast model

Montelukast PBPK predictions in children were evaluated using pharmacokinetic (PK) data reported in the following studies: 

- Knorr B, Holland S, Rogers JD, Nguyen HH, Reiss TF. Montelukast adult (10-mg film-coated tablet) and pediatric (5-mg chewable tablet) dose selections. J Allergy Clin Immunol. 2000 Sep;106(3 Suppl):S171-8.
- Friesen CA, Kearns GL, Andre L, Neustrom M, Roberts CC, Abdel-Rahman SM. Clinical efficacy and pharmacokinetics of montelukast in dyspeptic children with duodenal eosinophilia. J Pediatr Gastroenterol Nutr. 2004 Mar;38(3):343-51.
- Kearns GL, Lu S, Maganti L, Li XS, Migoya E, Ahmed T, Knorr B, Reiss TF. Pharmacokinetics and safety of montelukast oral granules in children 1 to 3 months of age with bronchiolitis. J Clin Pharmacol. 2008 Apr;48(4):502-11. doi: 10.1177/0091270008314251. Epub 2008 Feb 22.
- Knorr B, Nguyen HH, Kearns GL, Villaran C, Boza ML, Reiss TF, Rogers JD, Zhang J, Larson P, Spielberg S. Montelukast dose selection in children ages 2 to 5 years: comparison of population pharmacokinetics between children and adults. J Clin Pharmacol. 2001 Jun;41(6):612-9.
- Knorr B, Larson P, Nguyen HH, Holland S, Reiss TF, Chervinsky P, Blake K, van Nispen CH, Noonan G, Freeman A, Haesen R, Michiels N, Rogers JD, Amin RD, Zhao J, Xu X, Seidenberg BC, Gertz BJ, Spielberg S. Montelukast dose selection in 6- to 14-year-olds: comparison of single-dose pharmacokinetics in children and adults. J Clin Pharmacol. 1999 Aug;39(8):786-93.
- Knorr B, Maganti L, Ramakrishnan R, Tozzi CA, Migoya E, Kearns G. Pharmacokinetics and safety of montelukast in children aged 3 to 6 months. J Clin Pharmacol. 2006 Jun;46(6):620-7.
- Migoya E1, Kearns GL, Hartford A, Zhao J, van Adelsberg J, Tozzi CA, Knorr B, Deutsch P. Pharmacokinetics of montelukast in asthmatic patients 6 to 24 months old. J Clin Pharmacol. 2004 May;44(5):487-94.

The pediatric PBPK model predicted the clearance values of montelukast observed in pediatric studies reasonably across all available age groups, ranging from 1 month to 11.9 years old. The ratios of mean predicted over observed area under the observed plasma concentrations (AUC) are illustrated in the table below as well as in the predicted versus observed AUC ratio plot, showing that most predictions in children were within 2-fold error of observed values.


![001_plotPKRatioAUC.png](images/002_Chapter_2__Pediatric_translation_qualification/001_Chapter_2_1__Montelukast_PK_Ratio_tables_and_Figures/001_plotPKRatioAUC.png)

GMFE (AUC) = 1.403891 

|AUC                   |Number|Ratio [%]|
|---------------------:|-----:|--------:|
|Points total          |56    |-        |
|Points within 1.5 fold|36    |64.2857  |
|Points within 2-fold  |50    |89.2857  |

|Study ID    |Age [y] |BodyWeight [kg]|Predicted AUC [ng*h/ml]|Observed AUC [ng*h/ml]|Pred/Obs AUC Ratio|
|-----------:|-------:|--------------:|----------------------:|---------------------:|-----------------:|
|Kearns 2008 |0.083333|4.0417         |0.68716                |30336.98              |0.68716           |
|Kearns 2008 |0.083333|4.0417         |0.71027                |29350.14              |0.71027           |
|Kearns 2008 |0.083333|4.0417         |1.07                   |19481.8               |1.07              |
|Kearns 2008 |0.083333|4.0417         |1.3651                 |15271.04              |1.3651            |
|Kearns 2008 |0.083333|4.0417         |1.473                  |14152.63              |1.473             |
|Kearns 2008 |0.16667 |4.5833         |0.51544                |19490.31              |0.51544           |
|Kearns 2008 |0.16667 |4.5833         |0.57786                |17384.8               |0.57786           |
|Kearns 2008 |0.16667 |4.5833         |0.62518                |16069.03              |0.62518           |
|Kearns 2008 |0.16667 |4.5833         |0.69017                |14555.88              |0.69017           |
|Kearns 2008 |0.16667 |4.5833         |0.78207                |12845.36              |0.78207           |
|Kearns 2008 |0.16667 |4.5833         |1.003                  |10016.44              |1.003             |
|Kearns 2008 |0.25    |5.125          |0.87804                |10024.69              |0.87804           |
|Kearns 2008 |0.25    |5.125          |1.0031                 |8774.445              |1.0031            |
|Kearns 2008 |0.25    |5.125          |1.2577                 |6998.658              |1.2577            |
|Kearns 2008 |0.25    |5.125          |1.6241                 |5419.723              |1.6241            |
|Kearns 2008 |0.25    |5.125          |1.7517                 |5024.989              |1.7517            |
|Kearns 2008 |0.25    |5.125          |2.373                  |3709.209              |2.373             |
|Kearns 2008 |0.33333 |5.6667         |0.88272                |9835.066              |0.88272           |
|Kearns 2008 |0.33333 |5.6667         |1.2507                 |6941.125              |1.2507            |
|Kearns 2008 |0.41667 |6.2083         |0.83884                |10369.89              |0.83884           |
|Kearns 2008 |0.41667 |6.2083         |0.88372                |9843.322              |0.88372           |
|Kearns 2008 |0.41667 |6.2083         |1.3407                 |6488.084              |1.3407            |
|Kearns 2008 |0.41667 |6.2083         |2.2944                 |3791.252              |2.2944            |
|Kearns 2008 |0.41667 |6.2083         |2.5126                 |3462.049              |2.5126            |
|Kearns 2008 |0.5     |6.75           |1.5587                 |6167.911              |1.5587            |
|Kearns 2008 |0.58333 |7.2917         |0.82859                |11833.5               |0.82859           |
|Kearns 2008 |0.66667 |7.8333         |0.90905                |10986.76              |0.90905           |
|Kearns 2008 |0.66667 |7.8333         |0.9608                 |10394.92              |0.9608            |
|Kearns 2008 |0.66667 |7.8333         |1.2049                 |8289.154              |1.2049            |
|Kearns 2008 |0.75    |8.375          |0.96238                |10534.24              |0.96238           |
|Kearns 2008 |0.75    |8.375          |2.1977                 |4612.969              |2.1977            |
|Kearns 2008 |0.83333 |8.9167         |2.6395                 |3897.288              |2.6395            |
|Kearns 2008 |0.91667 |9.4583         |0.65661                |15879.4               |0.65661           |
|Kearns 2008 |0.91667 |9.4583         |0.79493                |13116.26              |0.79493           |
|Kearns 2008 |0.91667 |9.4583         |2.0224                 |5155.535              |2.0224            |
|Kearns 2008 |1       |10             |0.56047                |18848.16              |0.56047           |
|Kearns 2008 |1       |10             |1.4402                 |7334.827              |1.4402            |
|Kearns 2008 |1       |10             |1.8565                 |5690.103              |1.8565            |
|Kearns 2008 |1.1667  |10.375         |1.7479                 |6167.137              |1.7479            |
|Kearns 2008 |1.4167  |10.9375        |1.0064                 |11060.03              |1.0064            |
|Kearns 2008 |1.5833  |11.3125        |0.74402                |15221.25              |0.74402           |
|Kearns 2008 |1.5833  |11.3125        |1.3104                 |8642.352              |1.3104            |
|Kearns 2008 |1.5833  |11.3125        |1.532                  |7392.36               |1.532             |
|Kearns 2008 |1.5833  |11.3125        |1.9049                 |5945.002              |1.9049            |
|Kearns 2008 |1.6667  |11.5           |0.79479                |14374.25              |0.79479           |
|Kearns 2008 |1.6667  |11.5           |0.95681                |11940.31              |0.95681           |
|Kearns 2008 |1.6667  |11.5           |1.0009                 |11414                 |1.0009            |
|Kearns 2008 |1.6667  |11.5           |1.0821                 |10558.23              |1.0821            |
|Kearns 2008 |1.75    |11.6875        |0.95891                |12013.84              |0.95891           |
|Kearns 2008 |1.75    |11.6875        |1.2453                 |9250.706              |1.2453            |
|Friesen 2004|11.9    |40.55          |1.0094                 |4387.2                |1.0094            |
|Knorr 1999  |7       |26             |1.1885                 |2929                  |1.1885            |
|Knorr 2001  |4       |17             |1.2432                 |2721                  |1.2432            |
|Knorr 2006  |0.33333 |6.8            |1.6366                 |3644.3                |1.6366            |
|Miyoga 2004 |1.5     |9              |1.2274                 |3629.2                |1.2274            |
|Miyoga 2004 |0.75    |9              |1.9503                 |2470.9                |1.9503            |

## Chapter 2.2: Montelukast Concentration-Time profiles in Children
#### Concentration-Time Profiles

Predicted versus observed plasma concentration-time profiles are listed below. Only simulations where observed data was available for comparison are shown.  Depending if the observed data were individual data or aggregated data, individual predictions or population predictions including variability are shown, respectively.
![001_plotPopulationTimeProfile.png](images/002_Chapter_2__Pediatric_translation_qualification/002_Chapter_2_2__Montelukast_Concentration-Time_profiles_in_Children/001_plotPopulationTimeProfile.png)

![002_plotPopulationTimeProfile.png](images/002_Chapter_2__Pediatric_translation_qualification/002_Chapter_2_2__Montelukast_Concentration-Time_profiles_in_Children/002_plotPopulationTimeProfile.png)

# Chapter 3: Adult PBPK model performance
## Evaluation of Adult PBPK models

The PBPK model of **montelukast** was developed with clinical pharmacokinetic data covering at least administrations given in children. Plasma concentrations following intravenous administration, oral administration, multiple dose application, fractions excreted to urine or bile and other clinical measurements were included for model development whenever available. 


## Chapter 3.1: Montelukast Input Tables
### Montelukast adult PBPK model

Montelukast is a selective and orally active leukotriene receptor antagonist that inhibits the cysteinyl leukotriene 'CysLT' receptor 1', used in the maintenance treatment of asthma. Montelukast is mainly metabolized by CYP2C8 (72%) [1].  Montelukast is a strongly lipophilic drug. The final lipophilicity was estimated to be lower than the reported values, as with lipophilicity values above 3-4 the drug already reached maximal permeability levels. The final montelukast model applies metabolism by CYP2C8, and minor involved enzymesCYP3A4/5 (16% ) CYP2C9 (12%) and glomerular filtration [1-3] and adequately described the pharmacokinetics of montelukast in adults.

The montelukast model was developed using data of the following publications:

- Bovill JG, Sebel PS, Blackburn CL, Oei-Lim V, Heykants JJ. The pharmacokinetics of sufentanil in surgical patients. Anesthesiology. 1984 Nov;61(5):502-6. (https://www.ncbi.nlm.nih.gov/pubmed/6238552)
- Knorr B, Holland S, Rogers JD, Nguyen HH, Reiss TF. Montelukast adult (10-mg film-coated tablet) and pediatric (5-mg chewable tablet) dose selections. J Allergy Clin Immunol. 2000 Sep;106(3 Suppl):S171-8.
(https://www.ncbi.nlm.nih.gov/pubmed/10984399)
- Zhao JJ, Rogers JD, Holland SD, Larson P, Amin RD, Haesen R, Freeman A, Seiberling M, Merz M, Cheng H. Pharmacokinetics and bioavailability of montelukast sodium (MK-0476) in healthy young and elderly volunteers.Biopharm Drug Dispos. 1997 Dec;18(9):769-77.
(https://www.ncbi.nlm.nih.gov/pubmed/9429741)
- Fey C, Thyroff-Friesinger U, Jones S. Bioequivalence of two formulations of montelukast sodium 4 mg oral granules in healthy adults. Clin Transl Allergy. 2014 Sep 18;4:29. doi: 10.1186/2045-7022-4-29. eCollection 2014.
https://www.ncbi.nlm.nih.gov/pubmed/25250173
- Cheng H, Leff JA, Amin R, Gertz BJ, De Smet M, Noonan N, Rogers JD, Malbecq W, Meisner D, Somers G. Pharmacokinetics, bioavailability, and safety of montelukast sodium (MK-0476) in healthy males and females. Pharm Res. 1996 Mar;13(3):445-8.
https://www.ncbi.nlm.nih.gov/pubmed/8692739

### References
[1] Marzolini C, Rajoli R, Battegay M, Elzi L, Back D, Siccardi M. Efavirenz Involving Simultaneous Inducing and Inhibitory Effects on Cytochromes. Clin Pharmacokinet. 2017 Apr;56(4):409-420. doi: 10.1007/s40262-016-0447-7.

[2] Filppula AM, Laitila J, Neuvonen PJ, Backman JT. Reevaluation of the microsomal metabolism of montelukast: major contribution by CYP2C8 at clinically relevant concentrations. Drug Metab Dispos. 2011 May;39(5):904-11. doi: 10.1124/dmd.110.037689. Epub 2011 Feb 2.

[3] Zhou W, Johnson TN, Bui KH, Cheung SYA, Li J, Xu H, Al-Huniti N, Zhou D. Predictive Performance of Physiologically Based Pharmacokinetic (PBPK) Modeling of Drugs Extensively Metabolized by Major Cytochrome P450s in Children. Clin Pharmacol Ther. 2018 Jul;104(1):188-200. doi: 10.1002/cpt.905. Epub 2017 Nov 20.

The compound properties used for input are illustrated below.
### Compound: Montelukast

#### Parameters

Name                                             | Value                  | Value Origin                                      | Alternative               | Default
------------------------------------------------ | ---------------------- | ------------------------------------------------- | ------------------------- | -------
Solubility at reference pH                       | 8.2E-06 mg/ml          | Internet-source: Drugbank (ALOGPS)                | Water Solubility (ALOGPS) | True   
Reference pH                                     | 7                      | Internet-source: Drugbank (ALOGPS)                | Water Solubility (ALOGPS) | True   
Lipophilicity                                    | 3.3153408097 Log Units | Parameter Identification-Parameter Identification | Fit                       | True   
Fraction unbound (plasma, reference value)       | 0.0018                 | Publication-Marzolini 2017                        | Marzolini 2017            | True   
Specific intestinal permeability (transcellular) | 0.0819181318 cm/min    | Parameter Identification-Parameter Identification | Fit                       | True   
Cl                                               | 1                      | Publication-Marzolini 2017                        |                           |        
Is small molecule                                | Yes                    |                                                   |                           |        
Molecular weight                                 | 586.2 g/mol            | Publication-Marzolini 2017                        |                           |        
Plasma protein binding partner                   | Albumin                |                                                   |                           |        
#### Calculation methods

Name                    | Value              
----------------------- | -------------------
Partition coefficients  | Rodgers and Rowland
Cellular permeabilities | PK-Sim Standard    
#### Processes

##### Metabolizing Enzyme: CYP2C8-Marzolini 2017

Molecule: CYP2C8
###### Parameters

Name                           | Value                       | Value Origin              
------------------------------ | --------------------------- | --------------------------
In vitro CL/recombinant enzyme | 3.6 µl/min/pmol rec. enzyme | Publication-Marzolini 2017
##### Metabolizing Enzyme: CYP3A4-Marzolini 2017

Molecule: CYP3A4
###### Parameters

Name                           | Value                       | Value Origin              
------------------------------ | --------------------------- | --------------------------
In vitro CL/recombinant enzyme | 1.8 µl/min/pmol rec. enzyme | Publication-Marzolini 2017
##### Metabolizing Enzyme: CYP2C9-Marzolini 2017

Molecule: CYP2C9
###### Parameters

Name                           | Value                        | Value Origin              
------------------------------ | ---------------------------- | --------------------------
In vitro CL/recombinant enzyme | 0.48 µl/min/pmol rec. enzyme | Publication-Marzolini 2017
##### Metabolizing Enzyme: CYP3A5-Filppula 2011

Molecule: CYP3A5
###### Parameters

Name                           | Value                        | Value Origin              
------------------------------ | ---------------------------- | --------------------------
In vitro CL/recombinant enzyme | 0.16 µl/min/pmol rec. enzyme | Publication-Marzolini 2017
##### Systemic Process: Glomerular Filtration-Marzolini 2017

Species: Human
###### Parameters

Name         | Value | Value Origin              
------------ | -----:| --------------------------
GFR fraction |     1 | Publication-Marzolini 2017
##### Systemic Process: Total Hepatic Clearance-Literatur (Cheng 1996)

Species: Human
###### Parameters

Name                          | Value                 | Value Origin                  
----------------------------- | --------------------- | ------------------------------
Body weight                   | 76.5 kg               | Publication-In Vivo-Cheng 1996
Fraction unbound (experiment) | 0.0018                |                               
Lipophilicity (experiment)    | 7.9 Log Units         |                               
Plasma clearance              | 0.608496732 ml/min/kg | Publication-In Vivo-Cheng 1996

## Chapter 3.2: Montelukast Diagnostics Plots
### Montelukast adult PBPK model performance

Below you find the input goodness-of-fit visual diagnostic plots for montelukast PBPK model performance (observed versus individually predicted plasma concentration and weighted residuals versus time) of all adult data.

![001_plotGOFMergedPredictedVsObserved.png](images/003_Chapter_3__Adult_PBPK_model_performance/002_Chapter_3_2__Montelukast_Diagnostics_Plots/001_plotGOFMergedPredictedVsObserved.png)

GMFE = 1.311215 

![003_plotGOFMergedResidualsOverTime.png](images/003_Chapter_3__Adult_PBPK_model_performance/002_Chapter_3_2__Montelukast_Diagnostics_Plots/003_plotGOFMergedResidualsOverTime.png)

GMFE = 1.311215 

## Chapter 3.3: Montelukast Concentration-Time profiles in Adults
#### Concentration-Time Profiles

Simulated versus observed plasma concentration-time profiles of all data are listed below.
![001_plotTimeProfile.png](images/003_Chapter_3__Adult_PBPK_model_performance/003_Chapter_3_3__Montelukast_Concentration-Time_profiles_in_Adults/001_plotTimeProfile.png)

![002_plotTimeProfile.png](images/003_Chapter_3__Adult_PBPK_model_performance/003_Chapter_3_3__Montelukast_Concentration-Time_profiles_in_Adults/002_plotTimeProfile.png)

![003_plotTimeProfile.png](images/003_Chapter_3__Adult_PBPK_model_performance/003_Chapter_3_3__Montelukast_Concentration-Time_profiles_in_Adults/003_plotTimeProfile.png)

![004_plotTimeProfile.png](images/003_Chapter_3__Adult_PBPK_model_performance/003_Chapter_3_3__Montelukast_Concentration-Time_profiles_in_Adults/004_plotTimeProfile.png)

![005_plotTimeProfile.png](images/003_Chapter_3__Adult_PBPK_model_performance/003_Chapter_3_3__Montelukast_Concentration-Time_profiles_in_Adults/005_plotTimeProfile.png)

![006_plotTimeProfile.png](images/003_Chapter_3__Adult_PBPK_model_performance/003_Chapter_3_3__Montelukast_Concentration-Time_profiles_in_Adults/006_plotTimeProfile.png)

![007_plotTimeProfile.png](images/003_Chapter_3__Adult_PBPK_model_performance/003_Chapter_3_3__Montelukast_Concentration-Time_profiles_in_Adults/007_plotTimeProfile.png)

![008_plotTimeProfile.png](images/003_Chapter_3__Adult_PBPK_model_performance/003_Chapter_3_3__Montelukast_Concentration-Time_profiles_in_Adults/008_plotTimeProfile.png)

![009_plotTimeProfile.png](images/003_Chapter_3__Adult_PBPK_model_performance/003_Chapter_3_3__Montelukast_Concentration-Time_profiles_in_Adults/009_plotTimeProfile.png)

![010_plotTimeProfile.png](images/003_Chapter_3__Adult_PBPK_model_performance/003_Chapter_3_3__Montelukast_Concentration-Time_profiles_in_Adults/010_plotTimeProfile.png)

![011_plotTimeProfile.png](images/003_Chapter_3__Adult_PBPK_model_performance/003_Chapter_3_3__Montelukast_Concentration-Time_profiles_in_Adults/011_plotTimeProfile.png)

![012_plotTimeProfile.png](images/003_Chapter_3__Adult_PBPK_model_performance/003_Chapter_3_3__Montelukast_Concentration-Time_profiles_in_Adults/012_plotTimeProfile.png)

![013_plotTimeProfile.png](images/003_Chapter_3__Adult_PBPK_model_performance/003_Chapter_3_3__Montelukast_Concentration-Time_profiles_in_Adults/013_plotTimeProfile.png)

![014_plotTimeProfile.png](images/003_Chapter_3__Adult_PBPK_model_performance/003_Chapter_3_3__Montelukast_Concentration-Time_profiles_in_Adults/014_plotTimeProfile.png)

![015_plotTimeProfile.png](images/003_Chapter_3__Adult_PBPK_model_performance/003_Chapter_3_3__Montelukast_Concentration-Time_profiles_in_Adults/015_plotTimeProfile.png)

![016_plotTimeProfile.png](images/003_Chapter_3__Adult_PBPK_model_performance/003_Chapter_3_3__Montelukast_Concentration-Time_profiles_in_Adults/016_plotTimeProfile.png)

![017_plotTimeProfile.png](images/003_Chapter_3__Adult_PBPK_model_performance/003_Chapter_3_3__Montelukast_Concentration-Time_profiles_in_Adults/017_plotTimeProfile.png)

![018_plotTimeProfile.png](images/003_Chapter_3__Adult_PBPK_model_performance/003_Chapter_3_3__Montelukast_Concentration-Time_profiles_in_Adults/018_plotTimeProfile.png)

![019_plotTimeProfile.png](images/003_Chapter_3__Adult_PBPK_model_performance/003_Chapter_3_3__Montelukast_Concentration-Time_profiles_in_Adults/019_plotTimeProfile.png)

![020_plotTimeProfile.png](images/003_Chapter_3__Adult_PBPK_model_performance/003_Chapter_3_3__Montelukast_Concentration-Time_profiles_in_Adults/020_plotTimeProfile.png)

![021_plotTimeProfile.png](images/003_Chapter_3__Adult_PBPK_model_performance/003_Chapter_3_3__Montelukast_Concentration-Time_profiles_in_Adults/021_plotTimeProfile.png)

![022_plotTimeProfile.png](images/003_Chapter_3__Adult_PBPK_model_performance/003_Chapter_3_3__Montelukast_Concentration-Time_profiles_in_Adults/022_plotTimeProfile.png)

![023_plotTimeProfile.png](images/003_Chapter_3__Adult_PBPK_model_performance/003_Chapter_3_3__Montelukast_Concentration-Time_profiles_in_Adults/023_plotTimeProfile.png)

![024_plotTimeProfile.png](images/003_Chapter_3__Adult_PBPK_model_performance/003_Chapter_3_3__Montelukast_Concentration-Time_profiles_in_Adults/024_plotTimeProfile.png)

