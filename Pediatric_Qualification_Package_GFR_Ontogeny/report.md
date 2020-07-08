# Pediatric Qualification Package: GFR Ontogeny




| Version                         | 1.1-OSP9.1                                                   |
| ------------------------------- | ------------------------------------------------------------ |
| Qualification Plan Release      | https://github.com/Open-Systems-Pharmacology/Pediatric_Qualification_Package_GFR_Ontogeny/releases/tag/v1.1 |
| OSP Version                     | 9.1                                                          |
| Qualification Framework Version | 2.2                                                          |





This qualification report is filed at:

https://github.com/Open-Systems-Pharmacology/OSP-Qualification-Reports

# Table of Contents
  * [Chapter 1: Introduction to Pediatric Translation](#chapter-1-introduction-to-pediatric-translation)
  * [Chapter 2: Pediatric translation qualification](#chapter-2-pediatric-translation-qualification)
    * [Chapter 2.1: Amikacin PK Ratio tables and Figures](#chapter-21-amikacin-pk-ratio-tables-and-figures)
    * [Chapter 2.2: Amikacin Concentration-Time profiles in Children](#chapter-22-amikacin-concentration-time-profiles-in-children)
    * [Chapter 2.3: Vancomycin PK Ratio tables and Figures](#chapter-23-vancomycin-pk-ratio-tables-and-figures)
    * [Chapter 2.4: Vancomycin Concentration-Time profiles in Children](#chapter-24-vancomycin-concentration-time-profiles-in-children)
  * [Chapter 3: Adult PBPK model performance](#chapter-3-adult-pbpk-model-performance)
    * [Chapter 3.1: Amikacin Input Tables](#chapter-31-amikacin-input-tables)
    * [Chapter 3.2: Amikacin Concentration-Time profiles in Adults](#chapter-32-amikacin-concentration-time-profiles-in-adults)
    * [Chapter 3.3: Vancomycin Input Tables](#chapter-33-vancomycin-input-tables)
    * [Chapter 3.4: Vancomycin Diagnostics Plots](#chapter-34-vancomycin-diagnostics-plots)
    * [Chapter 3.5: Vancomycin Concentration-Time profiles in Adults](#chapter-35-vancomycin-concentration-time-profiles-in-adults)
# Chapter 1: Introduction to Pediatric Translation
The presented qualification report evaluates the predictive performance of the OSP suite to predict glomerular filtration rate (GFR)-mediated drug clearance in children.

Therefore, PBPK models of specific *in vivo* probe substances covering children aged below 6 months up to adolescents were built and evaluated. All models are whole-body PBPK models, allowing for dynamic pediatric translation in all organs. The qualification report demonstrates the level of confidence of the OSP suite with regard to reliable PBPK predictions of age related GFR-mediated drug clearance during model-informed drug development. The presented PBPK models as well as the respective qualification plan and qualification report are provided open-source and transparently documented (https://github.com/Open-Systems-Pharmacology/Pediatric-Qualification-Package-GFR). 


## Translation of Adult PBPK to Children

Using a developed and validated (adult) PBPK model for an *in vivo* probe substance, a pediatric PBPK model can be established for children by translating physiology, clearance processes (as parameterized in the adult model) and age-dependent protein binding including the variability therein.[[1](#reference)]

The PBPK models are developed with clinical data of healthy adult subjects obtained from the literature. Plasma concentrations following multiple-dose application, mass balance information and other clinical measurements need to be included for model development, if available. During model translation from adults to children for a specific substance, uncertainties in data-quality caused by impact of disease or the target study population, inaccurate in vitro assay-techniques regarding mass balance, as well as study differences may cause not being able to adequately predict the PK in children for all reported studies. 

Prediction performance of the PBPK model for these probe substances in children are then shown by means of e.g. predicted versus observed clearance-ratio plots, of which the results support an adequate prediction of the ontogeny function for the application of PBPK model translation of adult PBPK to children.

For qualification purpose, during the translation of adult PBPK to children the following assumptions and considerations were made: 

- when translating an adult model to children, it was assumed that the metabolism and excretion pathways are qualitatively the same in children as in adults.
- no further changes to input parameters other than those for the physiology and protein binding. All other parameters (e.g. lipophilicity) were kept unchanged. 

## Anthropometric and Physiological Information 

Regarding the age-dependencies of the relevant anthropometric (height, weight) and physiological parameters (e.g. blood flows, organ volumes, binding protein concentrations, hematocrit, cardiac output) in children was gathered from the literature and has been previously published [[2](#reference)]. The information was incorporated into PK-Sim® and was used as default values for the simulations in children.

The  applied ontogeny and variability of plasma proteins that are integrated into PK-Sim® for translation to children are described in the publicly available ‘PK-Sim® Ontogeny Database Version 7.3' [[3](#reference)] or otherwise referenced for the specific process.

### Qualification of **GFR ontogeny**

For the qualification of the GFR elimination of compounds, the following probe substances was included:

- Amikacin [[4](#reference)]
- Vancomycin [[5](#reference)]

### References

[1] [Maharaj AR, Barrett JS, Edginton AN. A workflow example of PBPK modeling to support pediatric research and development: case study with lorazepam. The AAPS journal. 2013;15(2): 455-464.](https://www.ncbi.nlm.nih.gov/pubmed/23344790)

[2] [Edginton AN, Schmitt W, Willmann S. Development and evaluation of a generic physiologically based pharmacokinetic model for children. Clin Pharmacokinet. 2006;45(10):1013-34.](https://www.ncbi.nlm.nih.gov/pubmed/16984214)

[3]  [OSPSuite.Documentation/PK-Sim Ontogeny Database Version 7.3.pdf ](https://github.com/Open-Systems-Pharmacology/OSPSuite.Documentation/blob/38cf71b384cfc25cfa0ce4d2f3addfd32757e13b/PK-Sim%20Ontogeny%20Database%20Version%207.3.pdf)

[4] [Amikacin-Model, Whole-body PBPK model of Amikacin. https://github.com/Open-Systems-Pharmacology/Amikacin-Model](https://github.com/incei/Amikacin-Model)

[5] [Vancomycin-Model, Whole-body PBPK model of Vancomycin. https://github.com/Open-Systems-Pharmacology/Amikacin-Model](https://github.com/incei/Vancomycin-Model)
# Chapter 2: Pediatric translation qualification
## Evaluation of Pediatric translation

All pediatric translations are pure retrospective predictions, no pediatric pharmacokinetic studies were used to inform model parameters. All parameters necessary to model the pediatric populations, such as demographics (age, weight, height), as well as dosing formulation information were taken from the respective pediatrics studies from literature in order to evaluate their predictive performance. 

The models were evaluated by ratio plots of area under the plasma concentration-time curve (AUC), or clearance (CL) values resulting from our predictions to the values observed during clinical studies, and by comparison of concentration-time profiles if available. As a quantitative measure of the descriptive and predictive performance of each model, the geometric mean fold error was calculated according to Eq. 1:

Eq. 1: GMFE=10^((Σ|log10(pred PK parameter∕obs PK parameter)|)∕n)

with GMFE = geometric mean fold error of all AUC or CL predictions of the respective model, pred PK parameter = predicted AUC or CL, obs PK parameter = observed AUC or CL, and n = number of observed values.

The ratios of predicted over observed mean AUC or CL values from all compound were also plotted across all age groups in the figure below. As illustrated, most of the prediction were within the 0.5 to 2.0 range (2-fold error). 

In the next sections the demographics as well as the evaluation results of the predictive performance of the specific compound PBPK models in children can be found.  


![005_plotPKRatioCL.png](images/002_Chapter_2__Pediatric_translation_qualification/005_plotPKRatioCL.png)

GMFE (CL) = 1.258017 

|CL                    |Number|Ratio [%]|
|---------------------:|-----:|--------:|
|Points total          |39    |-        |
|Points within 1.5 fold|32    |82.0513  |
|Points within 2-fold  |38    |97.4359  |

|Study ID       |Age [y]  |BodyWeight [kg]|Predicted CL [ml/min/kg]|Observed CL [ml/min/kg]|Pred/Obs CL Ratio|
|--------------:|--------:|--------------:|-----------------------:|----------------------:|----------------:|
|Vogelstein 1977|15       |77             |0.71181                 |1.74                   |0.71181          |
|Vogelstein 1977|15       |62.5           |0.95476                 |1.44                   |0.95476          |
|Vogelstein 1977|9        |21.5           |0.83703                 |2.56                   |0.83703          |
|Vogelstein 1977|13       |51             |1.0188                  |1.35                   |1.0188           |
|Vogelstein 1977|12       |27.1902        |0.93839                 |2.64                   |0.93839          |
|Vogelstein 1977|7        |27.4           |0.81617                 |2.19                   |0.81617          |
|Vogelstein 1977|4        |14             |0.58013                 |4.22                   |0.58013          |
|Vogelstein 1977|6        |17.3           |0.94756                 |2.63                   |0.94756          |
|Vogelstein 1977|6        |15.5           |0.61107                 |4.26                   |0.61107          |
|Vogelstein 1977|7        |15.9           |1.1941                  |2.3                    |1.1941           |
|Vogelstein 1977|14       |39.5           |0.95879                 |1.91                   |0.95879          |
|Vogelstein 1977|10       |32.8           |0.83954                 |2.3                    |0.83954          |
|Vogelstein 1977|14       |45.5           |0.80729                 |2.23                   |0.80729          |
|Vogelstein 1977|11       |35.2           |0.73927                 |2.58                   |0.73927          |
|Vogelstein 1977|13       |27.7           |0.77547                 |2.86                   |0.77547          |
|Vogelstein 1977|8        |20.8           |0.86162                 |2.88                   |0.86162          |
|Vogelstein 1977|6        |15.5           |0.77799                 |3.31                   |0.77799          |
|Vogelstein 1977|13       |49             |0.75956                 |1.88                   |0.75956          |
|Vogelstein 1977|7        |20.6           |1.1459                  |2.06                   |1.1459           |
|Vogelstein 1977|16       |35.0809        |0.89535                 |2.47                   |0.89535          |
|Treluyer 2002  |0.013333 |3.5867         |1.3259                  |0.053                  |1.3259           |
|Treluyer 2002  |0.04     |3.76           |1.1067                  |0.073                  |1.1067           |
|Treluyer 2002  |0.065833 |3.9279         |0.97612                 |0.095                  |0.97612          |
|Treluyer 2002  |0.079167 |4.0146         |0.9348                  |0.106                  |0.9348           |
|Treluyer 2002  |0.10583  |4.1879         |0.94232                 |0.118                  |0.94232          |
|Treluyer 2002  |0.14583  |4.4479         |1.0535                  |0.12                   |1.0535           |
|Treluyer 2002  |0.51583  |6.8529         |1.1539                  |0.127                  |1.1539           |
|Treluyer 2002  |0.7675   |8.4888         |0.96098                 |0.15                   |0.96098          |
|Treluyer 2002  |2.0242   |12.3044        |0.74412                 |0.181                  |0.74412          |
|Treluyer 2002  |4.0608   |16.8869        |0.66347                 |0.19                   |0.66347          |
|Treluyer 2002  |6.085    |21.821         |0.6195                  |0.196                  |0.6195           |
|Treluyer 2002  |7.09     |24.434         |0.67841                 |0.177                  |0.67841          |
|Belfayol 1996  |7        |23.5           |0.82769                 |56.3                   |0.82769          |
|Schaad 1980    |0.0071184|3.07           |1.1238                  |3.6416                 |1.1238           |
|Schaad 1980    |0.25833  |4.9            |1.3072                  |8.0925                 |1.3072           |
|Schaad 1980    |0.35833  |5.2            |0.84901                 |14.0462                |0.84901          |
|Schaad 1980    |3.917    |15.5           |0.47009                 |61.2428                |0.47009          |
|Schaad 1980    |5.583    |20             |0.5881                  |59.0636                |0.5881           |
|Schaad 1980    |7.583    |26.7           |0.57141                 |74.3584                |0.57141          |

## Chapter 2.1: Amikacin PK Ratio tables and Figures
### Amikacin model

Amikacin PBPK predictions in children were evaluated using pharmacokinetic (PK) data reported in the following studies: 

- Tréluyer JM, Merlé Y, Tonnelier S, Rey E, Pons G. Nonparametric population pharmacokinetic analysis of amikacin in neonates, infants, and children. Antimicrob Agents Chemother. 2002 May;46(5):1381-7.
- Vogelstein B, Kowarski A, Lietman PS. The pharmacokinetics of amikacin in children. J Pediatr. 1977 Aug;91(2):333-9.
- Belfayol L, Talon P, Eveillard M, Alet P, Fauvelle F. Pharmacokinetics of once-daily amikacin in pediatric patients. Clin Microbiol Infect. 1996 Feb;2(3):186-191.

The pediatric PBPK model reasonably well predicted the clearance values of amikacin  pediatric studies across all available age groups, ranging from 0.16 months to 16 years old. The ratios of mean predicted over observed clearance values are illustrated in the table below as well as in the predicted versus observed clearance ratio plot, showing that all predictions in children were within 2-fold error of observed values.


![001_plotPKRatioCL.png](images/002_Chapter_2__Pediatric_translation_qualification/001_Chapter_2_1__Amikacin_PK_Ratio_tables_and_Figures/001_plotPKRatioCL.png)

GMFE (CL) = 1.219861 

|CL                    |Number|Ratio [%]|
|---------------------:|-----:|--------:|
|Points total          |33    |-        |
|Points within 1.5 fold|29    |87.8788  |
|Points within 2-fold  |33    |100      |

|Study ID       |Age [y] |BodyWeight [kg]|Predicted CL [ml/min/kg]|Observed CL [ml/min/kg]|Pred/Obs CL Ratio|
|--------------:|-------:|--------------:|-----------------------:|----------------------:|----------------:|
|Vogelstein 1977|15      |77             |0.71181                 |1.74                   |0.71181          |
|Vogelstein 1977|15      |62.5           |0.95476                 |1.44                   |0.95476          |
|Vogelstein 1977|9       |21.5           |0.83703                 |2.56                   |0.83703          |
|Vogelstein 1977|13      |51             |1.0188                  |1.35                   |1.0188           |
|Vogelstein 1977|12      |27.1902        |0.93839                 |2.64                   |0.93839          |
|Vogelstein 1977|7       |27.4           |0.81617                 |2.19                   |0.81617          |
|Vogelstein 1977|4       |14             |0.58013                 |4.22                   |0.58013          |
|Vogelstein 1977|6       |17.3           |0.94756                 |2.63                   |0.94756          |
|Vogelstein 1977|6       |15.5           |0.61107                 |4.26                   |0.61107          |
|Vogelstein 1977|7       |15.9           |1.1941                  |2.3                    |1.1941           |
|Vogelstein 1977|14      |39.5           |0.95879                 |1.91                   |0.95879          |
|Vogelstein 1977|10      |32.8           |0.83954                 |2.3                    |0.83954          |
|Vogelstein 1977|14      |45.5           |0.80729                 |2.23                   |0.80729          |
|Vogelstein 1977|11      |35.2           |0.73927                 |2.58                   |0.73927          |
|Vogelstein 1977|13      |27.7           |0.77547                 |2.86                   |0.77547          |
|Vogelstein 1977|8       |20.8           |0.86162                 |2.88                   |0.86162          |
|Vogelstein 1977|6       |15.5           |0.77799                 |3.31                   |0.77799          |
|Vogelstein 1977|13      |49             |0.75956                 |1.88                   |0.75956          |
|Vogelstein 1977|7       |20.6           |1.1459                  |2.06                   |1.1459           |
|Vogelstein 1977|16      |35.0809        |0.89535                 |2.47                   |0.89535          |
|Treluyer 2002  |0.013333|3.5867         |1.3259                  |0.053                  |1.3259           |
|Treluyer 2002  |0.04    |3.76           |1.1067                  |0.073                  |1.1067           |
|Treluyer 2002  |0.065833|3.9279         |0.97612                 |0.095                  |0.97612          |
|Treluyer 2002  |0.079167|4.0146         |0.9348                  |0.106                  |0.9348           |
|Treluyer 2002  |0.10583 |4.1879         |0.94232                 |0.118                  |0.94232          |
|Treluyer 2002  |0.14583 |4.4479         |1.0535                  |0.12                   |1.0535           |
|Treluyer 2002  |0.51583 |6.8529         |1.1539                  |0.127                  |1.1539           |
|Treluyer 2002  |0.7675  |8.4888         |0.96098                 |0.15                   |0.96098          |
|Treluyer 2002  |2.0242  |12.3044        |0.74412                 |0.181                  |0.74412          |
|Treluyer 2002  |4.0608  |16.8869        |0.66347                 |0.19                   |0.66347          |
|Treluyer 2002  |6.085   |21.821         |0.6195                  |0.196                  |0.6195           |
|Treluyer 2002  |7.09    |24.434         |0.67841                 |0.177                  |0.67841          |
|Belfayol 1996  |7       |23.5           |0.82769                 |56.3                   |0.82769          |

## Chapter 2.2: Amikacin Concentration-Time profiles in Children
#### Concentration-Time Profiles

Predicted versus observed plasma concentration-time profiles are listed below. Only simulations where observed data was available for comparison are shown.  Depending if the observed data were individual data or aggregated data, individual predictions or population predictions including variability are shown, respectively.
## Chapter 2.3: Vancomycin PK Ratio tables and Figures
### Vancomycin model

Vancomycin PBPK predictions in children were evaluated using pharmacokinetic (PK) data reported in the following studies: 

- Schaad UB, McCracken GH Jr, Nelson JD. Clinical pharmacology and efficacy of vancomycin in pediatric patients. J Pediatr. 1980 Jan;96(1):119-26.

The pediatric PBPK model predicted the clearance values of vancomycin observed in pediatric studies reasonably across all available age groups, ranging from 0.085 months to 7.58 years old. The ratios of mean predicted over observed clearance values are illustrated in the table below as well as in the predicted versus observed clearance ratio plot, showing that all predictions in children were within 2-fold error of observed values.


![001_plotPKRatioCL.png](images/002_Chapter_2__Pediatric_translation_qualification/003_Chapter_2_3__Vancomycin_PK_Ratio_tables_and_Figures/001_plotPKRatioCL.png)

GMFE (CL) = 1.490238 

|CL                    |Number|Ratio [%]|
|---------------------:|-----:|--------:|
|Points total          |6     |-        |
|Points within 1.5 fold|3     |50       |
|Points within 2-fold  |5     |83.3333  |

|Study ID   |Age [y]  |BodyWeight [kg]|Predicted CL [ml/min]|Observed CL [ml/min]|Pred/Obs CL Ratio|
|----------:|--------:|--------------:|--------------------:|-------------------:|----------------:|
|Schaad 1980|0.0071184|3.07           |1.1238               |3.6416              |1.1238           |
|Schaad 1980|0.25833  |4.9            |1.3072               |8.0925              |1.3072           |
|Schaad 1980|0.35833  |5.2            |0.84901              |14.0462             |0.84901          |
|Schaad 1980|3.917    |15.5           |0.47009              |61.2428             |0.47009          |
|Schaad 1980|5.583    |20             |0.5881               |59.0636             |0.5881           |
|Schaad 1980|7.583    |26.7           |0.57141              |74.3584             |0.57141          |

## Chapter 2.4: Vancomycin Concentration-Time profiles in Children
#### Concentration-Time Profiles

Predicted versus observed plasma concentration-time profiles are listed below. Only simulations where observed data was available for comparison are shown.  Depending if the observed data were individual data or aggregated data, individual predictions or population predictions including variability are shown, respectively.
![001_plotPopulationTimeProfile.png](images/002_Chapter_2__Pediatric_translation_qualification/004_Chapter_2_4__Vancomycin_Concentration-Time_profiles_in_Children/001_plotPopulationTimeProfile.png)

![002_plotPopulationTimeProfile.png](images/002_Chapter_2__Pediatric_translation_qualification/004_Chapter_2_4__Vancomycin_Concentration-Time_profiles_in_Children/002_plotPopulationTimeProfile.png)

![003_plotPopulationTimeProfile.png](images/002_Chapter_2__Pediatric_translation_qualification/004_Chapter_2_4__Vancomycin_Concentration-Time_profiles_in_Children/003_plotPopulationTimeProfile.png)

![004_plotPopulationTimeProfile.png](images/002_Chapter_2__Pediatric_translation_qualification/004_Chapter_2_4__Vancomycin_Concentration-Time_profiles_in_Children/004_plotPopulationTimeProfile.png)

![005_plotPopulationTimeProfile.png](images/002_Chapter_2__Pediatric_translation_qualification/004_Chapter_2_4__Vancomycin_Concentration-Time_profiles_in_Children/005_plotPopulationTimeProfile.png)

![006_plotPopulationTimeProfile.png](images/002_Chapter_2__Pediatric_translation_qualification/004_Chapter_2_4__Vancomycin_Concentration-Time_profiles_in_Children/006_plotPopulationTimeProfile.png)

![007_plotPopulationTimeProfile.png](images/002_Chapter_2__Pediatric_translation_qualification/004_Chapter_2_4__Vancomycin_Concentration-Time_profiles_in_Children/007_plotPopulationTimeProfile.png)

![008_plotPopulationTimeProfile.png](images/002_Chapter_2__Pediatric_translation_qualification/004_Chapter_2_4__Vancomycin_Concentration-Time_profiles_in_Children/008_plotPopulationTimeProfile.png)

![009_plotPopulationTimeProfile.png](images/002_Chapter_2__Pediatric_translation_qualification/004_Chapter_2_4__Vancomycin_Concentration-Time_profiles_in_Children/009_plotPopulationTimeProfile.png)

![010_plotPopulationTimeProfile.png](images/002_Chapter_2__Pediatric_translation_qualification/004_Chapter_2_4__Vancomycin_Concentration-Time_profiles_in_Children/010_plotPopulationTimeProfile.png)

![011_plotPopulationTimeProfile.png](images/002_Chapter_2__Pediatric_translation_qualification/004_Chapter_2_4__Vancomycin_Concentration-Time_profiles_in_Children/011_plotPopulationTimeProfile.png)

![012_plotPopulationTimeProfile.png](images/002_Chapter_2__Pediatric_translation_qualification/004_Chapter_2_4__Vancomycin_Concentration-Time_profiles_in_Children/012_plotPopulationTimeProfile.png)

# Chapter 3: Adult PBPK model performance
## Evaluation of Adult PBPK models

The PBPK models of **amikacin**, and **vancomycin** were developed with clinical pharmacokinetic data covering at least administrations given in children. Plasma concentrations following intravenous administration, oral administration, multiple dose application, fractions excreted to urine or bile and other clinical measurements were included for model development whenever available. 


## Chapter 3.1: Amikacin Input Tables
### Amikacin adult PBPK model

Amikacin is a semi-synthetic aminoglycoside antibiotic used for a number of bacterial infections. Amikacin is adminstered in several forms, including intravenous or intramuscular injection. The PBPK of Amikacin has been previously developed in PK-Sim using clinical studies in preterm-neonates. [1] Here we have evaluated its predictive performance of glomerular filtration rate (GFR) mediated clearance in adults and term born children. In this chapter we show that amikacin adequately described the pharmacokinetics of amikacin in adults, based on the PBPK model build and reported in preterm-neonates.

The Amikacin model was evaluated in its performance in adults using data of the following  publication:

- Walker JM, Wise R, Mitchard M. The pharmacokinetics of amikacin and gentamicin in volunteers: a comparison of individual differences. J Antimicrob Chemother. 1979 Jan;5(1):95-9.
(https://academic.oup.com/jac/article/5/1/95/747852)

### References
[1] Claassen K, Thelen K, Coboeken K, Gaub T, Lippert J, Allegaert K, Willmann S1. Development of a Physiologically-Based Pharmacokinetic Model for Preterm Neonates: Evaluation with In Vivo Data. Curr Pharm Des. 2015;21(39):5688-98.

The compound properties used for input are illustrated below.


### Compound: Amikacin

#### Parameters

Name                                       | Value           | Value Origin                                                          | Alternative | Default
------------------------------------------ | --------------- | --------------------------------------------------------------------- | ----------- | -------
Solubility at reference pH                 | 185000 mg/l     | Publication-In Vitro-Drugbank - YALKOWSKY,SH & DANNENFELSER,RM (1992) | Measurement | True   
Reference pH                               | 7               | Publication-In Vitro-Drugbank - YALKOWSKY,SH & DANNENFELSER,RM (1992) | Measurement | True   
Lipophilicity                              | -0.48 Log Units | Publication-Other-Claassen et al 2015                                 | Measurement | True   
Fraction unbound (plasma, reference value) | 1               | Publication-Other-Claassen et al 2015                                 | Measurement | True   
Is small molecule                          | Yes             |                                                                       |             |        
Molecular weight                           | 588.6 g/mol     | Publication-Claassen et al 2015                                       |             |        
Plasma protein binding partner             | Albumin         |                                                                       |             |        
#### Calculation methods

Name                    | Value          
----------------------- | ---------------
Partition coefficients  | PK-Sim Standard
Cellular permeabilities | PK-Sim Standard
#### Processes

##### Systemic Process: Glomerular Filtration-Claassen et al 2015

Species: Human
###### Parameters

Name         | Value | Value Origin                   
------------ | -----:| -------------------------------
GFR fraction |     1 | Publication-Claassen et al 2015

## Chapter 3.2: Amikacin Concentration-Time profiles in Adults
#### Concentration-Time Profiles

Simulated versus observed plasma concentration-time profiles of all data are listed below.
![001_plotTimeProfile.png](images/003_Chapter_3__Adult_PBPK_model_performance/002_Chapter_3_2__Amikacin_Concentration-Time_profiles_in_Adults/001_plotTimeProfile.png)

![002_plotTimeProfile.png](images/003_Chapter_3__Adult_PBPK_model_performance/002_Chapter_3_2__Amikacin_Concentration-Time_profiles_in_Adults/002_plotTimeProfile.png)

![003_plotTimeProfile.png](images/003_Chapter_3__Adult_PBPK_model_performance/002_Chapter_3_2__Amikacin_Concentration-Time_profiles_in_Adults/003_plotTimeProfile.png)

![004_plotTimeProfile.png](images/003_Chapter_3__Adult_PBPK_model_performance/002_Chapter_3_2__Amikacin_Concentration-Time_profiles_in_Adults/004_plotTimeProfile.png)

![005_plotPopulationTimeProfile.png](images/003_Chapter_3__Adult_PBPK_model_performance/002_Chapter_3_2__Amikacin_Concentration-Time_profiles_in_Adults/005_plotPopulationTimeProfile.png)

![006_plotPopulationTimeProfile.png](images/003_Chapter_3__Adult_PBPK_model_performance/002_Chapter_3_2__Amikacin_Concentration-Time_profiles_in_Adults/006_plotPopulationTimeProfile.png)

## Chapter 3.3: Vancomycin Input Tables
### Vancomycin adult PBPK model

Vancomycin is a glycopeptide antibiotic related to ristocetin that inhibits bacterial cell wall assembly and is used to treat a number of bacterial infections. It can be administered intravenously, as well as orally in case of diarrhea therapy. Vancomyin is mainly eliminated via glomerular filtration (GFR). A previous PBPK model for vancomycin using PK-Sim was reported by Radke et al. [1], with the dose fraction extreted unchanged into urine in adults beeing 90% with 10% hepatic elimination. Our final vancomycin model was rebuild that applies only GFR mediated clearance that adequately described the pharmacokinetics in adults. No further improvement of vancomycin pharmacokinetics could be determined after introducing hepatic clearance.

The vancomyin model was developed using data of the following publications:

- Boeckh M, Lode H, Borner K, Höffken G, Wagner J, Koeppe P. Pharmacokinetics and serum bactericidal activity of vancomycin alone and in combination with ceftazidime in healthy volunteers. Antimicrob Agents Chemother. 1988 Jan;32(1):92-5.

  (https://www.ncbi.nlm.nih.gov/pubmed/3279907)

- Healy DP, Polk RE, Garson ML, Rock DT, Comstock TJ. Comparison of steady-state pharmacokinetics of two dosage regimens of vancomycin in normal volunteers. Antimicrob Agents Chemother. 1987 Mar;31(3):393-7.

  (https://www.ncbi.nlm.nih.gov/pubmed/3579256)

### References

[1] Radke C, Horn D, Lanckohr C, Ellger B, Meyer M, Eissing T, Hempel G. Development of a Physiologically Based Pharmacokinetic Modelling Approach to Predict the Pharmacokinetics of Vancomycin in Critically Ill Septic Patients. Clin Pharmacokinet. 2017 Jul;56(7):759-779. doi: 10.1007/s40262-016-0475-3.
(https://www.ncbi.nlm.nih.gov/pubmed/28039606)

The compound properties used for input are illustrated below.


### Compound: Vancomycin

#### Parameters

Name                                       | Value                  | Value Origin                                      | Alternative | Default
------------------------------------------ | ---------------------- | ------------------------------------------------- | ----------- | -------
Solubility at reference pH                 | 225 mg/l               | Internet-Drugbank                                 | Drugbank    | True   
Reference pH                               | 7                      | Internet-Drugbank                                 | Drugbank    | True   
Lipophilicity                              | 2.2307891407 Log Units | Parameter Identification-Parameter Identification | LogP        | True   
Fraction unbound (plasma, reference value) | 0.67                   | Parameter Identification-Parameter Identification | Measurement | True   
Is small molecule                          | Yes                    |                                                   |             |        
Molecular weight                           | 1449.3 g/mol           | Publication-Other-Radke 2017                      |             |        
Plasma protein binding partner             | Albumin                |                                                   |             |        
#### Calculation methods

Name                    | Value                   
----------------------- | ------------------------
Partition coefficients  | Schmitt                 
Cellular permeabilities | Charge dependent Schmitt
#### Processes

##### Systemic Process: Glomerular Filtration-Zhou et al. 2016 GFR

Species: Human
###### Parameters

Name         | Value | Value Origin               
------------ | -----:| ---------------------------
GFR fraction |     1 | Publication-Other-Zhou 2016
##### Systemic Process: Total Hepatic Clearance-Radtke 2017

Species: Human
###### Parameters

Name                          | Value          | Value Origin                                                                                                         
----------------------------- | -------------- | ---------------------------------------------------------------------------------------------------------------------
Fraction unbound (experiment) | 0.67           |                                                                                                                      
Lipophilicity (experiment)    | 2.45 Log Units |                                                                                                                      
Plasma clearance              | 0.11 ml/min/kg |                                                                                                                      
Specific clearance            | 0 1/min        | Parameter Identification-Parameter Identification-Value updated from 'Parameter Identification 3' on 2018-07-13 11:16

## Chapter 3.4: Vancomycin Diagnostics Plots
### Vancomycin adult PBPK model performance

Below you find the input goodness-of-fit visual diagnostic plots for vancomycin PBPK model performance (observed versus individually simulated plasma concentration and weighted residuals versus time) of all adult data.


![001_plotGOFMergedPredictedVsObserved.png](images/003_Chapter_3__Adult_PBPK_model_performance/004_Chapter_3_4__Vancomycin_Diagnostics_Plots/001_plotGOFMergedPredictedVsObserved.png)

GMFE = 1.108921 

![003_plotGOFMergedResidualsOverTime.png](images/003_Chapter_3__Adult_PBPK_model_performance/004_Chapter_3_4__Vancomycin_Diagnostics_Plots/003_plotGOFMergedResidualsOverTime.png)

GMFE = 1.108921 

## Chapter 3.5: Vancomycin Concentration-Time profiles in Adults
#### Concentration-Time Profiles

Simulated versus observed plasma concentration-time profiles of all data are listed below.
![001_plotTimeProfile.png](images/003_Chapter_3__Adult_PBPK_model_performance/005_Chapter_3_5__Vancomycin_Concentration-Time_profiles_in_Adults/001_plotTimeProfile.png)

![002_plotTimeProfile.png](images/003_Chapter_3__Adult_PBPK_model_performance/005_Chapter_3_5__Vancomycin_Concentration-Time_profiles_in_Adults/002_plotTimeProfile.png)

![003_plotTimeProfile.png](images/003_Chapter_3__Adult_PBPK_model_performance/005_Chapter_3_5__Vancomycin_Concentration-Time_profiles_in_Adults/003_plotTimeProfile.png)

![004_plotTimeProfile.png](images/003_Chapter_3__Adult_PBPK_model_performance/005_Chapter_3_5__Vancomycin_Concentration-Time_profiles_in_Adults/004_plotTimeProfile.png)

![005_plotTimeProfile.png](images/003_Chapter_3__Adult_PBPK_model_performance/005_Chapter_3_5__Vancomycin_Concentration-Time_profiles_in_Adults/005_plotTimeProfile.png)

![006_plotTimeProfile.png](images/003_Chapter_3__Adult_PBPK_model_performance/005_Chapter_3_5__Vancomycin_Concentration-Time_profiles_in_Adults/006_plotTimeProfile.png)

![007_plotTimeProfile.png](images/003_Chapter_3__Adult_PBPK_model_performance/005_Chapter_3_5__Vancomycin_Concentration-Time_profiles_in_Adults/007_plotTimeProfile.png)

![008_plotTimeProfile.png](images/003_Chapter_3__Adult_PBPK_model_performance/005_Chapter_3_5__Vancomycin_Concentration-Time_profiles_in_Adults/008_plotTimeProfile.png)

