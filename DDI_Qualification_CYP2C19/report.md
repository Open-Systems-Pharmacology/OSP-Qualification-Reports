# CYP2C19 DDI Qualification



| Version                         | 1.2-OSP11.1                                                   |
| ------------------------------- | ------------------------------------------------------------ |
| Qualification Plan Release      | https://github.com/Open-Systems-Pharmacology/Qualification-DDI-CYP2C19/releases/tag/v1.2 |
| OSP Version                     | 11.1                                                          |
| Qualification Framework Version | 2.3                                                          |





This qualification report is filed at:

https://github.com/Open-Systems-Pharmacology/OSP-Qualification-Reports
# Table of Contents
  * [1 Introduction](#1-introduction)
    * [1.1 Objective](#11-objective)
    * [1.2 CYP2C19 DDI Network](#12-cyp2c19-ddi-network)
      * [Omeprazole - Moclobemide DDI](#omeprazole---moclobemide-ddi)
      * [Omeprazole - Fluvoxamine DDI](#omeprazole---fluvoxamine-ddi)
      * [S-Mephenytoin - Fluvoxamine DDI](#s-mephenytoin---fluvoxamine-ddi)
      * [Moclobemide - Omeprazole DDI](#moclobemide---omeprazole-ddi)
  * [2 Qualification of Use Case CYP2C19-mediated DDI](#2-qualification-of-use-case-cyp2c19-mediated-ddi)
    * [Perpetrator](#perpetrator)
      * [Fluvoxamine](#fluvoxamine)
      * [Moclobemide](#moclobemide)
      * [Omeprazole](#omeprazole)
    * [Victim](#victim)
      * [Moclobemide](#moclobemide)
      * [Omeprazole](#omeprazole)
      * [S-Mephenytoin](#s-mephenytoin)
  * [3 Concentration-Time Profiles](#3-concentration-time-profiles)
    * [3.1 Omeprazole - Moclobemide DDI](#31-omeprazole---moclobemide-ddi)
    * [3.2 Omeprazole - Fluvoxamine DDI](#32-omeprazole---fluvoxamine-ddi)
    * [3.3 S-Mephenytoin - Fluvoxamine DDI](#33-s-mephenytoin---fluvoxamine-ddi)
    * [3.4 Moclobemide - Omeprazole DD](#34-moclobemide---omeprazole-dd)
  * [4 Conclusion](#4-conclusion)
  * [5 References](#5-references)
  * [6 Appendix](#6-appendix)
    * [6.1 Open Systems Pharmacology Suite (OSPS) Introduction](#61-open-systems-pharmacology-suite-osps-introduction)
    * [6.2 Mathematical Implementation of Drug-Drug Interactions](#62-mathematical-implementation-of-drug-drug-interactions)
    * [6.3 Automatic (re)-qualification workflow](#63-automatic-re-qualification-workflow)
  * [7 Glossary](#7-glossary)
# 1 Introduction
                   

## 1.1 Objective
This qualification report evaluates the developed PBPK drug-drug interactions (DDI) models network for the ability to perform simulations with the intended purpose to predict cytochrome P450 2C19 (**CYP2C19**)-mediated DDI.

To demonstrate the level of confidence, the predictive performance of the platform for this intended purpose is assessed via a network of PBPK models of selected index CYP2C19 DDI perpetrators, and respective sensitive CYP2C19 victim drugs and a comprehensive dataset from published clinical DDI studies. All PBPK models represent whole-body PBPK models, which allow dynamic DDI simulations in organs expressing CYP2C19.

The respective *qualification plan* to produce this *qualification report* is transparently documented and provided open-source (https://github.com/Open-Systems-Pharmacology/OSP-Qualification-Reports). The same applies for all presented PBPK models including *evaluation reports* on model building and evaluation of each model (https://github.com/Open-Systems-Pharmacology/OSP-PBPK-Model-Library).

*Evaluation reports* including descriptions on model building and detailed evaluations of the included models are documented separately (see [Section 1.2](#12-cyp2c19-ddi-network)).

Please refer to the [Appendix](#6-appendix) to learn more details:

- An overview over the Open Systems Pharmacology Suite is given in chapter [Section 6.1](#61-open-systems-pharmacology-suite-osps-introduction)

- [Section 6.2](#62-mathematical-implementation-of-drug-drug-interactions) shows the implementation of the underlying mathematical equations for drug-drug interactions in the OSP suite.

- A detailed general description of the performed qualification workflow (*qualification plan*, *qualification report*, etc.) can be found in chapter [Section 6.3](#63-automatic-re-qualification-workflow).
## 1.2 CYP2C19 DDI Network
CYP2C19 is an important enzyme for the metabolism of about 10% of therapeutical drugs, including proton pump inhibitors (PPIs, e.g., omeprazole), antidepressants (e.g., imipramine), anticonvulsants (phenytoin, S-mephenytoin), hypnotics and sedatives (e.g., phenobarbital), antimalarial (proguanil), antiretroviral (nelfinavir), antifungal (voriconazole), and antiplatelet drugs (clopidogrel) ([Goldstein 2001](#5-references),  [Desta 2002](#5-references)). Genetic polymorphism exists for CYP2C19 expression, with approximately 3%–5% of European and 15%–20% of Asian populations being poor metabolizers with no CYP2C19 activity  ([Goldstein 2001](#5-references),  [Bertilsson 1995](#5-references)). Based on the metabolic capacity of CYP2C19, individuals can be divided into four categories: extensive metabolizers (EMs) carrying normal alleles, intermediate metabolizers (IMs) carrying one defective allele, poor metabolizers (PMs) carrying two defective alleles, and ultra-rapid metabolizers (UMs) homozygous for alleles which increase the CYP2C19 expression or activity higher than in EMs. Well-known substrates of CYP2C19 are mephenytoin, omeprazole, and moclobemide.

Like other CYPs, CYP2C19 is subject to induction and/or inhibition by a number of compounds, which can result in significant drug interactions in clinical practice.

The U.S. Food and Drug Administration (FDA) lists several perpetrator and victim drugs of interactions in the CYP2C19 network ([Goldstein 2001](#5-references)). For instance, omeprazole is a sensitive index substrate for CYP2C19, and fluvoxamine is listed as a strong clinical index inhibitor for CYP2C19 pathway.

To qualify the developed models for the prediction of the CYP2C19 DDI potential of new drugs, a set of verified PBPK models of index perpetrators and respective CYP2C19 DDI victim drugs is specified to set up a CYP2C19-mediated DDI modeling network.

The following perpetrator compounds were selected: 

- **Fluvoxamine** (strong CYP2C19 inhibitor)
  Model snapshot and evaluation plan (*release* **alt_v1.0**): https://github.com/Open-Systems-Pharmacology/Fluvoxamine-Model/releases/tag/alt_v1.0
- **Omeprazole** (moderate CYP2C19 inhibitor)
  Model snapshot and evaluation plan (*release* **v1.1**): https://github.com/Open-Systems-Pharmacology/Omeprazole-Model/releases/tag/v1.1
- **Moclobemide** (moderate CYP2C19 inhibitor)
  Model snapshot and evaluation plan (*release* **v1.1**): https://github.com/Open-Systems-Pharmacology/Moclobemide-Model/releases/tag/v1.1


The following sensitive CYP2C19 substrates as victim drugs were selected:

- **Omeprazole**
  Model snapshot and evaluation plan (*release* **v1.1**): https://github.com/Open-Systems-Pharmacology/Omeprazole-Model/releases/tag/v1.1
- **S-Mephenytoin**
  Model snapshot and evaluation plan (*release* **v1.1**): https://github.com/Open-Systems-Pharmacology/S-Mephenytoin-Model/releases/tag/v1.1
- **Moclobemide**
  Model snapshot and evaluation plan (*release* **v1.1**): https://github.com/Open-Systems-Pharmacology/Moclobemide-Model/releases/tag/v1.1

The following interaction studies were predicted and used to qualify/optimize the final network:

- Strong CYP2C19 inhibition

  - Fluvoxamine - omeprazole
  - Fluvoxamine - S-Mephenytoin
- Moderate CYP2C19 inhibition
  - Omeprazole – moclobemide
  - Moclobemide - omeprazole

**Figure 1** shows the specified and developed DDI modeling network of interacting perpetrator and victim drugs.

**Figure** **1: CYP2C19 DDI modeling network**
![DDI CYP2C19 network](images/DDI_CYP2C19_Compound_Network.png)

The Ki values used to predict the interactions are listed in [Table 1](#table-1).

| **Inhibitor category** | **Inhibitor** | **Substrate**  | **Ki**                                                       | **Reference**                                                |
| ---------------------- | ------------- | -------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| Strong CYP2C19         | Fluvoxamine   | Omeprazole     | 3.6 nM                                                       | [Iga 2016](#5-references)                                    |
|                        |               | S-Mephenytoin | 2.6 nM                                                       | [Iga 2016](#5-references)                                    |
| Moderate CYP2C19       | Moclobemide   | Omeprazole     | 203.83 µM<sup>1</sup><br />TDI 94.85 µM                      | Fit                                                          |
|                        | Omeprazole    | Moclobemide    | S-ome: 3.1 µM<br />TDI 0.3 µM<br />R-ome: 5.3 µM<br />TDI 1.6 µM | [Liu 2005](#5-references)<br />[Wu 2014](#5-references)<br />[Liu 2005](#5-references)<br />[Wu 2014](#5-references) |

**Table 1:**<a name="table-1"></a> Ki values used in CYP2C19 DDI network. <sup>1</sup>Literature value = 204 µM

The published DDI studies between the respective perpetrators and victim drugs were simulated and compared to observed data. The following sections give an overview of the clinical studies being part of this qualification report.
### Omeprazole - Moclobemide DDI
The omeprazole-moclobemide interaction was evaluated using clinical DDI studies listed in [Table 2](#table-2).

| **Source**                | **Route** | **Dose [mg] /** **Schedule \*** | **Pop.** | **Sex** | **N** | **Form.** | **Comment**       |
| ------------------------- | --------- | ------------------------------- | -------- | ------- | ----- | --------- | ----------------- |
| [Cho 2002](#5-references) | p.o       | 20                              | HV asian | -       | -     | capsule   | EM +/-moclobemide |
| [Cho 2002](#5-references) | p.o       | 20                              | HV asian | -       | -     | capsule   | PM +/-moclobemide |

**Table 2:**<a name="table-2"></a> Literature sources of clinical concentration data of omeprazole used for DDI prediction qualification with moclobemide. *-: respective information was not provided in the literature source; \*:single dose unless otherwise specified; EM: extensive metabolizers; PM: poor metabolizers*

A dynamical DDI simulation with moclobemide and omeprazole was conducted and compared to literature data. Both compounds act as CYP2C19 inhibitors and victims. The predefined typical Japanese subject (age = 30 y, weight = 61.87 kg, height = 168.99 cm, BMI = 21.67 kg/m2) was used with CYP3A4, CYP2C19, CYP2D6 and CYP1A2 expressions from RT PCR database in PK-Sim and adapted CYP2C19 expression in gut (see evaluation report of omeprazole for more details). Additional enzyme "FMO (other)" was added and expressed in liver only.

In [Cho 2002](#5-references), sixteen volunteers, of whom eight were extensive metabolizers (EM) and eight were poor metabolizers (PM) for CYP2C19, received oral doses of 40 mg omeprazole with or without 300 mg moclobemide co-administration. 

The pharmacokinetic change of omeprazole, omeprazole sulphone and 5-hydroxyomeprazole concentrations were assessed to test for an interaction between omeprazole and moclobemide.
### Omeprazole - Fluvoxamine DDI
The omeprazole-fluvoxamine interaction was evaluated using clinical DDI studies listed in [Table 3](#table-3).

| **Source**                           | **Route** | **Dose [mg] /** **Schedule \*** | **Pop.**    | **Sex** | **N** | **Form.** | **Comment**          |
| ------------------------------------ | --------- | ------------------------------- | ----------- | ------- | ----- | --------- | -------------------- |
| [Yasui-Furukori 2004](#5-references) | p.o.      | 40                              | HV japanese | M - F   | 6     | omepral   | hmEM +/- fluvoxamine |
| [Yasui-Furukori 2004](#5-references) | p.o.      | 40                              | HV japanese | M - F   | 6     | omepral   | PM +/- fluvoxamine   |

**Table 3:**<a name="table-3"></a> Literature sources of clinical concentration data of omeprazole used for DDI prediction qualification with fluvoxamine. *\*:single dose unless otherwise specified; hmEM: homozygous extensive metabolizers; PM: poor metabolizers*

A dynamical DDI simulation with fluvoxamine as CYP2C19 inhibitor and omeprazole as victim was conducted and compared to literature data. The predefined typical Japanese subject (age = 30 y, weight = 61.87 kg, height = 168.99 cm, BMI = 21.67 kg/m2) was used with CYP3A4, CYP2C19, CYP2D6 and CYP1A2 expression from RT PCR database in PK-Sim and adapted CYP2C19 expression in gut (see evaluation report of omeprazole for more details). Additional enzyme "FMO (other)" was added and expressed in liver only. The Ki value of 3.6 nmol/l for the inhibition of CYP2C19 by fluvoxamine was selected in agreement with literature data ([Iga 2016](#5-references)).

In [Yasui-Furukori 2004](#5-references), eighteen volunteers, of whom six were homozygous extensive metabolizers (hmEMs), six were heterozygous EMs (htEMs) and six were poor metabolizers (PMs) for CYP2C19, received two six-day courses of either daily 50 mg fluvoxamine (split in 25 mg twice daily) or placebo in a randomized fashion with a single oral 40 mg dose of omeprazole on day six in both cases. Plasma concentrations of omeprazole and its metabolites, 5-hydroxyomeprazole, omeprazole sulphone, and fluvoxamine were monitored up to 8 h after the dosing.

### S-Mephenytoin - Fluvoxamine DDI
The S-mephenytoin-fluvoxamine interaction was evaluated using clinical DDI studies listed in [Table 4](#table-4).

| **Source**                | **Route** | **Dose [mg]/**  **Schedule \*** | **Pop.** | **Sex** | **N** | **Form.** | **Comment**                                                  |
| ------------------------- | --------- | ------------------------------- | -------- | ------- | ----- | --------- | ------------------------------------------------------------ |
| [Yao 2003](#5-references) | p.o.      | 100 mg s.d.                     | HV       | m/f     | 12    | -         | S-mephenytoin, with  and without Fluvoxamine MD of 37.5, 62.5 and 87.5 mg/day |

**Table 4:**<a name="table-4"></a> Literature sources of clinical concentration data of S-mephenytoin used for DDI prediction qualification with fluvoxamine. *-: respective information was not provided in the literature source; \*:single dose unless otherwise specified*

A dynamical DDI simulation with fluvoxamine was used to predict the effect of a strong CYP2C19 inhibitor on S-mephenytoin exposure. The predefined “Standard European Male for DDI” individual (age = 30 y, weight = 73 kg, height = 176 cm, BMI = 23.57 kg/m2) with adapted CYP2C19 expression in gut (see evaluation report of omeprazole for more details) was used. Ki value of 2.6 nmol/l for the inhibition of CYP2C19 was selected.

Predictions were compared to clinical results from [Yao 2003](#5-references), where the effect of different fluvoxamine doses in S-Mephenytoin was investigated. 100 mg S-mephenytoin were administered after 7 days of placebo or fluvoxamine treatment (27.5, 45.8, or 64.1 mg).
### Moclobemide - Omeprazole DDI
The moclobemide-omeprazole interaction was evaluated using clinical DDI studies listed in [Table 5](#table-5).

| **Source**               | **Route** | **Dose [mg]/**  **Schedule \*** | **Pop.** | **Sex** | **N** | **Form.** | **Comment**       |
| ------------------------ | --------- | ------------------------------- | -------- | ------- | ----- | --------- | ----------------- |
| [Yu 2001](#5-references) | p.o       | 300 s.d.                        | HV-Asian | m       | 8     | tablet    | EM +/- omeprazole |

**Table 5:**<a name="table-5"></a> Literature sources of clinical concentration data of moclobemide used for DDI prediction qualification omeprazole. *\*:single dose unless otherwise specified; EM: extensive metabolizers*

A dynamical DDI simulation with moclobemide and omeprazole was conducted and compared to literature data. Both compounds act as CYP2C19 inhibitors and victims. 300 mg moclobemide with or without a single dose of 40 mg omeprazole (racemate, i.e. 20 mg S-omeprazole and 20 mg R-omeprazole) was simulated. The predefined typical Japanese subject (age = 30 y, weight = 61.87 kg, height = 168.99 cm, BMI = 21.67 kg/m2) was used with CYP3A4, CYP2C19, CYP2D6 and CYP1A2 expressions from RT PCR database in PK-Sim and adapted CYP2C19 expression in gut (see evaluation report of omeprazole for more details). Additional enzyme "FMO (other)" was added and expressed in liver only.
# 2 Qualification of Use Case CYP2C19-mediated DDI
The following section shows the correlations between observed and model-predicted AUC and C<sub>max</sub> ratios, respectively.

Specifically, the PBPK model performance for the PK parameters **AUC ratio (AUCR)** and **C<sub>max</sub> ratio (CMAXR)** is assessed via:

- predicted (*Pred*) vs. observed (*Obs*) plots

- *Pred*/*Obs* vs. *Obs* plots

- geometric mean fold error (GMFE):
  
  ![GMFE equation](images/GFME_equation.PNG)
  
- number of AUCR and CMAXR falling within 2-fold error range and within the limits as suggested by [Guest et al. 2011](#5-references)
  
- detailed table of results for each study


In the plots,

- the dotted lines denote 0.50–2.00 (2-fold) criterion,

- the solid lines denote the limits as suggested by [Guest et al. 2011](#5-references),

- the bold solid line denotes the unity line,

- each color represents one combination of drugs


***


![001_plotDDIRatioAUCPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP2C19-mediated_DDI/001_plotDDIRatioAUCPredictedVsObserved.png)

![002_plotDDIRatioAUCResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP2C19-mediated_DDI/002_plotDDIRatioAUCResidualsVsObserved.png)

![003_plotDDIRatioCMAXPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP2C19-mediated_DDI/003_plotDDIRatioCMAXPredictedVsObserved.png)

![004_plotDDIRatioCMAXResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP2C19-mediated_DDI/004_plotDDIRatioCMAXResidualsVsObserved.png)

GMFE (AUC) = 1.252722 

GMFE (CMAX) = 1.173692 

|AUC                       |Number|Ratio [%]|
|-------------------------:|-----:|--------:|
|Points total              |8     |-        |
|Points within Guest et al.|5     |62.5     |
|Points within 2-fold      |7     |87.5     |

|CMAX                      |Number|Ratio [%]|
|-------------------------:|-----:|--------:|
|Points total              |8     |-        |
|Points within Guest et al.|4     |50       |
|Points within 2-fold      |8     |100      |

|DataID|Perpetrator               |Victim           |Predicted AUC Ratio|Observed AUC Ratio|Pred/Obs AUC Ratio|Predicted CMAX Ratio|Observed CMAX Ratio|Pred/Obs CMAX Ratio|Reference          |
|-----:|-------------------------:|----------------:|------------------:|-----------------:|-----------------:|-------------------:|------------------:|------------------:|------------------:|
|11050 |Fluvoxamine, 50 mg, PO,   |Omeprazole, PO   |2.5885             |5.34              |0.48473           |1.9815              |3.48               |0.56938            |Yasui-Furukori 2004|
|11052 |Fluvoxamine, 50 mg, PO,   |Omeprazole, PO   |0.99972            |1.21              |0.82621           |1.0009              |1.12               |0.89367            |Yasui-Furukori 2004|
|11048 |Moclobemide, 300 mg, PO,  |Omeprazole, PO   |1.5319             |2.05              |0.74726           |1.252               |1.67               |0.74972            |Cho 2002           |
|11049 |Moclobemide, 300 mg, PO,  |Omeprazole, PO   |1                  |1.16              |0.86207           |1.0003              |0.97               |1.0312             |Cho 2002           |
|15001 |Fluvoxamine, 27.5 mg, PO, |S-Mephenytoin, PO|3.8498             |4.64              |0.82969           |2.1352              |2.12               |1.0071             |Yao 2003           |
|15002 |Fluvoxamine, 45.8 mg, PO, |S-Mephenytoin, PO|6.336              |6.7               |0.94567           |2.492               |2.4                |1.0383             |Yao 2003           |
|15003 |Fluvoxamine, 64.1 mg, PO, |S-Mephenytoin, PO|8.076              |9.89              |0.81658           |2.6329              |2.42               |1.088              |Yao 2003           |
|10027 |Omeprazole, 40 mg, PO,    |Moclobemide , PO |1.3133             |1.31              |1.0025            |0.94799             |1.11               |0.85404            |Yu 2001            |

## Perpetrator

### Fluvoxamine

![001_plotDDIRatioAUCPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP2C19-mediated_DDI/001_Perpetrator/001_Fluvoxamine/001_plotDDIRatioAUCPredictedVsObserved.png)

![002_plotDDIRatioAUCResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP2C19-mediated_DDI/001_Perpetrator/001_Fluvoxamine/002_plotDDIRatioAUCResidualsVsObserved.png)

![003_plotDDIRatioCMAXPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP2C19-mediated_DDI/001_Perpetrator/001_Fluvoxamine/003_plotDDIRatioCMAXPredictedVsObserved.png)

![004_plotDDIRatioCMAXResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP2C19-mediated_DDI/001_Perpetrator/001_Fluvoxamine/004_plotDDIRatioCMAXResidualsVsObserved.png)

GMFE (AUC) = 1.312656 

GMFE (CMAX) = 1.174613 

|AUC                       |Number|Ratio [%]|
|-------------------------:|-----:|--------:|
|Points total              |5     |-        |
|Points within Guest et al.|3     |60       |
|Points within 2-fold      |4     |80       |

|CMAX                      |Number|Ratio [%]|
|-------------------------:|-----:|--------:|
|Points total              |5     |-        |
|Points within Guest et al.|3     |60       |
|Points within 2-fold      |5     |100      |

### Moclobemide

![001_plotDDIRatioAUCPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP2C19-mediated_DDI/001_Perpetrator/002_Moclobemide/001_plotDDIRatioAUCPredictedVsObserved.png)

![002_plotDDIRatioAUCResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP2C19-mediated_DDI/001_Perpetrator/002_Moclobemide/002_plotDDIRatioAUCResidualsVsObserved.png)

![003_plotDDIRatioCMAXPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP2C19-mediated_DDI/001_Perpetrator/002_Moclobemide/003_plotDDIRatioCMAXPredictedVsObserved.png)

![004_plotDDIRatioCMAXResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP2C19-mediated_DDI/001_Perpetrator/002_Moclobemide/004_plotDDIRatioCMAXResidualsVsObserved.png)

GMFE (AUC) = 1.245930 

GMFE (CMAX) = 1.172789 

|AUC                       |Number|Ratio [%]|
|-------------------------:|-----:|--------:|
|Points total              |2     |-        |
|Points within Guest et al.|1     |50       |
|Points within 2-fold      |2     |100      |

|CMAX                      |Number|Ratio [%]|
|-------------------------:|-----:|--------:|
|Points total              |2     |-        |
|Points within Guest et al.|1     |50       |
|Points within 2-fold      |2     |100      |

### Omeprazole

![001_plotDDIRatioAUCPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP2C19-mediated_DDI/001_Perpetrator/003_Omeprazole/001_plotDDIRatioAUCPredictedVsObserved.png)

![002_plotDDIRatioAUCResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP2C19-mediated_DDI/001_Perpetrator/003_Omeprazole/002_plotDDIRatioAUCResidualsVsObserved.png)

![003_plotDDIRatioCMAXPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP2C19-mediated_DDI/001_Perpetrator/003_Omeprazole/003_plotDDIRatioCMAXPredictedVsObserved.png)

![004_plotDDIRatioCMAXResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP2C19-mediated_DDI/001_Perpetrator/003_Omeprazole/004_plotDDIRatioCMAXResidualsVsObserved.png)

GMFE (AUC) = 1.002530 

GMFE (CMAX) = 1.170904 

|AUC                       |Number|Ratio [%]|
|-------------------------:|-----:|--------:|
|Points total              |1     |-        |
|Points within Guest et al.|1     |100      |
|Points within 2-fold      |1     |100      |

|CMAX                      |Number|Ratio [%]|
|-------------------------:|-----:|--------:|
|Points total              |1     |-        |
|Points within Guest et al.|0     |0        |
|Points within 2-fold      |1     |100      |

## Victim

### Moclobemide

![001_plotDDIRatioAUCPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP2C19-mediated_DDI/002_Victim/001_Moclobemide/001_plotDDIRatioAUCPredictedVsObserved.png)

![002_plotDDIRatioAUCResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP2C19-mediated_DDI/002_Victim/001_Moclobemide/002_plotDDIRatioAUCResidualsVsObserved.png)

![003_plotDDIRatioCMAXPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP2C19-mediated_DDI/002_Victim/001_Moclobemide/003_plotDDIRatioCMAXPredictedVsObserved.png)

![004_plotDDIRatioCMAXResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP2C19-mediated_DDI/002_Victim/001_Moclobemide/004_plotDDIRatioCMAXResidualsVsObserved.png)

GMFE (AUC) = 1.002530 

GMFE (CMAX) = 1.170904 

|AUC                       |Number|Ratio [%]|
|-------------------------:|-----:|--------:|
|Points total              |1     |-        |
|Points within Guest et al.|1     |100      |
|Points within 2-fold      |1     |100      |

|CMAX                      |Number|Ratio [%]|
|-------------------------:|-----:|--------:|
|Points total              |1     |-        |
|Points within Guest et al.|0     |0        |
|Points within 2-fold      |1     |100      |

### Omeprazole

![001_plotDDIRatioAUCPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP2C19-mediated_DDI/002_Victim/002_Omeprazole/001_plotDDIRatioAUCPredictedVsObserved.png)

![002_plotDDIRatioAUCResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP2C19-mediated_DDI/002_Victim/002_Omeprazole/002_plotDDIRatioAUCResidualsVsObserved.png)

![003_plotDDIRatioCMAXPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP2C19-mediated_DDI/002_Victim/002_Omeprazole/003_plotDDIRatioCMAXPredictedVsObserved.png)

![004_plotDDIRatioCMAXResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP2C19-mediated_DDI/002_Victim/002_Omeprazole/004_plotDDIRatioCMAXResidualsVsObserved.png)

GMFE (AUC) = 1.403132 

GMFE (CMAX) = 1.282224 

|AUC                       |Number|Ratio [%]|
|-------------------------:|-----:|--------:|
|Points total              |4     |-        |
|Points within Guest et al.|1     |25       |
|Points within 2-fold      |3     |75       |

|CMAX                      |Number|Ratio [%]|
|-------------------------:|-----:|--------:|
|Points total              |4     |-        |
|Points within Guest et al.|1     |25       |
|Points within 2-fold      |4     |100      |

### S-Mephenytoin

![001_plotDDIRatioAUCPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP2C19-mediated_DDI/002_Victim/003_S_Mephenytoin/001_plotDDIRatioAUCPredictedVsObserved.png)

![002_plotDDIRatioAUCResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP2C19-mediated_DDI/002_Victim/003_S_Mephenytoin/002_plotDDIRatioAUCResidualsVsObserved.png)

![003_plotDDIRatioCMAXPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP2C19-mediated_DDI/002_Victim/003_S_Mephenytoin/003_plotDDIRatioCMAXPredictedVsObserved.png)

![004_plotDDIRatioCMAXResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP2C19-mediated_DDI/002_Victim/003_S_Mephenytoin/004_plotDDIRatioCMAXResidualsVsObserved.png)

GMFE (AUC) = 1.159976 

GMFE (CMAX) = 1.043965 

|AUC                       |Number|Ratio [%]|
|-------------------------:|-----:|--------:|
|Points total              |3     |-        |
|Points within Guest et al.|3     |100      |
|Points within 2-fold      |3     |100      |

|CMAX                      |Number|Ratio [%]|
|-------------------------:|-----:|--------:|
|Points total              |3     |-        |
|Points within Guest et al.|3     |100      |
|Points within 2-fold      |3     |100      |

# 3 Concentration-Time Profiles
The following section shows concentration time profiles of the victim drugs of the simulated DDI studies in comparison to observed data.




## 3.1 Omeprazole - Moclobemide DDI
                   

![001_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/001_3_1_Omeprazole_-_Moclobemide_DDI/001_plotComparisonTimeProfile.png)

![002_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/001_3_1_Omeprazole_-_Moclobemide_DDI/002_plotComparisonTimeProfile.png)

## 3.2 Omeprazole - Fluvoxamine DDI
                   

![001_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/002_3_2_Omeprazole_-_Fluvoxamine_DDI/001_plotComparisonTimeProfile.png)

![002_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/002_3_2_Omeprazole_-_Fluvoxamine_DDI/002_plotComparisonTimeProfile.png)

## 3.3 S-Mephenytoin - Fluvoxamine DDI
                   

![001_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/003_3_3_S-Mephenytoin_-_Fluvoxamine_DDI/001_plotComparisonTimeProfile.png)

## 3.4 Moclobemide - Omeprazole DD
                   

![001_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/004_3_4_Moclobemide_-_Omeprazole_DD/001_plotComparisonTimeProfile.png)

# 4 Conclusion
The predicted perpetrator/victim drug concentration-time profiles, DDI AUC and Cmax ratios confirmed that the developed PBPK models are well suited to characterize the CYP2C19 DDI network over the full range of reported DDI studies. Identical Ki values could be used for the moderate CYP2C19 inhibitors and substrates moclobemide (204 μM) and omeprazole (R: 5.3 μM / S: 3.1 μM) in their dynamic DDI interactions. For the strong inhibition of CYP2C19 by fluvoxamine, substrate dependent Ki values were used: 3100 nM and 2.6 nM for Omeprazole and S-mephenytoin, respectively.

**Fluvoxamine** 

- CYP2C19 inhibition:
  - DDI simulations with omeprazole as substrate demonstrate an excellent prediction (ratio pred/obs = around 1) of the inhibitory potential of fluvoxamine on CYP2C19 for both EM and PM for CYP2C19.
  - DDI simulations with s-Mephenytoin as substrate demonstrate an excellent prediction (ratio pred/obs = around 1 and within 2-fold) of the inhibitory potential of fluvoxamine on CYP2C19. However, DDI predictions tend to get slightly overpredicted for higher fluvoxamine doses. 

**Omeprazole**

- Perpetrator:

  - DDI simulations with omeprazole as inhibitor of CYP2C19 demonstrated a good prediction of moclobemide levels (within 2-fold).

- Substrate:

  - DDI simulations with fluvoxamine as inhibitor of omeprazole demonstrated an excellent prediction of omeprazole levels on CYP2C19 for both PM and EM (ratio pred/obs = around 1 and within 2-fold).  Despite some model underprediction in both treatment and control groups, the predicted AUC and Cmax ratios well match the observed ones.
  - DDI simulations with moclobemide as inhibitor of omeprazole demonstrated good prediction of omeprazole levels on CYP2C19. The levels for EM were slightly underpredicted (pred/obs CmaxR = 0.77). Predictions for PM were excellent.

**S-Mephenytoin**

+ Substrate: DDI simulations with S-mephenytoin as a substrate demonstrate an excellent prediction (ratio pred/obs = around 1 and within 2-fold) of the inhibitory potential of fluvoxamine on CYP2C19. However, DDI predictions tend to get slightly overpredicted for Cmax with higher fluvoxamine doses. 

**Moclobemide** 

- Perpetrator: DDI simulations with moclobemide as inhibitor of omeprazole demonstrated good prediction of omeprazole levels for different CYP2C19 phenotypes. The levels for EM were slightly underpredicted. Predictions for PM were excellent.
- Substrate: DDI simulations with omeprazole as inhibitor of moclobemide demonstrated a good prediction of moclobemide levels.
# 5 References
**Bertilsson 1995** Bertilsson, L. (1995). Geographical / Interracial Differences/interracial differences in Current State of Knowledge of Cytochromes P450 ( CYP ). *Clin Pharmacokinet Concepts*. 1995;polymorphic drug oxidation. Clinical pharmacokinetics, 29(3):), 192-209. 

**Cho 2002** Cho JY, Yu KS, Jang IJ, Yang BH, Shin SG, Yim DS. Omeprazole hydroxylation is inhibited by a single dose of moclobemide in homozygotic em genotype for CYP2C19. *Br J Clin Pharmacol*. 2002;53(4):393-397.

**Desta 2002** Desta Z, Zhao X, Shin JG, Flockhart DA. Clinical significance of the cytochrome P450 2C19 genetic polymorphism. Clin Pharmacokinet. 2002;41(12):913-58. doi: 10.2165/00003088-200241120-00002. PMID: 12222994.

**FDA** U.S. Food and Drug Administration. Drug development and drug interactions: table of substrates, inhibitors and inducers. Website: https://www.fda.gov/drugs/drug-interactions-labeling/drug-development-and-drug-interactions-table-substrates-inhibitors-and-inducers (2020). Accessed 06 May 2022.

**Goldstein 2001** Goldstein JA. (2001). Clinical relevance of genetic polymorphisms in the human CYP2C subfamily. *Br J Clin Pharmacol*. 2001;British journal of clinical pharmacology, 52(4):), 349-355.

**Guest 2011** Guest EJ, Aarons L, Houston JB, Rostami-Hodjegan A, Galetin A. Critique of the two-fold measure of prediction success for ratios: application for the assessment of drug-drug interactions. Drug Metab Dispos. 2011 Feb;39(2):170-3.

**Iga 2016** Iga K. Dynamic and Static Simulations of Fluvoxamine-Perpetrated Drug-Drug Interactions Using Multiple Cytochrome P450 Inhibition Modeling, and Determination of Perpetrator-Specific CYP Isoform Inhibition Constants and Fractional CYP Isoform Contributions to Vic. *J Pharm Sci*.Victim Clearance. Journal of Pharmaceutical Sciences. 2016 Mar;105(3):1307-1317–17.

**Liu 2005** Liu KH, Kim MJ, Shon JH, et al. Stereoselective inhibition of cytochrome P450 forms by lansoprazole and omeprazole in vitro. *Xenobiotica*. 2005;35(1):27-38

**Wu 2014** Wu F, Gaohua L, Zhao P, Jamei M, Huang S-M, Bashaw ED, et al. Predicting Nonlinear Pharmacokinetics of Omeprazole Enantiomers and Racemic Drug Using Physiologically Based Pharmacokinetic Modeling and Simulation: Application to Predict Drug/Genetic Interactions. *Pharmaceutical Research*. 2014 Aug;31(8):1919–29.

**Yao 2003**  Yao C, Kunze KL, Trager WF, Kharasch ED, Levy RH. Comparison of in vitro and in vivo inhibition potencies of fluvoxamine toward CYP2C19. *Drug Metab Dispos*. 2003;31(5):565-571.

**Yasui-Furukori 2004** Yasui-Furukori N, Takahata T, Nakagami T, et al. Different inhibitory effect of fluvoxamine on omeprazole metabolism between CYP2C19 genotypes. *Br J Clin Pharmacol*. 2004;57(4):487-494.

**Yu 2001** Yu K, Yim DS, Cho J-Y, Park SS. Effect of omeprazole on the pharmacokinetics of moclobemide according to the genetic polymorphism of CYP2C19. Clinical Pharmacology & Therapeutics. 2001 Apr;69(4):266–73.
# 6 Appendix
                   

## 6.1 Open Systems Pharmacology Suite (OSPS) Introduction
Open Systems Pharmacology Suite (OSP suite) is a tool for PBPK modeling and simulation of drugs in laboratory animals and humans. PK-Sim® and MoBi® are part of the OSP suite [[1](#references-for-osps-introduction)].  PK-Sim® is based on a generic PBPK-model with 18 organs and tissues. One of the main assumptions is that all compartments are well-stirred. Represented organs/tissues include arterial and venous blood, adipose tissue (separable adipose, excluding yellow marrow), brain, lung, bone (including yellow marrow), gonads, heart, kidneys, large intestine, liver, muscle, portal vein, pancreas, skin, small intestine, spleen and stomach, as shown in **Figure 1**.

Each organ consists of four sub-compartments namely the plasma, blood cells (which together build the vascular space), interstitial space, and cellular space. Distribution between the plasma and blood cells as well as between the interstitial and cellular compartments can be permeability-limited. In the brain, the permeation barrier is located between the vascular and the interstitial space. PK-Sim® estimates model parameters (intestinal permeability [[2](#references-for-osps-introduction)] organ partition coefficients (tissue-to-plasma partition coefficients) [[3,4](#references-for-osps-introduction)], and permeabilities) from physico-chemical properties of compounds (molecular weight, pKa, acid/base properties) and the composition of each tissue compartment (lipids, water and proteins). Partition coefficients can be calculated using a variety of methods available in PK-Sim®, for example the internal PK-Sim® method [[3,4](#references-for-osps-introduction)] or that of Rodgers and Rowland [[5-7](#references-for-osps-introduction)]. 

Physiological databases included in the software incorporate the dependencies of organ composition, organ weights, organ blood flows and gastrointestinal parameters (gastrointestinal length, radius of each section, intestinal surface area, gastrointestinal transit times, and pH in different intestinal segments [[2](#references-for-osps-introduction)]), with the user-defined body weight and height and ethnicity of the individual [[8](#references-for-osps-introduction)]. Thereby, PK Sim® allows generating realistic virtual populations. For a detailed description of the PBPK model structure implemented in PK Sim®, see Willmann et al. [[2,4,8,9](#references-for-osps-introduction)] or the OSP Suite homepage (<https://docs.open-systems-pharmacology.org/mechanistic-modeling-of-pharmacokinetics-and-dynamics/modeling-concepts>).


**Figure** **1: Structure of the Whole Body PBPK Model integrated in PK-Sim®**

![generic PBPK model](images/PK-Sim_PBPK_generic_model_scheme.png)




## References for OSPS introduction

[1] [www.open-systems-pharmacology.org](http://www.open-systems-pharmacology.org/)

[2] [Willmann S, Schmitt W, Keldenich J, Lippert J, Dressman JB. A physiological model for the estimation of the fraction dose absorbed in humans.J Med Chem. 2004 Jul 29;47(16):4022-31.](https://www.ncbi.nlm.nih.gov/pubmed/15267240)

[3] [Haerter MW, K.J., Schmitt W, *Estimation of physicochemical and ADME parameters.* , in *Handbook of Combinatorial Chemistry: Drugs, Catalysts, Materials*, H.W. Nicolaou KC HR, Editor. 2002, Wiley VCH Verlag GmbH: Weinheim, Germany. p. 743-60.](https://onlinelibrary.wiley.com/doi/pdf/10.1002/3527603034.ch26)

[4] [Willmann S, Lippert J, Schmitt W. From physicochemistry to absorption and distribution: predictive mechanistic modelling and computational tools. Expert Opin Drug Metab Toxicol. 2005 Jun;1(1):159-68.](https://www.ncbi.nlm.nih.gov/pubmed/16922658)

[5] [Rodgers, T, D. Leahy, and M. Rowland. Physiologically based pharmacokinetic modeling 1: predicting the tissue distribution of moderate-to-strong bases. J Pharm Sci. 2005 Jun;94(6):1259-76.](https://www.ncbi.nlm.nih.gov/pubmed/15858854)

[6] [Rodgers T, Rowland M. Physiologically based pharmacokinetic modelling 2: predicting the tissue distribution of acids, very weak bases, neutrals and zwitterions. J Pharm Sci. 2006 Jun;95(6):1238-57.](https://www.ncbi.nlm.nih.gov/pubmed/16639716)

[7] [Rodgers T, Rowland M. Mechanistic approaches to volume of distribution predictions: understanding the processes. Pharm Res. 2007 May;24(5):918-33.](https://www.ncbi.nlm.nih.gov/pubmed/17372687)

[8] [Willmann S, Höhn K, Edginton A, Sevestre M, Solodenko J, Weiss W, Lippert J, Schmitt W. Development of a physiology-based whole-body population model for assessing the influence of individual variability on the pharmacokinetics of drugs. J Pharmacokinet Pharmacodyn. 2007 Jun;34(3):401-31.](https://www.ncbi.nlm.nih.gov/pubmed/17431751)

[9] [Willmann S, Lippert J, Sevestre M, Solodenko J, Fois F, Schmitt W. PK-Sim®: a physiologically based pharmacokinetic ‘whole-body’ model. Biosilico 2003.1(4):121-24.](https://www.sciencedirect.com/science/article/pii/S1478538203023424?via%3Dihub)


## 6.2 Mathematical Implementation of Drug-Drug Interactions


**DDI modeling: Competitive inhibition** 

A detailed representation of the mathematical implementation of competitive enzyme inhibition  can be found in the OSP manual [here](https://docs.open-systems-pharmacology.org/working-with-pk-sim/pk-sim-documentation/pk-sim-compounds-defining-inhibition-induction-processes#competitive-inhibition-simple-setting-with-one-inhibitor).



**DDI modeling: Mechanism-based inhibition**

A detailed representation of the mathematical implementation of mechanism-based enzyme inhibition  can be found in the OSP manual [here](https://docs.open-systems-pharmacology.org/working-with-pk-sim/pk-sim-documentation/pk-sim-compounds-defining-inhibition-induction-processes#irreversible-inhibition).



**DDI modeling: Induction**

A detailed representation of the mathematical implementation of enzyme induction can be found in the OSP manual [here](https://docs.open-systems-pharmacology.org/working-with-pk-sim/pk-sim-documentation/pk-sim-compounds-defining-inhibition-induction-processes#enzyme-induction).


## 6.3 Automatic (re)-qualification workflow
[Open Systems Pharmacology](http://www.open-systems-pharmacology.org) provides a dynamic landscape of model repositories and a database of observed clinical data. Additionally, a technical framework to assess confidence of a specific intended use has been developed (qualification runner and reporting engine). This framework allows for an automatic (re)-qualification workflow of the OSP suite, comprising the following steps (**Figure 1**):

- PBPK model development and verification with observed data,

- Qualification plan generation,

- Qualification plan execution,

- Qualification report generation.

  

**Figure 1: OSP suite automatic (re)-qualification workflow**
![OSP qualification workflow](images/OSP_Qualification_Workflow_1.png)



In a first step, the respective qualification scenario is saved in a special qualification repository on [GitHub](https://github.com/Open-Systems-Pharmacology/). This qualification scenario repository contains a detailed qualification plan that links and combines respective models and data to address the use case that shall be qualified. Therefore, the qualification plan consists of: 

- PK-Sim project files,
- Additional model building steps (if applicable),
- Description of potential cross-dependencies between PK-Sim project files (if applicable),
- Observed data (needed for model development and verification),
- Qualification scenario description text modules
- Detailed report settings to describe the generation of charts and qualification measures. 

PK-Sim projects, observed data sets, and qualification scenario text modules are deposited in distinct repositories and are referenced by the qualification plan (**Figure 2**).



**Figure 2: Qualification scenario repository landscape on GitHub**
![OSP qualification workflow detail](images/OSP_Qualification_Workflow_2.png)



In a second step the [qualification runner](https://github.com/Open-Systems-Pharmacology/QualificationRunner) processes the qualification plan, i.e. all project parts are exported and prepared for the [reporting engine](https://github.com/Open-Systems-Pharmacology/Reporting-Engine). The reporting engine provides a validated environment (currently implemented in MATLAB®, a transfer to R is in development) for model execution and finally generates the qualification report. This report contains the evaluation of the individual PBPK models with observed data (i.e. standard goodness of fit plots, visual predictive checks) and a comprehensive qualification of the specific use case assessing the predictive performance of the OSP suite by means of a predefined set of qualification measures and charts. 

The automated execution of the described workflow can be triggered to assess re-qualification in case new data, changes in model structure or parameterization, or new OSP suite releases arise.




# 7 Glossary
| ADME    | Absorption, Distribution, Metabolism,  Excretion             |
| ------- | ------------------------------------------------------------ |
| AUC     | Area under the plasma concentration  versus time curve       |
| AUCinf  | AUC until infinity                                           |
| AUClast | AUC until last measurable sample                             |
| AUCR    | Area under the plasma concentration  versus time curve Ratio |
| b.i.d.  | Twice daily (bis in diem)                                    |
| CL      | Clearance                                                    |
| Clint   | Intrinsic liver clearance                                    |
| Cmax    | Maximum concentration                                        |
| CmaxR   | Maximum concentration Ratio                                  |
| CYP     | Cytochrome P450 oxidase                                      |
| CYP1A2  | Cytochrome P450 1A2 oxidase                                  |
| CYP2C19 | Cytochrome P450 2C19 oxidase                                 |
| CYP3A4  | Cytochrome P450 3A4 oxidase                                  |
| DDI     | Drug-drug interaction                                        |
| e.c.    | Enteric coated                                               |
| EE      | Ethinylestradiol                                             |
| EM      | Extensive metabolizers                                       |
| fm      | Fraction metabolized                                         |
| FMO     | Flavin-containing monooxygenase                              |
| fu      | Fraction unbound                                             |
| FDA     | Food and Drug administration                                 |
| GFR     | Glomerular filtration rate                                   |
| HLM     | Human liver microsomes                                       |
| hm      | homozygous                                                   |
| ht      | heterozygous                                                 |
| IM      | Intermediate metabolizers                                    |
| i.v.    | Intravenous                                                  |
| IVIVE   | In Vitro to In  Vivo Extrapolation                           |
| Ka      | Absorption rate constant                                     |
| kcat    | Catalyst rate constant                                       |
| Ki      | Inhibitor constant                                           |
| Kinact  | Rate of enzyme inactivation                                  |
| Km      | Michaelis Menten constant                                    |
| m.d.    | Multiple dose                                                |
| OSP     | Open Systems Pharmacology                                    |
| PBPK    | Physiologically-based pharmacokinetics                       |
| PK      | Pharmacokinetics                                             |
| PI      | Parameter identification                                     |
| PM      | Poor metabolizers                                            |
| RT-PCR  | Reverse transcription polymerase chain  reaction             |
| p.o.    | Per os                                                       |
| q.d.    | Once daily (quaque diem)                                     |
| SD      | Single Dose                                                  |
| SE      | Standard error                                               |
| s.d.SPC | Single dose Summary of Product Characteristics                |
| SD      | Standard deviation                                           |
| TDI     | Time dependent inhibition                                    |
| t.i.d   | Three times a day (ter in die)                               |
| UGT     | Uridine  5'-diphospho-glucuronosyltransferase                |
| UM      | Ultra-rapid metabolizers                                     |
