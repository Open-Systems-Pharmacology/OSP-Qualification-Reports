# Pediatric Qualification Package: CYP3A4 Ontogeny





| Version                         | 1.2-OSP9.1                                                   |
| ------------------------------- | ------------------------------------------------------------ |
| Qualification Plan Release      | https://github.com/Open-Systems-Pharmacology/Pediatric_Qualification_Package_CYP3A4_Ontogeny/releases/tag/v1.2 |
| OSP Version                     | 9.1                                                          |
| Qualification Framework Version | 2.2                                                          |





This qualification report is filed at:

https://github.com/Open-Systems-Pharmacology/OSP-Qualification-Reports
# Table of Contents
  * [Chapter 1: Introduction to Pediatric Translation and CYP3A4 Ontogeny Qualification](#chapter-1-introduction-to-pediatric-translation-and-cyp3a4-ontogeny-qualification)
  * [Chapter 2: Pediatric translation qualification results](#chapter-2-pediatric-translation-qualification-results)
    * [Chapter 2.1: Sufentanil PK Ratio tables and Figures](#chapter-21-sufentanil-pk-ratio-tables-and-figures)
    * [Chapter 2.2: Sufentanil Concentration-Time profiles in Children](#chapter-22-sufentanil-concentration-time-profiles-in-children)
    * [Chapter 2.3: Alfentanil PK Ratio tables and Figures](#chapter-23-alfentanil-pk-ratio-tables-and-figures)
    * [Chapter 2.4: Alfentanil Concentration-Time profiles in Children](#chapter-24-alfentanil-concentration-time-profiles-in-children)
  * [Chapter 3: Adult PBPK model building and performance](#chapter-3-adult-pbpk-model-building-and-performance)
    * [Chapter 3.1: Sufentanil Input Tables](#chapter-31-sufentanil-input-tables)
    * [Chapter 3.2: Sufentanil Diagnostics Plots](#chapter-32-sufentanil-diagnostics-plots)
    * [Chapter 3.3: Sufentanil Concentration-Time profiles in Adults](#chapter-33-sufentanil-concentration-time-profiles-in-adults)
    * [Chapter 3.4: Alfentanil Input Tables](#chapter-34-alfentanil-input-tables)
# Chapter 1: Introduction to Pediatric Translation and CYP3A4 Ontogeny Qualification
The presented qualification report evaluates the predictive performance of the OSP suite to predict cytochrome P450 3A4 (CYP3A4)-mediated drug clearance in children.

Therefore, PBPK models of specific *in vivo* probe substances covering children aged below 6 months up to adolescents were built and evaluated. All models are whole-body PBPK models, allowing for dynamic pediatric translation in organs expressing CYP3A4. The qualification report demonstrates the level of confidence of the OSP suite with regard to reliable PBPK predictions of age-related CYP3A4-mediated drug clearance during model-informed drug development. The presented PBPK models as well as the respective qualification plan and qualification report are provided open-source and transparently documented (https://github.com/Open-Systems-Pharmacology/Pediatric-Qualification-Package-CYP3A4). 


## Translation of Adult PBPK to Children

Using a developed and validated (adult) PBPK model for an *in vivo* probe substance, a pediatric PBPK model can be established for children by translating physiology, clearance processes (as parameterized in the adult model) and age-dependent protein binding including the variability therein.[[1](#reference)]

The PBPK models are developed with clinical data of healthy adult subjects obtained from the literature, covering available dosing ranges for e.g. intravenous as well as oral administration, to capture both systemic clearance as well gut-wall metabolic clearance processes. For orally administered drugs, the same formulations that are used in children should ideally be included in the model for adults. Plasma concentrations following multiple-dose application, mass balance information and other clinical measurements need to be included for model development, if available. During model translation from adults to children for a specific substance, uncertainties in data-quality caused by impact of disease or the target study population, inaccurate in vitro assay-techniques regarding mass balance, as well as study differences may cause not being able to adequately predict the PK in children for all reported studies. 

Prediction performance of the PBPK model for these probe substances in children are then shown by means of e.g. predicted versus observed area under the plasma concentration (AUC)-ratio plots, of which the results support an adequate prediction of the ontogeny function for the application of PBPK model translation of adult PBPK to children.

For qualification purpose, during the translation of adult PBPK to children the following assumptions and considerations were made: 

- when translating an adult model to children, it was assumed that the metabolism and excretion pathways are qualitatively the same in children as in adults.
- no further changes to input parameters other than those for the physiology and protein binding. All other parameters (e.g. lipophilicity, intestinal permeability, solubility) were kept unchanged.

## Anthropometric and Physiological Information 

Regarding the age-dependencies of the relevant anthropometric (height, weight) and physiological parameters (e.g. blood flows, organ volumes, binding protein concentrations, hematocrit, cardiac output) in children was gathered from the literature and has been previously published [[2](#reference)]. The information was incorporated into PK-Sim® and was used as default values for the simulations in children.

The  applied ontogeny and variability of plasma proteins and active processes that are integrated into PK-Sim® for translation to children are described in the publicly available ‘PK-Sim® Ontogeny Database Version 7.3' [[3](#reference)] or otherwise referenced for the specific process.

## Qualification of **CYP3A4 enzyme ontogeny**

To qualify the OSP suite for the pediatric translation of the pharmacokinetics of new drugs that are metabolized by CYP3A4, the following set of probe substances was included:

- Alfentanil [[4](#reference)]

- Sufentanil [[5](#reference)]

## References

[1] [Maharaj AR, Barrett JS, Edginton AN. A workflow example of PBPK modeling to support pediatric research and development: case study with lorazepam. The AAPS journal. 2013;15(2): 455-464.](https://www.ncbi.nlm.nih.gov/pubmed/23344790)

[2] [Edginton AN, Schmitt W, Willmann S. Development and evaluation of a generic physiologically based pharmacokinetic model for children. Clin Pharmacokinet. 2006;45(10):1013-34.](https://www.ncbi.nlm.nih.gov/pubmed/16984214)

[3]  [OSPSuite.Documentation/PK-Sim Ontogeny Database Version 7.3.pdf ](https://github.com/Open-Systems-Pharmacology/OSPSuite.Documentation/blob/38cf71b384cfc25cfa0ce4d2f3addfd32757e13b/PK-Sim%20Ontogeny%20Database%20Version%207.3.pdf)

[4] [Alfentanil-Model, Whole-body PBPK model of Alfentanil. https://github.com/Open-Systems-Pharmacology/Alfentanil-Model](https://github.com/incei/Alfentanil-Model)

[5] [Sufentanil-Model, Whole-body PBPK model of Sufentanil. https://github.com/Open-Systems-Pharmacology/Sufentanil-Model](https://github.com/incei/Sufentanil-Model)
# Chapter 2: Pediatric translation qualification results
## Evaluation of Pediatric translation

All pediatric translations are pure retrospective predictions, no pediatric pharmacokinetic studies were used to inform model parameters. All parameters necessary to model the pediatric populations, such as demographics (age, weight, height), as well as dosing formulation information were taken from the respective pediatrics studies from literature in order to evaluate their predictive performance. 

The models were evaluated by ratio plots of area under the plasma concentration-time curve (AUC), or clearance (CL) values resulting from our predictions to the values observed during clinical studies, and by comparison of concentration-time profiles if available. As a quantitative measure of the descriptive and predictive performance of each model, the geometric mean fold error was calculated according to Eq. 1:

Eq. 1: GMFE=10^((Σ|log10(pred PK parameter∕obs PK parameter)|)∕n)

with GMFE = geometric mean fold error of all AUC or CL predictions of the respective model, pred PK parameter = predicted AUC or CL, obs PK parameter = observed AUC or CL, and n = number of observed values.

The ratios of predicted over observed mean AUC or CL values from all compound were also plotted across all age groups in the figure below. As illustrated, most of the prediction were within the 0.5 to 2.0 range (2-fold error). 

In the next sections the demographics as well as the evaluation results of the predictive performance of the specific compound PBPK models in children can be found.  


![005_plotPKRatioAUC.png](images/002_Chapter_2__Pediatric_translation_qualification_results/005_plotPKRatioAUC.png)

GMFE (AUC) = 1.254230 

|AUC                   |Number|Ratio [%]|
|---------------------:|-----:|--------:|
|Points total          |39    |-        |
|Points within 1.5 fold|29    |74.359   |
|Points within 2-fold  |38    |97.4359  |

|Study ID          |Age [y]|BodyWeight [kg]|Predicted AUC [mg*min/ml]|Observed AUC [mg*min/ml]|Pred/Obs AUC Ratio|
|-----------------:|------:|--------------:|------------------------:|-----------------------:|-----------------:|
|Davis 1987        |1.2917 |8.9            |0.54048                  |0.00082873              |0.54048           |
|Davis 1987        |0.43333|5.3            |1.0284                   |0.00054546              |1.0284            |
|Guay 1991         |2.0833 |12.1           |0.60119                  |0.00010838              |0.60119           |
|Guay 1991         |2.5833 |16             |0.85776                  |4.63e-05                |0.85776           |
|Guay 1991         |2.6667 |11.3           |1.1327                   |8.92e-05                |1.1327            |
|Guay 1991         |3.25   |16             |1.0509                   |8.26e-05                |1.0509            |
|Guay 1991         |3.8333 |14.2           |0.84204                  |6.63e-05                |0.84204           |
|Guay 1991         |4.5833 |15             |0.66053                  |6.73e-05                |0.66053           |
|Guay 1991         |4.5833 |19             |0.63325                  |0.00013487              |0.63325           |
|Guay 1991         |4.8333 |17.5           |1.2509                   |6.99e-05                |1.2509            |
|Guay 1991         |5.25   |18.5           |1.0375                   |4.36e-05                |1.0375            |
|Guay 1991         |5.25   |19.65          |1.0358                   |8.53e-05                |1.0358            |
|Guay 1991         |5.3333 |24             |0.8349                   |0.0001355               |0.8349            |
|Guay 1991         |5.3333 |24             |0.8415                   |7.55e-05                |0.8415            |
|Guay 1991         |5.75   |14.5           |0.49761                  |0.00015183              |0.49761           |
|Guay 1991         |5.9167 |28.2           |0.72904                  |0.00012754              |0.72904           |
|Guay 1991         |5.9167 |25             |0.84016                  |5.71e-05                |0.84016           |
|Guay 1991         |6.9167 |29.6           |1.0091                   |6.17e-05                |1.0091            |
|Guay 1991         |7.5    |23.5           |0.76862                  |3.5e-05                 |0.76862           |
|Guay 1991         |7.5    |15.2           |0.99104                  |7.36e-05                |0.99104           |
|Guay 1991         |8.75   |22.6           |0.92858                  |5.65e-05                |0.92858           |
|den Hollander 1992|0.92   |6.5            |1.0835                   |21.1                    |1.0835            |
|den Hollander 1992|0.83   |6.4            |1.6551                   |14                      |1.6551            |
|den Hollander 1992|0.99   |8.5            |1.1878                   |19.8                    |1.1878            |
|den Hollander 1992|0.3    |5.1            |1.654                    |18.5                    |1.654             |
|den Hollander 1992|0.92   |6.149          |1.2302                   |15.9                    |1.2302            |
|den Hollander 1992|1.3    |10.4           |0.96258                  |24.3                    |0.96258           |
|den Hollander 1992|9      |25.6           |1.972                    |11.3                    |1.972             |
|den Hollander 1992|3.5    |14.4           |1.1349                   |18.6                    |1.1349            |
|den Hollander 1992|5.5    |19.5           |1.0307                   |20.7                    |1.0307            |
|den Hollander 1992|3.5    |18.5           |1.0082                   |22.7                    |1.0082            |
|Meistelman 1987   |4.7    |20             |0.77382                  |0.0058824               |0.77382           |
|Meistelman 1987   |5.5    |20             |1.247                    |0.0033898               |1.247             |
|Meistelman 1987   |7.7    |23             |1.7537                   |0.0024096               |1.7537            |
|Meistelman 1987   |4.5    |14             |0.83022                  |0.0043478               |0.83022           |
|Meistelman 1987   |4.8    |24             |0.99562                  |0.0054054               |0.99562           |
|Meistelman 1987   |4.5    |20             |1.1192                   |0.0041667               |1.1192            |
|Meistelman 1987   |6.2    |23             |1.0098                   |0.0045455               |1.0098            |
|Meistelman 1987   |4.9    |22             |0.65818                  |0.0074074               |0.65818           |

## Chapter 2.1: Sufentanil PK Ratio tables and Figures
### Sufentanil model

Sufentanil PBPK predictions in children were evaluated using pharmacokinetic (PK) data reported in the following studies: 

- Davis PJ, Cook DR, Stiller RL, Davin-Robinson KA. Pharmacodynamics and pharmacokinetics of high-dose sufentanil in infants and children undergoing cardiac surgery. Anesth Analg. 1987 Mar;66(3):203-8.
- Guay J, Gaudreault P, Tang A, Goulet B, Varin F. Pharmacokinetics of sufentanil in normal children. Can J Anaesth. 1992 Jan;39(1):14-20.

The pediatric PBPK model predicted the clearance values of sufentanil observed in pediatric studies reasonably across all available age groups, ranging from 5 months to 8.75 years old. The ratios of mean predicted over observed clearance values are illustrated in the table below as well as in the predicted versus observed clearance ratio plot, showing that most predictions in children were within 2-fold error of observed values.


![001_plotPKRatioAUC.png](images/002_Chapter_2__Pediatric_translation_qualification_results/001_Chapter_2_1__Sufentanil_PK_Ratio_tables_and_Figures/001_plotPKRatioAUC.png)

GMFE (AUC) = 1.251766 

|AUC                   |Number|Ratio [%]|
|---------------------:|-----:|--------:|
|Points total          |21    |-        |
|Points within 1.5 fold|16    |76.1905  |
|Points within 2-fold  |20    |95.2381  |

|Study ID  |Age [y]|BodyWeight [kg]|Predicted AUC [mg*min/ml]|Observed AUC [mg*min/ml]|Pred/Obs AUC Ratio|
|---------:|------:|--------------:|------------------------:|-----------------------:|-----------------:|
|Davis 1987|1.2917 |8.9            |0.54048                  |0.00082873              |0.54048           |
|Davis 1987|0.43333|5.3            |1.0284                   |0.00054546              |1.0284            |
|Guay 1991 |2.0833 |12.1           |0.60119                  |0.00010838              |0.60119           |
|Guay 1991 |2.5833 |16             |0.85776                  |4.63e-05                |0.85776           |
|Guay 1991 |2.6667 |11.3           |1.1327                   |8.92e-05                |1.1327            |
|Guay 1991 |3.25   |16             |1.0509                   |8.26e-05                |1.0509            |
|Guay 1991 |3.8333 |14.2           |0.84204                  |6.63e-05                |0.84204           |
|Guay 1991 |4.5833 |15             |0.66053                  |6.73e-05                |0.66053           |
|Guay 1991 |4.5833 |19             |0.63325                  |0.00013487              |0.63325           |
|Guay 1991 |4.8333 |17.5           |1.2509                   |6.99e-05                |1.2509            |
|Guay 1991 |5.25   |18.5           |1.0375                   |4.36e-05                |1.0375            |
|Guay 1991 |5.25   |19.65          |1.0358                   |8.53e-05                |1.0358            |
|Guay 1991 |5.3333 |24             |0.8349                   |0.0001355               |0.8349            |
|Guay 1991 |5.3333 |24             |0.8415                   |7.55e-05                |0.8415            |
|Guay 1991 |5.75   |14.5           |0.49761                  |0.00015183              |0.49761           |
|Guay 1991 |5.9167 |28.2           |0.72904                  |0.00012754              |0.72904           |
|Guay 1991 |5.9167 |25             |0.84016                  |5.71e-05                |0.84016           |
|Guay 1991 |6.9167 |29.6           |1.0091                   |6.17e-05                |1.0091            |
|Guay 1991 |7.5    |23.5           |0.76862                  |3.5e-05                 |0.76862           |
|Guay 1991 |7.5    |15.2           |0.99104                  |7.36e-05                |0.99104           |
|Guay 1991 |8.75   |22.6           |0.92858                  |5.65e-05                |0.92858           |

## Chapter 2.2: Sufentanil Concentration-Time profiles in Children
#### Concentration-Time Profiles

Predicted versus observed plasma concentration-time profiles are listed below. Only simulations where observed data was available for comparison are shown.  Depending if the observed data were individual data or aggregated data, individual predictions or population predictions including variability are shown, respectively.
![001_plotTimeProfile.png](images/002_Chapter_2__Pediatric_translation_qualification_results/002_Chapter_2_2__Sufentanil_Concentration-Time_profiles_in_Children/001_plotTimeProfile.png)

![002_plotTimeProfile.png](images/002_Chapter_2__Pediatric_translation_qualification_results/002_Chapter_2_2__Sufentanil_Concentration-Time_profiles_in_Children/002_plotTimeProfile.png)

![003_plotTimeProfile.png](images/002_Chapter_2__Pediatric_translation_qualification_results/002_Chapter_2_2__Sufentanil_Concentration-Time_profiles_in_Children/003_plotTimeProfile.png)

![004_plotTimeProfile.png](images/002_Chapter_2__Pediatric_translation_qualification_results/002_Chapter_2_2__Sufentanil_Concentration-Time_profiles_in_Children/004_plotTimeProfile.png)

![005_plotTimeProfile.png](images/002_Chapter_2__Pediatric_translation_qualification_results/002_Chapter_2_2__Sufentanil_Concentration-Time_profiles_in_Children/005_plotTimeProfile.png)

![006_plotTimeProfile.png](images/002_Chapter_2__Pediatric_translation_qualification_results/002_Chapter_2_2__Sufentanil_Concentration-Time_profiles_in_Children/006_plotTimeProfile.png)

## Chapter 2.3: Alfentanil PK Ratio tables and Figures
### Alfentanil model

Alfentanil PBPK predictions in children were evaluated using pharmacokinetic (PK) data reported in the following studies: 

- den Hollander JM, Hennis PJ, Burm AG, Vletter AA, Bovill JG. Pharmacokinetics of alfentanil before and after cardiopulmonary bypass in pediatric patients undergoing cardiac surgery: Part I. J Cardiothorac Vasc Anesth. 1992 Jun;6(3):308-12.
- Meistelman C, Saint-Maurice C, Lepaul M, Levron JC, Loose JP, Mac Gee K. A comparison of alfentanil pharmacokinetics in children and adults. Anesthesiology. 1987 Jan;66(1):13-6.

The pediatric PBPK model predicted the AUC values of alfentanil observed in pediatric studies reasonably across all available age groups, ranging from 3.6 months to 9 years old. The ratios of mean predicted over observed AUC values are illustrated in the table below as well as in the predicted versus observed AUC ratio plot, showing that most predictions in children were within 2-fold error of observed values. Another reported study on alfentanil pharmacokinetics in children [1] showed systematically higher exposure for most individuals compared to the other herein included studies. This deviation may have been caused by different impact of individual pathophysiologies of the target study population, inaccurate in vitro assay-techniques or other study differences. 

### References

[1] Goresky GV, Koren G, Sabourin MA, Sale JP, Strunin L., The pharmacokinetics of alfentanil in children. Anesthesiology. 1987 Nov;67(5):654-9.
![001_plotPKRatioAUC.png](images/002_Chapter_2__Pediatric_translation_qualification_results/003_Chapter_2_3__Alfentanil_PK_Ratio_tables_and_Figures/001_plotPKRatioAUC.png)

GMFE (AUC) = 1.257111 

|AUC                   |Number|Ratio [%]|
|---------------------:|-----:|--------:|
|Points total          |18    |-        |
|Points within 1.5 fold|13    |72.2222  |
|Points within 2-fold  |18    |100      |

|Study ID          |Age [y]|BodyWeight [kg]|Predicted AUC [mg*min/l]|Observed AUC [mg*min/l]|Pred/Obs AUC Ratio|
|-----------------:|------:|--------------:|-----------------------:|----------------------:|-----------------:|
|den Hollander 1992|0.92   |6.5            |1.0835                  |21.1                   |1.0835            |
|den Hollander 1992|0.83   |6.4            |1.6551                  |14                     |1.6551            |
|den Hollander 1992|0.99   |8.5            |1.1878                  |19.8                   |1.1878            |
|den Hollander 1992|0.3    |5.1            |1.654                   |18.5                   |1.654             |
|den Hollander 1992|0.92   |6.149          |1.2302                  |15.9                   |1.2302            |
|den Hollander 1992|1.3    |10.4           |0.96258                 |24.3                   |0.96258           |
|den Hollander 1992|9      |25.6           |1.972                   |11.3                   |1.972             |
|den Hollander 1992|3.5    |14.4           |1.1349                  |18.6                   |1.1349            |
|den Hollander 1992|5.5    |19.5           |1.0307                  |20.7                   |1.0307            |
|den Hollander 1992|3.5    |18.5           |1.0082                  |22.7                   |1.0082            |
|Meistelman 1987   |4.7    |20             |0.77382                 |0.0058824              |0.77382           |
|Meistelman 1987   |5.5    |20             |1.247                   |0.0033898              |1.247             |
|Meistelman 1987   |7.7    |23             |1.7537                  |0.0024096              |1.7537            |
|Meistelman 1987   |4.5    |14             |0.83022                 |0.0043478              |0.83022           |
|Meistelman 1987   |4.8    |24             |0.99562                 |0.0054054              |0.99562           |
|Meistelman 1987   |4.5    |20             |1.1192                  |0.0041667              |1.1192            |
|Meistelman 1987   |6.2    |23             |1.0098                  |0.0045455              |1.0098            |
|Meistelman 1987   |4.9    |22             |0.65818                 |0.0074074              |0.65818           |

## Chapter 2.4: Alfentanil Concentration-Time profiles in Children
#### Concentration-Time Profiles

Predicted versus observed plasma concentration-time profiles are listed below. Only simulations where observed data was available for comparison are shown.  Depending if the observed data were individual data or aggregated data, individual predictions or population predictions including variability are shown, respectively.
![001_plotTimeProfile.png](images/002_Chapter_2__Pediatric_translation_qualification_results/004_Chapter_2_4__Alfentanil_Concentration-Time_profiles_in_Children/001_plotTimeProfile.png)

![002_plotTimeProfile.png](images/002_Chapter_2__Pediatric_translation_qualification_results/004_Chapter_2_4__Alfentanil_Concentration-Time_profiles_in_Children/002_plotTimeProfile.png)

![003_plotPopulationTimeProfile.png](images/002_Chapter_2__Pediatric_translation_qualification_results/004_Chapter_2_4__Alfentanil_Concentration-Time_profiles_in_Children/003_plotPopulationTimeProfile.png)

![004_plotPopulationTimeProfile.png](images/002_Chapter_2__Pediatric_translation_qualification_results/004_Chapter_2_4__Alfentanil_Concentration-Time_profiles_in_Children/004_plotPopulationTimeProfile.png)

# Chapter 3: Adult PBPK model building and performance
## Evaluation of Adult PBPK models

The PBPK models of **sufentanil** and **alfentanil** were developed with clinical pharmacokinetic data covering at least administrations given in children. Plasma concentrations following intravenous administration, oral administration, multiple dose application, fractions excreted to urine or bile and other clinical measurements were included for model development whenever available. 


## Chapter 3.1: Sufentanil Input Tables
### Sufentanil adult PBPK model

Sufentanil is a potent synthetic opioid. Like other opioids, sufentanil creates a stable hemodynamic environment in cardiovascularly compromised pediatric patients. Sufentanil has a high lipid solubility, which accounts for the fast onset when given intravenously. The commercial solution comes as preservative‐free sufentanil citrate, injectable with a pH of 4.5–7.0 (Jansen‐Cilag AB, Sweden). Sufentanil is solely metabolised by CYP3A4. Due to the high hepatic extraction ratio, for the overall clearance of sufentanil both CYP3A4 values as well as liver blood flow rate play dominant roles in the elimination in adult populations. The final sufentanil model applies metabolism by CYP3A4 and glomerular filtration and adequately described the pharmacokinetics of sufentanil in adults.

The Sufentanil model was developed using data of the following publications:

- Bovill JG, Sebel PS, Blackburn CL, Oei-Lim V, Heykants JJ. The pharmacokinetics of sufentanil in surgical patients. Anesthesiology. 1984 Nov;61(5):502-6. (https://www.ncbi.nlm.nih.gov/pubmed/6238552)
- Willsie SK, Evashenk MA2, Hamel LG, Hwang SS, Chiang YK, Palmer PP. Pharmacokinetic properties of single- and repeated-dose sufentanil sublingual tablets in healthy volunteers. Clin Ther. 2015 Jan 1;37(1):145-55. doi: 10.1016/j.clinthera.2014.11.001. Epub 2014 Dec 24.
(https://www.ncbi.nlm.nih.gov/pubmed/25544247)

The compound properties used for input are illustrated below.
### Compound: Sufentanil

#### Parameters

Name                                       | Value                | Value Origin                                      | Alternative              | Default
------------------------------------------ | -------------------- | ------------------------------------------------- | ------------------------ | -------
Solubility at reference pH                 | 0.076 mg/l           | Internet-Other-ROY,SD & FLYNN,GL (1988)           | ROY,SD & FLYNN,GL (1988) | True   
Reference pH                               | 7                    | Internet-Other-ROY,SD & FLYNN,GL (1988)           | ROY,SD & FLYNN,GL (1988) | True   
Lipophilicity                              | 2.896 Log Units      | Parameter Identification-Parameter Identification | Fitted LogP              | True   
Fraction unbound (plasma, reference value) | 0.075                | Publication-Zhou et al. 2017                      | Zhou et al. 2017         | True   
Is small molecule                          | Yes                  |                                                   |                          |        
Molecular weight                           | 386.6 g/mol          | Publication-Zhou et al. 2017                      |                          |        
Plasma protein binding partner             | α1-acid glycoprotein |                                                   |                          |        
#### Calculation methods

Name                    | Value          
----------------------- | ---------------
Partition coefficients  | Schmitt        
Cellular permeabilities | PK-Sim Standard
#### Processes

##### Systemic Process: Glomerular Filtration-GFR

Species: Human
###### Parameters

Name         | Value | Value Origin                
------------ | -----:| ----------------------------
GFR fraction |     1 | Publication-Zhou et al. 2017
##### Metabolizing Enzyme: CYP3A4-Zhou et al. 2017

Species: Human
Molecule: CYP3A4
###### Parameters

Name                | Value              | Value Origin                                     
------------------- | ------------------ | -------------------------------------------------
Intrinsic clearance | 9.6138746106 l/min | Parameter Identification-Parameter Identification

## Chapter 3.2: Sufentanil Diagnostics Plots
### Sufentanil adult PBPK model performance

Below you find the input goodness-of-fit visual diagnostic plots for sufentanil PBPK model performance (observed versus individually simulated plasma concentration and weighted residuals versus time) of all adult data.


![001_plotGOFMergedPredictedVsObserved.png](images/003_Chapter_3__Adult_PBPK_model_building_and_performance/002_Chapter_3_2__Sufentanil_Diagnostics_Plots/001_plotGOFMergedPredictedVsObserved.png)

GMFE = 1.402222 

![003_plotGOFMergedResidualsOverTime.png](images/003_Chapter_3__Adult_PBPK_model_building_and_performance/002_Chapter_3_2__Sufentanil_Diagnostics_Plots/003_plotGOFMergedResidualsOverTime.png)

GMFE = 1.402222 

## Chapter 3.3: Sufentanil Concentration-Time profiles in Adults
#### Concentration-Time Profiles

Simulated versus observed plasma concentration-time profiles of all data are listed below.
![001_plotTimeProfile.png](images/003_Chapter_3__Adult_PBPK_model_building_and_performance/003_Chapter_3_3__Sufentanil_Concentration-Time_profiles_in_Adults/001_plotTimeProfile.png)

![002_plotTimeProfile.png](images/003_Chapter_3__Adult_PBPK_model_building_and_performance/003_Chapter_3_3__Sufentanil_Concentration-Time_profiles_in_Adults/002_plotTimeProfile.png)

![003_plotTimeProfile.png](images/003_Chapter_3__Adult_PBPK_model_building_and_performance/003_Chapter_3_3__Sufentanil_Concentration-Time_profiles_in_Adults/003_plotTimeProfile.png)

![004_plotTimeProfile.png](images/003_Chapter_3__Adult_PBPK_model_building_and_performance/003_Chapter_3_3__Sufentanil_Concentration-Time_profiles_in_Adults/004_plotTimeProfile.png)

![005_plotTimeProfile.png](images/003_Chapter_3__Adult_PBPK_model_building_and_performance/003_Chapter_3_3__Sufentanil_Concentration-Time_profiles_in_Adults/005_plotTimeProfile.png)

![006_plotTimeProfile.png](images/003_Chapter_3__Adult_PBPK_model_building_and_performance/003_Chapter_3_3__Sufentanil_Concentration-Time_profiles_in_Adults/006_plotTimeProfile.png)

## Chapter 3.4: Alfentanil Input Tables
### Alfentanil model

Alfentanil is another potent, short-acting synthetic opioid analgesic drug, used for anaesthesia in surgery, which is solely metabolized by CYP3A4, with less than 1% of an alfentanil dose being excreted unchanged in urine after intravenous administration. The model has been build and evaluated in healthy adults and published by Hanke et al. [1] The model applies metabolism by CYP3A4 and glomerular filtration. The alfentanil PBPK model adequately described the pharmacokinetics of alfentanil in adults. Additionally the model has been republished and fully described including evaluation documentation of the adult PBPK model in Github under 'https://github.com/Open-Systems-Pharmacology/Alfentanil-Model/tree/v2.0' [2].

### References

[1] Hanke N, Frechen S, Moj D, Britz H, Eissing T, Wendl T, Lehr T. PBPK models for CYP3A4 and P-gp DDI prediction: a modeling network of rifampicin, itraconazole, clarithromycin, midazolam, alfentanil and digoxin. CPT: Pharmacometrics & Systems Pharmacology (2018), https://doi.org/10.1002/psp4.12343.

[2] https://github.com/Open-Systems-Pharmacology/Alfentanil-Model/tree/v2.0

The compound properties used for input are illustrated below.
### Compound: Alfentanil

#### Parameters

Name                                             | Value                   | Value Origin                                                                                                          | Alternative | Default
------------------------------------------------ | ----------------------- | --------------------------------------------------------------------------------------------------------------------- | ----------- | -------
Solubility at reference pH                       | 992 mg/l                | Publication-Hanke 2018                                                                                                | Baneyx 2014 | True   
Reference pH                                     | 6.5                     | Publication-Hanke 2018                                                                                                | Baneyx 2014 | True   
Lipophilicity                                    | 1.8463211883 Log Units  | Parameter Identification-Parameter Identification-Value updated from 'Parameter Identification 4' on 2019-09-06 11:28 | Fit         | True   
Fraction unbound (plasma, reference value)       | 0.1                     | Parameter Identification-Parameter Identification-Value updated from 'Parameter Identification 4' on 2019-09-06 11:28 | Healthy     | True   
Permeability                                     | 0.0068752756625 cm/min  | Parameter Identification-Parameter Identification-Value updated from 'Parameter Identification 4' on 2019-09-06 11:28 | Optimized   | True   
Specific intestinal permeability (transcellular) | 0.00057373577138 cm/min | Parameter Identification-Parameter Identification-Value updated from 'Parameter Identification 4' on 2019-09-06 11:28 | Optimized   | True   
Is small molecule                                | Yes                     |                                                                                                                       |             |        
Molecular weight                                 | 416.52 g/mol            | Publication-Drugbank                                                                                                  |             |        
Plasma protein binding partner                   | α1-acid glycoprotein    |                                                                                                                       |             |        
#### Calculation methods

Name                    | Value              
----------------------- | -------------------
Partition coefficients  | Rodgers and Rowland
Cellular permeabilities | PK-Sim Standard    
#### Processes

##### Metabolizing Enzyme: CYP3A4-1st order CL

Species: Human
Molecule: CYP3A4
###### Parameters

Name                | Value              | Value Origin                                                                                                         
------------------- | ------------------ | ---------------------------------------------------------------------------------------------------------------------
Intrinsic clearance | 0.5272297928 l/min | Parameter Identification-Parameter Identification-Value updated from 'Parameter Identification 4' on 2019-09-06 11:28
##### Systemic Process: Glomerular Filtration-GFR

Species: Human
###### Parameters

Name         | Value | Value Origin          
------------ | -----:| ----------------------
GFR fraction |  0.06 | Publication-Hanke 2018

