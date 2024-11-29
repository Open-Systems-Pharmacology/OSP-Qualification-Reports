# CYP1A2 DDI Qualification



| Version                         | 1.2-OSP11.3                                                   |
| ------------------------------- | ------------------------------------------------------------ |
| Qualification Plan Release      | https://github.com/Open-Systems-Pharmacology/Qualification-DDI-CYP1A2/releases/tag/v1.2 |
| OSP Version                     | 11.3                                                          |
| Qualification Framework Version | 2.3                                                          |





This qualification report is filed at:

https://github.com/Open-Systems-Pharmacology/OSP-Qualification-Reports
# Table of Contents
  * [1 Introduction](#1-introduction)
    * [1.1 Objective](#11-objective)
    * [1.2 CYP1A2 DDI Network](#12-cyp1a2-ddi-network)
      * [Caffeine - Ethinylestradiol DDI](#caffeine---ethinylestradiol-ddi)
      * [Tizanidine - Ethinylestradiol DDI](#tizanidine---ethinylestradiol-ddi)
      * [Caffeine - Fluvoxamine DDI](#caffeine---fluvoxamine-ddi)
      * [Tizanidine - Fluvoxamine DDI](#tizanidine---fluvoxamine-ddi)
      * [Tizanidine - Mexiletine DDI](#tizanidine---mexiletine-ddi)
      * [Caffeine - Mexiletine DDI](#caffeine---mexiletine-ddi)
      * [Mexiletine - Fluvoxamine DDI](#mexiletine---fluvoxamine-ddi)
  * [2 Qualification of Use Case CYP1A2-mediated DDI](#2-qualification-of-use-case-cyp1a2-mediated-ddi)
    * [Perpetrator](#perpetrator)
      * [Ethinylestradiol](#ethinylestradiol)
      * [Fluvoxamine](#fluvoxamine)
      * [Mexiletine](#mexiletine)
    * [Victim](#victim)
      * [Caffeine](#caffeine)
      * [Mexiletine](#mexiletine)
      * [Tizanidine](#tizanidine)
  * [3 Concentration-Time Profiles](#3-concentration-time-profiles)
    * [3.1 Tizanidine - Ethinylestradiol DDI](#31-tizanidine---ethinylestradiol-ddi)
    * [3.2 Caffeine - Fluvoxamine DDI](#32-caffeine---fluvoxamine-ddi)
    * [3.3 Tizanidine - Fluvoxamine DDI](#33-tizanidine---fluvoxamine-ddi)
    * [3.4 Tizanidine - Mexiletine DDI](#34-tizanidine---mexiletine-ddi)
    * [3.5 Caffeine - Mexiletine DDI](#35-caffeine---mexiletine-ddi)
    * [3.6 Mexiletine - Fluvoxamine DDI](#36-mexiletine---fluvoxamine-ddi)
  * [4 Conclusion](#4-conclusion)
  * [5 References](#5-references)
  * [6 Appendix](#6-appendix)
    * [6.1 Open Systems Pharmacology Suite (OSPS) Introduction](#61-open-systems-pharmacology-suite-osps-introduction)
    * [6.2 Mathematical Implementation of Drug-Drug Interactions](#62-mathematical-implementation-of-drug-drug-interactions)
    * [6.3 Automatic (re)-qualification workflow](#63-automatic-re-qualification-workflow)
  * [7 Glossary](#7-glossary)
# 1 Introduction
                   

## 1.1 Objective
This qualification report evaluates the developed PBPK drug-drug interactions (DDI) models network for the ability to perform simulations with the intended purpose to predict cytochrome P450 1A2 (**CYPA12**)-mediated DDI.

To demonstrate the level of confidence, the predictive performance of the platform for this intended purpose is assessed via a network of PBPK models of selected index CYP1A2 DDI perpetrators, and respective sensitive CYP1A2 victim drugs and a comprehensive dataset from published clinical DDI studies. All PBPK models represent whole-body PBPK models, which allow dynamic DDI simulations in organs expressing CYP1A2.

The respective *qualification plan* to produce this *qualification report* is transparently documented and provided open-source (https://github.com/Open-Systems-Pharmacology/OSP-Qualification-Reports). The same applies for all presented PBPK models including *evaluation reports* on model building and evaluation of each model (https://github.com/Open-Systems-Pharmacology/OSP-PBPK-Model-Library).

*Evaluation reports* including descriptions on model building and detailed evaluations of the included models are documented separately (see [Section 1.2](#12-cyp1a2-ddi-network)).

Please refer to the [Appendix](#6-appendix) to learn more details:

- An overview over the Open Systems Pharmacology Suite is given in chapter [Section 6.1](#61-open-systems-pharmacology-suite-osps-introduction)

- [Section 6.2](#62-mathematical-implementation-of-drug-drug-interactions) shows the implementation of the underlying mathematical equations for drug-drug interactions in the OSP suite.

- A detailed general description of the performed qualification workflow (*qualification plan*, *qualification report*, etc.) can be found in chapter [Section 6.3](#63-automatic-re-qualification-workflow).

  



## 1.2 CYP1A2 DDI Network
CYP1A2 is involved in the elimination of about 15% of all therapeutic drugs (e.g., clozapine, tacrine, tizanidine, and theophylline), a number of procarcinogens (e.g. benzo[*a*]pyrene and aflatoxin B1), and several important endogenous compounds (e.g. steroids and arachidonic acids) ([Zhou 2009](#5-references), [Goldstein 2001](#5-references)). This enzyme is exclusively expressed in the liver and can be markedly induced by smoking. Well-known substrates of CYP1A2 include caffeine and tizanidine.

Like other CYPs, CYP1A2 is subject to induction and/or inhibition by a number of compounds, which can result in significant drug interactions in clinical practice. 

The U.S. Food and Drug Administration (FDA) lists several perpetrator and victim drugs of interactions in the CYP1A2 network ([FDA](#5-references)). For instance, caffeine and tizanidine are classified as sensitive index substrates for CYP1A2, and fluvoxamine is listed as a strong clinical index inhibitor of CYP1A2.

To qualify the developed models for the prediction of the CYP1A2 DDI potential of new drugs, a set of verified PBPK models of index perpetrators and respective CYP1A2 DDI victim drugs is specified to set up a CYP1A2-mediated DDI modeling network.

The following perpetrator compounds were selected: 

- **Fluvoxamine** (strong CYP1A2 inhibitor)
  Model snapshot and evaluation plan (*release* **alt_v1.0**): https://github.com/Open-Systems-Pharmacology/Fluvoxamine-Model/releases/tag/alt_v1.0
- **Ethinylestradiol** (moderate CYP1A2 inhibitor)
  Model snapshot and evaluation plan (*release* **v1.1**): https://github.com/Open-Systems-Pharmacology/Ethinylestradiol-Model/releases/tag/v1.1
- **Mexiletine** (moderate CYP1A2 inhibitor)
  Model snapshot and evaluation plan (*release* **v1.1**): https://github.com/Open-Systems-Pharmacology/Mexiletine-Model/releases/tag/v1.1


The following sensitive CYP1A2 substrates as victim drugs were selected:

- **Caffeine**
  PK-Sim compound template
- **Tizanidine**
  Model snapshot and evaluation plan (*release* **v1.1**): https://github.com/Open-Systems-Pharmacology/Tizanidine-Model/releases/tag/v1.1
- **Mexiletine**
  Model snapshot and evaluation plan (*release* **v1.1**): https://github.com/Open-Systems-Pharmacology/Mexiletine-Model/releases/tag/v1.1

The following interaction studies were predicted and used to qualify/optimize the final network:

- Strong CYP1A2 inhibition

  - Fluvoxamine - caffeine
  - Fluvoxamine - tizanidine
  - Fluvoxamine - mexiletine
- Moderate CYP1A2 inhibition
  - Mexiletine - caffeine
  - Mexiletine - tizanidine
  - Ethinylestradiol - caffeine
  - Ethinylestradiol - tizanidine

**Figure 1** shows the specified and developed DDI modeling network of interacting perpetrator and victim drugs.

**Figure** **1: CYP1A2 DDI modeling network**
![DDI CYP1A2 network](images/DDI_CYP1A2_Compound_Network.png)

The Ki values used to predict the interactions are listed in [Table 1](#table-1).

| **Inhibitor category** | **Inhibitor**         | **Substrate** | **Ki**    | **Reference**             |
| ---------------------- | --------------------- | ------------- | --------- | ------------------------- |
| Strong CYP1A2          | Fluvoxamine           | caffeine      | 2.97 nM   | [Iga 2016](#5-references) |
|                        |                       | tizanidine    | 0.8697 nM | Fit<sup>1</sup>           |
|                        |                       | mexiletine    | 2.97 nM   | [Iga 2016](#5-references) |
| Moderate CYP1A2        | Mexiletine            | caffeine      | 0.28 µM   | [Wei 1999](#5-references) |
|                        |                       | tizanidine    | 0.28 µM   | [Wei 1999](#5-references) |
|                        | Ethinylestradiol (EE) | caffeine      | 0.48 µM   | Fit<sup>2</sup>           |
|                        |                       | tizanidine    | 0.48 µM   | Fit<sup>2</sup>           |

**Table 1:**<a name="table-1"></a> Ki values used in CYP1A2 DDI network. <sup>1</sup>Lowest literature value = 0.9 nM; <sup>2</sup>Literature value = 10.6 µM

The published DDI studies between the respective perpetrators and victim drugs were simulated and compared to observed data. The following sections give an overview of the clinical studies being part of this qualification report.
### Caffeine - Ethinylestradiol DDI
A dynamical DDI simulation with ethinylestradiol as CYP1A2 inhibitor and caffeine as victim was conducted and compared to literature data. No profiles of caffeine under this interaction were available, but [Balogh 1995](#5-references) reported a 55% decrease in caffeine CL due to ethinylestradiol co-administration and report AUCR and CmaxR.
### Tizanidine - Ethinylestradiol DDI
The tizanidine-ethinylestradiol interaction was evaluated using clinical DDI studies listed in [Table 2](#table-2).

| **Source**                     | **Route** | **Dose [mg] /** **Schedule \*** | **Pop.** | **Sex** | **N** | **Form.** |
| ------------------------------ | --------- | ------------------------------- | -------- | ------- | ----- | --------- |
| [Granfors 2005](#5-references) | p.o.      | EE: 0.02<br />Tizanidine: 4     | HV       | f       | 15    | tablet    |

**Table 2:**<a name="table-2"></a> Literature sources of clinical concentration data of tizanidine used for DDI prediction qualification with ethinylestradiol. *EE: ethinylestradiol*

A dynamical DDI simulation with ethinylestradiol as moderate CYP1A2 inhibitor and tizanidine as victim drug was conducted and compared to literature data. Clinical observations were derived from [Granfors 2005](#5-references) in which 15 healthy women using Oral contraceptives (OCs) (ethinylestradiol + gestodene) and 15 healthy women without OCs (control subjects) ingested a single dose of 4 mg tizanidine.
### Caffeine - Fluvoxamine DDI
The caffeine-fluvoxamine interaction was evaluated using clinical DDI studies listed in [Table 3](#table-3).

| **Source**                        | **Route** | **Dose [mg] /** **Schedule \***                            | **Pop.** | Age [yrs] (mean) | Weight [kg] (mean) | **Sex** | **N** | **Form.** |
| --------------------------------- | --------- | ---------------------------------------------------------- | -------- | ---------------- | ------------------ | ------- | ----- | --------- |
| [Jeppesen 1996](#5-references)    | p.o.      | 200 caffeine,<br />50 mg 4 days, 100 mg 8 days fluvoxamine | HV       | 27               | -                  | -       | 8     | Tablet    |
| [Culm-Merdek 2005](#5-references) | p.o.      | 250 caffeine,<br />100 b.i.d. fluvoxamine                  | HV       | 50               | 82                 | m/f     | 7     | Capsule   |

**Table 3:**<a name="table-3"></a> Literature sources of clinical concentration data of caffeine used for DDI prediction qualification with fluvoxamine.

A dynamical DDI simulation with fluvoxamine as CYP1A2 inhibitor and caffeine as victim was conducted and compared to literature data. For caffeine the template model included in PK-Sim was used. Two published clinical studies were found where fluvoxamine and caffeine were given together. Fluvoxamine is a strong inhibitor of CYP1A2 and increases the AUC of caffeine by 7 to 14-fold.

In [Jeppesen 1996](#5-references), subjects in one group received 50 mg fluvoxamine-maleate on the first 4 days followed by 100 mg q.d. for 8 days. On day 8 they received a single dose of 200 mg caffeine. The other group received caffeine without fluvoxamine co-treatment.

In [Culm-Merdek 2005](#5-references), seven healthy subjects received single 250 mg dose of caffeine (or matching placebo) together with fluvoxamine (four doses of 100 mg over 2 days) or with matching placebo in a cross-over fashion. 

The simulated caffeine levels with co-administered fluvoxamine were underpredicted. However, the pre-dose concentrations of caffeine were not 0 in the test group. It may be speculated that subjects may not have refrained completely from caffeine containing beverages before the test period. To investigate this hypothesis, a simulation was conducted where a dose of 100 mg caffeine (corresponding approximately to the caffeine content of one cup of coffee ([Caffeine quantities, FDA](#5-references))) was given 24 hours before the administration of caffeine-tablets as per the study protocol. The resulting simulation results support this hypothesis. Hence it was not deemed necessary to adjust the underlying caffeine or fluvoxamine models but rather conclude that the clinical study potentially was facing issues with subjects not compliant with the protocol rules and drank coffee the morning before the study day. The final DDI simulations were therefore conducted with administration of 100 mg caffeine 24 hours prior study protocol.
### Tizanidine - Fluvoxamine DDI
The tizanidine-fluvoxamine interaction was evaluated using clinical DDI studies listed in [Table 4](#table-4).

| **Source**                     | **Route** | **Dose [mg] /** **Schedule \***          | **Pop.** | Age [yrs] | Weight [kg] | **Sex** | **N** | **Form.** |
| ------------------------------ | --------- | ---------------------------------------- | -------- | --------- | ----------- | ------- | ----- | --------- |
| [Granfors 2004](#5-references) | p.o.      | 4 mg tizanidine,<br />100 mg fluvoxamine | HV       | 21-31     | 65-83       | m       | 10    | Tablet    |

**Table 4:**<a name="table-4"></a> Literature sources of clinical concentration data of tizanidine used for DDI prediction qualification with fluvoxamine. *\*:single dose*

In the clinical study reported by [Granfors 2004](#5-references), a single oral dose of 4 mg tizanidine was given after treatment with fluvoxamine (100mg fluvoxamine-maleate ~73.3 mg free base, q.d. for 4 days).

Initially, the Ki value for the inhibition of CYP1A2 by fluvoxamine reported by [Iga 2016](#5-references) was used. While the predicted Cmax ratio matched closely the observed value, the AUC ratio was underpredicted by a factor of 2.1. Since the predictions of the tizanidine profiles without co-administration of fluvoxamine matched the observations very well, it was concluded that the most plausible reason for the under prediction was the value of Ki, as the fraction metabolized via CYP1A2 was already 99%. Hence Ki was optimized using the data from [Granfors 2004](#5-references). A Ki value of 0.8697 +/- 0.1935 nmol/L was estimated, which is still in line with the Ki values derived for other CYP1A2 substrates.
### Tizanidine - Mexiletine DDI
The tizanidine-mexiletine interaction was evaluated using clinical DDI studies listed in [Table 5](#table-5).

| **Source**                 | **Route** | **Dose [mg] /** **Schedule \***              | **Pop.** | **Sex** | **N** | **Form.** |
| -------------------------- | --------- | -------------------------------------------- | -------- | ------- | ----- | --------- |
| [Momo 2010](#5-references) | p.o.      | 2 mg tizanidine,<br />50 mg b.i.d mexiletine | HV       | m       | 12    | Tablet    |

**Table 5:**<a name="table-5"></a> Literature sources of clinical concentration data of tizanidine used for DDI prediction qualification with mexiletine.

A dynamical DDI simulation with mexiletine as CYP1A2 inhibitor and tizanidine as victim was conducted and compared to literature data from [Momo 2010](#5-references). The same Ki as for the caffeine interaction simulation was used (0.28 µM). The predefined “Standard European Male for DDI” individual (age = 30 y, weight = 73 kg, height = 176 cm, BMI = 23.57 kg/m2) was used.

The pharmacokinetics of tizanidine was examined in an open-label study in 12 healthy participants after a single dose of tizanidine (2 mg) with and without mexiletine co-administration (50 mg, 3 times as a pretreatment for a day and 2 times on the study day).
### Caffeine - Mexiletine DDI
The caffeine-mexiletine interaction was evaluated using clinical DDI studies listed in [Table 6](#table-6).

| **Source**                   | **Route** | **Dose [mg] /** **Schedule \***   | **Pop.** | **N** |
| ---------------------------- | --------- | --------------------------------- | -------- | ----- |
| [Joeres 1987](#5-references) | p.o.      | 366 caffeine,<br />200 mexiletine | HV       | 6     |

**Table 6:**<a name="table-6"></a> Literature sources of clinical concentration data of caffeine used for DDI prediction qualification with mexiletine.

A dynamical DDI simulation with mexiletine as CYP1A2 inhibitor and caffeine as victim was conducted and compared to literature data.

Clinical observations of caffeine-mexiletine interaction were derived from [Joeres 1987](#5-references) where 6 healthy volunteers received 366 mg caffeine (400 mg caffeine monohydrate) after an overnight fast, together with 200 mg mexiletine orally. One week later caffeine was administered alone. 

The in-built caffeine template model included in PK-Sim was used for caffeine predictions.

Competitive inhibition was assumed on CYP1A2 enzyme between caffeine (substrate) and mexiletine (inhibitor) with an inhibitory constant of 0.28 µM. No reported values were found for mexiletine Ki on CYP1A2 and caffeine as substrate, so the inhibitory constant for methoxyresofurin ([Ko 1997](#5-references)) was used [calculated in vivo, unbound Ki for methoxyresofurin].
### Mexiletine - Fluvoxamine DDI
The mexiletine-fluvoxamine interaction was evaluated using clinical DDI studies listed in [Table 7](#table-7).

| **Source**                     | **Route** | **Dose [mg] /** **Schedule \***              | **Pop.**    | **Sex** | **N** | **Form.** |
| ------------------------------ | --------- | -------------------------------------------- | ----------- | ------- | ----- | --------- |
| [Kusumoto 2001](#5-references) | p.o.      | 166.62 mexiletine<br />50 b.i.d. fluvoxamine | HV japanese | m       | 6     | -         |

**Table 7:**<a name="table-7"></a> Literature sources of clinical concentration data of mexiletine used for DDI prediction qualification with fluvoxamine. *\*:single dose*

A dynamical DDI simulation with fluvoxamine as CYP1A2 inhibitor and mexiletine as victim was conducted and compared to literature data ([Kusumoto 2001](#5-references)). A typical Japanese subject (age = 30 y, weight = 61.87 kg, height = 168.99 cm, BMI = 21.67 kg/m2) was created in PK-Sim from predefined database "Japanese (2015)" by adding CYP2D6 and CYP1A2 expressions from PK-Sim RT PCR database.

A randomized crossover design with two phases was used. Each subject received an oral dose of mexiletine (200 mg) or fluvoxamine (50 mg twice a day) for 7 days, and on the eighth day they received mexiletine and fluvoxamine concomitantly.
# 2 Qualification of Use Case CYP1A2-mediated DDI
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


![001_plotDDIRatioAUCPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP1A2-mediated_DDI/001_plotDDIRatioAUCPredictedVsObserved.png)

![002_plotDDIRatioAUCResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP1A2-mediated_DDI/002_plotDDIRatioAUCResidualsVsObserved.png)

![003_plotDDIRatioCMAXPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP1A2-mediated_DDI/003_plotDDIRatioCMAXPredictedVsObserved.png)

![004_plotDDIRatioCMAXResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP1A2-mediated_DDI/004_plotDDIRatioCMAXResidualsVsObserved.png)

GMFE (AUC) = 1.396312 

GMFE (CMAX) = 1.219248 

|AUC                       |Number|Ratio [%]|
|-------------------------:|-----:|--------:|
|Points total              |8     |-        |
|Points within Guest et al.|6     |75       |
|Points within 2-fold      |7     |87.5     |

|CMAX                      |Number|Ratio [%]|
|-------------------------:|-----:|--------:|
|Points total              |8     |-        |
|Points within Guest et al.|7     |87.5     |
|Points within 2-fold      |8     |100      |

|DataID|Perpetrator                    |Victim        |Predicted AUC Ratio|Observed AUC Ratio|Pred/Obs AUC Ratio|Predicted CMAX Ratio|Observed CMAX Ratio|Pred/Obs CMAX Ratio|Reference       |
|-----:|------------------------------:|-------------:|------------------:|-----------------:|-----------------:|-------------------:|------------------:|------------------:|---------------:|
|14002 |Ethinylestradiol, 20 mg, PO,   |Tizanidine, PO|4.4136             |3.92              |1.1259            |3.751               |3.02               |1.2421             |Granfors 2005   |
|14004 |Fluvoxamine, 100 mg, PO,       |Caffeine, PO  |10.1               |7.16              |1.4106            |1.0794              |1.09               |0.99028            |Jeppesen 1996   |
|14006 |Fluvoxamine, 100 mg, PO,       |Caffeine, PO  |13.8497            |13.71             |1.0102            |1.3449              |1.4                |0.96065            |Culm-Merdek 2005|
|13017 |Fluvoxamine, 100 mg, PO,       |Tizanidine, PO|39.2197            |33                |1.1885            |16.0045             |12.1               |1.3227             |Granfors 2004   |
|14008 |Mexiletine, 200 mg, PO,        |Caffeine, PO  |1.6676             |2.83              |0.58924           |1.0001              |1.89               |0.52917            |Joeres 1987     |
|13018 |Mexiletine, 50 mg, PO,         |Tizanidine, PO|2.4837             |3.42              |0.72624           |2.4179              |3.22               |0.75089            |Momo 2010       |
|14010 |Fluvoxamine, 50 mg, PO,        |Mexiletine, PO|1.3081             |1.55              |0.84396           |1.081               |1.16               |0.93188            |Kusumoto 2001   |
|6110  |Ethinylestradiol, 0.03 mg, PO, |Caffeine, PO  |5.8295             |2.13              |2.7368            |1.0983              |1.15               |0.95502            |Balogh 1995     |

## Perpetrator

### Ethinylestradiol

![001_plotDDIRatioAUCPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP1A2-mediated_DDI/001_Perpetrator/001_Ethinylestradiol/001_plotDDIRatioAUCPredictedVsObserved.png)

![002_plotDDIRatioAUCResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP1A2-mediated_DDI/001_Perpetrator/001_Ethinylestradiol/002_plotDDIRatioAUCResidualsVsObserved.png)

![003_plotDDIRatioCMAXPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP1A2-mediated_DDI/001_Perpetrator/001_Ethinylestradiol/003_plotDDIRatioCMAXPredictedVsObserved.png)

![004_plotDDIRatioCMAXResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP1A2-mediated_DDI/001_Perpetrator/001_Ethinylestradiol/004_plotDDIRatioCMAXResidualsVsObserved.png)

GMFE (AUC) = 1.755403 

GMFE (CMAX) = 1.140423 

|AUC                       |Number|Ratio [%]|
|-------------------------:|-----:|--------:|
|Points total              |2     |-        |
|Points within Guest et al.|1     |50       |
|Points within 2-fold      |1     |50       |

|CMAX                      |Number|Ratio [%]|
|-------------------------:|-----:|--------:|
|Points total              |2     |-        |
|Points within Guest et al.|2     |100      |
|Points within 2-fold      |2     |100      |

### Fluvoxamine

![001_plotDDIRatioAUCPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP1A2-mediated_DDI/001_Perpetrator/002_Fluvoxamine/001_plotDDIRatioAUCPredictedVsObserved.png)

![002_plotDDIRatioAUCResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP1A2-mediated_DDI/001_Perpetrator/002_Fluvoxamine/002_plotDDIRatioAUCResidualsVsObserved.png)

![003_plotDDIRatioCMAXPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP1A2-mediated_DDI/001_Perpetrator/002_Fluvoxamine/003_plotDDIRatioCMAXPredictedVsObserved.png)

![004_plotDDIRatioCMAXResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP1A2-mediated_DDI/001_Perpetrator/002_Fluvoxamine/004_plotDDIRatioCMAXResidualsVsObserved.png)

GMFE (AUC) = 1.190201 

GMFE (CMAX) = 1.105209 

|AUC                       |Number|Ratio [%]|
|-------------------------:|-----:|--------:|
|Points total              |4     |-        |
|Points within Guest et al.|4     |100      |
|Points within 2-fold      |4     |100      |

|CMAX                      |Number|Ratio [%]|
|-------------------------:|-----:|--------:|
|Points total              |4     |-        |
|Points within Guest et al.|4     |100      |
|Points within 2-fold      |4     |100      |

### Mexiletine

![001_plotDDIRatioAUCPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP1A2-mediated_DDI/001_Perpetrator/003_Mexiletine/001_plotDDIRatioAUCPredictedVsObserved.png)

![002_plotDDIRatioAUCResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP1A2-mediated_DDI/001_Perpetrator/003_Mexiletine/002_plotDDIRatioAUCResidualsVsObserved.png)

![003_plotDDIRatioCMAXPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP1A2-mediated_DDI/001_Perpetrator/003_Mexiletine/003_plotDDIRatioCMAXPredictedVsObserved.png)

![004_plotDDIRatioCMAXResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP1A2-mediated_DDI/001_Perpetrator/003_Mexiletine/004_plotDDIRatioCMAXResidualsVsObserved.png)

GMFE (AUC) = 1.528665 

GMFE (CMAX) = 1.586400 

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

## Victim

### Caffeine

![001_plotDDIRatioAUCPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP1A2-mediated_DDI/002_Victim/001_Caffeine/001_plotDDIRatioAUCPredictedVsObserved.png)

![002_plotDDIRatioAUCResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP1A2-mediated_DDI/002_Victim/001_Caffeine/002_plotDDIRatioAUCResidualsVsObserved.png)

![003_plotDDIRatioCMAXPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP1A2-mediated_DDI/002_Victim/001_Caffeine/003_plotDDIRatioCMAXPredictedVsObserved.png)

![004_plotDDIRatioCMAXResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP1A2-mediated_DDI/002_Victim/001_Caffeine/004_plotDDIRatioCMAXResidualsVsObserved.png)

GMFE (AUC) = 1.603950 

GMFE (CMAX) = 1.200931 

|AUC                       |Number|Ratio [%]|
|-------------------------:|-----:|--------:|
|Points total              |4     |-        |
|Points within Guest et al.|2     |50       |
|Points within 2-fold      |3     |75       |

|CMAX                      |Number|Ratio [%]|
|-------------------------:|-----:|--------:|
|Points total              |4     |-        |
|Points within Guest et al.|3     |75       |
|Points within 2-fold      |4     |100      |

### Mexiletine

![001_plotDDIRatioAUCPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP1A2-mediated_DDI/002_Victim/002_Mexiletine/001_plotDDIRatioAUCPredictedVsObserved.png)

![002_plotDDIRatioAUCResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP1A2-mediated_DDI/002_Victim/002_Mexiletine/002_plotDDIRatioAUCResidualsVsObserved.png)

![003_plotDDIRatioCMAXPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP1A2-mediated_DDI/002_Victim/002_Mexiletine/003_plotDDIRatioCMAXPredictedVsObserved.png)

![004_plotDDIRatioCMAXResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP1A2-mediated_DDI/002_Victim/002_Mexiletine/004_plotDDIRatioCMAXResidualsVsObserved.png)

GMFE (AUC) = 1.184895 

GMFE (CMAX) = 1.073104 

|AUC                       |Number|Ratio [%]|
|-------------------------:|-----:|--------:|
|Points total              |1     |-        |
|Points within Guest et al.|1     |100      |
|Points within 2-fold      |1     |100      |

|CMAX                      |Number|Ratio [%]|
|-------------------------:|-----:|--------:|
|Points total              |1     |-        |
|Points within Guest et al.|1     |100      |
|Points within 2-fold      |1     |100      |

### Tizanidine

![001_plotDDIRatioAUCPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP1A2-mediated_DDI/002_Victim/003_Tizanidine/001_plotDDIRatioAUCPredictedVsObserved.png)

![002_plotDDIRatioAUCResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP1A2-mediated_DDI/002_Victim/003_Tizanidine/002_plotDDIRatioAUCResidualsVsObserved.png)

![003_plotDDIRatioCMAXPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP1A2-mediated_DDI/002_Victim/003_Tizanidine/003_plotDDIRatioCMAXPredictedVsObserved.png)

![004_plotDDIRatioCMAXResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP1A2-mediated_DDI/002_Victim/003_Tizanidine/004_plotDDIRatioCMAXResidualsVsObserved.png)

GMFE (AUC) = 1.225948 

GMFE (CMAX) = 1.298197 

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




## 3.1 Tizanidine - Ethinylestradiol DDI
                   

![001_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/001_3_1_Tizanidine_-_Ethinylestradiol_DDI/001_plotComparisonTimeProfile.png)

## 3.2 Caffeine - Fluvoxamine DDI
                   

![001_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/002_3_2_Caffeine_-_Fluvoxamine_DDI/001_plotComparisonTimeProfile.png)

![002_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/002_3_2_Caffeine_-_Fluvoxamine_DDI/002_plotComparisonTimeProfile.png)

## 3.3 Tizanidine - Fluvoxamine DDI
                   

![001_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/003_3_3_Tizanidine_-_Fluvoxamine_DDI/001_plotComparisonTimeProfile.png)

## 3.4 Tizanidine - Mexiletine DDI
                   

![001_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/004_3_4_Tizanidine_-_Mexiletine_DDI/001_plotComparisonTimeProfile.png)

## 3.5 Caffeine - Mexiletine DDI
                   

![001_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/005_3_5_Caffeine_-_Mexiletine_DDI/001_plotComparisonTimeProfile.png)

## 3.6 Mexiletine - Fluvoxamine DDI
                   

![001_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/006_3_6_Mexiletine_-_Fluvoxamine_DDI/001_plotComparisonTimeProfile.png)

# 4 Conclusion
The predicted perpetrator/victim drug concentration-time profiles, DDI AUC and Cmax ratios confirmed that the developed PBPK models are well suited to characterize the CYP1A2 DDI network over the full range of reported DDI studies. The same Ki values could be used by the moderate CYP1A2 inhibitors EE (0.48 μM) and mexiletine (0.28 μM) with regards to all tested substrates (caffeine and tizanidine). For the strong inhibition of CYP1A2 by fluvoxamine, the same Ki value (2.97 nM) could be used for both caffeine and mexiletine as substrate. In contrast, for tizanidine the Ki (0.9 nM) needed to be refitted to capture the data.

**Fluvoxamine** 

- CYP1A2 inhibition:
  - DDI simulations with caffeine, tizanidine, and mexiletine demonstrate an excellent prediction (ratio pred/obs = around 1 and within 2-fold) of the inhibitory potential of fluvoxamine on CYP1A2.

**Tizanidine**

- Substrate:

  - DDI simulations with fluvoxamine as inhibitor of tizanidine demonstrated a good prediction of tizanidine levels (pred/obs AUCR and pred/obs CmaxR within 2-fold) when using an optimized value of fluvoxamine Ki.
  - DDI simulations with mexiletine as inhibitor of tizanidine demonstrated an underprediction of tizanidine levels but were within 2-fold of observed ratios. Tizanidine is underpredicted both with and without mexiletine, probably due to an un-modelled food effect
  - DDI predictions with ethinylestradiol (EE) using a TDI mechanism was necessary to describe the      observed interaction with tizanidine. DDI simulations with ethinylestradiol demonstrated a good prediction of tizanidine levels when using TDI.

**Mexiletine**

+ Perpetrator:
  + DDI simulations with mexiletine as inhibitor of caffeine demonstrated an underprediction of caffeine levels but were within 2-fold of observed ratios.
  + DDI simulations with mexiletine as inhibitor of tizanidine demonstrated an underprediction of      tizanidine levels but were within 2-fold of observed ratios.
  + Overall, DDI predictions with mexiletine as an inhibitor tend to lead to underprediction of both AUCR and CmaxR but were within 2-fold of observed ratios.
+ Substrate:
  + DDI simulations with fluvoxamine as inhibitor of mexiletine demonstrated an excellent prediction of mexiletine levels.

**Ethinylestradiol**

- A TDI mechanism on CYP1A2 was introduced to describe tizanidine DDI study data.

- Perpetrator: 

  - DDI simulations with EE as inhibitor of caffeine demonstrated a good prediction of caffeine levels (pred/obs AUCR and pred/obs CmaxR within 2-fold).
  - DDI simulations with EE as inhibitor of tizanidine demonstrated a good prediction of tizanidine levels (pred/obs AUCR and pred/obs CmaxR within 2-fold).
# 5 References
**Balogh 1995** Balogh A, Boerner A, Kuhnz W, Klinger G, Vollanth R, Henschel L. Influence of ethinylestradiol-containing combination oral contraceptives with gestodene or levonorgestrel on caffeine elimination. *Eur J Clin Pharmacol*. 1995;48(2):161-166.

**Caffeine quantities, FDA**  Website: https://www.fda.gov/consumers/consumer-updates/spilling-beans-how-much-caffeine-too-much

**Culm-Merdek 2005** Culm-Merdek KE, Von Moltke LL, Harmatz JS, Greenblatt DJ. Fluvoxamine impairs single-dose caffeine clearance without altering caffeine pharmacodynamics. Br J Clin Pharmacol. 2005;60(5):486-493.

**FDA** U.S. Food and Drug Administration. Drug development and drug interactions: table of substrates, inhibitors and inducers. Website: https://www.fda.gov/drugs/drug-interactions-labeling/drug-development-and-drug-interactions-table-substrates-inhibitors-and-inducers (2020). Accessed 06 May 2022.

**Goldstein 2001** Goldstein JA., J. A. (2001). Clinical relevance of genetic polymorphisms in the human CYP2C subfamily. *Br J Clin Pharmacol*. 2001;British journal of clinical pharmacology, 52(4):), 349-355.

**Granfors 2004** Granfors M, Backman JT, Neuvonen M. Fluvoxamine drastically increases concentrations and effects of tizanidine: a potentially hazardous interaction. *Clinical Pharmacology & Therapeutics*. 2004 Apr;75(4):331–41.

**Granfors 2005** Granfors MT, Backman JT, Laitila J, Neuvonen PJ. Oral contraceptives containing ethinyl estradiol and gestodene markedly increase plasma concentrations and effects of tizanidine by inhibiting cytochrome P450 1A2. *Clin Pharmacol Ther*. 2005;78(4):400-411.

**Guest 2011** Guest EJ, Aarons L, Houston JB, Rostami-Hodjegan A, Galetin A. Critique of the two-fold measure of prediction success for ratios: application for the assessment of drug-drug interactions. Drug Metab Dispos. 2011 Feb;39(2):170-3.

**Iga 2016** Iga K. Dynamic and Static Simulations of Fluvoxamine-Perpetrated Drug-Drug Interactions Using Multiple Cytochrome P450 Inhibition Modeling, and Determination of Perpetrator-Specific CYP Isoform Inhibition Constants and Fractional CYP Isoform Contributions to Vic. *J Pharm Sci*.Victim Clearance. Journal of Pharmaceutical Sciences. 2016 Mar;105(3):1307-1317–17.

**Jeppesen 1996** Jeppesen U, Loft S, Poulsen H, Brosen K. A fluvoxamine-caffeine interaction study. Pharmacogenetics. 1996;(6):213-222.

**Joeres 1987** Joeres, R., Klinker, H., Heusler, H., Epping, J., Richter, E. (1987). Influence of mexiletine on caffeine elimination*. Pharmacology & therapeutics*, 33(1), 163-169.

**Ko 1997** Ko JW, Sukhova N, Thacker D, Chen P, Flockhart DA. Evaluation of omeprazole and lansoprazole as inhibitors of cytochrome P450 isoforms. *Drug Metab Dispos*. 1997;25(7):853-862.

**Kusumoto 2001** Kusumoto M, Ueno K, Oda A, et al. Effect of fluvoxamine on the pharmacokinetics of mexiletine in healthy Japanese men. *Clin Pharmacol Ther*. 2001;69(3):104-107. 

**Momo 2010** Momo K, Homma M, Osaka Y, Inomata SI, Tanaka M, Kohda Y. Effects of mexiletine, a CYP1A2 inhibitor, on tizanidine pharmacokinetics and pharmacodynamics. *J Clin Pharmacol*. 2010;50(3):331-337.

**Wei 1999** Wei X, Dai R, Zhai S, Thummel KE, Friedman FK, Vestal RE. Inhibition of human liver cytochrome P-450 1A2 by the class IB antiarrhythmics mexiletine, lidocaine, and tocainide. *J Pharmacol Exp Ther*. 1999;289(2):853-858.

**Zhou 2009** Zhou SF, Yang LP, Zhou ZW, Liu YH, Chan E. Insights into the substrate specificity, inhibitors, regulation, and polymorphisms and the clinical impact of human cytochrome P450 1A2. AAPS J. 2009 Sep;11(3):481-94. doi: 10.1208/s12248-009-9127-y. Epub 2009 Jul 10. PMID: 19590965; PMCID: PMC2758120.

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
