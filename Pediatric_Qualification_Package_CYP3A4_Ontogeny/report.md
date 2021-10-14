# Pediatric Qualification Package: CYP3A4 Ontogeny





| Version                         | 1.3-OSP10.0                                                  |
| ------------------------------- | ------------------------------------------------------------ |
| Qualification Plan Release      | https://github.com/Open-Systems-Pharmacology/Pediatric_Qualification_Package_CYP3A4_Ontogeny/releases/tag/v1.3 |
| OSP Version                     | 10.0                                                         |
| Qualification Framework Version | 2.3                                                          |





This qualification report is filed at:

https://github.com/Open-Systems-Pharmacology/OSP-Qualification-Reports
# Table of Contents
  * [1 Introduction to Pediatric Translation and CYP3A4 Ontogeny Qualification](#1-introduction-to-pediatric-translation-and-cyp3a4-ontogeny-qualification)
  * [2 Pediatric translation qualification results](#2-pediatric-translation-qualification-results)
    * [2.1 Sufentanil PK Ratio tables and Figures](#21-sufentanil-pk-ratio-tables-and-figures)
    * [2.2 Sufentanil Concentration-Time profiles in Children](#22-sufentanil-concentration-time-profiles-in-children)
    * [2.3 Alfentanil PK Ratio tables and Figures](#23-alfentanil-pk-ratio-tables-and-figures)
    * [2.4 Alfentanil Concentration-Time profiles in Children](#24-alfentanil-concentration-time-profiles-in-children)
  * [3 References](#3-references)
# 1 Introduction to Pediatric Translation and CYP3A4 Ontogeny Qualification
The presented qualification report evaluates the predictive performance of the OSP suite to predict cytochrome P450 3A4 (CYP3A4)-mediated drug clearance in children.

Therefore, PBPK models of specific *in vivo* probe substances covering children aged below 6 months up to adolescents were built and evaluated. All models are whole-body PBPK models, allowing for dynamic pediatric translation in organs expressing CYP3A4. The qualification report demonstrates the level of confidence of the OSP suite with regard to reliable PBPK predictions of age-related CYP3A4-mediated drug clearance during model-informed drug development. The presented PBPK models as well as the respective qualification plan and qualification report are provided open-source and transparently documented (https://github.com/Open-Systems-Pharmacology/Pediatric_Qualification_Package_CYP3A4_Ontogeny). 


## Translation of Adult PBPK to Children

Using a developed and validated (adult) PBPK model for an *in vivo* probe substance, a pediatric PBPK model can be established for children by translating physiology, clearance processes (as parameterized in the adult model) and age-dependent protein binding including the variability therein.[[Maharaj 2013](#3-references)] 

The PBPK models are developed with clinical data of healthy adult subjects obtained from the literature, covering available dosing ranges for e.g. intravenous as well as oral administration, to capture both systemic clearance as well gut-wall metabolic clearance processes. For orally administered drugs, the same formulations that are used in children should ideally be included in the model for adults. Plasma concentrations following multiple-dose application, mass balance information and other clinical measurements need to be included for model development, if available. During model translation from adults to children for a specific substance, uncertainties in data-quality caused by impact of disease or the target study population, inaccurate in vitro assay-techniques regarding mass balance, as well as study differences may cause not being able to adequately predict the PK in children for all reported studies. 

Prediction performance of the PBPK model for these probe substances in children are then shown by means of e.g. predicted versus observed area under the plasma concentration (AUC)-ratio plots, of which the results support an adequate prediction of the ontogeny function for the application of PBPK model translation of adult PBPK to children.

For qualification purpose, during the translation of adult PBPK to children the following assumptions and considerations were made: 

- when translating an adult model to children, it was assumed that the metabolism and excretion pathways are qualitatively the same in children as in adults.
- no further changes to input parameters other than those for the physiology and protein binding. All other parameters (e.g. lipophilicity, intestinal permeability, solubility) were kept unchanged.

## Anthropometric and Physiological Information 

Regarding the age-dependencies of the relevant anthropometric (height, weight) and physiological parameters (e.g. blood flows, organ volumes, binding protein concentrations, hematocrit, cardiac output) in children was gathered from the literature and has been previously published [[Edginton 2006](#3-references)]. The information was incorporated into PK-Sim® and was used as default values for the simulations in children.

The  applied ontogeny and variability of plasma proteins and active processes that are integrated into PK-Sim® for translation to children are described in the publicly available ‘PK-Sim® Ontogeny Database Version 7.3' [[Ontogeny Database](#3-references)] or otherwise referenced for the specific process.

## Qualification of **CYP3A4 enzyme ontogeny**

To qualify the OSP suite for the pediatric translation of the pharmacokinetics of new drugs that are metabolized by CYP3A4, the following set of probe substances was included:

- Alfentanil [[Alfentanil-Model](#3-references)]

- Sufentanil [[Sufentanil-Model](#3-references)]

The adult PBPK model reports and the corresponding PK-Sim project files are filed at: https://github.com/Open-Systems-Pharmacology/OSP-PBPK-Model-Library/


# 2 Pediatric translation qualification results
## Evaluation of Pediatric translation

All pediatric translations are pure retrospective predictions, no pediatric pharmacokinetic studies were used to inform model parameters. All parameters necessary to model the pediatric populations, such as demographics (age, weight, height), as well as dosing formulation information were taken from the respective pediatrics studies from literature in order to evaluate their predictive performance. 

The models were evaluated by ratio plots of area under the plasma concentration-time curve (AUC), or clearance (CL) values resulting from our predictions to the values observed during clinical studies, and by comparison of concentration-time profiles if available. As a quantitative measure of the descriptive and predictive performance of each model, the geometric mean fold error was calculated according to Eq. 1:

Eq. 1: GMFE=10^((Σ|log10(pred PK parameter∕obs PK parameter)|)∕n)

with GMFE = geometric mean fold error of all AUC or CL predictions of the respective model, pred PK parameter = predicted AUC or CL, obs PK parameter = observed AUC or CL, and n = number of observed values.

The ratios of predicted over observed mean AUC or CL values from all compound were also plotted across all age groups in the figure below. As illustrated, most of the prediction were within the 0.5 to 2.0 range (2-fold error). 

In the next sections the demographics as well as the evaluation results of the predictive performance of the specific compound PBPK models in children can be found.  


![005_plotPKRatioAUC.png](images/002_2_Pediatric_translation_qualification_results/005_plotPKRatioAUC.png)

GMFE (AUC) = 1.248221 

|AUC                   |Number|Ratio [%]|
|---------------------:|-----:|--------:|
|Points total          |39    |-        |
|Points within 1.5 fold|29    |74.359   |
|Points within 2-fold  |38    |97.4359  |

|Study ID          |Age [y]|BodyWeight [kg]|Predicted AUC [mg*min/ml]|Observed AUC [mg*min/ml]|Pred/Obs AUC Ratio|
|-----------------:|------:|--------------:|------------------------:|-----------------------:|-----------------:|
|Davis 1987        |1.2917 |8.9            |0.00044791               |0.00082873              |0.54048           |
|Davis 1987        |0.43333|5.3            |0.00056094               |0.00054546              |1.0284            |
|Guay 1991         |2.0833 |12.1           |6.5157e-05               |0.00010838              |0.60119           |
|Guay 1991         |2.5833 |16             |3.9715e-05               |4.63e-05                |0.85776           |
|Guay 1991         |2.6667 |11.3           |0.00010103               |8.92e-05                |1.1327            |
|Guay 1991         |3.25   |16             |8.6803e-05               |8.26e-05                |1.0509            |
|Guay 1991         |3.8333 |14.2           |5.5827e-05               |6.63e-05                |0.84204           |
|Guay 1991         |4.5833 |15             |4.4454e-05               |6.73e-05                |0.66053           |
|Guay 1991         |4.5833 |19             |8.5408e-05               |0.00013487              |0.63325           |
|Guay 1991         |4.8333 |17.5           |8.744e-05                |6.99e-05                |1.2509            |
|Guay 1991         |5.25   |18.5           |4.5236e-05               |4.36e-05                |1.0375            |
|Guay 1991         |5.25   |19.65          |8.8355e-05               |8.53e-05                |1.0358            |
|Guay 1991         |5.3333 |24             |0.00011313               |0.0001355               |0.8349            |
|Guay 1991         |5.3333 |24             |6.3533e-05               |7.55e-05                |0.8415            |
|Guay 1991         |5.75   |14.5           |7.5552e-05               |0.00015183              |0.49761           |
|Guay 1991         |5.9167 |28.2           |9.2983e-05               |0.00012754              |0.72904           |
|Guay 1991         |5.9167 |25             |4.7973e-05               |5.71e-05                |0.84016           |
|Guay 1991         |6.9167 |29.6           |6.2262e-05               |6.17e-05                |1.0091            |
|Guay 1991         |7.5    |23.5           |2.6902e-05               |3.5e-05                 |0.76862           |
|Guay 1991         |7.5    |15.2           |7.2941e-05               |7.36e-05                |0.99104           |
|Guay 1991         |8.75   |22.6           |5.2465e-05               |5.65e-05                |0.92858           |
|den Hollander 1992|0.92   |6.5            |20.8285                  |21.1                    |0.98713           |
|den Hollander 1992|0.83   |6.4            |21.1387                  |14                      |1.5099            |
|den Hollander 1992|0.99   |8.5            |22.5826                  |19.8                    |1.1405            |
|den Hollander 1992|0.3    |5.1            |28.1617                  |18.5                    |1.5223            |
|den Hollander 1992|0.92   |6.149          |17.7933                  |15.9                    |1.1191            |
|den Hollander 1992|1.3    |10.4           |21.2314                  |24.3                    |0.87372           |
|den Hollander 1992|9      |25.6           |19.4014                  |11.3                    |1.7169            |
|den Hollander 1992|3.5    |14.4           |18.8753                  |18.6                    |1.0148            |
|den Hollander 1992|5.5    |19.5           |18.9084                  |20.7                    |0.91345           |
|den Hollander 1992|3.5    |18.5           |20.4828                  |22.7                    |0.90233           |
|Meistelman 1987   |4.7    |20             |0.0040913                |0.0058824               |0.69552           |
|Meistelman 1987   |5.5    |20             |0.0037913                |0.0033898               |1.1184            |
|Meistelman 1987   |7.7    |23             |0.0037738                |0.0024096               |1.5661            |
|Meistelman 1987   |4.5    |14             |0.0032523                |0.0043478               |0.74804           |
|Meistelman 1987   |4.8    |24             |0.0048364                |0.0054054               |0.89473           |
|Meistelman 1987   |4.5    |20             |0.0041944                |0.0041667               |1.0067            |
|Meistelman 1987   |6.2    |23             |0.0041079                |0.0045455               |0.90373           |
|Meistelman 1987   |4.9    |22             |0.0043792                |0.0074074               |0.59119           |

## 2.1 Sufentanil PK Ratio tables and Figures
### Sufentanil model

Sufentanil PBPK predictions in children were evaluated using pharmacokinetic (PK) data reported in the following studies: 

- Davis PJ, Cook DR, Stiller RL, Davin-Robinson KA. Pharmacodynamics and pharmacokinetics of high-dose sufentanil in infants and children undergoing cardiac surgery. Anesth Analg. 1987 Mar;66(3):203-8.[[Davis 1987](#3-references)]
- Guay J, Gaudreault P, Tang A, Goulet B, Varin F. Pharmacokinetics of sufentanil in normal children. Can J Anaesth. 1992 Jan;39(1):14-20.[[Guay 1992](#3-references)]

The pediatric PBPK model predicted the clearance values of sufentanil observed in pediatric studies reasonably across all available age groups, ranging from 5 months to 8.75 years old. The ratios of mean predicted over observed clearance values are illustrated in the table below as well as in the predicted versus observed clearance ratio plot, showing that most predictions in children were within 2-fold error of observed values.


![001_plotPKRatioAUC.png](images/002_2_Pediatric_translation_qualification_results/001_2_1_Sufentanil_PK_Ratio_tables_and_Figures/001_plotPKRatioAUC.png)

GMFE (AUC) = 1.251766 

|AUC                   |Number|Ratio [%]|
|---------------------:|-----:|--------:|
|Points total          |21    |-        |
|Points within 1.5 fold|16    |76.1905  |
|Points within 2-fold  |20    |95.2381  |

|Study ID  |Age [y]|BodyWeight [kg]|Predicted AUC [mg*min/ml]|Observed AUC [mg*min/ml]|Pred/Obs AUC Ratio|
|---------:|------:|--------------:|------------------------:|-----------------------:|-----------------:|
|Davis 1987|1.2917 |8.9            |0.00044791               |0.00082873              |0.54048           |
|Davis 1987|0.43333|5.3            |0.00056094               |0.00054546              |1.0284            |
|Guay 1991 |2.0833 |12.1           |6.5157e-05               |0.00010838              |0.60119           |
|Guay 1991 |2.5833 |16             |3.9715e-05               |4.63e-05                |0.85776           |
|Guay 1991 |2.6667 |11.3           |0.00010103               |8.92e-05                |1.1327            |
|Guay 1991 |3.25   |16             |8.6803e-05               |8.26e-05                |1.0509            |
|Guay 1991 |3.8333 |14.2           |5.5827e-05               |6.63e-05                |0.84204           |
|Guay 1991 |4.5833 |15             |4.4454e-05               |6.73e-05                |0.66053           |
|Guay 1991 |4.5833 |19             |8.5408e-05               |0.00013487              |0.63325           |
|Guay 1991 |4.8333 |17.5           |8.744e-05                |6.99e-05                |1.2509            |
|Guay 1991 |5.25   |18.5           |4.5236e-05               |4.36e-05                |1.0375            |
|Guay 1991 |5.25   |19.65          |8.8355e-05               |8.53e-05                |1.0358            |
|Guay 1991 |5.3333 |24             |0.00011313               |0.0001355               |0.8349            |
|Guay 1991 |5.3333 |24             |6.3533e-05               |7.55e-05                |0.8415            |
|Guay 1991 |5.75   |14.5           |7.5552e-05               |0.00015183              |0.49761           |
|Guay 1991 |5.9167 |28.2           |9.2983e-05               |0.00012754              |0.72904           |
|Guay 1991 |5.9167 |25             |4.7973e-05               |5.71e-05                |0.84016           |
|Guay 1991 |6.9167 |29.6           |6.2262e-05               |6.17e-05                |1.0091            |
|Guay 1991 |7.5    |23.5           |2.6902e-05               |3.5e-05                 |0.76862           |
|Guay 1991 |7.5    |15.2           |7.2941e-05               |7.36e-05                |0.99104           |
|Guay 1991 |8.75   |22.6           |5.2465e-05               |5.65e-05                |0.92858           |

## 2.2 Sufentanil Concentration-Time profiles in Children
#### Concentration-Time Profiles

Predicted versus observed plasma concentration-time profiles are listed below. Only simulations where observed data was available for comparison are shown.  Depending if the observed data were individual data or aggregated data, individual predictions or population predictions including variability are shown, respectively.
![001_plotTimeProfile.png](images/002_2_Pediatric_translation_qualification_results/002_2_2_Sufentanil_Concentration-Time_profiles_in_Children/001_plotTimeProfile.png)

![002_plotTimeProfile.png](images/002_2_Pediatric_translation_qualification_results/002_2_2_Sufentanil_Concentration-Time_profiles_in_Children/002_plotTimeProfile.png)

![003_plotTimeProfile.png](images/002_2_Pediatric_translation_qualification_results/002_2_2_Sufentanil_Concentration-Time_profiles_in_Children/003_plotTimeProfile.png)

![004_plotTimeProfile.png](images/002_2_Pediatric_translation_qualification_results/002_2_2_Sufentanil_Concentration-Time_profiles_in_Children/004_plotTimeProfile.png)

![005_plotTimeProfile.png](images/002_2_Pediatric_translation_qualification_results/002_2_2_Sufentanil_Concentration-Time_profiles_in_Children/005_plotTimeProfile.png)

![006_plotTimeProfile.png](images/002_2_Pediatric_translation_qualification_results/002_2_2_Sufentanil_Concentration-Time_profiles_in_Children/006_plotTimeProfile.png)

## 2.3 Alfentanil PK Ratio tables and Figures
### Alfentanil model

Alfentanil PBPK predictions in children were evaluated using pharmacokinetic (PK) data reported in the following studies: 

- den Hollander JM, Hennis PJ, Burm AG, Vletter AA, Bovill JG. Pharmacokinetics of alfentanil before and after cardiopulmonary bypass in pediatric patients undergoing cardiac surgery: Part I. J Cardiothorac Vasc Anesth. 1992 Jun;6(3):308-12.[[Meistelman 1987](#3-references)]
- Meistelman C, Saint-Maurice C, Lepaul M, Levron JC, Loose JP, Mac Gee K. A comparison of alfentanil pharmacokinetics in children and adults. Anesthesiology. 1987 Jan;66(1):13-6.[[den Hollander 1992](#3-references)]

The pediatric PBPK model predicted the AUC values of alfentanil observed in pediatric studies reasonably across all available age groups, ranging from 3.6 months to 9 years old. The ratios of mean predicted over observed AUC values are illustrated in the table below as well as in the predicted versus observed AUC ratio plot, showing that most predictions in children were within 2-fold error of observed values. Another reported study on alfentanil pharmacokinetics in children [[Goresky 1987](#3-references)] showed systematically higher exposure for most individuals compared to the other herein included studies. This deviation may have been caused by different impact of individual pathophysiology of the target study population, inaccurate in vitro assay-techniques or other study differences. 


![001_plotPKRatioAUC.png](images/002_2_Pediatric_translation_qualification_results/003_2_3_Alfentanil_PK_Ratio_tables_and_Figures/001_plotPKRatioAUC.png)

GMFE (AUC) = 1.244097 

|AUC                   |Number|Ratio [%]|
|---------------------:|-----:|--------:|
|Points total          |18    |-        |
|Points within 1.5 fold|13    |72.2222  |
|Points within 2-fold  |18    |100      |

|Study ID          |Age [y]|BodyWeight [kg]|Predicted AUC [mg*min/l]|Observed AUC [mg*min/l]|Pred/Obs AUC Ratio|
|-----------------:|------:|--------------:|-----------------------:|----------------------:|-----------------:|
|den Hollander 1992|0.92   |6.5            |20.8285                 |21.1                   |0.98713           |
|den Hollander 1992|0.83   |6.4            |21.1387                 |14                     |1.5099            |
|den Hollander 1992|0.99   |8.5            |22.5826                 |19.8                   |1.1405            |
|den Hollander 1992|0.3    |5.1            |28.1617                 |18.5                   |1.5223            |
|den Hollander 1992|0.92   |6.149          |17.7933                 |15.9                   |1.1191            |
|den Hollander 1992|1.3    |10.4           |21.2314                 |24.3                   |0.87372           |
|den Hollander 1992|9      |25.6           |19.4014                 |11.3                   |1.7169            |
|den Hollander 1992|3.5    |14.4           |18.8753                 |18.6                   |1.0148            |
|den Hollander 1992|5.5    |19.5           |18.9084                 |20.7                   |0.91345           |
|den Hollander 1992|3.5    |18.5           |20.4828                 |22.7                   |0.90233           |
|Meistelman 1987   |4.7    |20             |0.0040913               |0.0058824              |0.69552           |
|Meistelman 1987   |5.5    |20             |0.0037913               |0.0033898              |1.1184            |
|Meistelman 1987   |7.7    |23             |0.0037738               |0.0024096              |1.5661            |
|Meistelman 1987   |4.5    |14             |0.0032523               |0.0043478              |0.74804           |
|Meistelman 1987   |4.8    |24             |0.0048364               |0.0054054              |0.89473           |
|Meistelman 1987   |4.5    |20             |0.0041944               |0.0041667              |1.0067            |
|Meistelman 1987   |6.2    |23             |0.0041079               |0.0045455              |0.90373           |
|Meistelman 1987   |4.9    |22             |0.0043792               |0.0074074              |0.59119           |

## 2.4 Alfentanil Concentration-Time profiles in Children
#### Concentration-Time Profiles

Predicted versus observed plasma concentration-time profiles are listed below. Only simulations where observed data was available for comparison are shown.  Depending if the observed data were individual data or aggregated data, individual predictions or population predictions including variability are shown, respectively.
![001_plotTimeProfile.png](images/002_2_Pediatric_translation_qualification_results/004_2_4_Alfentanil_Concentration-Time_profiles_in_Children/001_plotTimeProfile.png)

![002_plotTimeProfile.png](images/002_2_Pediatric_translation_qualification_results/004_2_4_Alfentanil_Concentration-Time_profiles_in_Children/002_plotTimeProfile.png)

![003_plotPopulationTimeProfile.png](images/002_2_Pediatric_translation_qualification_results/004_2_4_Alfentanil_Concentration-Time_profiles_in_Children/003_plotPopulationTimeProfile.png)

![004_plotPopulationTimeProfile.png](images/002_2_Pediatric_translation_qualification_results/004_2_4_Alfentanil_Concentration-Time_profiles_in_Children/004_plotPopulationTimeProfile.png)

# 3 References
**Alfentanil-Model** Alfentanil-Model, Whole-body PBPK model of Alfentanil. (https://github.com/Open-Systems-Pharmacology/Alfentanil-Model) 

**Davis 1987** Davis PJ, Cook DR, Stiller RL, Davin-Robinson KA. Pharmacodynamics and pharmacokinetics of high-dose sufentanil in infants and children undergoing cardiac surgery. Anesth Analg. 1987 Mar;66(3):203-8.

**den Hollander 1992** den Hollander JM, Hennis PJ, Burm AG, Vletter AA, Bovill JG. Pharmacokinetics of alfentanil before and after cardiopulmonary bypass in pediatric patients undergoing cardiac surgery: Part I. J Cardiothorac Vasc Anesth. 1992 Jun;6(3):308-12.

**Edginton 2006** Edginton AN, Schmitt W, Willmann S. Development and evaluation of a generic physiologically based pharmacokinetic model for children. Clin Pharmacokinet. 2006;45(10):1013-34.

**Goresky 1987** Goresky GV, Koren G, Sabourin MA, Sale JP, Strunin L., The pharmacokinetics of alfentanil in children. Anesthesiology. 1987 Nov;67(5):654-9.

**Guay 1992** Guay J, Gaudreault P, Tang A, Goulet B, Varin F. Pharmacokinetics of sufentanil in normal children. Can J Anaesth. 1992 Jan;39(1):14-20.

**Maharaj 2013** Maharaj AR, Barrett JS, Edginton AN. A workflow example of PBPK modeling to support pediatric research and development: case study with lorazepam. The AAPS journal. 2013;15(2): 455-464.

**Meistelman 1987** Meistelman C, Saint-Maurice C, Lepaul M, Levron JC, Loose JP, Mac Gee K. A comparison of alfentanil pharmacokinetics in children and adults. Anesthesiology. 1987 Jan;66(1):13-6.

**Ontogeny Database** OSPSuite.Documentation/PK-Sim Ontogeny Database Version 7.3.pdf (https://github.com/Open-Systems-Pharmacology/OSPSuite.Documentation/blob/38cf71b384cfc25cfa0ce4d2f3addfd32757e13b/PK-Sim%20Ontogeny%20Database%20Version%207.3.pdf)

**Sufentanil-Model** Sufentanil-Model, Whole-body PBPK model of Sufentanil. (https://github.com/Open-Systems-Pharmacology/Sufentanil-Model)
