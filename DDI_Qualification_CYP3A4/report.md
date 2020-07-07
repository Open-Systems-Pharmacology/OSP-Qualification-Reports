# CYP3A4 DDI Qualification




| Version                         | 1.0-OSP9.1                                                   |
| ------------------------------- | ------------------------------------------------------------ |
| Qualification Plan Release      | https://github.com/Open-Systems-Pharmacology/Qualification-DDI-CYP3A4/releases/tag/v1.0 |
| OSP Version                     | 9.1                                                          |
| Qualification Framework Version | 2.2                                                          |





This qualification report is filed at:

https://github.com/Open-Systems-Pharmacology/OSP-Qualification-Reports
# Table of Contents
  * [1 Introduction](#1-introduction)
    * [1.1 Objective](#11-objective)
    * [1.2 CYP3A4 DDI Network](#12-cyp3a4-ddi-network)
      * [Clarithromycin - Midazolam DDI](#clarithromycin---midazolam-ddi)
      * [Clarithromycin - Triazolam DDI](#clarithromycin---triazolam-ddi)
      * [Erythromycin - Alfentanil DDI](#erythromycin---alfentanil-ddi)
      * [Erythromycin - Alprazolam DDI](#erythromycin---alprazolam-ddi)
      * [Erythromycin - Midazolam DDI](#erythromycin---midazolam-ddi)
      * [Erythromycin - Triazolam DDI](#erythromycin---triazolam-ddi)
      * [Fluvoxamine - Alprazolam DDI](#fluvoxamine---alprazolam-ddi)
      * [Fluvoxamine - Midazolam DDI](#fluvoxamine---midazolam-ddi)
      * [Itraconazole - Alprazolam DDI](#itraconazole---alprazolam-ddi)
      * [Itraconazole - Midazolam DDI](#itraconazole---midazolam-ddi)
      * [Itraconazole - Triazolam DDI](#itraconazole---triazolam-ddi)
      * [Verapamil - Midazolam DDI](#verapamil---midazolam-ddi)
      * [Efavirenz - Alfentanil-DDI](#efavirenz---alfentanil-ddi)
      * [Efavirenz - Midazolam DDI](#efavirenz---midazolam-ddi)
      * [Rifampicin - Alfentanil DDI](#rifampicin---alfentanil-ddi)
      * [Rifampicin - Alprazolam DDI](#rifampicin---alprazolam-ddi)
      * [Rifampicin - Midazolam DDI](#rifampicin---midazolam-ddi)
      * [Rifampicin - Triazolam DDI](#rifampicin---triazolam-ddi)
  * [2 Qualification of Use Case CYP3A4-mediated DDI](#2-qualification-of-use-case-cyp3a4-mediated-ddi)
    * [Mechanism](#mechanism)
      * [Competitive Inhibition](#competitive-inhibition)
      * [Induction](#induction)
      * [Mechanism based Inactivation](#mechanism-based-inactivation)
    * [Perpetrator](#perpetrator)
      * [Clarithromycin](#clarithromycin)
      * [Efavirenz](#efavirenz)
      * [Erythromycin](#erythromycin)
      * [Fluvoxamine](#fluvoxamine)
      * [Itraconazole](#itraconazole)
      * [Rifampicin](#rifampicin)
      * [Verapamil](#verapamil)
    * [Victim](#victim)
      * [Alfentanil](#alfentanil)
      * [Alprazolam](#alprazolam)
      * [Midazolam](#midazolam)
      * [Triazolam](#triazolam)
  * [3 Concentration-Time Profiles](#3-concentration-time-profiles)
    * [3.1 Clarithromycin - Midazolam DDI](#31-clarithromycin---midazolam-ddi)
    * [3.2 Clarithromycin - Triazolam DDI](#32-clarithromycin---triazolam-ddi)
    * [3.3 Erythromycin - Alfentanil DDI](#33-erythromycin---alfentanil-ddi)
    * [3.4 Erythromycin - Alprazolam DDI](#34-erythromycin---alprazolam-ddi)
    * [3.5 Erythromycin - Midazolam DDI](#35-erythromycin---midazolam-ddi)
    * [3.6 Erythromycin - Triazolam DDI](#36-erythromycin---triazolam-ddi)
    * [3.7 Fluvoxamine - Alprazolam DDI](#37-fluvoxamine---alprazolam-ddi)
    * [3.8 Fluvoxamine - Midazolam DDI](#38-fluvoxamine---midazolam-ddi)
    * [3.9 Itraconazole - Alprazolam DDI](#39-itraconazole---alprazolam-ddi)
    * [3.10 Itraconazole - Midazolam DDI](#310-itraconazole---midazolam-ddi)
    * [3.11 Itraconazole - Triazolam DDI](#311-itraconazole---triazolam-ddi)
    * [3.12 Verapamil - Midazolam DDI](#312-verapamil---midazolam-ddi)
    * [3.13 Efavirenz - Alfentanil DDI](#313-efavirenz---alfentanil-ddi)
    * [3.14 Efavirenz - Midazolam DDI](#314-efavirenz---midazolam-ddi)
    * [3.15 Rifampicin - Alfentanil DDI](#315-rifampicin---alfentanil-ddi)
    * [3.16 Rifampicin - Alprazolam DDI](#316-rifampicin---alprazolam-ddi)
    * [3.17 Rifampicin - Midazolam DDI](#317-rifampicin---midazolam-ddi)
    * [3.18 Rifampicin - Triazolam DDI](#318-rifampicin---triazolam-ddi)
  * [4 References](#4-references)
  * [5 Appendix](#5-appendix)
    * [5.1 Open Systems Pharmacology Suite (OSPS) Introduction](#51-open-systems-pharmacology-suite-osps-introduction)
    * [5.2 Mathematical Implementation of Drug-Drug Interactions](#52-mathematical-implementation-of-drug-drug-interactions)
    * [5.3 Automatic (re)-qualification workflow](#53-automatic-re-qualification-workflow)
# 1 Introduction
                   

## 1.1 Objective
This **qualification report** evaluates for the PBPK platform **PK-Sim** (as part of the open systems pharmacology (OSP) suite) the ability to perform simulations with the intended purpose to predict cytochrome P450 3A4 (**CYP3A4**)-mediated drug-drug interactions (**DDI**).

To demonstrate the level of confidence, the predictive performance of the platform for this indented purpose is assessed via a network of PBPK models of selected index CYP3A4 DDI perpetrators (covering the range from strong induction to strong inhibition), and respective sensitive index CYP3A4 victim drugs and a comprehensive dataset from published clinical DDI studies. All PBPK models represent whole-body PBPK models, which allow dynamic DDI simulations in organs expressing CYP3A4. 

The respective *qualification plan* to produce this *qualification report* is transparently documented and provided open-source (https://github.com/Open-Systems-Pharmacology/OSP-Qualification-Reports). The same applies for all presented PBPK models including *evaluation reports* on model building and evaluation of each model (https://github.com/Open-Systems-Pharmacology/OSP-PBPK-Model-Library).

*Evaluation reports* including descriptions on model building and detailed evaluations of the included models are documented separately (see [Section 1.2](#12-CYP3A4-DDI-Network)).

Please refer to the [Appendix](#5-Appendix) to learn more details:

- An overview over the Open Systems Pharmacology Suite is given in chapter [Section 5.1](#51-Open-Systems-Pharmacology-Suite-(OSPS)-Introduction)

- [Section 5.2](#52-Mathematical-Implementation-of-Drug-Drug-Interactions) shows the implementation of the underlying mathematical equations for drug-drug interactions in the OSP suite.

- A detailed general description of the performed qualification workflow (*qualification plan*, *qualification report*, etc.) can be found in chapter [Section 5.3](#53-Automatic-(re)-qualification-workflow).

  



## 1.2 CYP3A4 DDI Network

To qualify the OSP suite for the prediction of the CYP3A4 DDI potential of new drugs, a set of verified PBPK models of index perpetrators, covering the range from strong CYP3A4 induction to strong inhibition, and respective CYP3A4 DDI victim drugs is specified to set up a CYP3A4-mediated DDI modeling network. 


The following perpetrator compounds were selected: 

- **Rifampicin** (strong CYP3A4 inducer)
  Model snapshot and evaluation plan (*release* **v1.0**): https://github.com/Open-Systems-Pharmacology/Rifampicin-Model/releases/tag/v1.0
- **Efavirenz** (moderate CYP3A4 inducer)
  Model snapshot and evaluation plan (*release* **v1.0**): https://github.com/Open-Systems-Pharmacology/Efavirenz-Model/releases/tag/v1.0
- **Fluvoxamine** (weak/moderate CYP3A4 inhibitor)
  Model snapshot and evaluation plan (*release* **v1.0**): https://github.com/Open-Systems-Pharmacology/Fluvoxamine-Model/releases/tag/v1.0
- **Verapamil** (moderate CYP3A4 inhibitor)
  Model snapshot and evaluation plan (*release* **v1.0**): https://github.com/Open-Systems-Pharmacology/Verapamil-Model/releases/tag/v1.0
- **Erythromycin** (moderate CYP3A4 inhibitor)
  Model snapshot and evaluation plan (*release* **v1.0**): https://github.com/Open-Systems-Pharmacology/Erythromycin-Model/releases/tag/v1.0
- **Clarithromycin** (strong CYP 3A4 inhibitor)
  Model snapshot and evaluation plan (*release* **v1.0**): https://github.com/Open-Systems-Pharmacology/Clarithromycin-Model/releases/tag/v1.0
- **Itraconazole** including metabolites (strong CYP3A4 inhibitor)
  Model snapshot and evaluation plan (*release* **v1.1**): https://github.com/Open-Systems-Pharmacology/Itraconazole-Model/releases/tag/v1.1


The following sensitive CYP3A4 substrates as victim drugs were selected:

- **Midazolam**
  Model snapshot and evaluation plan (*release* **v1.0**): https://github.com/Open-Systems-Pharmacology/Midazolam-Model/releases/tag/v1.0
- **Triazolam**
  Model snapshot and evaluation plan (*release* **v1.0**): https://github.com/Open-Systems-Pharmacology/Triazolam-Model/releases/tag/v1.0
- **Alprazolam**
  Model snapshot and evaluation plan (*release* **v1.0**): https://github.com/Open-Systems-Pharmacology/Alprazolam-Model/releases/tag/v1.0
- **Alfentanil**
  Model snapshot and evaluation plan (*release* **v2.0**): https://github.com/Open-Systems-Pharmacology/Alfentanil-Model/releases/tag/v2.0



**Figure 1** shows the prespecified and developed DDI modeling network of interacting perpetrator and victim drugs for the OSP suite qualification of predicting CYP3A4-mediated DDI.



**Figure** **1: CYP3A4 DDI modeling network**
![DDI CYP3A4 network](images/DDI_CYP3A4_Compound_Network.png)



The published DDI studies between the respective perpetrators and victim drugs were simulated and compared to observed data. The following sections give an overview of the clinical studies being part of this qualification report. The respective data identifier (DataID) refers to the **ID** of the dataset in the [OSP PK database](https://github.com/Open-Systems-Pharmacology/Database-for-observed-data).


### Clarithromycin - Midazolam DDI
The release of the snapshot containing the respective simulations can be found here:
https://github.com/Open-Systems-Pharmacology/Clarithromycin-Midazolam-DDI/releases/tag/v1.0.

The clarithromycin-midazolam interaction was evaluated using eight clinical DDI studies quantifying the interaction following ten different dosing regimens ([Gorski 1998](#4-References), [Gurley 2006](#4-References), [Gurley 2008a](#4-References), [Markert 2013](#4-References), [Prueksaritanont 2017](#4-References), [Quinney 2008](#4-References), [van Dyk 2018](#4-References), [Yeates 1997](#4-References)).



| DataID | Enzyme | Perpetrator / victim       | Study design                                                 | Comment                                                      | Clinical study                        |
| ------ | ------ | -------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------- |
| 175    | CYP3A4 | Clarithromycin / midazolam | Clarithromycin: 500 mg po BID for 7 days<br />Midazolam: 0.05 mg/kg iv single dose, 2 hours after the 13<sup>th</sup> clarithromycin dose |                                                              | [Gorski 1998](#4-References)          |
| 173    | CYP3A4 | Clarithromycin / midazolam | Clarithromycin: 500 mg po BID for 7 days<br />Midazolam: 4 mg po single dose, 2 hours after the 13<sup>th</sup> clarithromycin dose |                                                              | [Gorski 1998](#4-References)          |
| 217    | CYP3A4 | Clarithromycin / midazolam | Clarithromycin: 500 mg po BID for 7 days<br />Midazolam: 8 mg po single dose, 2 hours after the 13<sup>th</sup> clarithromycin dose |                                                              | [Gurley 2006](#4-References)          |
| 223    | CYP3A4 | Clarithromycin / midazolam | Clarithromycin: 500 mg po BID for 7 days<br />Midazolam: 8 mg po single dose, 2 hours after the 13<sup>th</sup> clarithromycin dose |                                                              | [Gurley 2008a](#4-References)         |
| 354    | CYP3A4 | Clarithromycin / midazolam | Clarithromycin: 500 mg po BID for 4 days<br />Midazolam: 3 mg po single dose, 0.25 hours after the 7<sup>th</sup> clarithromycin dose |                                                              | [Markert 2013](#4-References)         |
| 1099   | CYP3A4 | Clarithromycin / midazolam | Clarithromycin: 500 mg po BID for 5 days<br />Midazolam: 0.01 mg po single dose, administered simultaneously with the 7<sup>th</sup> clarithromycin dose |                                                              | [Prueksaritanont 2017](#4-References) |
| 2027   | CYP3A4 | Clarithromycin / midazolam | Clarithromycin: 500 mg po BID for 7 days<br />Midazolam: 0.05 mg/kg iv single dose, 2 hours after the 13<sup>th</sup> clarithromycin dose |                                                              | [Quinney 2008](#4-References)         |
| 2030   | CYP3A4 | Clarithromycin / midazolam | Clarithromycin: 500 mg po BID for 7 days<br />Midazolam: 3.5 mg po single dose, 2 hours after the 13<sup>th</sup> clarithromycin dose |                                                              | [Quinney 2008](#4-References)         |
| 2004   | CYP3A4 | Clarithromycin / midazolam | Rifampicin: 300 mg po QD for 7 days<br />Wash-out phase for 3 days<br />Clarithromycin: 250 mg po BID for 3 days<br />Midazolam: 1 mg po single dose, 12 hours after the last rifampicin dose and again 12 hours after the last clarithromycin dose | Only assessment in Caucasian subjects simulated.<br />AUC<sub>0-6h</sub> ratio reported and simulated for comparison. | [van Dyk 2018](#4-References)         |
| 469    | CYP3A4 | Clarithromycin / midazolam | Clarithromycin: 250 mg po BID for 5 days<br />Midazolam: 15 mg po single dose, 1.5 hours after the 9<sup>th</sup> clarithromycin dose |                                                              | [Yeates 1997](#4-References)          |


### Clarithromycin - Triazolam DDI
The release of the snapshot containing the respective simulations can be found here:
https://github.com/Open-Systems-Pharmacology/Clarithromycin-Triazolam-DDI/releases/tag/v1.0

The clarithromycin-triazolam interaction was evaluated using one clinical DDI study ([Greenblatt 1998a](#4-References)).



| DataID | Enzyme | Perpetrator / victim       | Study design                                                 | Clinical study                    |
| ------ | ------ | -------------------------- | ------------------------------------------------------------ | --------------------------------- |
| 1102   | CYP3A4 | Clarithromycin / triazolam | Clarithromycin: 500 mg po twice daily at irregular time intervals for 2 days<br />Triazolam: 0.125 mg po single dose, 1 hour after the 3<sup>rd</sup> clarithromycin dose | [Greenblatt 1998a](#4-References) |


### Erythromycin - Alfentanil DDI
The release of the snapshot containing the respective simulations can be found here:
https://github.com/Open-Systems-Pharmacology/Erythromycin-Alfentanil-DDI/releases/tag/v1.0.

The erythromycin-alfentanil interaction was evaluated using one clinical DDI study ([Bartkowski 1989](#4-References)) quantifying the interaction following two different dosing regimens. Additionally, the plasma concentration-time profile of an individual investigated in this study was subsequently reported in a later study ([Bartkowski 1993](#4-References)).



| DataID | Enzyme | Perpetrator / victim      | Study design                                                 | Clinical study                   |
| ------ | ------ | ------------------------- | ------------------------------------------------------------ | -------------------------------- |
| 779    | CYP3A4 | Erythromycin / alfentanil | Erythromycin: 500 mg po single dose (enteric coated tablet containing erythromycin as free base)<br />Alfentanil: 0.05 mg/kg iv single dose, 1.5 hours after erythromycin dose | [Bartkowski 1989](#4-References) |
| 780    | CYP3A4 | Erythromycin / alfentanil | Erythromycin: 500 mg po BID for 7 days (enteric coated tablet containing erythromycin as free base)<br />Alfentanil: 0.05 mg/kg iv single dose, 1.5 hours after the 13<sup>th</sup> erythromycin dose | [Bartkowski 1989](#4-References) |



### Erythromycin - Alprazolam DDI
The release of the snapshot containing the respective simulations can be found here:
https://github.com/Open-Systems-Pharmacology/Erythromycin-Alprazolam-DDI/releases/tag/v1.0.

The erythromycin-alprazolam interaction was evaluated using one clinical DDI study ([Yasui 1996](#4-References)).



| DataID | Enzyme | Perpetrator / victim      | Study design                                                 | Clinical study              |
| ------ | ------ | ------------------------- | ------------------------------------------------------------ | --------------------------- |
| 777    | CYP3A4 | Erythromycin / alprazolam | Erythromycin: 400 mg po TID for 10 days (filmcoated tablet containing erythromycin stearate)<br />Alprazolam: 0.8 mg po single dose, 2 hours after the 22<sup>nd</sup> erythromycin dose | [Yasui 1996](#4-References) |



### Erythromycin - Midazolam DDI
The release of the snapshot containing the respective simulations can be found here:
https://github.com/Open-Systems-Pharmacology/Erythromycin-Midazolam-DDI/releases/tag/v1.0.

The erythromycin-midazolam interaction was evaluated using five clinical DDI studies quantifying the interaction following nine different dosing regimens ([Carls 2014](#4-References), [Okudaira 2007](#4-References), [Olkkola 1993](#4-References), [Swart 2002](#4-References), [Zimmermann 1996](#4-References)).



| DataID | Enzyme | Perpetrator / victim     | Study design                                                 | Comment                                                      | Clinical study                   |
| ------ | ------ | ------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | -------------------------------- |
| 828    | CYP3A4 | Erythromycin / midazolam | Erythromycin: 250 mg po single dose (filmcoated tablet containing erythromycin stearate)<br />Midazolam: 0.03 mg po single dose, 1 hour after erythromycin dose | AUC<sub>2-4h</sub> ratio reported and simulated for comparison. | [Carls 2014](#4-References)      |
| 829    | CYP3A4 | Erythromycin / midazolam | Erythromycin: 1000 mg single dose (filmcoated tablet containing erythromycin stearate)<br />Midazolam: 0.03 mg po single dose, 1 hour after erythromycin dose | AUC<sub>2-4h</sub> ratio reported and simulated for comparison. | [Carls 2014](#4-References)      |
| 362    | CYP3A4 | Erythromycin / midazolam | Erythromycin: 200 mg po four times daily for 7 days (filmcoated tablet containing erythromycin stearate)<br />Midazolam: 2.5 mg po single dose, 1 hour after the 5<sup>th</sup> erythromycin dose | Subjects received 5 mg midazolam po in control phase         | [Okudaira 2007](#4-References)   |
| 363    | CYP3A4 | Erythromycin / midazolam | Erythromycin: 200 mg po four times daily for 7 days (filmcoated tablet containing erythromycin stearate)<br />Midazolam: 2.5 mg po single dose, 1 hour after the 13<sup>th</sup> erythromycin dose | Subjects received 5 mg midazolam po in control phase         | [Okudaira 2007](#4-References)   |
| 364    | CYP3A4 | Erythromycin / midazolam | Erythromycin: 200 mg po four times daily for 7 days (filmcoated tablet containing erythromycin stearate)<br />Midazolam: 2.5 mg po single dose, 1 hour after the 25<sup>th</sup> erythromycin dose | Subjects received 5 mg midazolam po in control phase         | [Okudaira 2007](#4-References)   |
| 368    | CYP3A4 | Erythromycin / midazolam | Erythromycin: 500 mg po TID for 6 days (enteric coated tablet containing erythromycin as free base)<br />Midazolam: 0.05 mg/kg iv single dose, 2 hours after the 17<sup>th</sup> erythromycin dose |                                                              | [Olkkola 1993](#4-References)    |
| 366    | CYP3A4 | Erythromycin / midazolam | Erythromycin: 500 mg po TID for 6 days (enteric coated tablet containing erythromycin as free base)<br />Midazolam: 15 mg po single dose, 2 hours after the 17<sup>th</sup> erythromycin dose |                                                              | [Olkkola 1993](#4-References)    |
| 420    | CYP3A4 | Erythromycin / midazolam | Erythromycin: 500 mg po QID for 5 days (filmcoated tablet containing erythromycin stearate)<br />Midazolam: 0.075 mg/kg mg iv single dose, together with the 96<sup>th</sup> erythromycin dose |                                                              | [Swart 2002](#4-References)      |
| 471    | CYP3A4 | Erythromycin / midazolam | Erythromycin: 500 mg po TID for 5 days (filmcoated tablet containing erythromycin stearate)<br />Midazolam: 0.8 mg po single dose, 1.5 hours after the 13<sup>th</sup> erythromycin dose |                                                              | [Zimmermann 1996](#4-References) |


### Erythromycin - Triazolam DDI
The release of the snapshot containing the respective simulations can be found here:
https://github.com/Open-Systems-Pharmacology/Erythromycin-Triazolam-DDI/releases/tag/v1.0.

The erythromycin-triazolam interaction was evaluated using two clinical DDI studies ([Greenblatt 1998](#4-References), [Phillips 1986](#4-References)).



| DataID | Enzyme | Perpetrator / victim     | Study design                                                 | Clinical study                   |
| ------ | ------ | ------------------------ | ------------------------------------------------------------ | -------------------------------- |
| 781    | CYP3A4 | Erythromycin / triazolam | Erythromycin: 500 mg po twice daily for 2 days<br />Triazolam: 0.125 mg po single dose, 1 hour after the 3<sup>rd</sup> erythromycin dose | [Greenblatt 1998](#4-References) |
| 757    | CYP3A4 | Erythromycin / triazolam | Erythromycin: 333 mg po TID for 3 days<br />Triazolam: 0.5 mg po single dose, together with the last erythromycin dose | [Phillips 1986](#4-References)   |



### Fluvoxamine - Alprazolam DDI
The release of the snapshot containing the respective simulations can be found here:
https://github.com/Open-Systems-Pharmacology/Fluvoxamine-Alprazolam-DDI/releases/tag/v1.0.

The fluvoxamine-alprazolam interaction was evaluated using one clinical DDI study quantifying the interaction following the first dose and in steady-state ([Fleishaker 1994](#4-References)).



| DataID | Enzyme | Perpetrator / victim     | Study design                                                 | Clinical study                   |
| ------ | ------ | ------------------------ | ------------------------------------------------------------ | -------------------------------- |
| 1104   | CYP3A4 | Fluvoxamine / alprazolam | Fluvoxamine: 50 mg fluvoxamine maleate QD for 3 days, followed by 100 mg fluvoxamine maleate QD for 7 days<br />Alprazolam: 1 mg po four times daily on Day 7 starting together with the 7<sup>th</sup> fluvoxamine dose | [Fleishaker 1994](#4-References) |
| 1113   | CYP3A4 | Fluvoxamine / alprazolam | Fluvoxamine: 50 mg fluvoxamine maleate QD for 3 days, followed by 100 mg fluvoxamine maleate QD for 7 days<br />Alprazolam: 1 mg po four times daily on Days 7 - 10 starting together with the 7<sup>th</sup> fluvoxamine dose | [Fleishaker 1994](#4-References) |



### Fluvoxamine - Midazolam DDI
The release of the snapshot containing the respective simulations can be found here:
https://github.com/Open-Systems-Pharmacology/Fluvoxamine-Midazolam-DDI/releases/tag/v1.0.

The fluvoxamine / midazolam interaction was evaluated using two clinical DDI studies ([Kashuba 1998](#4-References), [Lam 2003](#4-References)).



| DataID | Enzyme | Perpetrator / victim    | Study design                                                 | Comment                                                      | Clinical study                 |
| ------ | ----------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------ | ------------------------------ |
| 2007 | CYP3A4 | Fluvoxamine / midazolam | Fluvoxamine: titrated to a daily dose of **150** mg (50 mg in the morning (6 a.m.), 50 mg in the evening (8 p.m.))<br />Midazolam: 0.025 mg/kg **iv** single dose, 3 hours after a morning fluvoxamine dose | **Observed data:**<br />Baseline (control) assessment: mean of six measures (every 2 weeks)<br />Phenotyping (fluvoxamine treatment) assessment:  mean of two measures (14 days and 28 days after the start of fluvoxamine treatment), midazolam administered at 9 a.m.<br />**Simulated**: the midazolam dose was administered 3 weeks after the start of fluvoxamine as an approximation of the two observed assessments | [Kashuba 1998](#4-References)  |
| 1089 | CYP3A4 | Fluvoxamine / midazolam | Fluvoxamine: titrated to a daily dose of **200** mg (100 mg BID)<br />Midazolam: 10 mg **po** single dose, 1 hour after a fluvoxamine steady state dose |  | [Lam 2003](#4-References) |
### Itraconazole - Alprazolam DDI
The release of the snapshot containing the respective simulations can be found here:
https://github.com/Open-Systems-Pharmacology/Itraconazole-Alprazolam-DDI/releases/tag/v1.0.

The itraconazole / alprazolam interaction was evaluated using one clinical DDI study ([Yasui 1998](#4-References)).



| DataID | Enzyme | Perpetrator / victim    | Study design                                                 | Comment                                                      | Clinical study                 |
| ------ | ----------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------ | ------------------------------ |
| 1026 | CYP3A4 | Itraconazole / alprazolam | Itraconazole: **200** mg po once daily (6 doses, capsule fasted)<br />Alprazolam: 0.8 mg **po** single dose, 1 hour after **4<sup>th</sup>** itraconazole dose |  | [Yasui 1998](#4-References) |
### Itraconazole - Midazolam DDI
The release of the snapshot containing the respective simulations can be found here:
https://github.com/Open-Systems-Pharmacology/Itraconazole-Midazolam-DDI/releases/tag/v1.0.

The itraconazole / midazolam interaction was evaluated using seven clinical DDI studies including 12 different clinical settings ([Ahonen 1995](#4-References), [Backman 1998](#4-References), [Olkkola 1994](#4-References), [Olkkola 1996](#4-References), [Prueksaritanont 2017](#4-References),  [Templeton 2010](#4-References), [Yu 2004](#4-References)).



| DataID | Enzyme | Perpetrator / victim     | Study design                                                 | Comment                                                      | Clinical study                         |
| ------ | ------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | -------------------------------------- | -------------------------------------- |
| 50 | CYP3A4 | Itraconazole / midazolam | Itraconazole: **100** mg po once daily (4 doses, capsule fasted)<br />Midazolam: 7.5 mg **po** single dose, simultaneous with **4<sup>th</sup>** itraconazole dose |                                                              | [Ahonen 1995](#4-References)          |
| 58 | CYP3A4 | Itraconazole / midazolam | Itraconazole: **200** mg po once daily (4 doses, capsule fasted)<br />Midazolam: 7.5 mg **po** single dose, 2 hours after **4<sup>th</sup>** itraconazole dose | Midazolam simulated as 15 mg for comparability to control phase, in which a 15 mg dose was given. | [Backman 1998](#4-References)         |
| 59 | CYP3A4 | Itraconazole / midazolam | Itraconazole: **200** mg po once daily (4 doses, capsule fasted)<br />Midazolam: 7.5 mg **po** single dose, **4 days** after **4<sup>th</sup>** itraconazole dose | Midazolam simulated as 15 mg for comparability to control phase, in which a 15 mg dose was given. | [Backman 1998](#4-References)         |
| 370 | CYP3A4 | Itraconazole / midazolam | Itraconazole: **200** mg po once daily (4 doses, capsule fasted)<br />Midazolam: 7.5 mg **po** single dose, 1 hours after **4<sup>th</sup>** itraconazole dose |                                                              | [Olkkola 1994](#4-References)         |
| 377 | CYP3A4 | Itraconazole / midazolam | Itraconazole: **200** mg po once daily (6 doses, capsule fasted)<br />Midazolam: 7.5 mg **po** single dose, 2 hours after **1<sup>st</sup>** itraconazole dose |                                                              | [Olkkola 1996](#4-References)         |
| 378 | CYP3A4 | Itraconazole / midazolam | Itraconazole: **200** mg po once daily (6 doses, capsule fasted)<br />Midazolam: 0.05 mg/kg **iv** single dose, 2 hours after **4<sup>th</sup>** itraconazole dose |                                                              | [Olkkola 1996](#4-References)         |
| 379 | CYP3A4 | Itraconazole / midazolam | Itraconazole: **200** mg po once daily (6 doses, capsule fasted)<br />Midazolam: 7.5 mg **po** single dose, 2 hours after **6<sup>th</sup>** itraconazole dose |                                                              | [Olkkola 1996](#4-References)         |
| 1097 | CYP3A4 | Itraconazole / midazolam | Itraconazole: **200** mg po once daily (5 doses) (solution fasted)<br />Midazolam: 10 µg **po** single dose, simultaneous with **4<sup>th</sup>** itraconazole dose |                                                              | [Prueksaritanont 2017](#4-References) |
| 424 | CYP3A4 | Itraconazole / midazolam | Itraconazole: **50** mg po **single dose** (solution fasted)<br />Midazolam: 2 mg po single dose, 4 hours after itraconazole dose |                                                              | [Templeton 2010](#4-References)       |
| 425 | CYP3A4 | Itraconazole / midazolam | Itraconazole: **100** mg po **single dose** (solution fasted)<br />Midazolam: 2 mg po **single dose**, 4 hours after itraconazole dose |                                                              | [Templeton 2010](#4-References)       |
| 426 | CYP3A4 | Itraconazole / midazolam | Itraconazole: **400** mg po **single dose** (solution fasted)<br />Midazolam: 2 mg po single dose, 4 hours after itraconazole dose |                                                              | [Templeton 2010](#4-References)       |
| 199 | CYP3A4 | Itraconazole / midazolam | Itraconazole: **200** mg po once daily (4 doses, capsule fasted)<br />Midazolam: 1 mg **iv** single dose, simultaneous with**4<sup>th</sup>** itraconazole dose | Only assessment in CYP3A5\*3/\*3 genotype subjects simulated. | [Yu 2004](#4-References) |


### Itraconazole - Triazolam DDI
The release of the snapshot containing the respective simulations can be found here:
https://github.com/Open-Systems-Pharmacology/Itraconazole-Triazolam-DDI/releases/tag/v1.0.

The itraconazole / triazolam interaction was evaluated using two clinical DDI studies including 5 different clinical settings ([Neuvonen 1996](#4-References), [Varhe 1994](#4-References)).



| DataID | Enzyme | Perpetrator / victim     | Study design                                                 | Comment                                                      | Clinical study                         |
| ------ | ------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | -------------------------------------- | -------------------------------------- |
| 1078 | CYP3A4 | Itraconazole / triazolam | Itraconazole: **200** mg po single dose (capsule fasted)<br />triazolam: 0.25 mg **po** single dose, **simultaneous** with itraconazole dose | 3 hours fasting before triazolam/itraconazole administration | [Neuvonen 1996](#4-References) |
| 1079 | CYP3A4 | Itraconazole / triazolam | Itraconazole: **200** mg po single dose (capsule fed)<br />triazolam: 0.25 mg **po** single dose, **3 hours** after itraconazole dose | itraconazole dose was taken after lunch | [Neuvonen 1996](#4-References) |
| 1080 | CYP3A4 | Itraconazole / triazolam | Itraconazole: **200** mg po single dose (capsule fed)<br />triazolam: 0.25 mg **po** single dose, **12 hours** after itraconazole dose | itraconazole dose was taken with a snack, 3 hours fasting before triazolam administration | [Neuvonen 1996](#4-References) |
| 1081 | CYP3A4 | Itraconazole / triazolam | Itraconazole: **200** mg po single dose (capsule fed)<br />triazolam: 0.25 mg **po** single dose, **24 hours** after itraconazole dose | itraconazole dose was taken with a snack, 3 hours fasting before triazolam administration | [Neuvonen 1996](#4-References) |
| 1029 | CYP3A4 | Itraconazole / triazolam | Itraconazole: **200** mg po once daily (4 doses, capsule fasted)<br />triazolam: 0.25 mg **po** single dose, 1 hour after **4<sup>th</sup>** itraconazole dose |                                                              | [Varhe 1994](#4-References) |


### Verapamil - Midazolam DDI
The release of the snapshot containing the respective simulations can be found here:
https://github.com/Open-Systems-Pharmacology/Verapamil-Midazolam-DDI/releases/tag/v1.0.

The verapamil / midazolam interaction was evaluated using two clinical DDI studies including 3 different clinical settings ([Backman 1994](#4-References), [Wang 2005](#4-References)).



| DataID | Enzyme | Perpetrator / victim     | Study design                                                 | Comment                                                      | Clinical study                         |
| ------ | ------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | -------------------------------------- | -------------------------------------- |
| 1108 | CYP3A4 | Verapamil / midazolam | Verapamil: **80** mg po three times a day (5 doses)<br />Midazolam: 15 mg **po** single dose, 1 hours after **4<sup>th</sup>** verapamil dose |                                                              | [Backman 1994](#4-References) |
| 1111 | CYP3A4 | Verapamil / midazolam | Verapamil: **240** mg po once daily (7 doses, sustained release)<br />Midazolam: 0.05 mg/kg **iv** single dose, 24 hours after the **7<sup>th</sup>** verapamil dose |         | [Wang 2005](#4-References) |
| 1116   | CYP3A4 | Verapamil / midazolam | Verapamil: **240** mg po once daily (7 doses, sustained release)<br />Midazolam: 4 mg/kg **po** single dose, 48 hours after the **7<sup>th</sup>** verapamil dose |         | [Wang 2005](#4-References) |


### Efavirenz - Alfentanil-DDI
The release of the snapshot containing the respective simulations can be found here:
https://github.com/Open-Systems-Pharmacology/Efavirenz-Alfentanil-DDI/releases/tag/v1.0.

The efavirenz-alfentanil interaction was evaluated using one clinical DDI study that includes iv and oral administration of alfentanil ([Kharasch 2012](#4-References)).



| DataID | Enzyme | Perpetrator / victim   | Study design                                                 | Comment | Clinical study                 |
| ------ | ------ | ---------------------- | ------------------------------------------------------------ | ------- | ------------------------------ |
| 801    | CYP3A4 | Efavirenz / alfentanil | Efavirenz: 600 mg po OD for 20 days<br />Alfentanil: 43 µg/kg po single dose, 1/2 hour after the 15<sup>th</sup> efavirenz dose |         | [Kharasch 2012](#4-References) |
| 803    | CYP3A4 | Efavirenz / alfentanil | Efavirenz: 600 mg po OD for 20 days<br />Alfentanil: 15 µg/kg iv single dose, 1/2 hour after the 16<sup>th</sup> efavirenz dose |         | [Kharasch 2012](#4-References) |



### Efavirenz - Midazolam DDI
The release of the snapshot containing the respective simulations can be found here:
https://github.com/Open-Systems-Pharmacology/Efavirenz-Midazolam-DDI/releases/tag/v1.0.

The efavirenz-midazolam interaction was evaluated using two clinical DDI studies, one using single dose and one using one multiple dose administration of efavirenz ([Katzenmaier 2010](#4-References), [Mikus 2017](#4-References)).



| DataID | Enzyme | Perpetrator / victim  | Study design                                                 | Comment | Clinical study                    |
| ------ | ------ | --------------------- | ------------------------------------------------------------ | ------- | --------------------------------- |
| 2041   | CYP3A4 | Efavirenz / midazolam | Efavirenz: 400 mg po OD over 14 days<br />Midazolam: 3 mg po single dose on day 14 together with efavirenz dose |         | [Katzenmaier 2010](#4-References) |
| 2044   | CYP3A4 | Efavirenz / midazolam | Efavirenz: 400 mg po SD on day 1<br />Midazolam: 4 mg po single dose, 12 hours (**day 1**) after efavirenz dose |         | [Mikus 2017](#4-References)       |
| 2045   | CYP3A4 | Efavirenz / midazolam | Efavirenz: 400 mg po SD on day 1<br />Midazolam: 2 mg iv single dose, 18 hours (**day 1**) after efavirenz dose |         | [Mikus 2017](#4-References)       |
| 2047   | CYP3A4 | Efavirenz / midazolam | Efavirenz: 400 mg po SD on day 1<br />Midazolam: 4 mg po single dose, 132 hours (**day 6**) after efavirenz dose |         | [Mikus 2017](#4-References)       |
| 2048   | CYP3A4 | Efavirenz / midazolam | Efavirenz: 400 mg po SD on day 1<br />Midazolam: 2 mg iv single dose, 138 hours (**day 6**) after efavirenz dose |         | [Mikus 2017](#4-References)       |
| 2049   | CYP3A4 | Efavirenz / midazolam | Efavirenz: 400 mg po SD on day 1<br />Midazolam: 4 mg po single dose, 252 hours (**day 11**) after efavirenz dose |         | [Mikus 2017](#4-References)       |
| 2050   | CYP3A4 | Efavirenz / midazolam | Efavirenz: 400 mg po SD on day 1<br />Midazolam: 2 mg iv single dose, 258 hours (**day 11**) after efavirenz dose |         | [Mikus 2017](#4-References)       |
| 2051   | CYP3A4 | Efavirenz / midazolam | Efavirenz: 400 mg po SD on day 1<br />Midazolam: 4 mg po single dose, 372 hours (**day 16**) after efavirenz dose |         | [Mikus 2017](#4-References)       |
| 2052   | CYP3A4 | Efavirenz / midazolam | Efavirenz: 400 mg po SD on day 1<br />Midazolam: 2 mg iv single dose, 378 hours (**day 16**) after efavirenz dose |         | [Mikus 2017](#4-References)       |
| 2053   | CYP3A4 | Efavirenz / midazolam | Efavirenz: 400 mg po SD on day 1<br />Midazolam: 4 mg po single dose, 516 hours (***day 22**) after efavirenz dose |         | [Mikus 2017](#4-References)       |
| 2054   | CYP3A4 | Efavirenz / midazolam | Efavirenz: 400 mg po SD on day 1<br />Midazolam: 2 mg iv single dose, 522 hours (**day 22**) after efavirenz dose |         | [Mikus 2017](#4-References)       |


### Rifampicin - Alfentanil DDI
The release of the snapshot containing the respective simulations can be found here:
https://github.com/Open-Systems-Pharmacology/Rifampicin-Alfentanil-DDI/releases/tag/v1.0.

The  rifampicin / alfentanil interaction was evaluated using 5 clinical DDI studies including 16 different clinical settings ([Kharasch 1997](#4-References), [Kharasch 2004](#4-References), [Kharasch 2011](#4-References), [Kharasch 2011b](#4-References), [Phimmasone 2001](#4-References)).

| DataID | Enzyme | Perpetrator / victim    | Study design                                                 | Comment                                                      | Clinical study                  |
| ------ | ------ | ----------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------- |
| 278    | CYP3A4 | Rifampicin / alfentanil | Rifampicin: **600** mg po once daily (5 doses)<br />Alfentanil: 20 µg/kg **IV** single dose, **24.5** h after **5<sup>th</sup>** rifampicin dose |                                                              | [Kharasch 1997](#4-References)   |
| 283    | CYP3A4 | Rifampicin / alfentanil | Rifampicin: **600** mg po once daily (6 doses)<br />Alfentanil: 15  µg/kg **IV** single dose, **9** h after **5<sup>th</sup>** rifampicin dose |                                                              | [Kharasch 2004](#4-References)   |
| 288    | CYP3A4 | Rifampicin / alfentanil | Rifampicin: **600** mg po once daily (6 doses)<br />Alfentanil: 60  µg/kg **PO** single dose, **9** h after **6<sup>th</sup>** rifampicin dose |                                                              | [Kharasch 2004](#4-References)   |
| 299    | CYP3A4 | Rifampicin / alfentanil | Rifampicin: **5** mg po once daily (6 doses)<br />Alfentanil: 15 µg/kg **IV** single dose, **13** h after **5<sup>th</sup>** rifampicin dose |                                                              | [Kharasch 2011](#4-References)   |
| 300    | CYP3A4 | Rifampicin / alfentanil | Rifampicin: **10** mg po once daily (6 doses)<br />Alfentanil: 15 µg/kg **IV** single dose, **13** h after **5<sup>th</sup>** rifampicin dose |                                                              | [Kharasch 2011](#4-References)   |
| 301    | CYP3A4 | Rifampicin / alfentanil | Rifampicin: **25** mg po once daily (6 doses)<br />Alfentanil: 15 µg/kg **IV** single dose, **13** h after **5<sup>th</sup>** rifampicin dose |                                                              | [Kharasch 2011](#4-References)   |
| 302    | CYP3A4 | Rifampicin / alfentanil | Rifampicin: **75** mg po once daily (6 doses)<br />Alfentanil: 15 µg/kg **IV** single dose, **13** h after **5<sup>th</sup>** rifampicin dose |                                                              | [Kharasch 2011](#4-References)   |
| 309    | CYP3A4 | Rifampicin / alfentanil | Rifampicin: **5** mg po once daily (6 doses)<br />Alfentanil: 75 µg/kg **PO** single dose, **13** h after **6<sup>th</sup>** rifampicin dose |                                                              | [Kharasch 2011](#4-References)   |
| 310    | CYP3A4 | Rifampicin / alfentanil | Rifampicin: **10** mg po once daily (6 doses)<br />Alfentanil: 75 µg/kg **PO** single dose, **13** h after **6<sup>th</sup>** rifampicin dose |                                                              | [Kharasch 2011](#4-References)   |
| 311    | CYP3A4 | Rifampicin / alfentanil | Rifampicin: **25** mg po once daily (6 doses)<br />Alfentanil: 75 µg/kg **PO** single dose, **13** h after **6<sup>th</sup>** rifampicin dose |                                                              | [Kharasch 2011](#4-References)   |
| 312    | CYP3A4 | Rifampicin / alfentanil | Rifampicin: **75** mg po once daily (6 doses)<br />Alfentanil: 75 µg/kg **PO** single dose, **13** h after **6<sup>th</sup>** rifampicin dose |                                                              | [Kharasch 2011](#4-References)   |
| 763    | CYP3A4 | Rifampicin / alfentanil | Rifampicin: **600** mg po once daily (6 doses)<br />Alfentanil: 1 mg **IV** single dose, **12** h after **5<sup>th</sup>** rifampicin dose | sequential administration of intravenous unlabeled alfentanil and oral deuterated alfentanil | [Kharasch 2011b](#4-References)  |
| 771    | CYP3A4 | Rifampicin / alfentanil | Rifampicin: **600** mg po once daily (6 doses)<br />Alfentanil: 4 mg **PO** single dose, **15** h after **5<sup>th</sup>** rifampicin dose | sequential administration of intravenous unlabeled alfentanil and oral deuterated alfentanil | [Kharasch 2011b](#4-References)  |
| 767    | CYP3A4 | Rifampicin / alfentanil | Rifampicin: **600** mg po once daily (6 doses)<br />Alfentanil: 1 mg **IV** single dose, **12** h after **6<sup>th</sup>** rifampicin dose | simultaneous administration of intravenous unlabeled alfentanil and oral deuterated alfentanil | [Kharasch 2011b](#4-References)  |
| 775    | CYP3A4 | Rifampicin / alfentanil | Rifampicin: **600** mg po once daily (6 doses)<br />Alfentanil: 4 mg **PO** single dose, **12** h after **6<sup>th</sup>** rifampicin dose | simultaneous administration of intravenous unlabeled alfentanil and oral deuterated alfentanil | [Kharasch 2011b](#4-References)  |
| 391    | CYP3A4 | Rifampicin / alfentanil | Rifampicin: **600** mg po once daily (5 doses)<br />Alfentanil: 15 µg/kg **IV** single dose, **11** h after **5<sup>th</sup>** rifampicin dose |                                                              | [Phimmasone 2001](#4-References) |

### Rifampicin - Alprazolam DDI
The release of the snapshot containing the respective simulations can be found here:
https://github.com/Open-Systems-Pharmacology/Rifampicin-Alprazolam-DDI/releases/tag/v1.0.

The rifampicin-alprazolam interaction was evaluated using two clinical DDI studies quantifying the interaction in three clinical settings ([Gashaw 2003](#4-References), [Schmider 1999](#4-References)).



| DataID | Enzyme | Perpetrator / victim    | Study design                                                 | Comments                                                     | Clinical study                 |
| ------ | ------ | ----------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------ |
| 2009   | CYP3A4 | Rifampicin / alprazolam | Rifampicin: 450 mg, five doses at irregular times intervals over 4 days<br />Alprazolam: 1 mg po single dose, 14 hours after the last rifampicin dose |                                                              | [Gashaw 2003](#4-References)   |
| 2010   | CYP3A4 | Rifampicin / alprazolam | Rifampicin: 450 mg, five doses at irregular times intervals over 4 days followed by a wash-out phase for 14 days<br />Alprazolam: 1 mg po single dose after the wash-out phase (i.e. 350 hours after the last rifampicin dose) |                                                              | [Gashaw 2003](#4-References)   |
| 1001   | CYP3A4 | Rifampicin / alprazolam | Rifampicin: 450 mg po QD for 4 days<br />Alprazolam: 1 mg po single dose, 24 hours after the last rifampicin dose | Administration time of alprazolam relative to rifampin not reported; it was assumed that alprazolam was administered 24h after the last rifampin dose | [Schmider 1999](#4-References) |



### Rifampicin - Midazolam DDI
The release of the snapshot containing the respective simulations can be found here:
https://github.com/Open-Systems-Pharmacology/Rifampicin-Midazolam-DDI/releases/tag/v1.0.

The  rifampicin / midazolam interaction was evaluated using 21 clinical DDI studies including 35 different clinical settings ([Backman 1996](#4-References), [Backman 1998](#4-References), [Chung 2006](#4-References), [Eap 2004](#4-References), [Gorski 2003](#4-References), [Gurley 2006](#4-References), [Gurley 2008a](#4-References), [Kharasch 1997](#4-References), [Kharasch 2004](#4-References), [Kharasch 2011](#4-References), [Kim 2018](#4-References), [Link 2008](#4-References), [Phimmasone 2001](#4-References), [Prueksaritanont 2017](#4-References), [Reitman 2011](#4-References), [Shin 2013](#4-References), [Shin 2016](#4-References), [Szalat 2007](#4-References), [van Dyk 2018](#4-References), [Wiesinger 2011](#4-References), [Yu 2004](#4-References)).

In the study by [Eap 2004](#4-References), the induction of CYP3A4 by rifampicin was evaluated using first 0.075 mg and one day later 7.5 and orally administered midazolam. The magnitude of the DDI with the low dose was much lower than for the higher dose (AUC ratio 0.44 vs. 0.09), which can actually only be explained by issues with the limit of detection after induction for the small midazolam dose considering the entire set of observed data. Therefore, as well as in [Almond 2016](#4-References), the dataset of the low dose setting was excluded from this analysis.



| DataID | Enzyme | Perpetrator / victim   | Study design                                                 | Comment                                                      | Clinical study                       |
| ------ | ------ | ---------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------ |
| 54     | CYP3A4 | Rifampicin / midazolam | Rifampicin: **600** mg po once daily (5 doses)<br />Midazolam: 15 mg **PO** single dose, **17** h after **5<sup>th</sup>** rifampicin dose |                                                              | [Backman 1996](#4-References)         |
| 56     | CYP3A4 | Rifampicin / midazolam | Rifampicin: **600** mg po once daily (5 doses)<br />Midazolam: 15 mg **PO** single dose, **17** h after **5<sup>th</sup>** rifampicin dose (Phase IV) |                                                              | [Backman 1998](#4-References)         |
| 57     | CYP3A4 | Rifampicin / midazolam | Rifampicin: **600** mg po once daily (5 doses)<br />Midazolam: 15 mg **PO** single dose, **7 days** after **5<sup>th</sup>** rifampicin dose (Phase V) |                                                              | [Backman 1998](#4-References)         |
| 113    | CYP3A4 | Rifampicin / midazolam | Rifampicin: **600** mg po once daily (9 doses)<br />Midazolam: 0.075 mg/kg **PO** single dose, **22** h after **7<sup>th</sup>** rifampicin dose |                                                              | [Chung 2006](#4-References)           |
| 129    | CYP3A4 | Rifampicin / midazolam | Rifampicin: **450** mg po once daily (5 doses)<br />Midazolam: 0.075 mg **PO** single dose, **18** h after **4<sup>th</sup>** rifampicin dose | Dataset excluded (see comment above) | [Eap 2004](#4-References)             |
| 132    | CYP3A4 | Rifampicin / midazolam | Rifampicin: **450** mg po once daily (5 doses)<br />Midazolam: 7.5 mg **PO** single dose, **18** h after **5<sup>th</sup>** rifampicin dose |                                                              | [Eap 2004](#4-References)             |
| 179    | CYP3A4 | Rifampicin / midazolam | Rifampicin: **600** mg po once daily (7 doses)<br />Midazolam: 0.05 mg/kg **IV** single dose, **12** h after **6<sup>th</sup>** rifampicin dose |                                                              | [Gorski 2003](#4-References)          |
| 177    | CYP3A4 | Rifampicin / midazolam | Rifampicin: **600** mg po once daily (7 doses)<br />Midazolam: 6 mg **PO** single dose, **12** h after **6<sup>th</sup>** rifampicin dose | Subjects received a 4 mg midazolam dose in control phase.    | [Gorski 2003](#4-References)          |
| 215    | CYP3A4 | Rifampicin / midazolam | Rifampicin: **300** mg po twice daily (14 doses, 7 days)<br />Midazolam: 8 mg **PO** single dose, **2** h after **13<sup>th</sup>** rifampicin dose |                                                              | [Gurley 2006](#4-References)          |
| 221    | CYP3A4 | Rifampicin / midazolam | Rifampicin: **300** mg po twice daily (14 doses, 7 days)<br />Midazolam: 8 mg **PO** single dose, **2** h after **13<sup>th</sup>** rifampicin dose |                                                              | [Gurley 2008a](#4-References)         |
| 276    | CYP3A4 | Rifampicin / midazolam | Rifampicin: **600** mg po once daily (5 doses)<br />Midazolam: 1 mg **IV** single dose, **24** h after **5<sup>th</sup>** rifampicin dose |                                                              | [Kharasch 1997](#4-References)        |
| 280    | CYP3A4 | Rifampicin / midazolam | Rifampicin: **600** mg po once daily (6 doses)<br />Midazolam: 1 mg **IV** single dose, **8** h after **5<sup>th</sup>** rifampicin dose |                                                              | [Kharasch 2004](#4-References)        |
| 286    | CYP3A4 | Rifampicin / midazolam | Rifampicin: **600** mg po once daily (6 doses)<br />Midazolam: 3 mg **PO** single dose, **8** h after **6<sup>th</sup>** rifampicin dose |                                                              | [Kharasch 2004](#4-References)        |
| 294    | CYP3A4 | Rifampicin / midazolam | Rifampicin: **5** mg po once daily (6 doses)<br />Midazolam: 1 mg **IV** single dose, **12** h after **5<sup>th</sup>** rifampicin dose |                                                              | [Kharasch 2011](#4-References)        |
| 295    | CYP3A4 | Rifampicin / midazolam | Rifampicin: **10** mg po once daily (6 doses)<br />Midazolam: 1 mg **IV** single dose, **12** h after **5<sup>th</sup>** rifampicin dose |                                                              | [Kharasch 2011](#4-References)        |
| 296    | CYP3A4 | Rifampicin / midazolam | Rifampicin: **25** mg po once daily (6 doses)<br />Midazolam: 1 mg **IV** single dose, **12** h after **5<sup>th</sup>** rifampicin dose |                                                              | [Kharasch 2011](#4-References)        |
| 297    | CYP3A4 | Rifampicin / midazolam | Rifampicin: **75** mg po once daily (6 doses)<br />Midazolam: 1 mg **IV** single dose, **12** h after **5<sup>th</sup>** rifampicin dose |                                                              | [Kharasch 2011](#4-References)        |
| 304    | CYP3A4 | Rifampicin / midazolam | Rifampicin: **5** mg po once daily (6 doses)<br />Midazolam: 3 mg **PO** single dose, **12** h after **6<sup>th</sup>** rifampicin dose |                                                              | [Kharasch 2011](#4-References)        |
| 305    | CYP3A4 | Rifampicin / midazolam | Rifampicin: **10** mg po once daily (6 doses)<br />Midazolam: 3 mg **PO** single dose, **12** h after **6<sup>th</sup>** rifampicin dose |                                                              | [Kharasch 2011](#4-References)        |
| 306    | CYP3A4 | Rifampicin / midazolam | Rifampicin: **25** mg po once daily (6 doses)<br />Midazolam: 3 mg **PO** single dose, **12** h after **6<sup>th</sup>** rifampicin dose |                                                              | [Kharasch 2011](#4-References)        |
| 307    | CYP3A4 | Rifampicin / midazolam | Rifampicin: **75** mg po once daily (6 doses)<br />Midazolam: 3 mg **PO** single dose, **12** h after **6<sup>th</sup>** rifampicin dose |                                                              | [Kharasch 2011](#4-References)        |
| 2036   | CYP3A4 | Rifampicin / midazolam | Rifampicin: **600** mg po once daily (10 doses)<br  />Midazolam: 2.5 mg **IV** single dose, **simultaneous** with **10<sup>th</sup>**  rifampicin dose | Only assessment in male subjects simulated.<br />Subjects received a 1 mg midazolam dose in control phase. Observed reported dose-normalized AUCR back-calculated to non dose-normalized AUCR. | [Kim 2018](#4-References)             |
| 342    | CYP3A4 | Rifampicin / midazolam | Rifampicin: **600** mg po once daily (6 doses)<br />Midazolam: 2 mg **IV** single dose, **24** h after **6<sup>th</sup>** rifampicin dose |                                                              | [Link 2008](#4-References)            |
| 344    | CYP3A4 | Rifampicin / midazolam | Rifampicin: **600** mg po once daily (6 doses)<br />Midazolam: 7.5 mg  **PO** single dose, **24** h after **6<sup>th</sup>** rifampicin dose |                                                              | [Link 2008](#4-References)            |
| 389    | CYP3A4 | Rifampicin / midazolam | Rifampicin: **600** mg po once daily (5 doses)<br />Midazolam: 1 mg **IV** single dose, **10** h after **5<sup>th</sup>** rifampicin dose |                                                              | [Phimmasone 2001](#4-References)      |
| 1098   | CYP3A4 | Rifampicin / midazolam | Rifampicin: **600** mg po SD<br />Midazolam: 10 µg  **PO** single dose, **simultaneous** with rifampicin dose |                                                              | [Prueksaritanont 2017](#4-References) |
| 392    | CYP3A4 | Rifampicin / midazolam | Rifampicin: **600** mg po once daily (4 weeks)<br />Midazolam: 2 mg **PO**  single dose, **simultaneous** with **28<sup>th</sup>** rifampicin dose | PK data of midazolam admintsered 28 days after the last rifampicin dose served as *control* (reference) | [Reitman 2011](#4-References)         |
| 393    | CYP3A4 | Rifampicin / midazolam | Rifampicin: **600** mg po once daily (4 weeks)<br />Midazolam: 2 mg **PO** single dose, **7 days** after **28<sup>th</sup>** rifampicin dose | PK data of midazolam admintsered 28 days after the last rifampicin dose served as *control* (reference) | [Reitman 2011](#4-References)         |
| 394    | CYP3A4 | Rifampicin / midazolam | Rifampicin: **600** mg po once daily (4 weeks)<br />Midazolam: 2 mg **PO** single dose, **14 days** after **28<sup>th</sup>** rifampicin dose | PK data of midazolam admintsered 28 days after the last rifampicin dose served as *control* (reference) | [Reitman 2011](#4-References)         |
| 1092   | CYP3A4 | Rifampicin / midazolam | Rifampicin: **600** mg po once daily (10 doses)<br  />Midazolam: 2.5 mg **IV** single dose, **simultaneous** h with **10<sup>th</sup>**  rifampicin dose | Subjects received a 1 mg midazolam dose in control phase. Observed reported dose-normalized AUCR back-calculated to non dose-normalized AUCR. | [Shin 2013](#4-References)            |
| 1095   | CYP3A4 | Rifampicin / midazolam | Rifampicin: **600** mg po once daily (10 doses)<br  />Midazolam: 2.5 mg **IV** single dose, **simultaneous** h with **10<sup>th</sup>**  rifampicin dose | Subjects received a 1 mg midazolam dose in control phase. Observed reported dose-normalized AUCR back-calculated to non dose-normalized AUCR. | [Shin 2016](#4-References)            |
| 422    | CYP3A4 | Rifampicin / midazolam | Rifampicin: **600** mg po once daily (7 doses)<br />Midazolam: 0.05 mg/kg **IV** single dose, **12** h after **12<sup>th</sup>** rifampicin dose |                                                              | [Szalat 2007](#4-References)          |
| 2002   | CYP3A4 | Rifampicin / midazolam | Rifampicin: **300** mg po once daily (7 doses)<br />Midazolam: 1 mg **PO** single dose, **12** h after **7<sup>th</sup>** rifampicin dose | Only assessment in Caucasian subjects simulated.<br />AUC<sub>0-6h</sub> ratio reported and simulated for comparison. | [van Dyk 2018](#4-References)         |
| 204 | CYP3A4 | Rifampicin / midazolam | Rifampicin: **10** mg po once daily (11 doses)<br />Midazolam: 1 mg **PO** single dose, **12** h after **8<sup>th</sup>** rifampicin dose | In the study midazolam was coadministered with either etonogestrel, dienogest, drospirenone, levonorgestrel or norethindrone. | [Wiesinger 2020](#4-References) |
| 205 | CYP3A4 | Rifampicin / midazolam | Rifampicin: 11 doses of **10** mg po once daily, followed by 11 doses of **600** mg po once daily<br />Midazolam: 1 mg **PO** single dose, **12** h after **8<sup>th</sup>** 600 mg rifampicin dose (after the 19<sup>th</sup> overall rifampicin dose) | In the study midazolam was coadministered with either etonogestrel, dienogest, drospirenone, levonorgestrel or norethindrone. | [Wiesinger 2020](#4-References) |
| 202    | CYP3A4 | Rifampicin / midazolam | Rifampicin: **600** mg po once daily (10 doses)<br />Midazolam: 2 mg **IV** single dose, **24** h after **10<sup>th</sup>** rifampicin dose | Only assessment in CYP3A5\*3/\*3 genotype subjects simulated.<br />Subjects received a 1 mg midazolam dose in control phase. Observed reported dose-normalized AUCR back-calculated to non dose-normalized AUCR. | [Yu 2004](#4-References)              |
### Rifampicin - Triazolam DDI
The release of the snapshot containing the respective simulations can be found here:
https://github.com/Open-Systems-Pharmacology/Rifampicin-Triazolam-DDI/releases/tag/v1.0.

The rifampicin-triazolam interaction was evaluated using one clinical DDI study ([Villikka 1997](#4-References)).



| DataID | Enzyme | Perpetrator / victim   | Study design                                                 | Comments | Clinical study                 |
| ------ | ------ | ---------------------- | ------------------------------------------------------------ | -------- | ------------------------------ |
| 1004   | CYP3A4 | Rifampicin / triazolam | Rifampicin: 600 mg QD for 5 days<br />Triazolam: 0.5 mg po single dose, 17 hours after the last rifampicin dose |          | [Villikka 1997](#4-References) |



# 2 Qualification of Use Case CYP3A4-mediated DDI
The following section shows the correlations between observed and model-predicted AUC and C<sub>max</sub> ratios, respectively.

Specifically, the PBPK model performance for the PK parameters **AUC ratio (AUCR)** and **C<sub>max</sub> ratio (CMAXR)** is assessed via:

- predicted (*Pred*) vs. observed (*Obs*) plots

- *Pred*/*Obs* vs. *Obs* plots

- geometric mean fold error (GMFE):
  
  ![GMFE equation](images/GFME_equation.PNG)
  
- number of AUCR and CMAXR falling within 2-fold error range and within the limits as suggested by [Guest et al. 2011](#4-References)
  
- detailed table of results for each study

  

In the plots,

- the dotted lines denote 0.50–2.00 (2-fold) criterion,

- the solid lines denote the limits as suggested by [Guest et al. 2011](#4-References),

- the bold solid line denotes the unity line,

- each color represents one combination of drugs,

- squares represent studies with intravenous administration of the victim drug and circles represent studies with oral administration of the victim drug.



***


![001_plotDDIRatioAUCPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/001_plotDDIRatioAUCPredictedVsObserved.png)

![002_plotDDIRatioAUCResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/002_plotDDIRatioAUCResidualsVsObserved.png)

![003_plotDDIRatioCMAXPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/003_plotDDIRatioCMAXPredictedVsObserved.png)

![004_plotDDIRatioCMAXResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/004_plotDDIRatioCMAXResidualsVsObserved.png)

GMFE (AUC) = 1.398739 

GMFE (CMAX) = 1.370621 

|AUC                       |Number|Ratio [%]|
|-------------------------:|-----:|--------:|
|Points total              |118   |-        |
|Points within Guest et al.|88    |74.5763  |
|Points within 2-fold      |102   |86.4407  |

|CMAX                      |Number|Ratio [%]|
|-------------------------:|-----:|--------:|
|Points total              |76    |-        |
|Points within Guest et al.|43    |56.5789  |
|Points within 2-fold      |70    |92.1053  |

|DataID|Perpetrator                                                                                                                                                                                                                       |Victim        |Predicted AUC Ratio|Observed AUC Ratio|Pred/Obs AUC Ratio|Predicted CMAX Ratio|Observed CMAX Ratio|Pred/Obs CMAX Ratio|Reference           |
|-----:|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------:|-------------:|------------------:|-----------------:|-----------------:|-------------------:|------------------:|------------------:|-------------------:|
|175   |Clarithromycin, 500 mg, PO, MD BID (7 days)                                                                                                                                                                                       |Midazolam, IV |3.0681             |2.6667            |1.1506            |1.2413              |-                  |-                  |Gorski 1998         |
|2027  |Clarithromycin, 500 mg, PO, MD BID (7 days)                                                                                                                                                                                       |Midazolam, IV |3.024              |3.2               |0.94501           |1.2413              |1.1724             |1.0587             |Quinney 2008        |
|173   |Clarithromycin, 500 mg, PO, MD BID (7 days)                                                                                                                                                                                       |Midazolam, PO |9.241              |7.1429            |1.2937            |3.0765              |-                  |-                  |Gorski 1998         |
|217   |Clarithromycin, 500 mg, PO, MD BID (7 days)                                                                                                                                                                                       |Midazolam, PO |7.8536             |8.3929            |0.93575           |2.7414              |3.7956             |0.72225            |Gurley 2006         |
|223   |Clarithromycin, 500 mg, PO, MD BID (7 days)                                                                                                                                                                                       |Midazolam, PO |7.6974             |5.4834            |1.4038            |2.7414              |2.1743             |1.2608             |Gurley 2008a        |
|354   |Clarithromycin, 500 mg, PO, MD BID (4 days)                                                                                                                                                                                       |Midazolam, PO |5.871              |5.5556            |1.0568            |2.6201              |-                  |-                  |Markert 2013        |
|1099  |Clarithromycin, 500 mg, PO, MD BID (5 days)                                                                                                                                                                                       |Midazolam, PO |7.8476             |4.84              |1.6214            |3.177               |2.69               |1.181              |Prueksaritanont 2017|
|2030  |Clarithromycin, 500 mg, PO, MD BID (7 days)                                                                                                                                                                                       |Midazolam, PO |9.0373             |8                 |1.1297            |3.1442              |2.75               |1.1433             |Quinney 2008        |
|2004  |Clarithromycin, 250 mg, PO, MD BID (3 days)                                                                                                                                                                                       |Midazolam, PO |1.4904             |1.9               |0.78442           |1.2571              |1.75               |0.71833            |van Dyk 2018        |
|469   |Clarithromycin, 250 mg, PO, MD BID (5 days)                                                                                                                                                                                       |Midazolam, PO |2.3757             |3.5716            |0.66518           |1.5939              |2.44               |0.65325            |Yeates 1996         |
|1102  |Clarithromycin, 500 mg, PO, MD OD (2 days)                                                                                                                                                                                        |Triazolam, PO |3.5766             |5.06              |0.70684           |2.0063              |1.968              |1.0194             |Greenblatt 1998a    |
|779   |Erythromycin, 500 mg, PO, SD                                                                                                                                                                                                      |Alfentanil, IV|1.0294             |1.0262            |1.0031            |1                   |-                  |-                  |Bartkowski 1989     |
|780   |Erythromycin, 500 mg, PO, MD BID (6 days)                                                                                                                                                                                         |Alfentanil, IV|1.6891             |1.4611            |1.1561            |1.0269              |-                  |-                  |Bartkowski 1989     |
|777   |Erythromycin, 400 mg, PO, MD TID (10 days)                                                                                                                                                                                        |Alprazolam, PO|1.7608             |2.4716            |0.71239           |1.0766              |1.1833             |0.90984            |Yasui 1996          |
|781   |Erythromycin, 500 mg, PO, MD OD (2 days)                                                                                                                                                                                          |Triazolam, PO |3.1373             |3.65              |0.85953           |1.8985              |1.768              |1.0738             |Greenblatt 1998a    |
|757   |Erythromycin, 333 mg, PO, MD TID (3 days)                                                                                                                                                                                         |Triazolam, PO |3.8729             |2.0597            |1.8803            |2.109               |1.4643             |1.4403             |Phillips 1986       |
|420   |Erythromycin, 500 mg, PO, MD QID (5 days)                                                                                                                                                                                         |Midazolam, IV |2.2865             |1.5978            |1.431             |1.027               |-                  |-                  |Swart 2002          |
|368   |Erythromycin, 500 mg, PO, MD TID (7 days)                                                                                                                                                                                         |Midazolam, IV |2.0362             |1.9619            |1.0379            |1.0191              |-                  |-                  |Olkkola 1993        |
|366   |Erythromycin, 500 mg, PO, MD TID (7 days)                                                                                                                                                                                         |Midazolam, PO |3.8438             |4.0674            |0.94501           |1.8908              |2.7                |0.70029            |Olkkola 1993        |
|471   |Erythromycin, 500 mg, PO, MD TID (3 days)                                                                                                                                                                                         |Midazolam, PO |4.8518             |3.8137            |1.2722            |2.205               |2.7114             |0.81322            |Zimmermann 1996     |
|362   |Erythromycin, 200 mg, PO, MD QID (2 days)                                                                                                                                                                                         |Midazolam, PO |1.2849             |1.16              |1.1077            |0.82212             |0.90909            |0.90434            |Okudaira 2007       |
|363   |Erythromycin, 200 mg, PO, MD QID (4 days)                                                                                                                                                                                         |Midazolam, PO |1.6208             |1.69              |0.95905           |0.92675             |1.2                |0.77229            |Okudaira 2007       |
|364   |Erythromycin, 200 mg, PO, MD QID (7 days)                                                                                                                                                                                         |Midazolam, PO |1.7031             |1.69              |1.0077            |0.94964             |1.1727             |0.80977            |Okudaira 2007       |
|828   |Erythromycin, 250 mg, PO, SD                                                                                                                                                                                                      |Midazolam, PO |3.5056             |1.7178            |2.0407            |3.2106              |-                  |-                  |Carls 2014          |
|829   |Erythromycin, 1000 mg, PO, SD                                                                                                                                                                                                     |Midazolam, PO |4.0618             |4.9912            |0.8138            |3.6258              |-                  |-                  |Carls 2014          |
|1104  |Fluvoxamine, 50/100 mg, PO, MD OD (10 days), 50 mg day 1-3, then 100 mg                                                                                                                                                           |Alprazolam, PO|1.006              |1.2551            |0.80147           |1.005               |1.1769             |0.85396            |Fleishaker 1994     |
|1113  |Fluvoxamine, 50/100 mg, PO, MD OD (10 days), 50 mg day 1-3, then 100 mg                                                                                                                                                           |Alprazolam, PO|1.025              |1.9631            |0.52212           |1.022               |1.8619             |0.54891            |Fleishaker 1994     |
|2007  |Fluvoxamine, 50/100 mg, PO, MD BID (4 weeks), dose titration to 150 mg/day over 7 days: 50 mg in the evening for 3 days, 50 mg in the morning and evening for the next 3 days, then 50 mg in the morning and 100 mg in the evening|Midazolam, IV |0.90009            |1.5               |0.60006           |0.24742             |-                  |-                  |Kashuba 1998        |
|1089  |Fluvoxamine, 50/100 mg, PO, MD OD (12 days), titrated from 50 mg BID to 100 mg BID administered for 6 days                                                                                                                        |Midazolam, PO |1.3882             |1.66              |0.83627           |1.2013              |1.63               |0.73701            |Lam 2003            |
|1026  |Itraconazole, 200 mg, PO, MD OD (6 days)                                                                                                                                                                                          |Alprazolam, PO|2.1755             |2.6627            |0.81702           |1.0999              |1.2868             |0.85474            |Yasui 1998          |
|378   |Itraconazole, 200 mg, PO, MD OD (4 days)                                                                                                                                                                                          |Midazolam, IV |2.2908             |3.2258            |0.71016           |1.0117              |-                  |-                  |Olkkola 1996        |
|199   |Itraconazole, 200 mg, PO, MD OD (4 days)                                                                                                                                                                                          |Midazolam, IV |2.4587             |3.3333            |0.73761           |1.0112              |-                  |-                  |Yu 2004             |
|50    |Itraconazole, 100 mg, PO, MD OD (4 days)                                                                                                                                                                                          |Midazolam, PO |3.4762             |5.7451            |0.60507           |1.9613              |2.5588             |0.7665             |Ahonen 1995         |
|58    |Itraconazole, 200 mg, PO, MD OD (4 days)                                                                                                                                                                                          |Midazolam, PO |4.8857             |7.97              |0.61301           |2.2277              |3.12               |0.71402            |Backman 1998        |
|59    |Itraconazole, 200 mg, PO, MD OD (4 days)                                                                                                                                                                                          |Midazolam, PO |1.1226             |2.63              |0.42685           |1.074               |1.92               |0.55939            |Backman 1998        |
|370   |Itraconazole, 200 mg, PO, MD OD (4 days)                                                                                                                                                                                          |Midazolam, PO |5.2845             |10.8              |0.48931           |2.2377              |3.4                |0.65813            |Olkkola 1994        |
|377   |Itraconazole, 200 mg, PO, SD                                                                                                                                                                                                      |Midazolam, PO |4.4916             |3.4               |1.3211            |2.1997              |1.8                |1.222              |Olkkola 1996        |
|379   |Itraconazole, 200 mg, PO, MD OD (6 days)                                                                                                                                                                                          |Midazolam, PO |6.244              |6.6               |0.94606           |2.5665              |2.5                |1.0266             |Olkkola 1996        |
|1097  |Itraconazole, 200 mg, PO, MD OD (5 days)                                                                                                                                                                                          |Midazolam, PO |19.4647            |7.04              |2.7649            |4.6651              |3.71               |1.2575             |Prueksaritanont 2017|
|424   |Itraconazole, 50 mg, PO, SD                                                                                                                                                                                                       |Midazolam, PO |3.2463             |2                 |1.6232            |2.2008              |-                  |-                  |Templeton 2010      |
|425   |Itraconazole, 200 mg, PO, SD                                                                                                                                                                                                      |Midazolam, PO |7.5749             |4.7               |1.6117            |3.4395              |-                  |-                  |Templeton 2010      |
|426   |Itraconazole, 400 mg, PO, SD                                                                                                                                                                                                      |Midazolam, PO |9.718              |5.4               |1.7996            |3.7303              |-                  |-                  |Templeton 2010      |
|1078  |Itraconazole, 200 mg, PO, SD                                                                                                                                                                                                      |Triazolam, PO |4.2543             |3.11              |1.3679            |1.9806              |1.41               |1.4047             |Neuvonen 1996       |
|1079  |Itraconazole, 200 mg, PO, SD                                                                                                                                                                                                      |Triazolam, PO |5.6094             |4.79              |1.1711            |2.4221              |1.76               |1.3762             |Neuvonen 1996       |
|1080  |Itraconazole, 200 mg, PO, SD                                                                                                                                                                                                      |Triazolam, PO |2.2531             |4.63              |0.48663           |1.6677              |1.76               |0.94754            |Neuvonen 1996       |
|1081  |Itraconazole, 200 mg, PO, SD                                                                                                                                                                                                      |Triazolam, PO |2.0999             |3.82              |0.54971           |1.3848              |1.71               |0.80984            |Neuvonen 1996       |
|1029  |Itraconazole, 200 mg, PO, MD OD (4 days)                                                                                                                                                                                          |Triazolam, PO |6.3835             |19.0287           |0.33547           |2.5312              |2.6854             |0.94257            |Varhe 1994          |
|1111  |Verapamil, 240 mg, PO, MD OD (7 days)                                                                                                                                                                                             |Midazolam, IV |1.4026             |1.4524            |0.96572           |1.1019              |-                  |-                  |Wang 2005           |
|1108  |Verapamil, 80 mg, PO, MD TID (2 days)                                                                                                                                                                                             |Midazolam, PO |2.0133             |2.9167            |0.69028           |1.4415              |1.9692             |0.732              |Backman 1994        |
|1116  |Verapamil, 240 mg, PO, MD OD (7 days)                                                                                                                                                                                             |Midazolam, PO |1.6228             |3.5056            |0.46293           |1.3474              |-                  |-                  |Wang 2005           |
|803   |Efavirenz, 600 mg, PO, MD OD (19 days)                                                                                                                                                                                            |Alfentanil, IV|0.56016            |0.54              |1.0373            |0.92176             |1.0978             |0.83962            |Kharasch 2012       |
|801   |Efavirenz, 600 mg, PO, MD OD (19 days)                                                                                                                                                                                            |Alfentanil, PO|0.23512            |0.22              |1.0687            |0.35697             |0.42857            |0.83293            |Kharasch 2012       |
|2045  |Efavirenz, 400 mg, PO, SD                                                                                                                                                                                                         |Midazolam, IV |0.83147            |0.78538           |1.0587            |0.93223             |-                  |-                  |Mikus 2017          |
|2048  |Efavirenz, 400 mg, PO, SD                                                                                                                                                                                                         |Midazolam, IV |0.78703            |0.77712           |1.0127            |0.91054             |-                  |-                  |Mikus 2017          |
|2050  |Efavirenz, 400 mg, PO, SD                                                                                                                                                                                                         |Midazolam, IV |0.85818            |0.9375            |0.9154            |0.94266             |-                  |-                  |Mikus 2017          |
|2052  |Efavirenz, 400 mg, PO, SD                                                                                                                                                                                                         |Midazolam, IV |0.91246            |0.85377           |1.0687            |0.96565             |-                  |-                  |Mikus 2017          |
|2054  |Efavirenz, 400 mg, PO, SD                                                                                                                                                                                                         |Midazolam, IV |0.94941            |0.92217           |1.0295            |0.9806              |-                  |-                  |Mikus 2017          |
|2041  |Efavirenz, 400 mg, PO, MD OD (14 days)                                                                                                                                                                                            |Midazolam, PO |0.11468            |0.1027            |1.1167            |0.23823             |0.1806             |1.3191             |Katzenmaier 2010    |
|2044  |Efavirenz, 400 mg, PO, SD                                                                                                                                                                                                         |Midazolam, PO |0.52615            |0.59055           |0.89095           |0.64634             |-                  |-                  |Mikus 2017          |
|2047  |Efavirenz, 400 mg, PO, SD                                                                                                                                                                                                         |Midazolam, PO |0.54604            |0.61417           |0.88907           |0.63889             |-                  |-                  |Mikus 2017          |
|2049  |Efavirenz, 400 mg, PO, SD                                                                                                                                                                                                         |Midazolam, PO |0.70578            |0.76968           |0.91697           |0.77859             |-                  |-                  |Mikus 2017          |
|2051  |Efavirenz, 400 mg, PO, SD                                                                                                                                                                                                         |Midazolam, PO |0.82               |0.74803           |1.0962            |0.86911             |-                  |-                  |Mikus 2017          |
|2053  |Efavirenz, 400 mg, PO, SD                                                                                                                                                                                                         |Midazolam, PO |0.89691            |0.83661           |1.0721            |0.92649             |-                  |-                  |Mikus 2017          |
|278   |Rifampicin, 600 mg, PO, MD OD (5 days)                                                                                                                                                                                            |Alfentanil, IV|0.35994            |0.36301           |0.99152           |0.89694             |-                  |-                  |Kharasch 1997       |
|283   |Rifampicin, 600 mg, PO, MD OD (6 days)                                                                                                                                                                                            |Alfentanil, IV|0.48775            |0.375             |1.3007            |1.2012              |1.0033             |1.1972             |Kharasch 2004       |
|299   |Rifampicin, 5 mg, PO, MD OD (6 days)                                                                                                                                                                                              |Alfentanil, IV|0.98467            |0.83              |1.1863            |1.3091              |1.0392             |1.2597             |Kharasch 2011       |
|300   |Rifampicin, 10 mg, PO, MD OD (6 days)                                                                                                                                                                                             |Alfentanil, IV|0.8489             |0.75              |1.1319            |1.2935              |1.049              |1.233              |Kharasch 2011       |
|301   |Rifampicin, 25 mg, PO, MD OD (6 days)                                                                                                                                                                                             |Alfentanil, IV|0.69485            |0.59              |1.1777            |1.2671              |1                  |1.2671             |Kharasch 2011       |
|302   |Rifampicin, 75 mg, PO, MD OD (6 days)                                                                                                                                                                                             |Alfentanil, IV|0.57591            |0.51              |1.1292            |1.2354              |1.0294             |1.2001             |Kharasch 2011       |
|763   |Rifampicin, 600 mg, PO, MD OD (6 days)                                                                                                                                                                                            |Alfentanil, IV|0.36165            |0.4               |0.90412           |0.89854             |-                  |-                  |Kharasch 2011b      |
|767   |Rifampicin, 600 mg, PO, MD OD (6 days)                                                                                                                                                                                            |Alfentanil, IV|0.35775            |0.4               |0.89439           |0.89637             |-                  |-                  |Kharasch 2011b      |
|391   |Rifampicin, 600 mg, PO, MD OD (5 days)                                                                                                                                                                                            |Alfentanil, IV|0.36297            |0.55              |0.65994           |0.89919             |-                  |-                  |Phimmasone 2001     |
|288   |Rifampicin, 600 mg, PO, MD OD (6 days)                                                                                                                                                                                            |Alfentanil, PO|0.038957           |0.045631          |0.85373           |0.087               |0.11111            |0.783              |Kharasch 2004       |
|309   |Rifampicin, 5 mg, PO, MD OD (6 days)                                                                                                                                                                                              |Alfentanil, PO|0.46082            |0.74              |0.62272           |0.59606             |0.86275            |0.69088            |Kharasch 2011       |
|310   |Rifampicin, 10 mg, PO, MD OD (6 days)                                                                                                                                                                                             |Alfentanil, PO|0.32444            |0.61              |0.53188           |0.46881             |0.86275            |0.5434             |Kharasch 2011       |
|311   |Rifampicin, 25 mg, PO, MD OD (6 days)                                                                                                                                                                                             |Alfentanil, PO|0.18757            |0.3               |0.62522           |0.31358             |0.4902             |0.63971            |Kharasch 2011       |
|312   |Rifampicin, 75 mg, PO, MD OD (6 days)                                                                                                                                                                                             |Alfentanil, PO|0.095562           |0.13              |0.73509           |0.18365             |0.2549             |0.72046            |Kharasch 2011       |
|771   |Rifampicin, 600 mg, PO, MD OD (6 days)                                                                                                                                                                                            |Alfentanil, PO|0.037884           |0.06              |0.6314            |0.083994            |-                  |-                  |Kharasch 2011b      |
|775   |Rifampicin, 600 mg, PO, MD OD (6 days)                                                                                                                                                                                            |Alfentanil, PO|0.037011           |0.06              |0.61684           |0.082592            |-                  |-                  |Kharasch 2011b      |
|2009  |Rifampicin, 450 mg, PO, MD, q.d. for 5 days                                                                                                                                                                                       |Alprazolam, PO|0.18831            |0.17935           |1.05              |0.67772             |-                  |-                  |Gashaw 2003         |
|2010  |Rifampicin, 450 mg, PO, MD, q.d. for 5 days                                                                                                                                                                                       |Alprazolam, PO|0.96233            |0.91667           |1.0498            |0.9951              |-                  |-                  |Gashaw 2003         |
|1001  |Rifampicin, 450 mg, PO, MD OD (4 days)                                                                                                                                                                                            |Alprazolam, PO|0.19839            |0.11726           |1.6919            |0.68932             |0.63816            |1.0802             |Schmider 1999       |
|179   |Rifampicin, 600 mg, PO, MD OD (7 days)                                                                                                                                                                                            |Midazolam, IV |0.49099            |0.44898           |1.0936            |0.75209             |-                  |-                  |Gorski 2003         |
|276   |Rifampicin, 600 mg, PO, MD OD (5 days)                                                                                                                                                                                            |Midazolam, IV |0.47342            |0.37931           |1.2481            |0.90482             |-                  |-                  |Kharasch 1997       |
|280   |Rifampicin, 600 mg, PO, MD OD (6 days)                                                                                                                                                                                            |Midazolam, IV |0.4757             |0.52113           |0.91284           |0.90853             |1.01               |0.89957            |Kharasch 2004       |
|294   |Rifampicin, 5 mg, PO, MD OD (6 days)                                                                                                                                                                                              |Midazolam, IV |0.78052            |0.84              |0.9292            |0.98019             |1.0323             |0.94956            |Kharasch 2011       |
|295   |Rifampicin, 10 mg, PO, MD OD (6 days)                                                                                                                                                                                             |Midazolam, IV |0.69874            |0.77              |0.90745           |0.9682              |1.0645             |0.90952            |Kharasch 2011       |
|296   |Rifampicin, 25 mg, PO, MD OD (6 days)                                                                                                                                                                                             |Midazolam, IV |0.60481            |0.63              |0.96001           |0.9493              |0.83871            |1.1319             |Kharasch 2011       |
|297   |Rifampicin, 75 mg, PO, MD OD (6 days)                                                                                                                                                                                             |Midazolam, IV |0.53126            |0.6               |0.88544           |0.92855             |1.3226             |0.70208            |Kharasch 2011       |
|2036  |Rifampicin, 600 mg, PO, MD OD (10 days)                                                                                                                                                                                           |Midazolam, IV |1.1815             |1.15              |1.0274            |2.2563              |-                  |-                  |Kim 2018            |
|342   |Rifampicin, 600 mg, PO, MD OD (6 days)                                                                                                                                                                                            |Midazolam, IV |0.47024            |0.65501           |0.71791           |0.90365             |1.106              |0.81708            |Link 2008           |
|389   |Rifampicin, 600 mg, PO, MD OD (5 days)                                                                                                                                                                                            |Midazolam, IV |0.47562            |0.51              |0.93258           |0.907               |-                  |-                  |Phimmasone 2001     |
|1092  |Rifampicin, 600 mg, PO, MD OD (10 days)                                                                                                                                                                                           |Midazolam, IV |1.179              |1.15              |1.0252            |2.2563              |-                  |-                  |Shin 2013           |
|1095  |Rifampicin, 600 mg, PO, MD OD (10 days)                                                                                                                                                                                           |Midazolam, IV |1.179              |1.225             |0.96247           |2.2563              |1.775              |1.2712             |Shin 2016           |
|422   |Rifampicin, 600 mg, PO, MD OD (7 days)                                                                                                                                                                                            |Midazolam, IV |0.491              |0.57947           |0.84732           |0.75222             |-                  |-                  |Szalat 2007         |
|202   |Rifampicin, 600 mg, PO, MD OD (10 days)                                                                                                                                                                                           |Midazolam, IV |0.76842            |0.83333           |0.92211           |1.9391              |-                  |-                  |Yu 2004             |
|54    |Rifampicin, 600 mg, PO, MD OD (5 days)                                                                                                                                                                                            |Midazolam, PO |0.038093           |0.041             |0.9291            |0.098048            |0.061818           |1.5861             |Backman 1996        |
|56    |Rifampicin, 600 mg, PO, MD OD (5 days)                                                                                                                                                                                            |Midazolam, PO |0.038143           |0.023             |1.6584            |0.098049            |0.054              |1.8157             |Backman 1998        |
|57    |Rifampicin, 600 mg, PO, MD OD (5 days)                                                                                                                                                                                            |Midazolam, PO |0.11806            |0.132             |0.89436           |0.22359             |0.202              |1.1069             |Backman 1998        |
|113   |Rifampicin, 600 mg, PO, MD OD (9 days)                                                                                                                                                                                            |Midazolam, PO |0.028231           |0.12449           |0.22677           |0.070021            |0.16957            |0.41294            |Chung 2006          |
|132   |Rifampicin, 450 mg, PO, MD OD (5 days)                                                                                                                                                                                            |Midazolam, PO |0.033758           |0.052239          |0.64622           |0.08487             |0.11154            |0.7609             |Eap 2004            |
|177   |Rifampicin, 600 mg, PO, MD OD (7 days)                                                                                                                                                                                            |Midazolam, PO |0.047548           |0.10335           |0.46006           |0.11675             |0.067039           |1.7415             |Gorski 2003         |
|215   |Rifampicin, 300 mg, PO, MD BID (7 days)                                                                                                                                                                                           |Midazolam, PO |0.043409           |0.057161          |0.75942           |0.10788             |0.12092            |0.89216            |Gurley 2006         |
|221   |Rifampicin, 300 mg, PO, MD BID (7 days)                                                                                                                                                                                           |Midazolam, PO |0.043409           |0.060317          |0.71968           |0.10788             |0.10762            |1.0023             |Gurley 2008a        |
|286   |Rifampicin, 600 mg, PO, MD OD (6 days)                                                                                                                                                                                            |Midazolam, PO |0.03579            |0.052632          |0.68001           |0.075637            |0.10989            |0.6883             |Kharasch 2004       |
|304   |Rifampicin, 5 mg, PO, MD OD (6 days)                                                                                                                                                                                              |Midazolam, PO |0.423              |0.8               |0.52875           |0.55551             |0.8                |0.69438            |Kharasch 2011       |
|305   |Rifampicin, 10 mg, PO, MD OD (6 days)                                                                                                                                                                                             |Midazolam, PO |0.29154            |0.68              |0.42874           |0.42549             |0.93333            |0.45588            |Kharasch 2011       |
|306   |Rifampicin, 25 mg, PO, MD OD (6 days)                                                                                                                                                                                             |Midazolam, PO |0.16305            |0.4               |0.40762           |0.27343             |0.50667            |0.53966            |Kharasch 2011       |
|307   |Rifampicin, 75 mg, PO, MD OD (6 days)                                                                                                                                                                                             |Midazolam, PO |0.080913           |0.25              |0.32365           |0.15436             |0.34               |0.45399            |Kharasch 2011       |
|344   |Rifampicin, 600 mg, PO, MD OD (6 days)                                                                                                                                                                                            |Midazolam, PO |0.030212           |0.015549          |1.943             |0.07709             |0.034865           |2.2111             |Link 2008           |
|1098  |Rifampicin, 600 mg, PO, SD                                                                                                                                                                                                        |Midazolam, PO |2.2421             |0.94              |2.3853            |1.88                |1.3                |1.4461             |Prueksaritanont 2017|
|392   |Rifampicin, 600 mg, PO, MD OD (28 days)                                                                                                                                                                                           |Midazolam, PO |0.20286            |0.123             |1.6493            |0.26564             |0.162              |1.6397             |Reitman 2011        |
|393   |Rifampicin, 600 mg, PO, MD OD (28 days)                                                                                                                                                                                           |Midazolam, PO |0.35124            |0.383             |0.91707           |0.48815             |0.403              |1.2113             |Reitman 2011        |
|394   |Rifampicin, 600 mg, PO, MD OD (28 days)                                                                                                                                                                                           |Midazolam, PO |0.91664            |0.815             |1.1247            |0.94285             |0.731              |1.2898             |Reitman 2011        |
|2002  |Rifampicin, 300 mg, PO, MD OD (7 days)                                                                                                                                                                                            |Midazolam, PO |0.041745           |0.25641           |0.16281           |0.08178             |0.375              |0.21808            |van Dyk 2018        |
|204   |Rifampicin, 10 mg, PO, MD OD (22 days)                                                                                                                                                                                            |Midazolam, PO |0.26874            |0.539             |0.4986            |0.40212             |0.63265            |0.6356             |Wiesinger 2020      |
|205   |Rifampicin, 600 mg, PO, MD OD (22 days)                                                                                                                                                                                           |Midazolam, PO |0.029266           |0.137             |0.21362           |0.06674             |0.18755            |0.35585            |Wiesinger 2020      |
|1004  |Rifampicin, 600 mg, PO, MD OD (5 days)                                                                                                                                                                                            |Triazolam, PO |0.033096           |0.051             |0.64895           |0.11455             |0.12414            |0.92277            |Villikka 1997       |

## Mechanism

### Competitive Inhibition

![001_plotDDIRatioAUCPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/001_Mechanism/001_Competitive_Inhibition/001_plotDDIRatioAUCPredictedVsObserved.png)

![002_plotDDIRatioAUCResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/001_Mechanism/001_Competitive_Inhibition/002_plotDDIRatioAUCResidualsVsObserved.png)

![003_plotDDIRatioCMAXPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/001_Mechanism/001_Competitive_Inhibition/003_plotDDIRatioCMAXPredictedVsObserved.png)

![004_plotDDIRatioCMAXResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/001_Mechanism/001_Competitive_Inhibition/004_plotDDIRatioCMAXResidualsVsObserved.png)

GMFE (AUC) = 1.630053 

GMFE (CMAX) = 1.305125 

|AUC                       |Number|Ratio [%]|
|-------------------------:|-----:|--------:|
|Points total              |22    |-        |
|Points within Guest et al.|12    |54.5455  |
|Points within 2-fold      |17    |77.2727  |

|CMAX                      |Number|Ratio [%]|
|-------------------------:|-----:|--------:|
|Points total              |16    |-        |
|Points within Guest et al.|12    |75       |
|Points within 2-fold      |16    |100      |

### Induction

![001_plotDDIRatioAUCPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/001_Mechanism/002_Induction/001_plotDDIRatioAUCPredictedVsObserved.png)

![002_plotDDIRatioAUCResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/001_Mechanism/002_Induction/002_plotDDIRatioAUCResidualsVsObserved.png)

![003_plotDDIRatioCMAXPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/001_Mechanism/002_Induction/003_plotDDIRatioCMAXPredictedVsObserved.png)

![004_plotDDIRatioCMAXResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/001_Mechanism/002_Induction/004_plotDDIRatioCMAXResidualsVsObserved.png)

GMFE (AUC) = 1.384442 

GMFE (CMAX) = 1.451894 

|AUC                       |Number|Ratio [%]|
|-------------------------:|-----:|--------:|
|Points total              |68    |-        |
|Points within Guest et al.|52    |76.4706  |
|Points within 2-fold      |59    |86.7647  |

|CMAX                      |Number|Ratio [%]|
|-------------------------:|-----:|--------:|
|Points total              |43    |-        |
|Points within Guest et al.|18    |41.8605  |
|Points within 2-fold      |37    |86.0465  |

### Mechanism based Inactivation

![001_plotDDIRatioAUCPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/001_Mechanism/003_Mechanism_based_Inactivation/001_plotDDIRatioAUCPredictedVsObserved.png)

![002_plotDDIRatioAUCResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/001_Mechanism/003_Mechanism_based_Inactivation/002_plotDDIRatioAUCResidualsVsObserved.png)

![003_plotDDIRatioCMAXPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/001_Mechanism/003_Mechanism_based_Inactivation/003_plotDDIRatioCMAXPredictedVsObserved.png)

![004_plotDDIRatioCMAXResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/001_Mechanism/003_Mechanism_based_Inactivation/004_plotDDIRatioCMAXResidualsVsObserved.png)

GMFE (AUC) = 1.271597 

GMFE (CMAX) = 1.240656 

|AUC                       |Number|Ratio [%]|
|-------------------------:|-----:|--------:|
|Points total              |28    |-        |
|Points within Guest et al.|24    |85.7143  |
|Points within 2-fold      |26    |92.8571  |

|CMAX                      |Number|Ratio [%]|
|-------------------------:|-----:|--------:|
|Points total              |17    |-        |
|Points within Guest et al.|13    |76.4706  |
|Points within 2-fold      |17    |100      |

## Perpetrator

### Clarithromycin

![001_plotDDIRatioAUCPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/002_Perpetrator/001_Clarithromycin/001_plotDDIRatioAUCPredictedVsObserved.png)

![002_plotDDIRatioAUCResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/002_Perpetrator/001_Clarithromycin/002_plotDDIRatioAUCResidualsVsObserved.png)

![003_plotDDIRatioCMAXPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/002_Perpetrator/001_Clarithromycin/003_plotDDIRatioCMAXPredictedVsObserved.png)

![004_plotDDIRatioCMAXResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/002_Perpetrator/001_Clarithromycin/004_plotDDIRatioCMAXResidualsVsObserved.png)

GMFE (AUC) = 1.257206 

GMFE (CMAX) = 1.235284 

|AUC                       |Number|Ratio [%]|
|-------------------------:|-----:|--------:|
|Points total              |11    |-        |
|Points within Guest et al.|11    |100      |
|Points within 2-fold      |11    |100      |

|CMAX                      |Number|Ratio [%]|
|-------------------------:|-----:|--------:|
|Points total              |8     |-        |
|Points within Guest et al.|8     |100      |
|Points within 2-fold      |8     |100      |

### Efavirenz

![001_plotDDIRatioAUCPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/002_Perpetrator/002_Efavirenz/001_plotDDIRatioAUCPredictedVsObserved.png)

![002_plotDDIRatioAUCResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/002_Perpetrator/002_Efavirenz/002_plotDDIRatioAUCResidualsVsObserved.png)

![003_plotDDIRatioCMAXPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/002_Perpetrator/002_Efavirenz/003_plotDDIRatioCMAXPredictedVsObserved.png)

![004_plotDDIRatioCMAXResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/002_Perpetrator/002_Efavirenz/004_plotDDIRatioCMAXResidualsVsObserved.png)

GMFE (AUC) = 1.075674 

GMFE (CMAX) = 1.235565 

|AUC                       |Number|Ratio [%]|
|-------------------------:|-----:|--------:|
|Points total              |13    |-        |
|Points within Guest et al.|12    |92.3077  |
|Points within 2-fold      |13    |100      |

|CMAX                      |Number|Ratio [%]|
|-------------------------:|-----:|--------:|
|Points total              |3     |-        |
|Points within Guest et al.|2     |66.6667  |
|Points within 2-fold      |3     |100      |

### Erythromycin

![001_plotDDIRatioAUCPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/002_Perpetrator/003_Erythromycin/001_plotDDIRatioAUCPredictedVsObserved.png)

![002_plotDDIRatioAUCResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/002_Perpetrator/003_Erythromycin/002_plotDDIRatioAUCResidualsVsObserved.png)

![003_plotDDIRatioCMAXPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/002_Perpetrator/003_Erythromycin/003_plotDDIRatioCMAXPredictedVsObserved.png)

![004_plotDDIRatioCMAXResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/002_Perpetrator/003_Erythromycin/004_plotDDIRatioCMAXResidualsVsObserved.png)

GMFE (AUC) = 1.242000 

GMFE (CMAX) = 1.231138 

|AUC                       |Number|Ratio [%]|
|-------------------------:|-----:|--------:|
|Points total              |14    |-        |
|Points within Guest et al.|11    |78.5714  |
|Points within 2-fold      |13    |92.8571  |

|CMAX                      |Number|Ratio [%]|
|-------------------------:|-----:|--------:|
|Points total              |8     |-        |
|Points within Guest et al.|4     |50       |
|Points within 2-fold      |8     |100      |

### Fluvoxamine

![001_plotDDIRatioAUCPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/002_Perpetrator/004_Fluvoxamine/001_plotDDIRatioAUCPredictedVsObserved.png)

![002_plotDDIRatioAUCResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/002_Perpetrator/004_Fluvoxamine/002_plotDDIRatioAUCResidualsVsObserved.png)

![003_plotDDIRatioCMAXPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/002_Perpetrator/004_Fluvoxamine/003_plotDDIRatioCMAXPredictedVsObserved.png)

![004_plotDDIRatioCMAXResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/002_Perpetrator/004_Fluvoxamine/004_plotDDIRatioCMAXResidualsVsObserved.png)

GMFE (AUC) = 1.477241 

GMFE (CMAX) = 1.425160 

|AUC                       |Number|Ratio [%]|
|-------------------------:|-----:|--------:|
|Points total              |4     |-        |
|Points within Guest et al.|1     |25       |
|Points within 2-fold      |4     |100      |

|CMAX                      |Number|Ratio [%]|
|-------------------------:|-----:|--------:|
|Points total              |3     |-        |
|Points within Guest et al.|1     |33.3333  |
|Points within 2-fold      |3     |100      |

### Itraconazole

![001_plotDDIRatioAUCPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/002_Perpetrator/005_Itraconazole/001_plotDDIRatioAUCPredictedVsObserved.png)

![002_plotDDIRatioAUCResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/002_Perpetrator/005_Itraconazole/002_plotDDIRatioAUCResidualsVsObserved.png)

![003_plotDDIRatioCMAXPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/002_Perpetrator/005_Itraconazole/003_plotDDIRatioCMAXPredictedVsObserved.png)

![004_plotDDIRatioCMAXResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/002_Perpetrator/005_Itraconazole/004_plotDDIRatioCMAXResidualsVsObserved.png)

GMFE (AUC) = 1.666102 

GMFE (CMAX) = 1.278893 

|AUC                       |Number|Ratio [%]|
|-------------------------:|-----:|--------:|
|Points total              |18    |-        |
|Points within Guest et al.|11    |61.1111  |
|Points within 2-fold      |13    |72.2222  |

|CMAX                      |Number|Ratio [%]|
|-------------------------:|-----:|--------:|
|Points total              |13    |-        |
|Points within Guest et al.|11    |84.6154  |
|Points within 2-fold      |13    |100      |

### Rifampicin

![001_plotDDIRatioAUCPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/002_Perpetrator/006_Rifampicin/001_plotDDIRatioAUCPredictedVsObserved.png)

![002_plotDDIRatioAUCResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/002_Perpetrator/006_Rifampicin/002_plotDDIRatioAUCResidualsVsObserved.png)

![003_plotDDIRatioCMAXPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/002_Perpetrator/006_Rifampicin/003_plotDDIRatioCMAXPredictedVsObserved.png)

![004_plotDDIRatioCMAXResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/002_Perpetrator/006_Rifampicin/004_plotDDIRatioCMAXResidualsVsObserved.png)

GMFE (AUC) = 1.469532 

GMFE (CMAX) = 1.469570 

|AUC                       |Number|Ratio [%]|
|-------------------------:|-----:|--------:|
|Points total              |55    |-        |
|Points within Guest et al.|40    |72.7273  |
|Points within 2-fold      |46    |83.6364  |

|CMAX                      |Number|Ratio [%]|
|-------------------------:|-----:|--------:|
|Points total              |40    |-        |
|Points within Guest et al.|16    |40       |
|Points within 2-fold      |34    |85       |

### Verapamil

![001_plotDDIRatioAUCPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/002_Perpetrator/007_Verapamil/001_plotDDIRatioAUCPredictedVsObserved.png)

![002_plotDDIRatioAUCResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/002_Perpetrator/007_Verapamil/002_plotDDIRatioAUCResidualsVsObserved.png)

![003_plotDDIRatioCMAXPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/002_Perpetrator/007_Verapamil/003_plotDDIRatioCMAXPredictedVsObserved.png)

![004_plotDDIRatioCMAXResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/002_Perpetrator/007_Verapamil/004_plotDDIRatioCMAXResidualsVsObserved.png)

GMFE (AUC) = 1.479805 

GMFE (CMAX) = 1.366122 

|AUC                       |Number|Ratio [%]|
|-------------------------:|-----:|--------:|
|Points total              |3     |-        |
|Points within Guest et al.|2     |66.6667  |
|Points within 2-fold      |2     |66.6667  |

|CMAX                      |Number|Ratio [%]|
|-------------------------:|-----:|--------:|
|Points total              |1     |-        |
|Points within Guest et al.|1     |100      |
|Points within 2-fold      |1     |100      |

## Victim

### Alfentanil

![001_plotDDIRatioAUCPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/003_Victim/001_Alfentanil/001_plotDDIRatioAUCPredictedVsObserved.png)

![002_plotDDIRatioAUCResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/003_Victim/001_Alfentanil/002_plotDDIRatioAUCResidualsVsObserved.png)

![003_plotDDIRatioCMAXPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/003_Victim/001_Alfentanil/003_plotDDIRatioCMAXPredictedVsObserved.png)

![004_plotDDIRatioCMAXResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/003_Victim/001_Alfentanil/004_plotDDIRatioCMAXResidualsVsObserved.png)

GMFE (AUC) = 1.265796 

GMFE (CMAX) = 1.327112 

|AUC                       |Number|Ratio [%]|
|-------------------------:|-----:|--------:|
|Points total              |20    |-        |
|Points within Guest et al.|16    |80       |
|Points within 2-fold      |20    |100      |

|CMAX                      |Number|Ratio [%]|
|-------------------------:|-----:|--------:|
|Points total              |12    |-        |
|Points within Guest et al.|3     |25       |
|Points within 2-fold      |12    |100      |

### Alprazolam

![001_plotDDIRatioAUCPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/003_Victim/002_Alprazolam/001_plotDDIRatioAUCPredictedVsObserved.png)

![002_plotDDIRatioAUCResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/003_Victim/002_Alprazolam/002_plotDDIRatioAUCResidualsVsObserved.png)

![003_plotDDIRatioCMAXPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/003_Victim/002_Alprazolam/003_plotDDIRatioCMAXPredictedVsObserved.png)

![004_plotDDIRatioCMAXResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/003_Victim/002_Alprazolam/004_plotDDIRatioCMAXResidualsVsObserved.png)

GMFE (AUC) = 1.337497 

GMFE (CMAX) = 1.242657 

|AUC                       |Number|Ratio [%]|
|-------------------------:|-----:|--------:|
|Points total              |7     |-        |
|Points within Guest et al.|5     |71.4286  |
|Points within 2-fold      |7     |100      |

|CMAX                      |Number|Ratio [%]|
|-------------------------:|-----:|--------:|
|Points total              |5     |-        |
|Points within Guest et al.|3     |60       |
|Points within 2-fold      |5     |100      |

### Midazolam

![001_plotDDIRatioAUCPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/003_Victim/003_Midazolam/001_plotDDIRatioAUCPredictedVsObserved.png)

![002_plotDDIRatioAUCResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/003_Victim/003_Midazolam/002_plotDDIRatioAUCResidualsVsObserved.png)

![003_plotDDIRatioCMAXPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/003_Victim/003_Midazolam/003_plotDDIRatioCMAXPredictedVsObserved.png)

![004_plotDDIRatioCMAXResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/003_Victim/003_Midazolam/004_plotDDIRatioCMAXResidualsVsObserved.png)

GMFE (AUC) = 1.413945 

GMFE (CMAX) = 1.432152 

|AUC                       |Number|Ratio [%]|
|-------------------------:|-----:|--------:|
|Points total              |82    |-        |
|Points within Guest et al.|62    |75.6098  |
|Points within 2-fold      |68    |82.9268  |

|CMAX                      |Number|Ratio [%]|
|-------------------------:|-----:|--------:|
|Points total              |50    |-        |
|Points within Guest et al.|30    |60       |
|Points within 2-fold      |44    |88       |

### Triazolam

![001_plotDDIRatioAUCPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/003_Victim/004_Triazolam/001_plotDDIRatioAUCPredictedVsObserved.png)

![002_plotDDIRatioAUCResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/003_Victim/004_Triazolam/002_plotDDIRatioAUCResidualsVsObserved.png)

![003_plotDDIRatioCMAXPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/003_Victim/004_Triazolam/003_plotDDIRatioCMAXPredictedVsObserved.png)

![004_plotDDIRatioCMAXResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/003_Victim/004_Triazolam/004_plotDDIRatioCMAXResidualsVsObserved.png)

GMFE (AUC) = 1.638541 

GMFE (CMAX) = 1.183830 

|AUC                       |Number|Ratio [%]|
|-------------------------:|-----:|--------:|
|Points total              |9     |-        |
|Points within Guest et al.|5     |55.5556  |
|Points within 2-fold      |7     |77.7778  |

|CMAX                      |Number|Ratio [%]|
|-------------------------:|-----:|--------:|
|Points total              |9     |-        |
|Points within Guest et al.|7     |77.7778  |
|Points within 2-fold      |9     |100      |

# 3 Concentration-Time Profiles
The following section shows concentration time profiles of the victim drugs of the simulated DDI studies in comparison to observed data (if available).




## 3.1 Clarithromycin - Midazolam DDI
                   

![001_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/001_3_1_Clarithromycin_-_Midazolam_DDI/001_plotComparisonTimeProfile.png)

![002_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/001_3_1_Clarithromycin_-_Midazolam_DDI/002_plotComparisonTimeProfile.png)

![003_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/001_3_1_Clarithromycin_-_Midazolam_DDI/003_plotComparisonTimeProfile.png)

![004_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/001_3_1_Clarithromycin_-_Midazolam_DDI/004_plotComparisonTimeProfile.png)

![005_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/001_3_1_Clarithromycin_-_Midazolam_DDI/005_plotComparisonTimeProfile.png)

![006_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/001_3_1_Clarithromycin_-_Midazolam_DDI/006_plotComparisonTimeProfile.png)

![007_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/001_3_1_Clarithromycin_-_Midazolam_DDI/007_plotComparisonTimeProfile.png)

![008_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/001_3_1_Clarithromycin_-_Midazolam_DDI/008_plotComparisonTimeProfile.png)

![009_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/001_3_1_Clarithromycin_-_Midazolam_DDI/009_plotComparisonTimeProfile.png)

![010_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/001_3_1_Clarithromycin_-_Midazolam_DDI/010_plotComparisonTimeProfile.png)

## 3.2 Clarithromycin - Triazolam DDI
                   

![001_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/002_3_2_Clarithromycin_-_Triazolam_DDI/001_plotComparisonTimeProfile.png)

## 3.3 Erythromycin - Alfentanil DDI
                   

![001_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/003_3_3_Erythromycin_-_Alfentanil_DDI/001_plotComparisonTimeProfile.png)

![002_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/003_3_3_Erythromycin_-_Alfentanil_DDI/002_plotComparisonTimeProfile.png)

## 3.4 Erythromycin - Alprazolam DDI
                   

![001_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/004_3_4_Erythromycin_-_Alprazolam_DDI/001_plotComparisonTimeProfile.png)

## 3.5 Erythromycin - Midazolam DDI
                   

![001_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/005_3_5_Erythromycin_-_Midazolam_DDI/001_plotComparisonTimeProfile.png)

![002_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/005_3_5_Erythromycin_-_Midazolam_DDI/002_plotComparisonTimeProfile.png)

![003_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/005_3_5_Erythromycin_-_Midazolam_DDI/003_plotComparisonTimeProfile.png)

![004_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/005_3_5_Erythromycin_-_Midazolam_DDI/004_plotComparisonTimeProfile.png)

![005_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/005_3_5_Erythromycin_-_Midazolam_DDI/005_plotComparisonTimeProfile.png)

![006_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/005_3_5_Erythromycin_-_Midazolam_DDI/006_plotComparisonTimeProfile.png)

## 3.6 Erythromycin - Triazolam DDI
                   

![001_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/006_3_6_Erythromycin_-_Triazolam_DDI/001_plotComparisonTimeProfile.png)

![002_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/006_3_6_Erythromycin_-_Triazolam_DDI/002_plotComparisonTimeProfile.png)

## 3.7 Fluvoxamine - Alprazolam DDI
                   

![001_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/007_3_7_Fluvoxamine_-_Alprazolam_DDI/001_plotComparisonTimeProfile.png)

![002_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/007_3_7_Fluvoxamine_-_Alprazolam_DDI/002_plotComparisonTimeProfile.png)

## 3.8 Fluvoxamine - Midazolam DDI
                   

![001_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/008_3_8_Fluvoxamine_-_Midazolam_DDI/001_plotComparisonTimeProfile.png)

![002_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/008_3_8_Fluvoxamine_-_Midazolam_DDI/002_plotComparisonTimeProfile.png)

## 3.9 Itraconazole - Alprazolam DDI
                   

![001_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/009_3_9_Itraconazole_-_Alprazolam_DDI/001_plotComparisonTimeProfile.png)

## 3.10 Itraconazole - Midazolam DDI
                   

![001_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/010_3_10_Itraconazole_-_Midazolam_DDI/001_plotComparisonTimeProfile.png)

![002_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/010_3_10_Itraconazole_-_Midazolam_DDI/002_plotComparisonTimeProfile.png)

![003_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/010_3_10_Itraconazole_-_Midazolam_DDI/003_plotComparisonTimeProfile.png)

![004_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/010_3_10_Itraconazole_-_Midazolam_DDI/004_plotComparisonTimeProfile.png)

![005_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/010_3_10_Itraconazole_-_Midazolam_DDI/005_plotComparisonTimeProfile.png)

![006_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/010_3_10_Itraconazole_-_Midazolam_DDI/006_plotComparisonTimeProfile.png)

![007_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/010_3_10_Itraconazole_-_Midazolam_DDI/007_plotComparisonTimeProfile.png)

![008_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/010_3_10_Itraconazole_-_Midazolam_DDI/008_plotComparisonTimeProfile.png)

![009_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/010_3_10_Itraconazole_-_Midazolam_DDI/009_plotComparisonTimeProfile.png)

## 3.11 Itraconazole - Triazolam DDI
                   

![001_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/011_3_11_Itraconazole_-_Triazolam_DDI/001_plotComparisonTimeProfile.png)

![002_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/011_3_11_Itraconazole_-_Triazolam_DDI/002_plotComparisonTimeProfile.png)

## 3.12 Verapamil - Midazolam DDI
                   

![001_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/012_3_12_Verapamil_-_Midazolam_DDI/001_plotComparisonTimeProfile.png)

![002_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/012_3_12_Verapamil_-_Midazolam_DDI/002_plotComparisonTimeProfile.png)

![003_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/012_3_12_Verapamil_-_Midazolam_DDI/003_plotComparisonTimeProfile.png)

## 3.13 Efavirenz - Alfentanil DDI
                   

![001_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/013_3_13_Efavirenz_-_Alfentanil_DDI/001_plotComparisonTimeProfile.png)

![002_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/013_3_13_Efavirenz_-_Alfentanil_DDI/002_plotComparisonTimeProfile.png)

## 3.14 Efavirenz - Midazolam DDI
                   

![001_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/014_3_14_Efavirenz_-_Midazolam_DDI/001_plotComparisonTimeProfile.png)

![002_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/014_3_14_Efavirenz_-_Midazolam_DDI/002_plotComparisonTimeProfile.png)

![003_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/014_3_14_Efavirenz_-_Midazolam_DDI/003_plotComparisonTimeProfile.png)

## 3.15 Rifampicin - Alfentanil DDI
                   

![001_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/015_3_15_Rifampicin_-_Alfentanil_DDI/001_plotComparisonTimeProfile.png)

![002_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/015_3_15_Rifampicin_-_Alfentanil_DDI/002_plotComparisonTimeProfile.png)

![003_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/015_3_15_Rifampicin_-_Alfentanil_DDI/003_plotComparisonTimeProfile.png)

![004_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/015_3_15_Rifampicin_-_Alfentanil_DDI/004_plotComparisonTimeProfile.png)

![005_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/015_3_15_Rifampicin_-_Alfentanil_DDI/005_plotComparisonTimeProfile.png)

![006_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/015_3_15_Rifampicin_-_Alfentanil_DDI/006_plotComparisonTimeProfile.png)

![007_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/015_3_15_Rifampicin_-_Alfentanil_DDI/007_plotComparisonTimeProfile.png)

![008_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/015_3_15_Rifampicin_-_Alfentanil_DDI/008_plotComparisonTimeProfile.png)

![009_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/015_3_15_Rifampicin_-_Alfentanil_DDI/009_plotComparisonTimeProfile.png)

![010_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/015_3_15_Rifampicin_-_Alfentanil_DDI/010_plotComparisonTimeProfile.png)

## 3.16 Rifampicin - Alprazolam DDI
                   

![001_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/016_3_16_Rifampicin_-_Alprazolam_DDI/001_plotComparisonTimeProfile.png)

![002_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/016_3_16_Rifampicin_-_Alprazolam_DDI/002_plotComparisonTimeProfile.png)

![003_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/016_3_16_Rifampicin_-_Alprazolam_DDI/003_plotComparisonTimeProfile.png)

## 3.17 Rifampicin - Midazolam DDI
                   

![001_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/017_3_17_Rifampicin_-_Midazolam_DDI/001_plotComparisonTimeProfile.png)

![002_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/017_3_17_Rifampicin_-_Midazolam_DDI/002_plotComparisonTimeProfile.png)

![003_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/017_3_17_Rifampicin_-_Midazolam_DDI/003_plotComparisonTimeProfile.png)

![004_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/017_3_17_Rifampicin_-_Midazolam_DDI/004_plotComparisonTimeProfile.png)

![005_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/017_3_17_Rifampicin_-_Midazolam_DDI/005_plotComparisonTimeProfile.png)

![006_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/017_3_17_Rifampicin_-_Midazolam_DDI/006_plotComparisonTimeProfile.png)

![007_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/017_3_17_Rifampicin_-_Midazolam_DDI/007_plotComparisonTimeProfile.png)

![008_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/017_3_17_Rifampicin_-_Midazolam_DDI/008_plotComparisonTimeProfile.png)

![009_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/017_3_17_Rifampicin_-_Midazolam_DDI/009_plotComparisonTimeProfile.png)

![010_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/017_3_17_Rifampicin_-_Midazolam_DDI/010_plotComparisonTimeProfile.png)

![011_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/017_3_17_Rifampicin_-_Midazolam_DDI/011_plotComparisonTimeProfile.png)

![012_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/017_3_17_Rifampicin_-_Midazolam_DDI/012_plotComparisonTimeProfile.png)

![013_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/017_3_17_Rifampicin_-_Midazolam_DDI/013_plotComparisonTimeProfile.png)

![014_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/017_3_17_Rifampicin_-_Midazolam_DDI/014_plotComparisonTimeProfile.png)

![015_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/017_3_17_Rifampicin_-_Midazolam_DDI/015_plotComparisonTimeProfile.png)

![016_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/017_3_17_Rifampicin_-_Midazolam_DDI/016_plotComparisonTimeProfile.png)

![017_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/017_3_17_Rifampicin_-_Midazolam_DDI/017_plotComparisonTimeProfile.png)

![018_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/017_3_17_Rifampicin_-_Midazolam_DDI/018_plotComparisonTimeProfile.png)

![019_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/017_3_17_Rifampicin_-_Midazolam_DDI/019_plotComparisonTimeProfile.png)

![020_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/017_3_17_Rifampicin_-_Midazolam_DDI/020_plotComparisonTimeProfile.png)

![021_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/017_3_17_Rifampicin_-_Midazolam_DDI/021_plotComparisonTimeProfile.png)

![022_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/017_3_17_Rifampicin_-_Midazolam_DDI/022_plotComparisonTimeProfile.png)

![023_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/017_3_17_Rifampicin_-_Midazolam_DDI/023_plotComparisonTimeProfile.png)

![024_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/017_3_17_Rifampicin_-_Midazolam_DDI/024_plotComparisonTimeProfile.png)

![025_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/017_3_17_Rifampicin_-_Midazolam_DDI/025_plotComparisonTimeProfile.png)

## 3.18 Rifampicin - Triazolam DDI
                   

![001_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/018_3_18_Rifampicin_-_Triazolam_DDI/001_plotComparisonTimeProfile.png)

# 4 References
**Almond 2016** Almond LM, Mukadam S, Gardner I, Okialda K, Wong S, Hatley O, Tay S, Rowland-Yeo K, Jamei M, Rostami-Hodjegan A, Kenny JR. Prediction of Drug-Drug Interactions Arising from CYP3A induction Using a Physiologically Based Dynamic Model. Drug Metab Dispos. 2016 Jun;44(6):821-32.

**Guest 2011** Guest EJ, Aarons L, Houston JB, Rostami-Hodjegan A, Galetin A. Critique of the two-fold measure of prediction success for ratios: application for the assessment of drug-drug interactions. Drug Metab Dispos. 2011 Feb;39(2):170-3.

**OSP PK Database** (https://github.com/Open-Systems-Pharmacology/Database-for-observed-data)



## Clarithromycin-Midazolam-DDI

**Gorski 1998** Gorski, J. C., Jones, D. R., Haehner‐Daniels, B. D., Hamman, M. A., O'Mara Jr, E. M., & Hall, S. D. (1998). The contribution of intestinal and hepatic CYP3A to the interaction between midazolam and clarithromycin. *Clinical Pharmacology & Therapeutics*, *64*(2), 133-143.

**Gurley 2006** Gurley, B., Hubbard, M. A., Williams, D. K., Thaden, J., Tong, Y., Gentry, W. B., ... & Cheboyina, S. (2006). Assessing the clinical significance of botanical supplementation on human cytochrome P450 3A activity: comparison of a milk thistle and black cohosh product to rifampin and clarithromycin. *The Journal of Clinical Pharmacology*, *46*(2), 201-213.

**Gurley 2008a** Gurley, B. J., Swain, A., Hubbard, M. A., Hartsfield, F., Thaden, J., Williams, D. K., ... & Tong, Y. (2008). Supplementation with goldenseal (Hydrastis canadensis), but not kava kava (Piper methysticum), inhibits human CYP3A activity in vivo. *Clinical Pharmacology & Therapeutics*, *83*(1), 61-69.

**Markert 2013** Markert, C., Hellwig, R., Burhenne, J., Hoffmann, M. M., Weiss, J., Mikus, G., & Haefeli, W. E. (2013). Interaction of ambrisentan with clarithromycin and its modulation by polymorphic SLCO1B1. *European journal of clinical pharmacology*, *69*(10), 1785-1793.

**Prueksaritanont 2017** Prueksaritanont, T., Tatosian, D. A., Chu, X., Railkar, R., Evers, R., Chavez‐Eng, C., ... & Cai, X. (2017). Validation of a microdose probe drug cocktail for clinical drug interaction assessments for drug transporters and CYP3A. *Clinical Pharmacology & Therapeutics*, *101*(4), 519-530.

**Quinney 2008** Quinney, S. K., Haehner, B. D., Rhoades, M. B., Lin, Z., Gorski, J. C., & Hall, S. D. (2008). Interaction between midazolam and clarithromycin in the elderly. *British journal of clinical pharmacology*, *65*(1), 98-109.

**van Dyk 2018** van Dyk, M., Marshall, J. C., Sorich, M. J., Wood, L. S., & Rowland, A. (2018). Assessment of inter-racial variability in CYP3A4 activity and inducibility among healthy adult males of Caucasian and South Asian ancestries. *European journal of clinical pharmacology*, *74*(7), 913-920.

**Yeates 1996** Yeates, R. A., Laufen, H., & Zimmermann, T. (1996). Interaction between midazolam and clarithromycin: comparison with azithromycin. *International journal of clinical pharmacology and therapeutics*, *34*(9), 400-405.



## Clarithromycin-Triazolam-DDI

**Greenblatt 1998a** Greenblatt DJ, von Moltke LL, Harmatz JS, Counihan M, Graf JA, Durol AL, Mertzanis P, Duan SX, Wright CE, Shader RI. Inhibition of triazolam clearance by macrolide antimicrobial agents: in vitro correlates and dynamic consequences. Clin Pharmacol Ther. 1998 Sep;64(3):278-85.



## Erythromycin-Alfentanil-DDI

**Bartkowski 1989** Bartkowski, R. R., Goldberg, M. E., Larijani, G. E., & Boerner, T. (1989). Inhibition of alfentanil metabolism by erythromycin. *Clinical Pharmacology & Therapeutics*, *46*(1), 99-102.

**Bartkowski 1993** Bartkowski, R. R., Goldberg, M. E., Huffnagle, S., & Epstein, R. H. (1993). Sufentanil disposition. Is it affected by erythromycin administration?. *Anesthesiology*, *78*(2), 260-265.



## Erythromycin-Alprazolam-DDI

**Yasui 1996** Yasui, N., Otani, K., Kaneko, S., Ohkubo, T., Osanai, T., Sugawara, K., ... & Ishizaki, T. (1996). A kinetic and dynamic study of oral alprazolam with and without erythromycin in humans: in vivo evidence for the involvement of CYP3A4 in alprazolam metabolism. *Clinical Pharmacology & Therapeutics*, *59*(5), 514-519.



## Erythromycin-Midazolam-DDI

**Carls 2014** Carls, A., Jedamzik, J., Witt, L., Hohmann, N., Burhenne, J., & Mikus, G. (2014). Systemic exposure of topical erythromycin in comparison to oral administration and the effect on cytochrome P450 3A4 activity. *British journal of clinical pharmacology*, *78*(6), 1433-1440.

**Okudaira 2007** Okudaira, T., Kotegawa, T., Imai, H., Tsutsumi, K., Nakano, S., & Ohashi, K. (2007). Effect of the treatment period with erythromycin on cytochrome P450 3A activity in humans. *The Journal of Clinical Pharmacology*, *47*(7), 871-876.

**Olkkola 1993** Olkkola, K. T., Aranko, K., Luurila, H., Hiller, A., Saarnivaara, L., Himberg, J. J., & Neuvonen, P. J. (1993). A potentially hazardous interaction between erythromycin and midazolam. *Clinical Pharmacology & Therapeutics*, *53*(3), 298-305.

**Swart 2002** Swart, E. L., van der Hoven, B., Johan Groeneveld, A. B., Touw, D. J., & Danhof, M. (2002). Correlation between midazolam and lignocaine pharmacokinetics and MEGX formation in healthy volunteers. *British journal of clinical pharmacology*, *53*(2), 133-139.

**Zimmermann 1996** Zimmermann, T., Yeates, R. A., Laufen, H., Scharpf, F., Leitold, M., & Wildfeuer, A. (1996). Influence of the antibiotics erythromycin and azithromycin on the pharmacokinetics and pharmacodynamics of midazolam. *Arzneimittel-Forschung*, *46*(2), 213-217.



## Erythromycin-Triazolam-DDI

**Greenblatt 1998** Greenblatt, D. J., von Moltke, L. L., Harmatz, J. S., Counihan, M., Graf, J. A., Durol, A. L. B., ... & Shader, R. I. (1998). Inhibition of triazolam clearance by macrolide antimicrobial agents: in vitro correlates and dynamic consequences. *Clinical Pharmacology & Therapeutics*, *64*(3), 278-285.

**Phillips 1986** Phillips, J. P., Antal, E. J., & Smith, R. B. (1986). A pharmacokinetic drug interaction between erythromycin and triazolam. *Journal of clinical psychopharmacology*, *6*(5), 297-299.



## Fluvoxamine-Midazolam-DDI

**Kashuba 1998** Kashuba AD1, Nafziger AN, Kearns GL, Leeder JS, Gotschall R, Rocci ML Jr, Kulawy RW, Beck DJ, Bertino JS Jr. Effect of fluvoxamine therapy on the activities of CYP1A2, CYP2D6, and CYP3A as determined by phenotyping. Clin Pharmacol Ther. 1998 Sep;64(3):257-68.

**Lam 2003** Lam YW1, Alfaro CL, Ereshefsky L, Miller M. Pharmacokinetic and pharmacodynamic interactions of oral midazolam with ketoconazole, fluoxetine, fluvoxamine, and nefazodone. J Clin Pharmacol. 2003 Nov;43(11):1274-82.



## Fluvoxamine-Alprazolam-DDI

**Fleishaker 1994** Fleishaker, J. C., & Hulst, L. K. (1994). A pharmacokinetic and pharmacodynamic evaluation of the combined administration of alprazolam and fluvoxamine. *European journal of clinical pharmacology*, *46*(1), 35-39.



## Itraconazole-Alprazolam-DDI

**Yasui 1998** Yasui  N, Kondo T, Otani K, Furukori H, Kaneko S, Ohkubo T, Nagasaki T, Sugawara K.  Effect of itraconazole on the single oral dose pharmacokinetics and  pharmacodynamics of alprazolam. Psychopharmacology (Berl). 1998  Oct;139(3):269-73.



## Itraconazole-Midazolam-DDI

**Ahonen 1995** Ahonen J, Olkkola KT, Neuvonen PJ. Effect of itraconazole and terbinafine on the pharmacokinetics and pharmacodynamics of midazolam in healthy volunteers. Br J Clin Pharmacol. 1995 Sep;40(3):270-2.

**Backman 1998** Backman JT, Kivistö KT, Olkkola KT, Neuvonen PJ. The area under the plasma concentration-time curve for oral midazolam is 400-fold larger during treatment with itraconazole than with rifampicin. Eur J Clin Pharmacol. 1998 Mar;54(1):53-8.

**Olkkola 1994** Olkkola KT, Backman JT, Neuvonen PJ. Midazolam should be avoided in patients receiving the systemic antimycotics ketoconazole or itraconazole. Clin Pharmacol Ther. 1994 May;55(5):481-5.

**Olkkola 1996** Olkkola KT, Ahonen J, Neuvonen PJ. The effects of the systemic antimycotics, itraconazole and fluconazole, on the pharmacokinetics and pharmacodynamics of intravenous and oral midazolam. Anesth Analg. 1996 Mar;82(3):511-6.

**Prueksaritanont 2017** Prueksaritanont T, Tatosian DA, Chu X, Railkar R, Evers R, Chavez-Eng C, Lutz R, Zeng W, Yabut J, Chan GH, Cai X, Latham AH, Hehman J, Stypinski D, Brejda J, Zhou C, Thornton B, Bateman KP, Fraser I,, Stoch SA. Validation of a microdose probe drug cocktail for clinical drug interaction assessments for drug transporters and CYP3A. Clin Pharmacol Ther. 2017 Apr;101(4):519-530.

**Templeton 2010** Templeton I, Peng CC, Thummel KE, Davis C, Kunze KL, Isoherranen N. Accurate prediction of dose-dependent CYP3A4 inhibition by itraconazole and its metabolites from in vitro inhibition data. Clin Pharmacol Ther. 2010 Oct;88(4):499-505.

**Yu 2004** Yu KS, Cho JY, Jang IJ, Hong KS, Chung JY, Kim JR, Lim HS, Oh DS, Yi SY, Liu KH, Shin JG, Shin SG. Effect of the CYP3A5 genotype on the pharmacokinetics of intravenous midazolam during inhibited and induced metabolic states. Clin Pharmacol Ther. 2004 Aug;76(2):104-12.



## Itraconazole-Triazolam-DDI

**Neuvonen 1996** Neuvonen PJ, Varhe A, Olkkola KT. The effect of ingestion time interval on the interaction between itraconazole and triazolam. Clin Pharmacol Ther. 1996 Sep;60(3):326-31.

**Varhe 1994** Varhe A, Olkkola KT, Neuvonen PJ. Oral triazolam is potentially hazardous to patients receiving systemic antimycotics ketoconazole or itraconazole. Clin Pharmacol Ther. 1994 Dec;56(6 Pt 1):601-7.



## Verapamil-Midazolam-DDI

**Backman 1994** Backman JT, Olkkola KT, Aranko K, Himberg JJ, Neuvonen PJ. Dose of midazolam should be reduced during diltiazem and verapamil treatments. Br J Clin Pharmacol. 1994 Mar;37(3):221-5.

**Wang 2005** Wang Y,  Jin Y, Hilligoss  JK, Ho H, Hamman MA, Hu Z, Gorski JD, Hall SD. Effect of CYP3A5 genotype on the extent of CYP3A inhibition by verapamil. Clin Pharmacol Ther. 2005; 77(2):P3.



## Efavirenz-Alfentanil-DDI

**Kharasch 2012** Kharasch ED, Whittington D, Ensign D, Hoffer C, Bedynek PS, Campbell S, Stubbert K, Crafford A, London A, Kim T. Mechanism of efavirenz influence on methadone pharmacokinetics and pharmacodynamics. Clin Pharmacol Ther. 2012 Apr;91(4):673-84.



## Efavirenz-Midazolam-DDI

**Katzenmaier 2010** Katzenmaier S, Markert C, Mikus G. Proposal of a new limited sampling strategy to predict CYP3A activity using a partial AUC of midazolam. Eur J Clin Pharmacol. 2010 Nov;66(11):1137-41.

**Mikus 2017** Mikus G, Heinrich T, Bödigheimer J, Röder C, Matthee AK, Weiss J, Burhenne J, Haefeli WE. Semisimultaneous Midazolam Administration to Evaluate the Time Course of CYP3A Activation by a Single Oral Dose of Efavirenz. J Clin Pharmacol. 2017 Jul;57(7):899-905.



## Rifampicin-Alfentanil-DDI

**Kharasch 1997** Kharasch ED, Russell M, Mautz D, Thummel KE, Kunze KL, Bowdle A, Cox K. The role of cytochrome P450 3A4 in alfentanil clearance. Implications for interindividual variability in disposition and perioperative drug interactions. Anesthesiology. 1997 Jul;87(1):36-50.

**Kharasch 2004** Kharasch ED, Walker A, Hoffer C, Sheffels P. Intravenous and oral alfentanil as in vivo probes for hepatic and first-pass cytochrome P450 3A activity: noninvasive assessment by use of pupillary miosis. Clin Pharmacol Ther. 2004 Nov;76(5):452-66.

**Kharasch 2011** Kharasch ED, Francis A, London A, Frey K, Kim T, Blood J. Sensitivity of intravenous and oral alfentanil and pupillary miosis as minimal and noninvasive probes for hepatic and first-pass CYP3A induction. Clin Pharmacol Ther. 2011 Jul;90(1):100-8.

**Kharasch 2011b** Kharasch ED, Vangveravong S, Buck N, London A, Kim T, Blood J, Mach RH. Concurrent assessment of hepatic and intestinal cytochrome P450 3A activities using deuterated alfentanil. Clin Pharmacol Ther. 2011 Apr;89(4):562-70.

**Phimmasone 2001** Phimmasone S, Kharasch ED. A pilot evaluation of alfentanil-induced miosis as a noninvasive probe for hepatic cytochrome P450 3A4 (CYP3A4) activity in humans. Clin Pharmacol Ther. 2001 Dec;70(6):505-17.



## Rifampicin-Alprazolam-DDI

**Gashaw 2003** Gashaw, I., Kirchheiner, J., Goldammer, M., Bauer, S., Seidemann, J., Zoller, K., ... & Brockmöller, J. (2003). Cytochrome p450 3A4 messenger ribonucleic acid induction by rifampin in human peripheral blood mononuclear cells: correlation with alprazolam pharmacokinetics. *Clinical Pharmacology & Therapeutics*, *74*(5), 448-457.

**Schmider 1999** Schmider, J., Brockmöller, J., Arold, G., Bauer, S., & Roots, I. (1999). Simultaneous assessment of CYP3A4 and CYP1A2 activity in vivo with alprazolam and caffeine. *Pharmacogenetics*, *9*(6), 725-734.



## Rifampicin-Midazolam-DDI

**Backman 1996** Backman JT, Olkkola KT, Neuvonen PJ. Rifampin drastically reduces plasma concentrations and effects of oral midazolam. Clin Pharmacol Ther. 1996 Jan;59(1):7-13.

**Backman 1998** Backman JT, Kivistö KT, Olkkola KT, Neuvonen PJ. The area under the plasma concentration-time curve for oral midazolam is 400-fold larger during treatment with itraconazole than with rifampicin. Eur J Clin Pharmacol. 1998 Mar;54(1):53-8.

**Chung 2006** Chung E, Nafziger AN, Kazierad DJ, Bertino JS Jr. Comparison of midazolam and simvastatin as cytochrome P450 3A probes. Clin Pharmacol Ther. 2006 Apr;79(4):350-61.

**Eap 2004** Eap CB, Buclin T, Cucchia G, Zullino D, Hustert E, Bleiber G, Golay KP, Aubert AC, Baumann P, Telenti A, Kerb R. Oral administration of a low dose of midazolam (75 microg) as an in vivo probe for CYP3A activity. Eur J Clin Pharmacol. 2004 Jun;60(4):237-46.

**Gorski 2003** Gorski JC, Vannaprasaht S, Hamman MA, Ambrosius WT, Bruce MA, Haehner-Daniels B, Hall SD. The effect of age, sex, and rifampin administration on intestinal and hepatic cytochrome P450 3A activity. Clin Pharmacol Ther. 2003 Sep;74(3):275-87.

**Gurley 2006** Gurley B, Hubbard MA, Williams DK, Thaden J, Tong Y, Gentry WB, Breen P, Carrier DJ, Cheboyina S. Assessing the clinical significance of botanical supplementation on human cytochrome P450 3A activity: comparison of a milk thistle and black cohosh product to rifampin and clarithromycin. J Clin Pharmacol. 2006 Feb;46(2):201-13.

**Gurley 2008a** Gurley BJ, Swain A, Hubbard MA, Hartsfield F, Thaden J, Williams DK, Gentry WB, Tong Y. Supplementation with goldenseal (Hydrastis canadensis), but not kava kava (Piper methysticum), inhibits human CYP3A activity in vivo. Clin Pharmacol Ther. 2008 Jan;83(1):61-9.

**Kharasch 1997** Kharasch ED, Russell M, Mautz D, Thummel KE, Kunze KL, Bowdle A, Cox K. The role of cytochrome P450 3A4 in alfentanil clearance. Implications for interindividual variability in disposition and perioperative drug interactions. Anesthesiology. 1997 Jul;87(1):36-50.

**Kharasch 2004** Kharasch ED, Walker A, Hoffer C, Sheffels P. Intravenous and oral alfentanil as in vivo probes for hepatic and first-pass cytochrome P450 3A activity: noninvasive assessment by use of pupillary miosis. Clin Pharmacol Ther. 2004 Nov;76(5):452-66.

**Kharasch 2011** Kharasch ED, Francis A, London A, Frey K, Kim T, Blood J. Sensitivity of intravenous and oral alfentanil and pupillary miosis as minimal and noninvasive probes for hepatic and first-pass CYP3A induction. Clin Pharmacol Ther. 2011 Jul;90(1):100-8.

**Kim 2018** Kim B, Lee J, Shin KH, Lee S, Yu KS, Jang IJ, Cho JY. Identification of ω- or (ω-1)-Hydroxylated Medium-Chain Acylcarnitines as Novel Urinary Biomarkers for CYP3A Activity. Clin Pharmacol Ther. 2018 May;103(5):879-887.

**Link 2008** Link B, Haschke M, Grignaschi N, Bodmer M, Aschmann YZ, Wenk M, Krähenbühl S. Pharmacokinetics of intravenous and oral midazolam in plasma and saliva in humans: usefulness of saliva as matrix for CYP3A phenotyping. Br J Clin Pharmacol. 2008 Oct;66(4):473-84.

**Phimmasone 2001** Phimmasone S, Kharasch ED. A pilot evaluation of alfentanil-induced miosis as a noninvasive probe for hepatic cytochrome P450 3A4 (CYP3A4) activity in humans. Clin Pharmacol Ther. 2001 Dec;70(6):505-17.

**Prueksaritanont 2017** Prueksaritanont T, Tatosian DA, Chu X, Railkar R, Evers R, Chavez-Eng C, Lutz R, Zeng W, Yabut J, Chan GH, Cai X, Latham AH, Hehman J, Stypinski D, Brejda J, Zhou C, Thornton B, Bateman KP, Fraser I, Stoch SA. Validation of a microdose probe drug cocktail for clinical drug interaction assessments for drug transporters and CYP3A. Clin Pharmacol Ther. 2017 Apr;101(4):519-530.

**Reitman 2011** Reitman ML, Chu X, Cai X, Yabut J, Venkatasubramanian R, Zajic S, Stone JA, Ding Y, Witter R, Gibson C, Roupe K, Evers R, Wagner JA, Stoch A. Rifampin's acute inhibitory and chronic inductive drug interactions: experimental and model-based approaches to drug-drug interaction trial design. Clin Pharmacol Ther. 2011 Feb;89(2):234-42.

**Shin 2013** Shin KH, Choi MH, Lim KS, Yu KS, Jang IJ, Cho JY. Evaluation of endogenous metabolic markers of hepatic CYP3A activity using metabolic profiling and midazolam clearance. Clin Pharmacol Ther. 2013 Nov;94(5):601-9.

**Shin 2016** Shin KH, Ahn LY, Choi MH, Moon JY, Lee J, Jang IJ, Yu KS, Cho JY. Urinary 6β-Hydroxycortisol/Cortisol Ratio Most Highly Correlates With Midazolam Clearance Under Hepatic CYP3A Inhibition and Induction in Females: A Pharmacometabolomics Approach. AAPS J. 2016 Sep;18(5):1254-1261.

**Szalat 2007** Szalat A, Gershkovich P, Ben-Ari A, Shaish A, Liberman Y, Boutboul E, Gotkine M, Hoffman A, Harats D, Leitersdorf E, Meiner V. Rifampicin-induced CYP3A4 activation in CTX patients cannot replace chenodeoxycholic acid treatment. Biochim Biophys Acta. 2007 Jul;1771(7):839-44.

**van Dyk 2018** van Dyk M, Marshall JC, Sorich MJ, Wood LS, Rowland A. Assessment of inter-racial variability in CYP3A4 activity and inducibility among healthy adult males of Caucasian and South Asian ancestries. Eur J Clin Pharmacol. 2018 Jul;74(7):913-920.

**Wiesinger 2020** Wiesinger H, Klein S, Rottmann A, Nowotn B, Riecke K, Gashaw I, Brudny-Klöppel M, Fricke R, Höchel J, Friedrich C. The effects of weak and strong CYP3A induction by rifampicin on the pharmacokinetics of five progestins and ethinylestradiol compared to midazolam. Clin Pharmacol Ther. 2020 Apr 10.

**Yu 2004** Yu KS, Cho JY, Jang IJ, Hong KS, Chung JY, Kim JR, Lim HS, Oh DS, Yi SY, Liu KH, Shin JG, Shin SG. Effect of the CYP3A5 genotype on the pharmacokinetics of intravenous midazolam during inhibited and induced metabolic states. Clin Pharmacol Ther. 2004 Aug;76(2):104-12.



## Rifampicin-Triazolam-DDI

**Villikka 1997** Villikka, K., Kivistö, K. T., Backman, J. T., Olkkola, K. T., & Neuvonen, P. J. (1997). Triazolam is ineffective in patients taking rifampin. *Clinical Pharmacology & Therapeutics*, *61*(1), 8-14.


# 5 Appendix
                   

## 5.1 Open Systems Pharmacology Suite (OSPS) Introduction
Open Systems Pharmacology Suite (OSP suite) is a tool for PBPK modeling and simulation of drugs in laboratory animals and humans. PK-Sim® and MoBi® are part of the OSP suite [[1](#References-for-OSPS-introduction)].  PK-Sim® is based on a generic PBPK-model with 18 organs and tissues. One of the main assumptions is that all compartments are well-stirred. Represented organs/tissues include arterial and venous blood, adipose tissue (separable adipose, excluding yellow marrow), brain, lung, bone (including yellow marrow), gonads, heart, kidneys, large intestine, liver, muscle, portal vein, pancreas, skin, small intestine, spleen and stomach, as shown in **Figure 1**.

Each organ consists of four sub-compartments namely the plasma, blood cells (which together build the vascular space), interstitial space, and cellular space. Distribution between the plasma and blood cells as well as between the interstitial and cellular compartments can be permeability-limited. In the brain, the permeation barrier is located between the vascular and the interstitial space. PK-Sim® estimates model parameters (intestinal permeability [[2](##References-for-OSPS-introduction)] organ partition coefficients (tissue-to-plasma partition coefficients) [[3,4](#References-for-OSPS-introduction)], and permeabilities) from physico-chemical properties of compounds (molecular weight, pKa, acid/base properties) and the composition of each tissue compartment (lipids, water and proteins). Partition coefficients can be calculated using a variety of methods available in PK-Sim®, for example the internal PK-Sim® method [[3,4](#References-for-OSPS-introduction)] or that of Rodgers and Rowland [[5-7](##References-for-OSPS-introduction)]. 

Physiological databases included in the software incorporate the dependencies of organ composition, organ weights, organ blood flows and gastrointestinal parameters (gastrointestinal length, radius of each section, intestinal surface area, gastrointestinal transit times, and pH in different intestinal segments [[2](#References-for-OSPS-introduction)]), with the user-defined body weight and height and ethnicity of the individual [[8](#References-for-OSPS-introduction)]. Thereby, PK Sim® allows generating realistic virtual populations. For a detailed description of the PBPK model structure implemented in PK Sim®, see Willmann et al. [[2,4,8,9](#References-for-OSPS-introduction)] or the OSP Suite homepage (<https://docs.open-systems-pharmacology.org/mechanistic-modeling-of-pharmacokinetics-and-dynamics/modeling-concepts>).


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


## 5.2 Mathematical Implementation of Drug-Drug Interactions


**DDI modeling: Competitive inhibition** 

A detailed representation of the mathematical implementation of competitive enzyme inhibition  can be found in the OSP manual [here](https://docs.open-systems-pharmacology.org/working-with-pk-sim/pk-sim-documentation/pk-sim-compounds-defining-inhibition-induction-processes#competitive-inhibition-simple-setting-with-one-inhibitor).



**DDI modeling: Mechanism-based inhibition**

A detailed representation of the mathematical implementation of mechanism-based enzyme inhibition  can be found in the OSP manual [here](https://docs.open-systems-pharmacology.org/working-with-pk-sim/pk-sim-documentation/pk-sim-compounds-defining-inhibition-induction-processes#irreversible-inhibition).



**DDI modeling: Induction**

A detailed representation of the mathematical implementation of enzyme induction can be found in the OSP manual [here](https://docs.open-systems-pharmacology.org/working-with-pk-sim/pk-sim-documentation/pk-sim-compounds-defining-inhibition-induction-processes#enzyme-induction).


## 5.3 Automatic (re)-qualification workflow
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




