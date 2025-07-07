# Pediatric Qualification Package: GFR Ontogeny

| Version                         | 1.0-OSP12.0                                                   |
| ------------------------------- | ------------------------------------------------------------ |
| Qualification Plan Release      | [https://github.com/Open-Systems-Pharmacology/Pediatric_Qualification_Package_GFR_Ontogeny/releases/tag/v1.0](https://github.com/Open-Systems-Pharmacology/Pediatric_Qualification_Package_GFR_Ontogeny/releases/tag/v1.0) |
| OSP Version                     | 12.0                                                          |
| Qualification Framework Version | 3.3                                                          |

This qualification report is filed at:

[https://github.com/Open-Systems-Pharmacology/OSP-Qualification-Reports](https://github.com/Open-Systems-Pharmacology/OSP-Qualification-Reports)

# Table of Contents

 * [1 Introduction to Pediatric Translation](#introduction)
 * [2 Pediatric translation qualification](#pediatric-translation-qualification)
   * [2.1 Amikacin PK Ratio tables and Figures](#amikacin-pk-ratios)
   * [2.2 Amikacin Concentration-Time profiles in Children](#amikacin-ct-profiles)
   * [2.3 Vancomycin PK Ratio tables and Figures](#vancomycin-pk-ratios)
   * [2.4 Vancomycin Concentration-Time profiles in Children](#vancomycin-ct-profiles)
 * [3 References](#main-references)

# 1 Introduction to Pediatric Translation<a id="introduction"></a>

The presented qualification report evaluates the predictive performance of the OSP suite to predict glomerular filtration rate (GFR)-mediated drug clearance in children.

Therefore, PBPK models of specific *in vivo* probe substances covering children aged below 6 months up to adolescents were built and evaluated. All models are whole-body PBPK models, allowing for pediatric translation in all organs. The qualification report demonstrates the level of confidence of the OSP suite with regard to reliable PBPK predictions of age related GFR-mediated drug clearance during model-informed drug development. The presented PBPK models as well as the respective qualification plan and qualification report are provided open-source and transparently documented ([https://github.com/Open-Systems-Pharmacology/Pediatric_Qualification_Package_GFR_Ontogeny](https://github.com/Open-Systems-Pharmacology/Pediatric_Qualification_Package_GFR_Ontogeny)). 

## Translation of Adult PBPK to Children

Using a developed and validated (adult) PBPK model for an *in vivo* probe substance, a pediatric PBPK model can be established for children at different ages by translating physiology, clearance processes (as parameterized in the adult model) and age-dependent protein binding including the variability therein.[[Maharaj 2013](#3-references)] 

The PBPK models are developed with clinical data of healthy adult subjects obtained from the literature. Plasma concentrations following multiple-dose application, mass balance information and other clinical measurements need to be included for model development, if available. During model translation from adults to children for a specific substance, uncertainties in data-quality caused by impact of disease or the target study population, inaccurate in vitro assay-techniques regarding mass balance, as well as study differences may cause not being able to adequately predict the PK in children for all reported studies. 

Prediction performance of the PBPK model for these probe substances in children are then shown by means of e.g. predicted versus observed clearance-ratio plots, of which the results support an adequate prediction of the ontogeny function for the application of PBPK model translation of adult PBPK to children.

For qualification purpose, during the translation of adult PBPK to children the following assumptions and considerations were made: 

- when translating an adult model to children, it was assumed that the metabolism and excretion pathways are qualitatively the same in children as in adults.
- no further changes to input parameters other than those for the physiology and protein binding. All other parameters (e.g. lipophilicity) were kept unchanged. 

## Anthropometric and Physiological Information 

Regarding the age-dependencies of the relevant anthropometric (height, weight) and physiological parameters (e.g. blood flows, organ volumes, binding protein concentrations, hematocrit, cardiac output) in children was gathered from the literature and has been previously published. [[Edginton 2006](#3-references)] The information was incorporated into PK-Sim® and was used as default values for the simulations in children.

The  applied ontogeny and variability of plasma proteins that are integrated into PK-Sim® for translation to children are described in the publicly available ‘PK-Sim® Ontogeny Database Version 7.3' [[Ontogeny Database](#3-references)] or otherwise referenced for the specific process.

### Qualification of **GFR ontogeny**

For the qualification of the GFR elimination of compounds, the following probe substances were included:

- Amikacin [[Amikacin-Model](#3-references)]
- Vancomycin [[Vancomycin-Model](#3-references)]

The adult PBPK model reports and the corresponding PK-Sim project files are filed at: [https://github.com/Open-Systems-Pharmacology/OSP-PBPK-Model-Library/](https://github.com/Open-Systems-Pharmacology/OSP-PBPK-Model-Library/)

# 2 Pediatric translation qualification<a id="pediatric-translation-qualification"></a>

## Evaluation of Pediatric translation

All pediatric translations are pure retrospective predictions, no pediatric pharmacokinetic studies were used to inform model parameters. All parameters necessary to model the pediatric populations, such as demographics (age, weight, height), as well as dosing formulation information were taken from the respective pediatrics studies from literature in order to evaluate their predictive performance. 

The models were evaluated by ratio plots of area under the plasma concentration-time curve (AUC), or clearance (CL) values resulting from our predictions to the values observed during clinical studies, and by comparison of concentration-time profiles if available. As a quantitative measure of the descriptive and predictive performance of each model, the geometric mean fold error was calculated according to Eq. 1:

Eq. 1: GMFE=10^((Σ|log10(pred PK parameter∕obs PK parameter)|)∕n)

with GMFE = geometric mean fold error of all AUC or CL predictions of the respective model, pred PK parameter = predicted AUC or CL, obs PK parameter = observed AUC or CL, and n = number of observed values.

The ratios of predicted over observed mean AUC or CL values from all compound were also plotted across all age groups in the figure below. As illustrated, most of the prediction were within the 0.5 to 2.0 range (2-fold error). 

In the next sections the demographics as well as the evaluation results of the predictive performance of the specific compound PBPK models in children can be found.  

<a id="figure-2-1"></a>

![](images/002_section_pediatric-translation-qualification/1_pk_ratio_plot_CL.png)

**Figure 2-1: Overall predictivity of the PBPK models. Open circles represent mean ratios of PBPK predicted clearance over observed clearance of all drugs in children 0.085 month to 16 years old. Blue dashed lines and red dotted lines represent the 1.5-fold and 2-fold error, respectively.**

<br>
<br>

<a id="table-2-1"></a>

**Table 2-1: Measure of Overall predictivity of the PBPK models. Open circles represent mean ratios of PBPK predicted clearance over observed clearance of all drugs in children 0.085 month to 16 years old. Blue dashed lines and red dotted lines represent the 1.5-fold and 2-fold error, respectively.**

|                       |Number |Ratio [%] |
|:----------------------|:------|:---------|
|Points total           |39     |-        |
|Points within 1.5 fold |32     |82.05     |
|Points within 2 fold   |38     |97.44     |

<br>
<br>

<a id="table-2-2"></a>

**Table 2-2: GMFE for Overall predictivity of the PBPK models. Open circles represent mean ratios of PBPK predicted clearance over observed clearance of all drugs in children 0.085 month to 16 years old. Blue dashed lines and red dotted lines represent the 1.5-fold and 2-fold error, respectively.**

|Parameter |GMFE |
|:---------|:----|
|CL        |1.26 |

<br>
<br>

<a id="table-2-3"></a>

**Table 2-3: Overall predictivity of the PBPK models. Open circles represent mean ratios of PBPK predicted clearance over observed clearance of all drugs in children 0.085 month to 16 years old. Blue dashed lines and red dotted lines represent the 1.5-fold and 2-fold error, respectively.**

|Study ID        |Age [year(s)] |Body Weight [kg] |Predicted CL [ml/min/kg] |Observed CL [ml/min/kg] |Pred/Obs CL Ratio |
|:---------------|:-------------|:----------------|:------------------------|:-----------------------|:-----------------|
|Vogelstein 1977 |15.00         |77.00            |1.24                     |1.74                    |0.71              |
|Vogelstein 1977 |15.00         |62.50            |1.37                     |1.44                    |0.95              |
|Vogelstein 1977 |9.00          |21.50            |2.14                     |2.56                    |0.84              |
|Vogelstein 1977 |13.00         |51.00            |1.37                     |1.35                    |1.02              |
|Vogelstein 1977 |12.00         |27.19            |2.48                     |2.64                    |0.94              |
|Vogelstein 1977 |7.00          |27.40            |1.78                     |2.19                    |0.81              |
|Vogelstein 1977 |4.00          |14.00            |2.44                     |4.22                    |0.58              |
|Vogelstein 1977 |6.00          |17.30            |2.49                     |2.63                    |0.95              |
|Vogelstein 1977 |6.00          |15.50            |2.60                     |4.26                    |0.61              |
|Vogelstein 1977 |7.00          |15.90            |2.74                     |2.30                    |1.19              |
|Vogelstein 1977 |14.00         |39.50            |1.83                     |1.91                    |0.96              |
|Vogelstein 1977 |10.00         |32.80            |1.93                     |2.30                    |0.84              |
|Vogelstein 1977 |14.00         |45.50            |1.80                     |2.23                    |0.81              |
|Vogelstein 1977 |11.00         |35.20            |1.90                     |2.58                    |0.74              |
|Vogelstein 1977 |13.00         |27.70            |2.22                     |2.86                    |0.77              |
|Vogelstein 1977 |8.00          |20.80            |2.48                     |2.88                    |0.86              |
|Vogelstein 1977 |6.00          |15.50            |2.57                     |3.31                    |0.78              |
|Vogelstein 1977 |13.00         |49.00            |1.43                     |1.88                    |0.76              |
|Vogelstein 1977 |7.00          |20.60            |2.36                     |2.06                    |1.14              |
|Vogelstein 1977 |16.00         |35.08            |2.21                     |2.47                    |0.89              |
|Treluyer 2002   |0.01          |3.59             |1.17                     |0.88                    |1.32              |
|Treluyer 2002   |0.04          |3.76             |1.34                     |1.22                    |1.10              |
|Treluyer 2002   |0.07          |3.93             |1.54                     |1.58                    |0.97              |
|Treluyer 2002   |0.08          |4.01             |1.65                     |1.77                    |0.93              |
|Treluyer 2002   |0.11          |4.19             |1.85                     |1.97                    |0.94              |
|Treluyer 2002   |0.15          |4.45             |2.10                     |2.00                    |1.05              |
|Treluyer 2002   |0.52          |6.85             |2.44                     |2.12                    |1.15              |
|Treluyer 2002   |0.77          |8.49             |2.40                     |2.50                    |0.96              |
|Treluyer 2002   |2.02          |12.30            |2.24                     |3.02                    |0.74              |
|Treluyer 2002   |4.06          |16.89            |2.10                     |3.17                    |0.66              |
|Treluyer 2002   |6.08          |21.82            |2.02                     |3.27                    |0.62              |
|Treluyer 2002   |7.09          |24.43            |2.00                     |2.95                    |0.68              |
|Belfayol 1996   |7.00          |23.50            |1.98                     |2.40                    |0.83              |
|Schaad 1980     |0.01          |3.07             |1.31                     |1.19                    |1.11              |
|Schaad 1980     |0.26          |4.90             |2.14                     |1.65                    |1.29              |
|Schaad 1980     |0.36          |5.20             |2.27                     |2.70                    |0.84              |
|Schaad 1980     |3.92          |15.50            |1.83                     |3.95                    |0.46              |
|Schaad 1980     |5.58          |20.00            |1.70                     |2.95                    |0.58              |
|Schaad 1980     |7.58          |26.70            |1.56                     |2.78                    |0.56              |

<br>
<br>

## 2.1 Amikacin PK Ratio tables and Figures<a id="amikacin-pk-ratios"></a>

### Amikacin model

Amikacin PBPK predictions in children were evaluated using pharmacokinetic (PK) data reported in the following studies: 

- Tréluyer JM, Merlé Y, Tonnelier S, Rey E, Pons G. Nonparametric population pharmacokinetic analysis of amikacin in neonates, infants, and children. Antimicrob Agents Chemother. 2002 May;46(5):1381-7.[[Tréluyer 2002](#3-references)]
- Vogelstein B, Kowarski A, Lietman PS. The pharmacokinetics of amikacin in children. J Pediatr. 1977 Aug;91(2):333-9.[Vogelstein 1977](#3-references)]
- Belfayol L, Talon P, Eveillard M, Alet P, Fauvelle F. Pharmacokinetics of once-daily amikacin in pediatric patients. Clin Microbiol Infect. 1996 Feb;2(3):186-191.[[Belfayol 1996](#3-references)]

The pediatric PBPK model reasonably well predicted the clearance values of amikacin  pediatric studies across all available age groups, ranging from 0.16 months to 16 years old. The ratios of mean predicted over observed clearance values are illustrated in the table below as well as in the predicted versus observed clearance ratio plot, showing that all predictions in children were within 2-fold error of observed values.

<a id="figure-2-2"></a>

![](images/002_section_pediatric-translation-qualification/003_section_amikacin-pk-ratios/5_pk_ratio_plot_CL.png)

**Figure 2-2: Overall predictivity of the amikacin PBPK model. Open circles represent mean ratios of PBPK predicted clearance over observed clearance of amikacin in children 0.16 months to 16 years old. Blue dashed lines and red dotted lines represent the 1.5-fold and 2-fold error, respectively.**

<br>
<br>

<a id="table-2-4"></a>

**Table 2-4: Measure of Overall predictivity of the amikacin PBPK model. Open circles represent mean ratios of PBPK predicted clearance over observed clearance of amikacin in children 0.16 months to 16 years old. Blue dashed lines and red dotted lines represent the 1.5-fold and 2-fold error, respectively.**

|                       |Number |Ratio [%] |
|:----------------------|:------|:---------|
|Points total           |33     |-        |
|Points within 1.5 fold |29     |87.88     |
|Points within 2 fold   |33     |100.00    |

<br>
<br>

<a id="table-2-5"></a>

**Table 2-5: GMFE for Overall predictivity of the amikacin PBPK model. Open circles represent mean ratios of PBPK predicted clearance over observed clearance of amikacin in children 0.16 months to 16 years old. Blue dashed lines and red dotted lines represent the 1.5-fold and 2-fold error, respectively.**

|Parameter |GMFE |
|:---------|:----|
|CL        |1.22 |

<br>
<br>

<a id="table-2-6"></a>

**Table 2-6: Overall predictivity of the amikacin PBPK model. Open circles represent mean ratios of PBPK predicted clearance over observed clearance of amikacin in children 0.16 months to 16 years old. Blue dashed lines and red dotted lines represent the 1.5-fold and 2-fold error, respectively.**

|Study ID        |Age [year(s)] |Body Weight [kg] |Predicted CL [ml/min/kg] |Observed CL [ml/min/kg] |Pred/Obs CL Ratio |
|:---------------|:-------------|:----------------|:------------------------|:-----------------------|:-----------------|
|Vogelstein 1977 |15.00         |77.00            |1.24                     |1.74                    |0.71              |
|Vogelstein 1977 |15.00         |62.50            |1.37                     |1.44                    |0.95              |
|Vogelstein 1977 |9.00          |21.50            |2.14                     |2.56                    |0.84              |
|Vogelstein 1977 |13.00         |51.00            |1.37                     |1.35                    |1.02              |
|Vogelstein 1977 |12.00         |27.19            |2.48                     |2.64                    |0.94              |
|Vogelstein 1977 |7.00          |27.40            |1.78                     |2.19                    |0.81              |
|Vogelstein 1977 |4.00          |14.00            |2.44                     |4.22                    |0.58              |
|Vogelstein 1977 |6.00          |17.30            |2.49                     |2.63                    |0.95              |
|Vogelstein 1977 |6.00          |15.50            |2.60                     |4.26                    |0.61              |
|Vogelstein 1977 |7.00          |15.90            |2.74                     |2.30                    |1.19              |
|Vogelstein 1977 |14.00         |39.50            |1.83                     |1.91                    |0.96              |
|Vogelstein 1977 |10.00         |32.80            |1.93                     |2.30                    |0.84              |
|Vogelstein 1977 |14.00         |45.50            |1.80                     |2.23                    |0.81              |
|Vogelstein 1977 |11.00         |35.20            |1.90                     |2.58                    |0.74              |
|Vogelstein 1977 |13.00         |27.70            |2.22                     |2.86                    |0.77              |
|Vogelstein 1977 |8.00          |20.80            |2.48                     |2.88                    |0.86              |
|Vogelstein 1977 |6.00          |15.50            |2.57                     |3.31                    |0.78              |
|Vogelstein 1977 |13.00         |49.00            |1.43                     |1.88                    |0.76              |
|Vogelstein 1977 |7.00          |20.60            |2.36                     |2.06                    |1.14              |
|Vogelstein 1977 |16.00         |35.08            |2.21                     |2.47                    |0.89              |
|Treluyer 2002   |0.01          |3.59             |1.17                     |0.88                    |1.32              |
|Treluyer 2002   |0.04          |3.76             |1.34                     |1.22                    |1.10              |
|Treluyer 2002   |0.07          |3.93             |1.54                     |1.58                    |0.97              |
|Treluyer 2002   |0.08          |4.01             |1.65                     |1.77                    |0.93              |
|Treluyer 2002   |0.11          |4.19             |1.85                     |1.97                    |0.94              |
|Treluyer 2002   |0.15          |4.45             |2.10                     |2.00                    |1.05              |
|Treluyer 2002   |0.52          |6.85             |2.44                     |2.12                    |1.15              |
|Treluyer 2002   |0.77          |8.49             |2.40                     |2.50                    |0.96              |
|Treluyer 2002   |2.02          |12.30            |2.24                     |3.02                    |0.74              |
|Treluyer 2002   |4.06          |16.89            |2.10                     |3.17                    |0.66              |
|Treluyer 2002   |6.08          |21.82            |2.02                     |3.27                    |0.62              |
|Treluyer 2002   |7.09          |24.43            |2.00                     |2.95                    |0.68              |
|Belfayol 1996   |7.00          |23.50            |1.98                     |2.40                    |0.83              |

<br>
<br>

## 2.2 Amikacin Concentration-Time profiles in Children<a id="amikacin-ct-profiles"></a>

#### Concentration-Time Profiles

For Amikacin, there were no reported plasma concentration-time data available from literature. Therefore only a comparison of predicted versus observed PK-parameters was made to evaluate the predictive performance of the Amikacin PBPK model in children. [[Section 2.1](#21-amikacin-pk-ratio-tables-and-figures)]

## 2.3 Vancomycin PK Ratio tables and Figures<a id="vancomycin-pk-ratios"></a>

### Vancomycin model

Vancomycin PBPK predictions in children were evaluated using pharmacokinetic (PK) data reported in the following studies: 

- Schaad UB, McCracken GH Jr, Nelson JD. Clinical pharmacology and efficacy of vancomycin in pediatric patients. J Pediatr. 1980 Jan;96(1):119-26.[[Schaad 1980](#3-references)]

The pediatric PBPK model predicted the clearance values of vancomycin observed in pediatric studies reasonably across all available age groups, ranging from 0.085 months to 7.58 years old. The ratios of mean predicted over observed clearance values are illustrated in the table below as well as in the predicted versus observed clearance ratio plot, showing that all predictions in children were within 2-fold error of observed values.

<a id="figure-2-3"></a>

![](images/002_section_pediatric-translation-qualification/005_section_vancomycin-pk-ratios/9_pk_ratio_plot_CL.png)

**Figure 2-3: Overall predictivity of the vancomycin PBPK model. Open circles represent mean ratios of PBPK predicted clearance over observed clearance of vancomycin in children 0.085 months to 7.58 years old. Blue dashed lines and red dotted lines represent the 1.5-fold and 2-fold error, respectively.**

<br>
<br>

<a id="table-2-7"></a>

**Table 2-7: Measure of Overall predictivity of the vancomycin PBPK model. Open circles represent mean ratios of PBPK predicted clearance over observed clearance of vancomycin in children 0.085 months to 7.58 years old. Blue dashed lines and red dotted lines represent the 1.5-fold and 2-fold error, respectively.**

|                       |Number |Ratio [%] |
|:----------------------|:------|:---------|
|Points total           |6      |-        |
|Points within 1.5 fold |3      |50.00     |
|Points within 2 fold   |5      |83.33     |

<br>
<br>

<a id="table-2-8"></a>

**Table 2-8: GMFE for Overall predictivity of the vancomycin PBPK model. Open circles represent mean ratios of PBPK predicted clearance over observed clearance of vancomycin in children 0.085 months to 7.58 years old. Blue dashed lines and red dotted lines represent the 1.5-fold and 2-fold error, respectively.**

|Parameter |GMFE |
|:---------|:----|
|CL        |1.50 |

<br>
<br>

<a id="table-2-9"></a>

**Table 2-9: Overall predictivity of the vancomycin PBPK model. Open circles represent mean ratios of PBPK predicted clearance over observed clearance of vancomycin in children 0.085 months to 7.58 years old. Blue dashed lines and red dotted lines represent the 1.5-fold and 2-fold error, respectively.**

|Study ID    |Age [year(s)] |Body Weight [kg] |Predicted CL [ml/min/kg] |Observed CL [ml/min/kg] |Pred/Obs CL Ratio |
|:-----------|:-------------|:----------------|:------------------------|:-----------------------|:-----------------|
|Schaad 1980 |0.01          |3.07             |1.31                     |1.19                    |1.11              |
|Schaad 1980 |0.26          |4.90             |2.14                     |1.65                    |1.29              |
|Schaad 1980 |0.36          |5.20             |2.27                     |2.70                    |0.84              |
|Schaad 1980 |3.92          |15.50            |1.83                     |3.95                    |0.46              |
|Schaad 1980 |5.58          |20.00            |1.70                     |2.95                    |0.58              |
|Schaad 1980 |7.58          |26.70            |1.56                     |2.78                    |0.56              |

<br>
<br>

## 2.4 Vancomycin Concentration-Time profiles in Children<a id="vancomycin-ct-profiles"></a>

#### Concentration-Time Profiles

Predicted versus observed plasma concentration-time profiles are listed below. Only simulations where observed data was available for comparison are shown.  Depending if the observed data were individual data or aggregated data, individual predictions or population predictions including variability are shown, respectively.

<a id="figure-2-4"></a>

![](images/002_section_pediatric-translation-qualification/006_section_vancomycin-ct-profiles/1_time_profile_plot_Vancomycin_Pediatrics_Schaad_1980_Fig_1c_POP.png)

**Figure 2-4: Time Profile Analysis**

<br>
<br>

<a id="figure-2-5"></a>

![](images/002_section_pediatric-translation-qualification/006_section_vancomycin-ct-profiles/2_time_profile_plot_Vancomycin_Pediatrics_Schaad_1980_Fig_1c_POP.png)

**Figure 2-5: Time Profile Analysis 1**

<br>
<br>

<a id="figure-2-6"></a>

![](images/002_section_pediatric-translation-qualification/006_section_vancomycin-ct-profiles/3_time_profile_plot_Vancomycin_Pediatrics_Schaad_1980_Fig_2a_POP.png)

**Figure 2-6: Time Profile Analysis**

<br>
<br>

<a id="figure-2-7"></a>

![](images/002_section_pediatric-translation-qualification/006_section_vancomycin-ct-profiles/4_time_profile_plot_Vancomycin_Pediatrics_Schaad_1980_Fig_2a_POP.png)

**Figure 2-7: Time Profile Analysis 1**

<br>
<br>

<a id="figure-2-8"></a>

![](images/002_section_pediatric-translation-qualification/006_section_vancomycin-ct-profiles/5_time_profile_plot_Vancomycin_Pediatrics_Schaad_1980_Fig_2b_POP.png)

**Figure 2-8: Time Profile Analysis**

<br>
<br>

<a id="figure-2-9"></a>

![](images/002_section_pediatric-translation-qualification/006_section_vancomycin-ct-profiles/6_time_profile_plot_Vancomycin_Pediatrics_Schaad_1980_Fig_2b_POP.png)

**Figure 2-9: Time Profile Analysis 1**

<br>
<br>

<a id="figure-2-10"></a>

![](images/002_section_pediatric-translation-qualification/006_section_vancomycin-ct-profiles/7_time_profile_plot_Vancomycin_Pediatrics_Schaad_1980_Fig_3a_POP.png)

**Figure 2-10: Time Profile Analysis**

<br>
<br>

<a id="figure-2-11"></a>

![](images/002_section_pediatric-translation-qualification/006_section_vancomycin-ct-profiles/8_time_profile_plot_Vancomycin_Pediatrics_Schaad_1980_Fig_3a_POP.png)

**Figure 2-11: Time Profile Analysis 1**

<br>
<br>

<a id="figure-2-12"></a>

![](images/002_section_pediatric-translation-qualification/006_section_vancomycin-ct-profiles/9_time_profile_plot_Vancomycin_Pediatrics_Schaad_1980_Fig_3b_POP.png)

**Figure 2-12: Time Profile Analysis**

<br>
<br>

<a id="figure-2-13"></a>

![](images/002_section_pediatric-translation-qualification/006_section_vancomycin-ct-profiles/10_time_profile_plot_Vancomycin_Pediatrics_Schaad_1980_Fig_3b_POP.png)

**Figure 2-13: Time Profile Analysis 1**

<br>
<br>

<a id="figure-2-14"></a>

![](images/002_section_pediatric-translation-qualification/006_section_vancomycin-ct-profiles/11_time_profile_plot_Vancomycin_Pediatrics_Schaad_1980_Fig_3c_POP.png)

**Figure 2-14: Time Profile Analysis**

<br>
<br>

<a id="figure-2-15"></a>

![](images/002_section_pediatric-translation-qualification/006_section_vancomycin-ct-profiles/12_time_profile_plot_Vancomycin_Pediatrics_Schaad_1980_Fig_3c_POP.png)

**Figure 2-15: Time Profile Analysis 1**

<br>
<br>

# 3 References<a id="main-references"></a>

**Amikacin-Model** Amikacin-Model, Whole-body PBPK model of Amikacin. ([https://github.com/Open-Systems-Pharmacology/Amikacin-Model](https://github.com/Open-Systems-Pharmacology/Amikacin-Model))

**Belfayol 1996 **Belfayol L, Talon P, Eveillard M, Alet P, Fauvelle F. Pharmacokinetics of once-daily amikacin in pediatric patients. Clin Microbiol Infect. 1996 Feb;2(3):186-191.

**Edginton 2006** Edginton AN, Schmitt W, Willmann S. Development and evaluation of a generic physiologically based pharmacokinetic model for children. Clin Pharmacokinet. 2006;45(10):1013-34.

**Maharaj 2013** Maharaj AR, Barrett JS, Edginton AN. A workflow example of PBPK modeling to support pediatric research and development: case study with lorazepam. The AAPS journal. 2013;15(2): 455-464.

**Ontogeny Database** OSPSuite.Documentation/PK-Sim Ontogeny Database Version 7.3.pdf ([https://github.com/Open-Systems-Pharmacology/OSPSuite.Documentation/blob/38cf71b384cfc25cfa0ce4d2f3addfd32757e13b/PK-Sim%20Ontogeny%20Database%20Version%207.3.pdf](https://github.com/Open-Systems-Pharmacology/OSPSuite.Documentation/blob/38cf71b384cfc25cfa0ce4d2f3addfd32757e13b/PK-Sim%20Ontogeny%20Database%20Version%207.3.pdf))

**Schaad 1980** Schaad UB, McCracken GH Jr, Nelson JD. Clinical pharmacology and efficacy of vancomycin in pediatric patients. J Pediatr. 1980 Jan;96(1):119-26.

**Tréluyer 2002** Tréluyer JM, Merlé Y, Tonnelier S, Rey E, Pons G. Nonparametric population pharmacokinetic analysis of amikacin in neonates, infants, and children. Antimicrob Agents Chemother. 2002 May;46(5):1381-7.

**Vancomycin-Model** Vancomycin-Model, Whole-body PBPK model of Vancomycin. ([https://github.com/Open-Systems-Pharmacology/Vancomycin-Model](https://github.com/Open-Systems-Pharmacology/Vancomycin-Model)) 

**Vogelstein 1977** Vogelstein B, Kowarski A, Lietman PS. The pharmacokinetics of amikacin in children. J Pediatr. 1977 Aug;91(2):333-9.

