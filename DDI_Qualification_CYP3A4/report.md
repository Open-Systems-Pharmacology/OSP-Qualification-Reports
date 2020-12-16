# CYP3A4 DDI Qualification




| Version                         | 1.1-OSP9.1                                                   |
| ------------------------------- | ------------------------------------------------------------ |
| Qualification Plan Release      | https://github.com/Open-Systems-Pharmacology/Qualification-DDI-CYP3A4/releases/tag/v1.1 |
| OSP Version                     | 9.1                                                          |
| Qualification Framework Version | 2.2                                                          |





This qualification report is filed at:

https://github.com/Open-Systems-Pharmacology/OSP-Qualification-Reports
# Table of Contents
  * [1 Introduction](#1-introduction)
    * [1.1 Objective](#11-objective)
    * [1.2 CYP3A4 DDI Network](#12-cyp3a4-ddi-network)
      * [Cimetidine - Alfentanil DDI](#cimetidine---alfentanil-ddi)
      * [Cimetidine - Alprazolam DDI](#cimetidine---alprazolam-ddi)
      * [Cimetidine - Midazolam DDI](#cimetidine---midazolam-ddi)
      * [Cimetidine - Triazolam DDI](#cimetidine---triazolam-ddi)
      * [Cimetidine - Verapamil DDI](#cimetidine---verapamil-ddi)
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
      * [Rifampicin - Verapamil DDI](#rifampicin---verapamil-ddi)
  * [2 Qualification of Use Case CYP3A4-mediated DDI](#2-qualification-of-use-case-cyp3a4-mediated-ddi)
    * [Mechanism](#mechanism)
      * [Competitive Inhibition](#competitive-inhibition)
      * [Induction](#induction)
      * [Mechanism based Inactivation](#mechanism-based-inactivation)
    * [Perpetrator](#perpetrator)
      * [Cimetidine](#cimetidine)
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
      * [Verapamil](#verapamil)
  * [3 Concentration-Time Profiles](#3-concentration-time-profiles)
    * [3.1 Cimetidine - Alfentanil DDI](#31-cimetidine---alfentanil-ddi)
    * [3.2 Cimetidine - Alprazolam DDI](#32-cimetidine---alprazolam-ddi)
    * [3.3 Cimetidine - Midazolam DDI](#33-cimetidine---midazolam-ddi)
    * [3.4 Cimetidine - Triazolam DDI](#34-cimetidine---triazolam-ddi)
    * [3.5 Cimetidine - Verapamil DDI](#35-cimetidine---verapamil-ddi)
    * [3.6 Clarithromycin - Midazolam DDI](#36-clarithromycin---midazolam-ddi)
    * [3.7 Clarithromycin - Triazolam DDI](#37-clarithromycin---triazolam-ddi)
    * [3.8 Erythromycin - Alfentanil DDI](#38-erythromycin---alfentanil-ddi)
    * [3.9 Erythromycin - Alprazolam DDI](#39-erythromycin---alprazolam-ddi)
    * [3.10 Erythromycin - Midazolam DDI](#310-erythromycin---midazolam-ddi)
    * [3.11 Erythromycin - Triazolam DDI](#311-erythromycin---triazolam-ddi)
    * [3.12 Fluvoxamine - Alprazolam DDI](#312-fluvoxamine---alprazolam-ddi)
    * [3.13 Fluvoxamine - Midazolam DDI](#313-fluvoxamine---midazolam-ddi)
    * [3.14 Itraconazole - Alprazolam DDI](#314-itraconazole---alprazolam-ddi)
    * [3.15 Itraconazole - Midazolam DDI](#315-itraconazole---midazolam-ddi)
    * [3.16 Itraconazole - Triazolam DDI](#316-itraconazole---triazolam-ddi)
    * [3.17 Verapamil - Midazolam DDI](#317-verapamil---midazolam-ddi)
    * [3.18 Efavirenz - Alfentanil DDI](#318-efavirenz---alfentanil-ddi)
    * [3.19 Efavirenz - Midazolam DDI](#319-efavirenz---midazolam-ddi)
    * [3.20 Rifampicin - Alfentanil DDI](#320-rifampicin---alfentanil-ddi)
    * [3.21 Rifampicin - Alprazolam DDI](#321-rifampicin---alprazolam-ddi)
    * [3.22 Rifampicin - Midazolam DDI](#322-rifampicin---midazolam-ddi)
    * [3.23 Rifampicin - Triazolam DDI](#323-rifampicin---triazolam-ddi)
    * [3.23 Rifampicin - Verapamil DDI](#323-rifampicin---verapamil-ddi)
  * [4 References](#4-references)
  * [5 Appendix](#5-appendix)
    * [5.1 Open Systems Pharmacology Suite (OSPS) Introduction](#51-open-systems-pharmacology-suite-osps-introduction)
    * [5.2 Mathematical Implementation of Drug-Drug Interactions](#52-mathematical-implementation-of-drug-drug-interactions)
    * [5.3 Automatic (re)-qualification workflow](#53-automatic-re-qualification-workflow)
# 1 Introduction
                   

## 1.1 Objective
This **qualification report** evaluates for the PBPK platform **PK-Sim** (as part of the open systems pharmacology (OSP) suite) the ability to perform simulations with the intended purpose to predict cytochrome P450 3A4 (**CYP3A4**)-mediated drug-drug interactions (**DDI**).

To demonstrate the level of confidence, the predictive performance of the platform for this indented purpose is assessed via a network of PBPK models of selected index CYP3A4 DDI perpetrators (covering the range from strong induction to strong inhibition), and respective sensitive index CYP3A4 victim drugs and a comprehensive dataset from published clinical DDI studies. All PBPK models represent whole-body PBPK models, which allow dynamic DDI simulations in organs expressing CYP3A4. 

The respective *qualification plan* to produce this *qualification report* is transparently provided open-source (https://github.com/Open-Systems-Pharmacology/OSP-Qualification-Reports). The same applies for all presented PBPK models including *evaluation reports* on model building and evaluation of each model (https://github.com/Open-Systems-Pharmacology/OSP-PBPK-Model-Library).

*Evaluation reports* including descriptions on model building and detailed evaluations of the included models are documented separately (see [Section 1.2](#12-CYP3A4-DDI-Network)).

Please refer to the [Appendix](#5-Appendix) to learn more details:

- An overview over the Open Systems Pharmacology Suite is given in chapter [Section 5.1](#51-Open-Systems-Pharmacology-Suite-(OSPS)-Introduction)

- [Section 5.2](#52-Mathematical-Implementation-of-Drug-Drug-Interactions) shows the implementation of the underlying mathematical equations for drug-drug interactions in the OSP suite.

- A detailed general description of the performed qualification workflow (*qualification plan*, *qualification report*, etc.) can be found in chapter [Section 5.3](#53-Automatic-(re)-qualification-workflow).

  



## 1.2 CYP3A4 DDI Network

To qualify the OSP suite for the prediction of the CYP3A4 DDI potential of new drugs, a set of verified PBPK models of index perpetrators, covering the range from strong CYP3A4 induction to strong inhibition, and respective CYP3A4 DDI victim drugs is specified to set up a CYP3A4-mediated DDI modeling network. 


The following perpetrator compounds were selected: 

- **Rifampicin** (strong CYP3A4 inducer)
  Model snapshot and evaluation plan (*release* **v1.1**): https://github.com/Open-Systems-Pharmacology/Rifampicin-Model/releases/tag/v1.1
- **Efavirenz** (moderate CYP3A4 inducer)
  Model snapshot and evaluation plan (*release* **v1.0**): https://github.com/Open-Systems-Pharmacology/Efavirenz-Model/releases/tag/v1.0
- **Cimetidine** (weak CYP3A4 inhibitor)
  Model snapshot and evaluation plan (*release* **v1.0**): https://github.com/Open-Systems-Pharmacology/Cimetidine-Model/releases/tag/v1.0
- **Fluvoxamine** (weak/moderate CYP3A4 inhibitor)
  Model snapshot and evaluation plan (*release* **v1.1**): https://github.com/Open-Systems-Pharmacology/Fluvoxamine-Model/releases/tag/v1.1
- **Verapamil** (moderate CYP3A4 inhibitor)
  Model snapshot and evaluation plan (*release* **v1.1**): https://github.com/Open-Systems-Pharmacology/Verapamil-Model/releases/tag/v1.1
- **Erythromycin** (moderate CYP3A4 inhibitor)
  Model snapshot and evaluation plan (*release* **v1.1**): https://github.com/Open-Systems-Pharmacology/Erythromycin-Model/releases/tag/v1.1
- **Clarithromycin** (strong CYP3A4 inhibitor)
  Model snapshot and evaluation plan (*release* **v1.1**): https://github.com/Open-Systems-Pharmacology/Clarithromycin-Model/releases/tag/v1.1
- **Itraconazole** including metabolites (strong CYP3A4 inhibitor)
  Model snapshot and evaluation plan (*release* **v1.2**): https://github.com/Open-Systems-Pharmacology/Itraconazole-Model/releases/tag/v1.2


The following sensitive CYP3A4 substrates as victim drugs were selected:

- **Midazolam**
  Model snapshot and evaluation plan (*release* **v1.0**): https://github.com/Open-Systems-Pharmacology/Midazolam-Model/releases/tag/v1.0
- **Triazolam**
  Model snapshot and evaluation plan (*release* **v1.0**): https://github.com/Open-Systems-Pharmacology/Triazolam-Model/releases/tag/v1.0
- **Alprazolam**
  Model snapshot and evaluation plan (*release* **v1.0**): https://github.com/Open-Systems-Pharmacology/Alprazolam-Model/releases/tag/v1.0
- **Alfentanil**
  Model snapshot and evaluation plan (*release* **v2.1**): https://github.com/Open-Systems-Pharmacology/Alfentanil-Model/releases/tag/v2.1



**Figure 1** shows the prespecified and developed DDI modeling network of interacting perpetrator and victim drugs for the OSP suite qualification of predicting CYP3A4-mediated DDI.



**Figure** **1: CYP3A4 DDI modeling network**
![DDI CYP3A4 network](images/DDI_CYP3A4_Compound_Network.png)

<sub>The arrows indicate where at least one clinical DDI study between the two connected substances was available and included in the model network. Red indicates inhibition and green indicates induction as the primary type of interaction. Thin arrows indicate weak, mid-thick arrows moderate and thick arrows strong CYP3A4 modulation by the perpetrator.</sub>



The published DDI studies between the respective perpetrators and victim drugs were simulated and compared to observed data. The following sections give an overview of the clinical studies being part of this qualification report. The respective data identifier (DataID) refers to the **ID** of the dataset in the [OSP PK database](https://github.com/Open-Systems-Pharmacology/Database-for-observed-data).


### Cimetidine - Alfentanil DDI
The release of the snapshot containing the respective simulations can be found here:
https://github.com/Open-Systems-Pharmacology/Cimetidine-Alfentanil-DDI/releases/tag/v1.0.

The cimetidine-alfentanil interaction was evaluated using a single clinical DDI study quantifying the interaction following two different dosing regimens ([Kienlen 1993](#4-References)).



| DataID | Enzyme | Perpetrator / victim       | Study design                                                 | Comment                                                      | Clinical study                        |
| ------ | ------ | -------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------- |
| 1344    | CYP3A4 | Cimetidine / alfentanil | Cimetidine: 1200 mg iv OD over 3 days<br />Alfentanil: 125 µg/kg iv on day 3 concomitantly with the cimetidine dose | No cross-over study! Parallel group design -> the two groups may not really be comparable given the low number of subjects and considering alfentanil PK variability | [Kienlen 1993](#4-References)          |


### Cimetidine - Alprazolam DDI
The release of the snapshot containing the respective simulations can be found here:
https://github.com/Open-Systems-Pharmacology/Cimetidine-Alprazolam-DDI/releases/tag/v1.0.

The cimetidine-alprazolam interaction was evaluated using two clinical DDI studies quantifying the interaction following two different dosing regimens ([Pourbaix 1985](#4-References), [Abernethy 1983](#4-References)).



| DataID | Enzyme | Perpetrator / victim       | Study design                                                 | Comment                                                      | Clinical study                        |
| ------ | ------ | -------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------- |
| 1340    | CYP3A4 | Cimetidine / alprazolam | Cimetidine: 200 mg po TID and 400 mg at bedtime over two weeks<br />Alprazolam: 0.5 mg po OD in the second week concomitantly with morning dose |                                                              | [Pourbaix 1985](#4-References)          |
| 1332    | CYP3A4 | Cimetidine / alprazolam | Cimetidine: 300 mg po QID (4 times)<br />Alprazolam: 1 mg po single dose concomitantly with cimetidine dose at 12 h |                                                              | [Abernethy 1983](#4-References)          |


### Cimetidine - Midazolam DDI
The release of the snapshot containing the respective simulations can be found here:
https://github.com/Open-Systems-Pharmacology/Cimetidine-Midazolam-DDI/releases/tag/v1.0.

The cimetidine-midazolam interaction was evaluated using five clinical DDI studies quantifying the interaction following six different dosing regimens ([Elliott 1984](#4-References), [Fee 1987](#4-References), [Greenblatt 1986](#4-References), [Martinez 1999](#4-References), [Salonen 1986](#4-References)).



| DataID | Enzyme | Perpetrator / victim       | Study design                                                 | Comment                                                      | Clinical study                        |
| ------ | ------ | -------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------- |
| 1346    | CYP3A4 | Cimetidine / midazolam | Cimetidine: 200 mg po TID and 400 mg nocte on day before study and 200 mg on study day <br />Midazolam: 7.5 mg po single dose, 2.5 hours after last cimetidine dose |                                                              | [Elliott 1984](#4-References)          |
| 1324    | CYP3A4 | Cimetidine / midazolam | Cimetidine: 400 mg po BID (3 times)<br />Midazolam: 15 mg po single dose, 1 hour after the last cimetidine dose |                                                              | [Fee 1987](#4-References)          |
| 1319    | CYP3A4 | Cimetidine / midazolam | Cimetidine: 300 mg po QID (8 times)<br />Midazolam: 5 mg iv single dose, concomitantly with the 5<sup>th</sup> cimetidine dose |                                                              | [Greenblatt 1986](#4-References)          |
| 1321    | CYP3A4 | Cimetidine / midazolam | Cimetidine: 300 mg po QID (8 times)<br />Midazolam: 15 mg po single dose concomitantly with the 5<sup>th</sup> cimetidine dose |                                                              | [Greenblatt 1986](#4-References)         |
| 1322    | CYP3A4 | Cimetidine / midazolam | Cimetidine: 800 mg po single dose <br />Midazolam: 7.5 mg po single dose concomitantly with cimetidine dose |                                                              | [Martinez 1999](#4-References)         |
| 1326   | CYP3A4 | Cimetidine / midazolam | Cimetidine: 400 mg po single dose<br />Midazolam: 15 mg po single dose 2 hours after cimetidine dose |                                                              | [Salonen 1986](#4-References) |


### Cimetidine - Triazolam DDI
The release of the snapshot containing the respective simulations can be found here:
https://github.com/Open-Systems-Pharmacology/Cimetidine-Triazolam-DDI/releases/tag/v1.0.

The cimetidine-triazolam interaction was evaluated using four clinical DDI studies quantifying the interaction following four different dosing regimens ([Pourbaix 1985](#4-References), [Abernethy 1983](#4-References), [Cox 1986](#4-References), [Friedman 1988](#4-References)).



| DataID | Enzyme | Perpetrator / victim       | Study design                                                 | Comment                                                      | Clinical study                        |
| ------ | ------ | -------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------- |
| 1342    | CYP3A4 | Cimetidine / triazolam | Cimetidine: 200 mg po TID and 400 mg at bedtime over two weeks<br />Triazolam: 0.5 mg po OD in the second week concomitantly with bedtime dose |                                                              | [Pourbaix 1985](#4-References)          |
| 1334    | CYP3A4 | Cimetidine / triazolam | Cimetidine: 300 mg po QID (4 times)<br />Triazolam: 0.5 mg po single dose concomitantly with cimetidine dose at 12 h |                                                              | [Abernethy 1983](#4-References)          |
| 1338    | CYP3A4 | Cimetidine / triazolam | Cimetidine: 300 mg po QID (4 times)<br />Triazolam: 0.5 mg intraduodenal single dose, 13 hours after study start |                                                              | [Cox 1986](#4-References)          |
| 1336    | CYP3A4 | Cimetidine / triazolam | Cimetidine: 300 mg po QID (8 times)<br />Triazolam: 0.5 mg po single dose concomitantly with the 5<sup>th</sup> cimetidine dose |                                                              | [Friedman 1988](#4-References)         |


### Cimetidine - Verapamil DDI
The release of the snapshot containing the respective simulations can be found here:
https://github.com/Open-Systems-Pharmacology/Cimetidine-Verapamil-DDI/releases/tag/v1.0.

The cimetidine-verapamil interaction was evaluated using a single clinical DDI study quantifying the interaction following two different dosing regimens ([Smith 1984](#4-References)).



| DataID | Enzyme | Perpetrator / victim       | Study design                                                 | Comment                                                      | Clinical study                        |
| ------ | ------ | -------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------- |
| 1328    | CYP3A4 | Cimetidine / verapamil | Cimetidine: 300 mg po QID over eight days<br />Verapamil: 10 mg iv on day 8 concomitantly with the morning dose |                                                              | [Smith 1984](#4-References)          |
| 1330    | CYP3A4 | Cimetidine / verapamil | Cimetidine: 300 mg po QID over eight days<br />Verapamil: 120 mg po on day 8 concomitantly with the morning dose |                                                              | [Smith 1984](#4-References)          |


### Clarithromycin - Midazolam DDI
The release of the snapshot containing the respective simulations can be found here:
https://github.com/Open-Systems-Pharmacology/Clarithromycin-Midazolam-DDI/releases/tag/v1.1

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
https://github.com/Open-Systems-Pharmacology/Clarithromycin-Triazolam-DDI/releases/tag/v1.1

The clarithromycin-triazolam interaction was evaluated using one clinical DDI study ([Greenblatt 1998a](#4-References)).



| DataID | Enzyme | Perpetrator / victim       | Study design                                                 | Clinical study                    |
| ------ | ------ | -------------------------- | ------------------------------------------------------------ | --------------------------------- |
| 1102   | CYP3A4 | Clarithromycin / triazolam | Clarithromycin: 500 mg po twice daily at irregular time intervals for 2 days<br />Triazolam: 0.125 mg po single dose, 1 hour after the 3<sup>rd</sup> clarithromycin dose | [Greenblatt 1998a](#4-References) |


### Erythromycin - Alfentanil DDI
The release of the snapshot containing the respective simulations can be found here:
https://github.com/Open-Systems-Pharmacology/Erythromycin-Alfentanil-DDI/releases/tag/v1.1

The erythromycin-alfentanil interaction was evaluated using one clinical DDI study ([Bartkowski 1989](#4-References)) quantifying the interaction following two different dosing regimens. Additionally, the plasma concentration-time profile of an individual investigated in this study was subsequently reported in a later study ([Bartkowski 1993](#4-References)).



| DataID | Enzyme | Perpetrator / victim      | Study design                                                 | Clinical study                   |
| ------ | ------ | ------------------------- | ------------------------------------------------------------ | -------------------------------- |
| 779    | CYP3A4 | Erythromycin / alfentanil | Erythromycin: 500 mg po single dose (enteric coated tablet containing erythromycin as free base)<br />Alfentanil: 0.05 mg/kg iv single dose, 1.5 hours after erythromycin dose | [Bartkowski 1989](#4-References) |
| 780    | CYP3A4 | Erythromycin / alfentanil | Erythromycin: 500 mg po BID for 7 days (enteric coated tablet containing erythromycin as free base)<br />Alfentanil: 0.05 mg/kg iv single dose, 1.5 hours after the 13<sup>th</sup> erythromycin dose | [Bartkowski 1989](#4-References) |



### Erythromycin - Alprazolam DDI
The release of the snapshot containing the respective simulations can be found here:
https://github.com/Open-Systems-Pharmacology/Erythromycin-Alprazolam-DDI/releases/tag/v1.1

The erythromycin-alprazolam interaction was evaluated using one clinical DDI study ([Yasui 1996](#4-References)).



| DataID | Enzyme | Perpetrator / victim      | Study design                                                 | Clinical study              |
| ------ | ------ | ------------------------- | ------------------------------------------------------------ | --------------------------- |
| 777    | CYP3A4 | Erythromycin / alprazolam | Erythromycin: 400 mg po TID for 10 days (filmcoated tablet containing erythromycin stearate)<br />Alprazolam: 0.8 mg po single dose, 2 hours after the 22<sup>nd</sup> erythromycin dose | [Yasui 1996](#4-References) |



### Erythromycin - Midazolam DDI
The release of the snapshot containing the respective simulations can be found here:
https://github.com/Open-Systems-Pharmacology/Erythromycin-Midazolam-DDI/releases/tag/v1.1

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
https://github.com/Open-Systems-Pharmacology/Erythromycin-Triazolam-DDI/releases/tag/v1.1

The erythromycin-triazolam interaction was evaluated using two clinical DDI studies ([Greenblatt 1998](#4-References), [Phillips 1986](#4-References)).



| DataID | Enzyme | Perpetrator / victim     | Study design                                                 | Clinical study                   |
| ------ | ------ | ------------------------ | ------------------------------------------------------------ | -------------------------------- |
| 781    | CYP3A4 | Erythromycin / triazolam | Erythromycin: 500 mg po twice daily for 2 days<br />Triazolam: 0.125 mg po single dose, 1 hour after the 3<sup>rd</sup> erythromycin dose | [Greenblatt 1998](#4-References) |
| 757    | CYP3A4 | Erythromycin / triazolam | Erythromycin: 333 mg po TID for 3 days<br />Triazolam: 0.5 mg po single dose, together with the last erythromycin dose | [Phillips 1986](#4-References)   |



### Fluvoxamine - Alprazolam DDI
The release of the snapshot containing the respective simulations can be found here:
https://github.com/Open-Systems-Pharmacology/Fluvoxamine-Alprazolam-DDI/releases/tag/v1.1

The fluvoxamine-alprazolam interaction was evaluated using one clinical DDI study quantifying the interaction following the first dose and in steady-state ([Fleishaker 1994](#4-References)).



| DataID | Enzyme | Perpetrator / victim     | Study design                                                 | Clinical study                   |
| ------ | ------ | ------------------------ | ------------------------------------------------------------ | -------------------------------- |
| 1104   | CYP3A4 | Fluvoxamine / alprazolam | Fluvoxamine: 50 mg fluvoxamine maleate QD for 3 days, followed by 100 mg fluvoxamine maleate QD for 7 days<br />Alprazolam: 1 mg po four times daily on Day 7 starting together with the 7<sup>th</sup> fluvoxamine dose | [Fleishaker 1994](#4-References) |
| 1113   | CYP3A4 | Fluvoxamine / alprazolam | Fluvoxamine: 50 mg fluvoxamine maleate QD for 3 days, followed by 100 mg fluvoxamine maleate QD for 7 days<br />Alprazolam: 1 mg po four times daily on Days 7 - 10 starting together with the 7<sup>th</sup> fluvoxamine dose | [Fleishaker 1994](#4-References) |



### Fluvoxamine - Midazolam DDI
The release of the snapshot containing the respective simulations can be found here:
https://github.com/Open-Systems-Pharmacology/Fluvoxamine-Midazolam-DDI/releases/tag/v1.1

The fluvoxamine / midazolam interaction was evaluated using two clinical DDI studies ([Kashuba 1998](#4-References), [Lam 2003](#4-References)).



| DataID | Enzyme | Perpetrator / victim    | Study design                                                 | Comment                                                      | Clinical study                 |
| ------ | ----------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------ | ------------------------------ |
| 2007 | CYP3A4 | Fluvoxamine / midazolam | Fluvoxamine: titrated to a daily dose of **150** mg (50 mg in the morning (6 a.m.), 50 mg in the evening (8 p.m.))<br />Midazolam: 0.025 mg/kg **iv** single dose, 3 hours after a morning fluvoxamine dose | **Observed data:**<br />Baseline (control) assessment: mean of six measures (every 2 weeks)<br />Phenotyping (fluvoxamine treatment) assessment:  mean of two measures (14 days and 28 days after the start of fluvoxamine treatment), midazolam administered at 9 a.m.<br />**Simulated**: the midazolam dose was administered 3 weeks after the start of fluvoxamine as an approximation of the two observed assessments | [Kashuba 1998](#4-References)  |
| 1089 | CYP3A4 | Fluvoxamine / midazolam | Fluvoxamine: titrated to a daily dose of **200** mg (100 mg BID)<br />Midazolam: 10 mg **po** single dose, 1 hour after a fluvoxamine steady state dose |  | [Lam 2003](#4-References) |
### Itraconazole - Alprazolam DDI
The release of the snapshot containing the respective simulations can be found here:
https://github.com/Open-Systems-Pharmacology/Itraconazole-Alprazolam-DDI/releases/tag/v1.1

The itraconazole / alprazolam interaction was evaluated using one clinical DDI study ([Yasui 1998](#4-References)).



| DataID | Enzyme | Perpetrator / victim    | Study design                                                 | Comment                                                      | Clinical study                 |
| ------ | ----------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------ | ------------------------------ |
| 1026 | CYP3A4 | Itraconazole / alprazolam | Itraconazole: **200** mg po once daily (6 doses, capsule fasted)<br />Alprazolam: 0.8 mg **po** single dose, 1 hour after **4<sup>th</sup>** itraconazole dose |  | [Yasui 1998](#4-References) |
### Itraconazole - Midazolam DDI
The release of the snapshot containing the respective simulations can be found here:
https://github.com/Open-Systems-Pharmacology/Itraconazole-Midazolam-DDI/releases/tag/v1.1

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
https://github.com/Open-Systems-Pharmacology/Itraconazole-Triazolam-DDI/releases/tag/v1.1

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
https://github.com/Open-Systems-Pharmacology/Verapamil-Midazolam-DDI/releases/tag/v1.1

The verapamil / midazolam interaction was evaluated using two clinical DDI studies including 3 different clinical settings ([Backman 1994](#4-References), [Wang 2005](#4-References)).



| DataID | Enzyme | Perpetrator / victim     | Study design                                                 | Comment                                                      | Clinical study                         |
| ------ | ------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | -------------------------------------- | -------------------------------------- |
| 1108 | CYP3A4 | Verapamil / midazolam | Verapamil: **80** mg po three times a day (5 doses)<br />Midazolam: 15 mg **po** single dose, 1 hours after **4<sup>th</sup>** verapamil dose |                                                              | [Backman 1994](#4-References) |
| 1111 | CYP3A4 | Verapamil / midazolam | Verapamil: **240** mg po once daily (7 doses, sustained release)<br />Midazolam: 0.05 mg/kg **iv** single dose, 24 hours after the **7<sup>th</sup>** verapamil dose |         | [Wang 2005](#4-References) |
| 1116   | CYP3A4 | Verapamil / midazolam | Verapamil: **240** mg po once daily (7 doses, sustained release)<br />Midazolam: 4 mg/kg **po** single dose, 48 hours after the **7<sup>th</sup>** verapamil dose |         | [Wang 2005](#4-References) |


### Efavirenz - Alfentanil-DDI
The release of the snapshot containing the respective simulations can be found here:
https://github.com/Open-Systems-Pharmacology/Efavirenz-Alfentanil-DDI/releases/tag/v1.1.

The efavirenz-alfentanil interaction was evaluated using one clinical DDI study that includes iv and oral administration of alfentanil ([Kharasch 2012](#4-References)).



| DataID | Enzyme | Perpetrator / victim   | Study design                                                 | Comment | Clinical study                 |
| ------ | ------ | ---------------------- | ------------------------------------------------------------ | ------- | ------------------------------ |
| 801    | CYP3A4 | Efavirenz / alfentanil | Efavirenz: 600 mg po OD for 20 days<br />Alfentanil: 43 µg/kg po single dose, 1/2 hour after the 15<sup>th</sup> efavirenz dose |         | [Kharasch 2012](#4-References) |
| 803    | CYP3A4 | Efavirenz / alfentanil | Efavirenz: 600 mg po OD for 20 days<br />Alfentanil: 15 µg/kg iv single dose, 1/2 hour after the 16<sup>th</sup> efavirenz dose |         | [Kharasch 2012](#4-References) |



### Efavirenz - Midazolam DDI
The release of the snapshot containing the respective simulations can be found here:
https://github.com/Open-Systems-Pharmacology/Efavirenz-Midazolam-DDI/releases/tag/v1.1

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
https://github.com/Open-Systems-Pharmacology/Rifampicin-Alfentanil-DDI/releases/tag/v1.1

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
https://github.com/Open-Systems-Pharmacology/Rifampicin-Alprazolam-DDI/releases/tag/v1.1

The rifampicin-alprazolam interaction was evaluated using two clinical DDI studies quantifying the interaction in three clinical settings ([Gashaw 2003](#4-References), [Schmider 1999](#4-References)).



| DataID | Enzyme | Perpetrator / victim    | Study design                                                 | Comments                                                     | Clinical study                 |
| ------ | ------ | ----------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------ |
| 2009   | CYP3A4 | Rifampicin / alprazolam | Rifampicin: 450 mg, five doses at irregular times intervals over 4 days<br />Alprazolam: 1 mg po single dose, 14 hours after the last rifampicin dose |                                                              | [Gashaw 2003](#4-References)   |
| 2010   | CYP3A4 | Rifampicin / alprazolam | Rifampicin: 450 mg, five doses at irregular times intervals over 4 days followed by a wash-out phase for 14 days<br />Alprazolam: 1 mg po single dose after the wash-out phase (i.e. 350 hours after the last rifampicin dose) |                                                              | [Gashaw 2003](#4-References)   |
| 1001   | CYP3A4 | Rifampicin / alprazolam | Rifampicin: 450 mg po QD for 4 days<br />Alprazolam: 1 mg po single dose, 24 hours after the last rifampicin dose | Administration time of alprazolam relative to rifampin not reported; it was assumed that alprazolam was administered 24h after the last rifampin dose | [Schmider 1999](#4-References) |



### Rifampicin - Midazolam DDI
The release of the snapshot containing the respective simulations can be found here:
https://github.com/Open-Systems-Pharmacology/Rifampicin-Midazolam-DDI/releases/tag/v1.1

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
https://github.com/Open-Systems-Pharmacology/Rifampicin-Triazolam-DDI/releases/tag/v1.1

The rifampicin-triazolam interaction was evaluated using one clinical DDI study ([Villikka 1997](#4-References)).



| DataID | Enzyme | Perpetrator / victim   | Study design                                                 | Comments | Clinical study                 |
| ------ | ------ | ---------------------- | ------------------------------------------------------------ | -------- | ------------------------------ |
| 1004   | CYP3A4 | Rifampicin / triazolam | Rifampicin: 600 mg QD for 5 days<br />Triazolam: 0.5 mg po single dose, 17 hours after the last rifampicin dose |          | [Villikka 1997](#4-References) |



### Rifampicin - Verapamil DDI
The release of the snapshot containing the respective simulations can be found here:
https://github.com/Open-Systems-Pharmacology/Rifampicin-Verapamil-DDI/releases/tag/v1.0

The  rifampicin / verapamil interaction was evaluated using 1 clinical DDI study including 2 different clinical settings ([Barbarash 1988](#4-References)).



| DataID | Enzyme, Transporter | Perpetrator / victim   | Study design                                                 | Comments | Clinical study                 |
| ------ | ------ | ---------------------- | ------------------------------------------------------------ | -------- | ------------------------------ |
| 2056   | CYP3A4 (and CYP2C8) | Rifampicin / verapamil | Rifampicin: 600 mg QD for 15 days<br />Verapamil: 10 mg iv single dose, 12 hours after the 13<sup>th</sup> rifampicin dose |          | [Barbarash 1988](#4-References) |
| 2058   | CYP3A4 (and CYP2C8), <br />P-gp* | Rifampicin / verapamil | Rifampicin: 600 mg QD for 15 days<br />Verapamil: 120 mg po single dose, 12 hours after the 15<sup>th</sup> rifampicin dose |          | [Barbarash 1988](#4-References) |

\* The substrate characteristics of verapamil towards P-gp are not considered in the verapamil PBPK model applied in this qualification (https://github.com/Open-Systems-Pharmacology/Verapamil-Model/releases/tag/v1.0).




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

GMFE (AUC) = 1.386372 

GMFE (CMAX) = 1.368272 

|AUC                       |Number|Ratio [%]|
|-------------------------:|-----:|--------:|
|Points total              |135   |-        |
|Points within Guest et al.|99    |73.3333  |
|Points within 2-fold      |118   |87.4074  |

|CMAX                      |Number|Ratio [%]|
|-------------------------:|-----:|--------:|
|Points total              |88    |-        |
|Points within Guest et al.|49    |55.6818  |
|Points within 2-fold      |80    |90.9091  |

|DataID|Perpetrator                                                                                                                                                                                                                       |Victim                  |Predicted AUC Ratio|Observed AUC Ratio|Pred/Obs AUC Ratio|Predicted CMAX Ratio|Observed CMAX Ratio|Pred/Obs CMAX Ratio|Reference           |
|-----:|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------:|-----------------------:|------------------:|-----------------:|-----------------:|-------------------:|------------------:|------------------:|-------------------:|
|1344  |Cimetidine, 1200 mg, IV, MD OD (2 days)                                                                                                                                                                                           |Alfentanil, IV          |1.0973             |2.8031            |0.39144           |1.0066              |-                  |-                  |Kienlen 1993        |
|1332  |Cimetidine, 300 mg, PO, MD QID (1 day)                                                                                                                                                                                            |Alprazolam, PO          |1.0087             |1.581             |0.63806           |1.0031              |1.0323             |0.97175            |Abernethy 1983      |
|1340  |Cimetidine, 200/400 mg, PO, (200mg): MD TID (17 days); (400mg): OD (17 days)                                                                                                                                                      |Alprazolam, PO          |1.0176             |1.7279            |0.58892           |1.0101              |1.8187             |0.55539            |Pourbaix 1985       |
|1319  |Cimetidine, 300 mg, PO, MD QID (2 days)                                                                                                                                                                                           |Midazolam, IV           |1.0103             |0.89256           |1.1319            |1.0001              |-                  |-                  |Greenblatt 1986     |
|1321  |Cimetidine, 300 mg, PO, MD QID (2 days)                                                                                                                                                                                           |Midazolam, PO           |1.1933             |1.1329            |1.0533            |1.1005              |1.0556             |1.0426             |Greenblatt 1986     |
|1322  |Cimetidine, 800 mg, PO, SD                                                                                                                                                                                                        |Midazolam, PO           |1.4776             |1.4973            |0.9868            |1.2463              |-                  |-                  |Martinez 1999       |
|1324  |Cimetidine, 400 mg, PO, MD: BID (1 day), OD (1 day)                                                                                                                                                                               |Midazolam, PO           |1.219              |1.3456            |0.9059            |1.1013              |-                  |-                  |Fee 1987            |
|1326  |Cimetidine, 400 mg, PO, SD                                                                                                                                                                                                        |Midazolam, PO           |1.1117             |1.3649            |0.8145            |1.1054              |1.3732             |0.80497            |Salonen 1986        |
|1346  |Cimetidine, 200/400 mg, PO, (200mg): MD TID (1 day), OD (1 day); (400mg): OD (1 day)                                                                                                                                              |Midazolam, PO           |1.0266             |2.016             |0.5092            |1.0235              |2.3833             |0.42945            |Elliott 1984        |
|1334  |Cimetidine, 300 mg, PO, MD QID (1 day)                                                                                                                                                                                            |Triazolam, PO           |1.6217             |1.5429            |1.0511            |1.419               |1.2041             |1.1785             |Abernethy 1983      |
|1336  |Cimetidine, 300 mg, PO, MD QID (2 days)                                                                                                                                                                                           |Triazolam, PO           |1.6243             |1.323             |1.2278            |1.4192              |1.3902             |1.0209             |Friedman 1988       |
|1342  |Cimetidine, 200/400 mg, PO, (200mg): MD TID (17 days); (400mg): OD (17 days)                                                                                                                                                      |Triazolam, PO           |1.6829             |2.2013            |0.76453           |1.4623              |1.5109             |0.96785            |Pourbaix 1985       |
|1338  |Cimetidine, 300 mg, PO, MD QID (1 day)                                                                                                                                                                                            |Triazolam, intraduodenal|1.4987             |1.5455            |0.96973           |1.3403              |1.3509             |0.99219            |Cox 1986            |
|1328  |Cimetidine, 300 mg, PO, MD QID (9 days)                                                                                                                                                                                           |Verapamil, IV           |1.0029             |0.70769           |1.4172            |1                   |0.95924            |1.0425             |Smith 1984          |
|1330  |Cimetidine, 300 mg, PO, MD QID (9 days)                                                                                                                                                                                           |Verapamil, PO           |1.5679             |1.3697            |1.1447            |1.47                |1.1333             |1.297              |Smith 1984          |
|175   |Clarithromycin, 500 mg, PO, MD BID (7 days)                                                                                                                                                                                       |Midazolam, IV           |3.0722             |2.6667            |1.1521            |1.2413              |-                  |-                  |Gorski 1998         |
|2027  |Clarithromycin, 500 mg, PO, MD BID (7 days)                                                                                                                                                                                       |Midazolam, IV           |3.0346             |3.2               |0.94832           |1.2413              |1.1724             |1.0587             |Quinney 2008        |
|173   |Clarithromycin, 500 mg, PO, MD BID (7 days)                                                                                                                                                                                       |Midazolam, PO           |9.2134             |7.1429            |1.2899            |3.0765              |-                  |-                  |Gorski 1998         |
|217   |Clarithromycin, 500 mg, PO, MD BID (7 days)                                                                                                                                                                                       |Midazolam, PO           |7.699              |8.3929            |0.91733           |2.7414              |3.7956             |0.72225            |Gurley 2006         |
|223   |Clarithromycin, 500 mg, PO, MD BID (7 days)                                                                                                                                                                                       |Midazolam, PO           |7.699              |5.4834            |1.4041            |2.7414              |2.1743             |1.2608             |Gurley 2008a        |
|354   |Clarithromycin, 500 mg, PO, MD BID (4 days)                                                                                                                                                                                       |Midazolam, PO           |6.0752             |5.5556            |1.0935            |2.6201              |-                  |-                  |Markert 2013        |
|1099  |Clarithromycin, 500 mg, PO, MD BID (5 days)                                                                                                                                                                                       |Midazolam, PO           |7.8478             |4.84              |1.6215            |3.177               |2.69               |1.181              |Prueksaritanont 2017|
|2030  |Clarithromycin, 500 mg, PO, MD BID (7 days)                                                                                                                                                                                       |Midazolam, PO           |9.3506             |8                 |1.1688            |3.1442              |2.75               |1.1433             |Quinney 2008        |
|2004  |Clarithromycin, 250 mg, PO, MD BID (3 days)                                                                                                                                                                                       |Midazolam, PO           |1.4904             |1.9               |0.7844            |1.2571              |1.75               |0.71833            |van Dyk 2018        |
|469   |Clarithromycin, 250 mg, PO, MD BID (5 days)                                                                                                                                                                                       |Midazolam, PO           |2.3752             |3.5716            |0.66504           |1.5939              |2.44               |0.65325            |Yeates 1996         |
|1102  |Clarithromycin, 500 mg, PO, MD OD (2 days)                                                                                                                                                                                        |Triazolam, PO           |3.5783             |5.06              |0.70718           |2.0063              |1.968              |1.0195             |Greenblatt 1998a    |
|779   |Erythromycin, 500 mg, PO, SD                                                                                                                                                                                                      |Alfentanil, IV          |1.0293             |1.0262            |1.0031            |1                   |-                  |-                  |Bartkowski 1989     |
|780   |Erythromycin, 500 mg, PO, MD BID (6 days)                                                                                                                                                                                         |Alfentanil, IV          |1.6878             |1.4611            |1.1551            |1.0269              |-                  |-                  |Bartkowski 1989     |
|777   |Erythromycin, 400 mg, PO, MD TID (10 days)                                                                                                                                                                                        |Alprazolam, PO          |1.7597             |2.4716            |0.71195           |1.0761              |1.1833             |0.90935            |Yasui 1996          |
|781   |Erythromycin, 500 mg, PO, MD OD (2 days)                                                                                                                                                                                          |Triazolam, PO           |3.1233             |3.65              |0.85569           |1.8985              |1.768              |1.0738             |Greenblatt 1998a    |
|757   |Erythromycin, 333 mg, PO, MD TID (3 days)                                                                                                                                                                                         |Triazolam, PO           |3.8725             |2.0597            |1.8802            |2.109               |1.4643             |1.4403             |Phillips 1986       |
|420   |Erythromycin, 500 mg, PO, MD QID (5 days)                                                                                                                                                                                         |Midazolam, IV           |2.3576             |1.5978            |1.4755            |1.027               |-                  |-                  |Swart 2002          |
|368   |Erythromycin, 500 mg, PO, MD TID (7 days)                                                                                                                                                                                         |Midazolam, IV           |2.0491             |1.9619            |1.0444            |1.0191              |-                  |-                  |Olkkola 1993        |
|366   |Erythromycin, 500 mg, PO, MD TID (7 days)                                                                                                                                                                                         |Midazolam, PO           |3.8603             |4.0674            |0.94909           |1.8908              |2.7                |0.70029            |Olkkola 1993        |
|471   |Erythromycin, 500 mg, PO, MD TID (3 days)                                                                                                                                                                                         |Midazolam, PO           |4.8526             |3.8137            |1.2724            |2.205               |2.7114             |0.81322            |Zimmermann 1996     |
|362   |Erythromycin, 200 mg, PO, MD QID (2 days)                                                                                                                                                                                         |Midazolam, PO           |1.2854             |1.16              |1.1081            |0.82212             |0.90909            |0.90434            |Okudaira 2007       |
|363   |Erythromycin, 200 mg, PO, MD QID (4 days)                                                                                                                                                                                         |Midazolam, PO           |1.6208             |1.69              |0.95908           |0.92675             |1.2                |0.77229            |Okudaira 2007       |
|364   |Erythromycin, 200 mg, PO, MD QID (7 days)                                                                                                                                                                                         |Midazolam, PO           |1.7024             |1.69              |1.0073            |0.94964             |1.1727             |0.80977            |Okudaira 2007       |
|828   |Erythromycin, 250 mg, PO, SD                                                                                                                                                                                                      |Midazolam, PO           |3.5088             |1.7178            |2.0426            |3.2106              |-                  |-                  |Carls 2014          |
|829   |Erythromycin, 1000 mg, PO, SD                                                                                                                                                                                                     |Midazolam, PO           |4.066              |4.9912            |0.81463           |3.6258              |-                  |-                  |Carls 2014          |
|1104  |Fluvoxamine, 50/100 mg, PO, MD OD (10 days), 50 mg day 1-3, then 100 mg                                                                                                                                                           |Alprazolam, PO          |1.006              |1.2551            |0.80147           |1.005               |1.1769             |0.85396            |Fleishaker 1994     |
|1113  |Fluvoxamine, 50/100 mg, PO, MD OD (10 days), 50 mg day 1-3, then 100 mg                                                                                                                                                           |Alprazolam, PO          |1.025              |1.9631            |0.52213           |1.022               |1.8619             |0.54891            |Fleishaker 1994     |
|2007  |Fluvoxamine, 50/100 mg, PO, MD BID (4 weeks), dose titration to 150 mg/day over 7 days: 50 mg in the evening for 3 days, 50 mg in the morning and evening for the next 3 days, then 50 mg in the morning and 100 mg in the evening|Midazolam, IV           |1.0403             |1.5               |0.69355           |1.0017              |-                  |-                  |Kashuba 1998        |
|1089  |Fluvoxamine, 50/100 mg, PO, MD OD (12 days), titrated from 50 mg BID to 100 mg BID administered for 6 days                                                                                                                        |Midazolam, PO           |1.4031             |1.66              |0.84522           |1.2015              |1.63               |0.73709            |Lam 2003            |
|1026  |Itraconazole, 200 mg, PO, MD OD (6 days)                                                                                                                                                                                          |Alprazolam, PO          |2.1733             |2.6627            |0.81622           |1.0994              |1.2868             |0.85432            |Yasui 1998          |
|378   |Itraconazole, 200 mg, PO, MD OD (4 days)                                                                                                                                                                                          |Midazolam, IV           |2.2908             |3.2258            |0.71016           |1.0117              |-                  |-                  |Olkkola 1996        |
|199   |Itraconazole, 200 mg, PO, MD OD (4 days)                                                                                                                                                                                          |Midazolam, IV           |2.4587             |3.3333            |0.73761           |1.0112              |-                  |-                  |Yu 2004             |
|50    |Itraconazole, 100 mg, PO, MD OD (4 days)                                                                                                                                                                                          |Midazolam, PO           |3.4803             |5.7451            |0.60579           |1.9613              |2.5588             |0.7665             |Ahonen 1995         |
|58    |Itraconazole, 200 mg, PO, MD OD (4 days)                                                                                                                                                                                          |Midazolam, PO           |4.8857             |7.97              |0.61301           |2.2277              |3.12               |0.71402            |Backman 1998        |
|59    |Itraconazole, 200 mg, PO, MD OD (4 days)                                                                                                                                                                                          |Midazolam, PO           |1.1256             |2.63              |0.42797           |1.074               |1.92               |0.55939            |Backman 1998        |
|370   |Itraconazole, 200 mg, PO, MD OD (4 days)                                                                                                                                                                                          |Midazolam, PO           |5.2868             |10.8              |0.48952           |2.2377              |3.4                |0.65813            |Olkkola 1994        |
|377   |Itraconazole, 200 mg, PO, SD                                                                                                                                                                                                      |Midazolam, PO           |4.4916             |3.4               |1.3211            |2.1997              |1.8                |1.222              |Olkkola 1996        |
|379   |Itraconazole, 200 mg, PO, MD OD (6 days)                                                                                                                                                                                          |Midazolam, PO           |6.244              |6.6               |0.94606           |2.5665              |2.5                |1.0266             |Olkkola 1996        |
|1097  |Itraconazole, 200 mg, PO, MD OD (5 days)                                                                                                                                                                                          |Midazolam, PO           |19.3578            |7.04              |2.7497            |4.6651              |3.71               |1.2575             |Prueksaritanont 2017|
|424   |Itraconazole, 50 mg, PO, SD                                                                                                                                                                                                       |Midazolam, PO           |3.2607             |2                 |1.6304            |2.2008              |-                  |-                  |Templeton 2010      |
|425   |Itraconazole, 200 mg, PO, SD                                                                                                                                                                                                      |Midazolam, PO           |7.6015             |4.7               |1.6173            |3.4395              |-                  |-                  |Templeton 2010      |
|426   |Itraconazole, 400 mg, PO, SD                                                                                                                                                                                                      |Midazolam, PO           |9.7471             |5.4               |1.805             |3.7303              |-                  |-                  |Templeton 2010      |
|1078  |Itraconazole, 200 mg, PO, SD                                                                                                                                                                                                      |Triazolam, PO           |4.2175             |3.11              |1.3561            |1.9807              |1.41               |1.4048             |Neuvonen 1996       |
|1079  |Itraconazole, 200 mg, PO, SD                                                                                                                                                                                                      |Triazolam, PO           |5.5923             |4.79              |1.1675            |2.4222              |1.76               |1.3763             |Neuvonen 1996       |
|1080  |Itraconazole, 200 mg, PO, SD                                                                                                                                                                                                      |Triazolam, PO           |2.252              |4.63              |0.48639           |1.6681              |1.76               |0.94776            |Neuvonen 1996       |
|1081  |Itraconazole, 200 mg, PO, SD                                                                                                                                                                                                      |Triazolam, PO           |2.0983             |3.82              |0.54928           |1.3854              |1.71               |0.81017            |Neuvonen 1996       |
|1029  |Itraconazole, 200 mg, PO, MD OD (4 days)                                                                                                                                                                                          |Triazolam, PO           |6.3408             |19.0287           |0.33322           |2.5313              |2.6854             |0.94261            |Varhe 1994          |
|1111  |Verapamil, 240 mg, PO, MD OD (7 days)                                                                                                                                                                                             |Midazolam, IV           |1.4027             |1.4524            |0.96579           |1.1019              |-                  |-                  |Wang 2005           |
|1108  |Verapamil, 80 mg, PO, MD TID (2 days)                                                                                                                                                                                             |Midazolam, PO           |2.0138             |2.9167            |0.69043           |1.4415              |1.9692             |0.732              |Backman 1994        |
|1116  |Verapamil, 240 mg, PO, MD OD (7 days)                                                                                                                                                                                             |Midazolam, PO           |1.6229             |3.5056            |0.46295           |1.3474              |-                  |-                  |Wang 2005           |
|803   |Efavirenz, 600 mg, PO, MD OD (19 days)                                                                                                                                                                                            |Alfentanil, IV          |0.55982            |0.54              |1.0367            |0.92176             |1.0978             |0.83962            |Kharasch 2012       |
|801   |Efavirenz, 600 mg, PO, MD OD (19 days)                                                                                                                                                                                            |Alfentanil, PO          |0.23488            |0.22              |1.0676            |0.35697             |0.42857            |0.83293            |Kharasch 2012       |
|2045  |Efavirenz, 400 mg, PO, SD                                                                                                                                                                                                         |Midazolam, IV           |0.83136            |0.78538           |1.0586            |0.93223             |-                  |-                  |Mikus 2017          |
|2048  |Efavirenz, 400 mg, PO, SD                                                                                                                                                                                                         |Midazolam, IV           |0.78761            |0.77712           |1.0135            |0.91054             |-                  |-                  |Mikus 2017          |
|2050  |Efavirenz, 400 mg, PO, SD                                                                                                                                                                                                         |Midazolam, IV           |0.85881            |0.9375            |0.91607           |0.94266             |-                  |-                  |Mikus 2017          |
|2052  |Efavirenz, 400 mg, PO, SD                                                                                                                                                                                                         |Midazolam, IV           |0.91313            |0.85377           |1.0695            |0.96565             |-                  |-                  |Mikus 2017          |
|2054  |Efavirenz, 400 mg, PO, SD                                                                                                                                                                                                         |Midazolam, IV           |0.9501             |0.92217           |1.0303            |0.9806              |-                  |-                  |Mikus 2017          |
|2041  |Efavirenz, 400 mg, PO, MD OD (14 days)                                                                                                                                                                                            |Midazolam, PO           |0.11474            |0.1027            |1.1172            |0.23823             |0.1806             |1.3191             |Katzenmaier 2010    |
|2044  |Efavirenz, 400 mg, PO, SD                                                                                                                                                                                                         |Midazolam, PO           |0.52617            |0.59055           |0.89098           |0.64634             |-                  |-                  |Mikus 2017          |
|2047  |Efavirenz, 400 mg, PO, SD                                                                                                                                                                                                         |Midazolam, PO           |0.54513            |0.61417           |0.88758           |0.6553              |-                  |-                  |Mikus 2017          |
|2049  |Efavirenz, 400 mg, PO, SD                                                                                                                                                                                                         |Midazolam, PO           |0.70481            |0.76968           |0.91571           |0.7843              |-                  |-                  |Mikus 2017          |
|2051  |Efavirenz, 400 mg, PO, SD                                                                                                                                                                                                         |Midazolam, PO           |0.819              |0.74803           |1.0949            |0.87157             |-                  |-                  |Mikus 2017          |
|2053  |Efavirenz, 400 mg, PO, SD                                                                                                                                                                                                         |Midazolam, PO           |0.8959             |0.83661           |1.0709            |0.92682             |-                  |-                  |Mikus 2017          |
|278   |Rifampicin, 600 mg, PO, MD OD (5 days)                                                                                                                                                                                            |Alfentanil, IV          |0.35971            |0.36301           |0.9909            |0.89694             |-                  |-                  |Kharasch 1997       |
|283   |Rifampicin, 600 mg, PO, MD OD (6 days)                                                                                                                                                                                            |Alfentanil, IV          |0.48813            |0.375             |1.3017            |1.2012              |1.0033             |1.1972             |Kharasch 2004       |
|299   |Rifampicin, 5 mg, PO, MD OD (6 days)                                                                                                                                                                                              |Alfentanil, IV          |0.98482            |0.83              |1.1865            |1.3091              |1.0392             |1.2597             |Kharasch 2011       |
|300   |Rifampicin, 10 mg, PO, MD OD (6 days)                                                                                                                                                                                             |Alfentanil, IV          |0.84898            |0.75              |1.132             |1.2935              |1.049              |1.233              |Kharasch 2011       |
|301   |Rifampicin, 25 mg, PO, MD OD (6 days)                                                                                                                                                                                             |Alfentanil, IV          |0.69486            |0.59              |1.1777            |1.2671              |1                  |1.2671             |Kharasch 2011       |
|302   |Rifampicin, 75 mg, PO, MD OD (6 days)                                                                                                                                                                                             |Alfentanil, IV          |0.57588            |0.51              |1.1292            |1.2354              |1.0294             |1.2001             |Kharasch 2011       |
|763   |Rifampicin, 600 mg, PO, MD OD (6 days)                                                                                                                                                                                            |Alfentanil, IV          |0.36202            |0.4               |0.90506           |0.89854             |-                  |-                  |Kharasch 2011b      |
|767   |Rifampicin, 600 mg, PO, MD OD (6 days)                                                                                                                                                                                            |Alfentanil, IV          |0.35767            |0.4               |0.89416           |0.89637             |-                  |-                  |Kharasch 2011b      |
|391   |Rifampicin, 600 mg, PO, MD OD (5 days)                                                                                                                                                                                            |Alfentanil, IV          |0.3631             |0.55              |0.66018           |0.89919             |-                  |-                  |Phimmasone 2001     |
|288   |Rifampicin, 600 mg, PO, MD OD (6 days)                                                                                                                                                                                            |Alfentanil, PO          |0.039185           |0.045631          |0.85873           |0.087               |0.11111            |0.783              |Kharasch 2004       |
|309   |Rifampicin, 5 mg, PO, MD OD (6 days)                                                                                                                                                                                              |Alfentanil, PO          |0.46114            |0.74              |0.62316           |0.59606             |0.86275            |0.69088            |Kharasch 2011       |
|310   |Rifampicin, 10 mg, PO, MD OD (6 days)                                                                                                                                                                                             |Alfentanil, PO          |0.32464            |0.61              |0.5322            |0.46881             |0.86275            |0.5434             |Kharasch 2011       |
|311   |Rifampicin, 25 mg, PO, MD OD (6 days)                                                                                                                                                                                             |Alfentanil, PO          |0.18765            |0.3               |0.62552           |0.31358             |0.4902             |0.63971            |Kharasch 2011       |
|312   |Rifampicin, 75 mg, PO, MD OD (6 days)                                                                                                                                                                                             |Alfentanil, PO          |0.095594           |0.13              |0.73534           |0.18365             |0.2549             |0.72046            |Kharasch 2011       |
|771   |Rifampicin, 600 mg, PO, MD OD (6 days)                                                                                                                                                                                            |Alfentanil, PO          |0.037949           |0.06              |0.63248           |0.083994            |-                  |-                  |Kharasch 2011b      |
|775   |Rifampicin, 600 mg, PO, MD OD (6 days)                                                                                                                                                                                            |Alfentanil, PO          |0.037079           |0.06              |0.61798           |0.082592            |-                  |-                  |Kharasch 2011b      |
|2009  |Rifampicin, 450 mg, PO, MD, q.d. for 5 days                                                                                                                                                                                       |Alprazolam, PO          |0.1875             |0.17935           |1.0455            |0.67772             |-                  |-                  |Gashaw 2003         |
|2010  |Rifampicin, 450 mg, PO, MD, q.d. for 5 days                                                                                                                                                                                       |Alprazolam, PO          |0.96407            |0.91667           |1.0517            |0.9951              |-                  |-                  |Gashaw 2003         |
|1001  |Rifampicin, 450 mg, PO, MD OD (4 days)                                                                                                                                                                                            |Alprazolam, PO          |0.19835            |0.11726           |1.6915            |0.68932             |0.63816            |1.0802             |Schmider 1999       |
|179   |Rifampicin, 600 mg, PO, MD OD (7 days)                                                                                                                                                                                            |Midazolam, IV           |0.49105            |0.44898           |1.0937            |0.75209             |-                  |-                  |Gorski 2003         |
|276   |Rifampicin, 600 mg, PO, MD OD (5 days)                                                                                                                                                                                            |Midazolam, IV           |0.47345            |0.37931           |1.2482            |0.90482             |-                  |-                  |Kharasch 1997       |
|280   |Rifampicin, 600 mg, PO, MD OD (6 days)                                                                                                                                                                                            |Midazolam, IV           |0.47571            |0.52113           |0.91284           |0.90853             |1.01               |0.89957            |Kharasch 2004       |
|294   |Rifampicin, 5 mg, PO, MD OD (6 days)                                                                                                                                                                                              |Midazolam, IV           |0.78053            |0.84              |0.9292            |0.98019             |1.0323             |0.94956            |Kharasch 2011       |
|295   |Rifampicin, 10 mg, PO, MD OD (6 days)                                                                                                                                                                                             |Midazolam, IV           |0.69874            |0.77              |0.90746           |0.9682              |1.0645             |0.90952            |Kharasch 2011       |
|296   |Rifampicin, 25 mg, PO, MD OD (6 days)                                                                                                                                                                                             |Midazolam, IV           |0.60481            |0.63              |0.96002           |0.9493              |0.83871            |1.1319             |Kharasch 2011       |
|297   |Rifampicin, 75 mg, PO, MD OD (6 days)                                                                                                                                                                                             |Midazolam, IV           |0.53127            |0.6               |0.88544           |0.92855             |1.3226             |0.70208            |Kharasch 2011       |
|2036  |Rifampicin, 600 mg, PO, MD OD (10 days)                                                                                                                                                                                           |Midazolam, IV           |1.1815             |1.15              |1.0274            |2.2563              |-                  |-                  |Kim 2018            |
|342   |Rifampicin, 600 mg, PO, MD OD (6 days)                                                                                                                                                                                            |Midazolam, IV           |0.47026            |0.65501           |0.71794           |0.90365             |1.106              |0.81708            |Link 2008           |
|389   |Rifampicin, 600 mg, PO, MD OD (5 days)                                                                                                                                                                                            |Midazolam, IV           |0.47603            |0.51              |0.93339           |0.907               |-                  |-                  |Phimmasone 2001     |
|1092  |Rifampicin, 600 mg, PO, MD OD (10 days)                                                                                                                                                                                           |Midazolam, IV           |1.1815             |1.15              |1.0274            |2.2563              |-                  |-                  |Shin 2013           |
|1095  |Rifampicin, 600 mg, PO, MD OD (10 days)                                                                                                                                                                                           |Midazolam, IV           |1.1815             |1.225             |0.96453           |2.2563              |1.775              |1.2712             |Shin 2016           |
|422   |Rifampicin, 600 mg, PO, MD OD (7 days)                                                                                                                                                                                            |Midazolam, IV           |0.49105            |0.57947           |0.84742           |0.75222             |-                  |-                  |Szalat 2007         |
|202   |Rifampicin, 600 mg, PO, MD OD (10 days)                                                                                                                                                                                           |Midazolam, IV           |0.83493            |0.83333           |1.0019            |1.8917              |-                  |-                  |Yu 2004             |
|54    |Rifampicin, 600 mg, PO, MD OD (5 days)                                                                                                                                                                                            |Midazolam, PO           |0.038106           |0.041             |0.92941           |0.098048            |0.061818           |1.5861             |Backman 1996        |
|56    |Rifampicin, 600 mg, PO, MD OD (5 days)                                                                                                                                                                                            |Midazolam, PO           |0.038143           |0.023             |1.6584            |0.098049            |0.054              |1.8157             |Backman 1998        |
|57    |Rifampicin, 600 mg, PO, MD OD (5 days)                                                                                                                                                                                            |Midazolam, PO           |0.11806            |0.132             |0.89436           |0.22359             |0.202              |1.1069             |Backman 1998        |
|113   |Rifampicin, 600 mg, PO, MD OD (9 days)                                                                                                                                                                                            |Midazolam, PO           |0.028237           |0.12449           |0.22682           |0.070021            |0.16957            |0.41294            |Chung 2006          |
|132   |Rifampicin, 450 mg, PO, MD OD (5 days)                                                                                                                                                                                            |Midazolam, PO           |0.033781           |0.052239          |0.64666           |0.08487             |0.11154            |0.7609             |Eap 2004            |
|177   |Rifampicin, 600 mg, PO, MD OD (7 days)                                                                                                                                                                                            |Midazolam, PO           |0.047557           |0.10335           |0.46015           |0.11675             |0.067039           |1.7415             |Gorski 2003         |
|215   |Rifampicin, 300 mg, PO, MD BID (7 days)                                                                                                                                                                                           |Midazolam, PO           |0.043421           |0.057161          |0.75962           |0.10788             |0.12092            |0.89216            |Gurley 2006         |
|221   |Rifampicin, 300 mg, PO, MD BID (7 days)                                                                                                                                                                                           |Midazolam, PO           |0.043421           |0.060317          |0.71987           |0.10788             |0.10762            |1.0023             |Gurley 2008a        |
|286   |Rifampicin, 600 mg, PO, MD OD (6 days)                                                                                                                                                                                            |Midazolam, PO           |0.035796           |0.052632          |0.68013           |0.075637            |0.10989            |0.6883             |Kharasch 2004       |
|304   |Rifampicin, 5 mg, PO, MD OD (6 days)                                                                                                                                                                                              |Midazolam, PO           |0.42307            |0.8               |0.52884           |0.55551             |0.8                |0.69438            |Kharasch 2011       |
|305   |Rifampicin, 10 mg, PO, MD OD (6 days)                                                                                                                                                                                             |Midazolam, PO           |0.2916             |0.68              |0.42882           |0.42549             |0.93333            |0.45588            |Kharasch 2011       |
|306   |Rifampicin, 25 mg, PO, MD OD (6 days)                                                                                                                                                                                             |Midazolam, PO           |0.16308            |0.4               |0.40769           |0.27343             |0.50667            |0.53966            |Kharasch 2011       |
|307   |Rifampicin, 75 mg, PO, MD OD (6 days)                                                                                                                                                                                             |Midazolam, PO           |0.080927           |0.25              |0.32371           |0.15436             |0.34               |0.45399            |Kharasch 2011       |
|344   |Rifampicin, 600 mg, PO, MD OD (6 days)                                                                                                                                                                                            |Midazolam, PO           |0.03022            |0.015549          |1.9435            |0.07709             |0.034865           |2.2111             |Link 2008           |
|1098  |Rifampicin, 600 mg, PO, SD                                                                                                                                                                                                        |Midazolam, PO           |2.2424             |0.94              |2.3856            |1.88                |1.3                |1.4461             |Prueksaritanont 2017|
|392   |Rifampicin, 600 mg, PO, MD OD (28 days)                                                                                                                                                                                           |Midazolam, PO           |0.20272            |0.123             |1.6481            |0.26564             |0.162              |1.6397             |Reitman 2011        |
|393   |Rifampicin, 600 mg, PO, MD OD (28 days)                                                                                                                                                                                           |Midazolam, PO           |0.35111            |0.383             |0.91673           |0.48815             |0.403              |1.2113             |Reitman 2011        |
|394   |Rifampicin, 600 mg, PO, MD OD (28 days)                                                                                                                                                                                           |Midazolam, PO           |0.91636            |0.815             |1.1244            |0.94285             |0.731              |1.2898             |Reitman 2011        |
|2002  |Rifampicin, 300 mg, PO, MD OD (7 days)                                                                                                                                                                                            |Midazolam, PO           |0.041765           |0.25641           |0.16288           |0.08178             |0.375              |0.21808            |van Dyk 2018        |
|204   |Rifampicin, 10 mg, PO, MD OD (22 days)                                                                                                                                                                                            |Midazolam, PO           |0.26865            |0.539             |0.49842           |0.40212             |0.63265            |0.6356             |Wiesinger 2020      |
|205   |Rifampicin, 600 mg, PO, MD OD (22 days)                                                                                                                                                                                           |Midazolam, PO           |0.029255           |0.137             |0.21354           |0.06674             |0.18755            |0.35585            |Wiesinger 2020      |
|1004  |Rifampicin, 600 mg, PO, MD OD (5 days)                                                                                                                                                                                            |Triazolam, PO           |0.033137           |0.051             |0.64975           |0.11455             |0.12414            |0.92277            |Villikka 1997       |
|2056  |Rifampicin, 600 mg, PO, MD OD (13 days)                                                                                                                                                                                           |Verapamil, IV           |0.84349            |0.81865           |1.0303            |0.97751             |-                  |-                  |Barbarash 1988      |
|2058  |Rifampicin, 600 mg, PO, MD OD (15 days)                                                                                                                                                                                           |Verapamil, PO           |0.10604            |0.06511           |1.6286            |0.14753             |0.036961           |3.9915             |Barbarash 1988      |

## Mechanism

### Competitive Inhibition

![001_plotDDIRatioAUCPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/001_Mechanism/001_Competitive_Inhibition/001_plotDDIRatioAUCPredictedVsObserved.png)

![002_plotDDIRatioAUCResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/001_Mechanism/001_Competitive_Inhibition/002_plotDDIRatioAUCResidualsVsObserved.png)

![003_plotDDIRatioCMAXPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/001_Mechanism/001_Competitive_Inhibition/003_plotDDIRatioCMAXPredictedVsObserved.png)

![004_plotDDIRatioCMAXResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/001_Mechanism/001_Competitive_Inhibition/004_plotDDIRatioCMAXResidualsVsObserved.png)

GMFE (AUC) = 1.488414 

GMFE (CMAX) = 1.272584 

|AUC                       |Number|Ratio [%]|
|-------------------------:|-----:|--------:|
|Points total              |37    |-        |
|Points within Guest et al.|21    |56.7568  |
|Points within 2-fold      |31    |83.7838  |

|CMAX                      |Number|Ratio [%]|
|-------------------------:|-----:|--------:|
|Points total              |27    |-        |
|Points within Guest et al.|18    |66.6667  |
|Points within 2-fold      |26    |96.2963  |

### Induction

![001_plotDDIRatioAUCPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/001_Mechanism/002_Induction/001_plotDDIRatioAUCPredictedVsObserved.png)

![002_plotDDIRatioAUCResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/001_Mechanism/002_Induction/002_plotDDIRatioAUCResidualsVsObserved.png)

![003_plotDDIRatioCMAXPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/001_Mechanism/002_Induction/003_plotDDIRatioCMAXPredictedVsObserved.png)

![004_plotDDIRatioCMAXResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/001_Mechanism/002_Induction/004_plotDDIRatioCMAXResidualsVsObserved.png)

GMFE (AUC) = 1.379900 

GMFE (CMAX) = 1.485651 

|AUC                       |Number|Ratio [%]|
|-------------------------:|-----:|--------:|
|Points total              |70    |-        |
|Points within Guest et al.|54    |77.1429  |
|Points within 2-fold      |61    |87.1429  |

|CMAX                      |Number|Ratio [%]|
|-------------------------:|-----:|--------:|
|Points total              |44    |-        |
|Points within Guest et al.|18    |40.9091  |
|Points within 2-fold      |37    |84.0909  |

### Mechanism based Inactivation

![001_plotDDIRatioAUCPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/001_Mechanism/003_Mechanism_based_Inactivation/001_plotDDIRatioAUCPredictedVsObserved.png)

![002_plotDDIRatioAUCResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/001_Mechanism/003_Mechanism_based_Inactivation/002_plotDDIRatioAUCResidualsVsObserved.png)

![003_plotDDIRatioCMAXPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/001_Mechanism/003_Mechanism_based_Inactivation/003_plotDDIRatioCMAXPredictedVsObserved.png)

![004_plotDDIRatioCMAXResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/001_Mechanism/003_Mechanism_based_Inactivation/004_plotDDIRatioCMAXResidualsVsObserved.png)

GMFE (AUC) = 1.277032 

GMFE (CMAX) = 1.240697 

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

### Cimetidine

![001_plotDDIRatioAUCPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/002_Perpetrator/001_Cimetidine/001_plotDDIRatioAUCPredictedVsObserved.png)

![002_plotDDIRatioAUCResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/002_Perpetrator/001_Cimetidine/002_plotDDIRatioAUCResidualsVsObserved.png)

![003_plotDDIRatioCMAXPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/002_Perpetrator/001_Cimetidine/003_plotDDIRatioCMAXPredictedVsObserved.png)

![004_plotDDIRatioCMAXResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/002_Perpetrator/001_Cimetidine/004_plotDDIRatioCMAXResidualsVsObserved.png)

GMFE (AUC) = 1.316350 

GMFE (CMAX) = 1.226719 

|AUC                       |Number|Ratio [%]|
|-------------------------:|-----:|--------:|
|Points total              |15    |-        |
|Points within Guest et al.|9     |60       |
|Points within 2-fold      |14    |93.3333  |

|CMAX                      |Number|Ratio [%]|
|-------------------------:|-----:|--------:|
|Points total              |11    |-        |
|Points within Guest et al.|6     |54.5455  |
|Points within 2-fold      |10    |90.9091  |

### Clarithromycin

![001_plotDDIRatioAUCPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/002_Perpetrator/002_Clarithromycin/001_plotDDIRatioAUCPredictedVsObserved.png)

![002_plotDDIRatioAUCResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/002_Perpetrator/002_Clarithromycin/002_plotDDIRatioAUCResidualsVsObserved.png)

![003_plotDDIRatioCMAXPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/002_Perpetrator/002_Clarithromycin/003_plotDDIRatioCMAXPredictedVsObserved.png)

![004_plotDDIRatioCMAXResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/002_Perpetrator/002_Clarithromycin/004_plotDDIRatioCMAXResidualsVsObserved.png)

GMFE (AUC) = 1.266724 

GMFE (CMAX) = 1.235285 

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

![001_plotDDIRatioAUCPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/002_Perpetrator/003_Efavirenz/001_plotDDIRatioAUCPredictedVsObserved.png)

![002_plotDDIRatioAUCResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/002_Perpetrator/003_Efavirenz/002_plotDDIRatioAUCResidualsVsObserved.png)

![003_plotDDIRatioCMAXPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/002_Perpetrator/003_Efavirenz/003_plotDDIRatioCMAXPredictedVsObserved.png)

![004_plotDDIRatioCMAXResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/002_Perpetrator/003_Efavirenz/004_plotDDIRatioCMAXResidualsVsObserved.png)

GMFE (AUC) = 1.075747 

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

![001_plotDDIRatioAUCPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/002_Perpetrator/004_Erythromycin/001_plotDDIRatioAUCPredictedVsObserved.png)

![002_plotDDIRatioAUCResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/002_Perpetrator/004_Erythromycin/002_plotDDIRatioAUCResidualsVsObserved.png)

![003_plotDDIRatioCMAXPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/002_Perpetrator/004_Erythromycin/003_plotDDIRatioCMAXPredictedVsObserved.png)

![004_plotDDIRatioCMAXResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/002_Perpetrator/004_Erythromycin/004_plotDDIRatioCMAXResidualsVsObserved.png)

GMFE (AUC) = 1.245268 

GMFE (CMAX) = 1.231222 

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

![001_plotDDIRatioAUCPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/002_Perpetrator/005_Fluvoxamine/001_plotDDIRatioAUCPredictedVsObserved.png)

![002_plotDDIRatioAUCResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/002_Perpetrator/005_Fluvoxamine/002_plotDDIRatioAUCResidualsVsObserved.png)

![003_plotDDIRatioCMAXPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/002_Perpetrator/005_Fluvoxamine/003_plotDDIRatioCMAXPredictedVsObserved.png)

![004_plotDDIRatioCMAXResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/002_Perpetrator/005_Fluvoxamine/004_plotDDIRatioCMAXResidualsVsObserved.png)

GMFE (AUC) = 1.420923 

GMFE (CMAX) = 1.425108 

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

![001_plotDDIRatioAUCPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/002_Perpetrator/006_Itraconazole/001_plotDDIRatioAUCPredictedVsObserved.png)

![002_plotDDIRatioAUCResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/002_Perpetrator/006_Itraconazole/002_plotDDIRatioAUCResidualsVsObserved.png)

![003_plotDDIRatioCMAXPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/002_Perpetrator/006_Itraconazole/003_plotDDIRatioCMAXPredictedVsObserved.png)

![004_plotDDIRatioCMAXResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/002_Perpetrator/006_Itraconazole/004_plotDDIRatioCMAXResidualsVsObserved.png)

GMFE (AUC) = 1.665952 

GMFE (CMAX) = 1.278882 

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

![001_plotDDIRatioAUCPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/002_Perpetrator/007_Rifampicin/001_plotDDIRatioAUCPredictedVsObserved.png)

![002_plotDDIRatioAUCResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/002_Perpetrator/007_Rifampicin/002_plotDDIRatioAUCResidualsVsObserved.png)

![003_plotDDIRatioCMAXPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/002_Perpetrator/007_Rifampicin/003_plotDDIRatioCMAXPredictedVsObserved.png)

![004_plotDDIRatioCMAXResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/002_Perpetrator/007_Rifampicin/004_plotDDIRatioCMAXResidualsVsObserved.png)

GMFE (AUC) = 1.460530 

GMFE (CMAX) = 1.505824 

|AUC                       |Number|Ratio [%]|
|-------------------------:|-----:|--------:|
|Points total              |57    |-        |
|Points within Guest et al.|42    |73.6842  |
|Points within 2-fold      |48    |84.2105  |

|CMAX                      |Number|Ratio [%]|
|-------------------------:|-----:|--------:|
|Points total              |41    |-        |
|Points within Guest et al.|16    |39.0244  |
|Points within 2-fold      |34    |82.9268  |

### Verapamil

![001_plotDDIRatioAUCPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/002_Perpetrator/008_Verapamil/001_plotDDIRatioAUCPredictedVsObserved.png)

![002_plotDDIRatioAUCResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/002_Perpetrator/008_Verapamil/002_plotDDIRatioAUCResidualsVsObserved.png)

![003_plotDDIRatioCMAXPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/002_Perpetrator/008_Verapamil/003_plotDDIRatioCMAXPredictedVsObserved.png)

![004_plotDDIRatioCMAXResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/002_Perpetrator/008_Verapamil/004_plotDDIRatioCMAXResidualsVsObserved.png)

GMFE (AUC) = 1.479636 

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

GMFE (AUC) = 1.307997 

GMFE (CMAX) = 1.327112 

|AUC                       |Number|Ratio [%]|
|-------------------------:|-----:|--------:|
|Points total              |21    |-        |
|Points within Guest et al.|16    |76.1905  |
|Points within 2-fold      |20    |95.2381  |

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

GMFE (AUC) = 1.397670 

GMFE (CMAX) = 1.275623 

|AUC                       |Number|Ratio [%]|
|-------------------------:|-----:|--------:|
|Points total              |9     |-        |
|Points within Guest et al.|5     |55.5556  |
|Points within 2-fold      |9     |100      |

|CMAX                      |Number|Ratio [%]|
|-------------------------:|-----:|--------:|
|Points total              |7     |-        |
|Points within Guest et al.|4     |57.1429  |
|Points within 2-fold      |7     |100      |

### Midazolam

![001_plotDDIRatioAUCPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/003_Victim/003_Midazolam/001_plotDDIRatioAUCPredictedVsObserved.png)

![002_plotDDIRatioAUCResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/003_Victim/003_Midazolam/002_plotDDIRatioAUCResidualsVsObserved.png)

![003_plotDDIRatioCMAXPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/003_Victim/003_Midazolam/003_plotDDIRatioCMAXPredictedVsObserved.png)

![004_plotDDIRatioCMAXResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/003_Victim/003_Midazolam/004_plotDDIRatioCMAXResidualsVsObserved.png)

GMFE (AUC) = 1.397505 

GMFE (CMAX) = 1.432862 

|AUC                       |Number|Ratio [%]|
|-------------------------:|-----:|--------:|
|Points total              |88    |-        |
|Points within Guest et al.|66    |75       |
|Points within 2-fold      |74    |84.0909  |

|CMAX                      |Number|Ratio [%]|
|-------------------------:|-----:|--------:|
|Points total              |53    |-        |
|Points within Guest et al.|32    |60.3774  |
|Points within 2-fold      |46    |86.7925  |

### Triazolam

![001_plotDDIRatioAUCPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/003_Victim/004_Triazolam/001_plotDDIRatioAUCPredictedVsObserved.png)

![002_plotDDIRatioAUCResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/003_Victim/004_Triazolam/002_plotDDIRatioAUCResidualsVsObserved.png)

![003_plotDDIRatioCMAXPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/003_Victim/004_Triazolam/003_plotDDIRatioCMAXPredictedVsObserved.png)

![004_plotDDIRatioCMAXResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/003_Victim/004_Triazolam/004_plotDDIRatioCMAXResidualsVsObserved.png)

GMFE (AUC) = 1.468759 

GMFE (CMAX) = 1.143534 

|AUC                       |Number|Ratio [%]|
|-------------------------:|-----:|--------:|
|Points total              |13    |-        |
|Points within Guest et al.|9     |69.2308  |
|Points within 2-fold      |11    |84.6154  |

|CMAX                      |Number|Ratio [%]|
|-------------------------:|-----:|--------:|
|Points total              |13    |-        |
|Points within Guest et al.|10    |76.9231  |
|Points within 2-fold      |13    |100      |

### Verapamil

![001_plotDDIRatioAUCPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/003_Victim/005_Verapamil/001_plotDDIRatioAUCPredictedVsObserved.png)

![002_plotDDIRatioAUCResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/003_Victim/005_Verapamil/002_plotDDIRatioAUCResidualsVsObserved.png)

![003_plotDDIRatioCMAXPredictedVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/003_Victim/005_Verapamil/003_plotDDIRatioCMAXPredictedVsObserved.png)

![004_plotDDIRatioCMAXResidualsVsObserved.png](images/002_2_Qualification_of_Use_Case_CYP3A4-mediated_DDI/003_Victim/005_Verapamil/004_plotDDIRatioCMAXResidualsVsObserved.png)

GMFE (AUC) = 1.284476 

GMFE (CMAX) = 1.754106 

|AUC                       |Number|Ratio [%]|
|-------------------------:|-----:|--------:|
|Points total              |4     |-        |
|Points within Guest et al.|3     |75       |
|Points within 2-fold      |4     |100      |

|CMAX                      |Number|Ratio [%]|
|-------------------------:|-----:|--------:|
|Points total              |3     |-        |
|Points within Guest et al.|0     |0        |
|Points within 2-fold      |2     |66.6667  |

# 3 Concentration-Time Profiles
The following section shows concentration time profiles of the victim drugs of the simulated DDI studies in comparison to observed data (if available).




## 3.1 Cimetidine - Alfentanil DDI
                   

![001_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/001_3_1_Cimetidine_-_Alfentanil_DDI/001_plotComparisonTimeProfile.png)

## 3.2 Cimetidine - Alprazolam DDI
                   

![001_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/002_3_2_Cimetidine_-_Alprazolam_DDI/001_plotComparisonTimeProfile.png)

![002_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/002_3_2_Cimetidine_-_Alprazolam_DDI/002_plotComparisonTimeProfile.png)

## 3.3 Cimetidine - Midazolam DDI
                   

![001_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/003_3_3_Cimetidine_-_Midazolam_DDI/001_plotComparisonTimeProfile.png)

![002_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/003_3_3_Cimetidine_-_Midazolam_DDI/002_plotComparisonTimeProfile.png)

![003_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/003_3_3_Cimetidine_-_Midazolam_DDI/003_plotComparisonTimeProfile.png)

![004_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/003_3_3_Cimetidine_-_Midazolam_DDI/004_plotComparisonTimeProfile.png)

![005_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/003_3_3_Cimetidine_-_Midazolam_DDI/005_plotComparisonTimeProfile.png)

![006_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/003_3_3_Cimetidine_-_Midazolam_DDI/006_plotComparisonTimeProfile.png)

## 3.4 Cimetidine - Triazolam DDI
                   

![001_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/004_3_4_Cimetidine_-_Triazolam_DDI/001_plotComparisonTimeProfile.png)

![002_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/004_3_4_Cimetidine_-_Triazolam_DDI/002_plotComparisonTimeProfile.png)

![003_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/004_3_4_Cimetidine_-_Triazolam_DDI/003_plotComparisonTimeProfile.png)

![004_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/004_3_4_Cimetidine_-_Triazolam_DDI/004_plotComparisonTimeProfile.png)

## 3.5 Cimetidine - Verapamil DDI
                   

![001_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/005_3_5_Cimetidine_-_Verapamil_DDI/001_plotComparisonTimeProfile.png)

![002_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/005_3_5_Cimetidine_-_Verapamil_DDI/002_plotComparisonTimeProfile.png)

## 3.6 Clarithromycin - Midazolam DDI
                   

![001_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/006_3_6_Clarithromycin_-_Midazolam_DDI/001_plotComparisonTimeProfile.png)

![002_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/006_3_6_Clarithromycin_-_Midazolam_DDI/002_plotComparisonTimeProfile.png)

![003_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/006_3_6_Clarithromycin_-_Midazolam_DDI/003_plotComparisonTimeProfile.png)

![004_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/006_3_6_Clarithromycin_-_Midazolam_DDI/004_plotComparisonTimeProfile.png)

![005_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/006_3_6_Clarithromycin_-_Midazolam_DDI/005_plotComparisonTimeProfile.png)

![006_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/006_3_6_Clarithromycin_-_Midazolam_DDI/006_plotComparisonTimeProfile.png)

![007_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/006_3_6_Clarithromycin_-_Midazolam_DDI/007_plotComparisonTimeProfile.png)

![008_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/006_3_6_Clarithromycin_-_Midazolam_DDI/008_plotComparisonTimeProfile.png)

![009_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/006_3_6_Clarithromycin_-_Midazolam_DDI/009_plotComparisonTimeProfile.png)

![010_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/006_3_6_Clarithromycin_-_Midazolam_DDI/010_plotComparisonTimeProfile.png)

## 3.7 Clarithromycin - Triazolam DDI
                   

![001_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/007_3_7_Clarithromycin_-_Triazolam_DDI/001_plotComparisonTimeProfile.png)

## 3.8 Erythromycin - Alfentanil DDI
                   

![001_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/008_3_8_Erythromycin_-_Alfentanil_DDI/001_plotComparisonTimeProfile.png)

![002_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/008_3_8_Erythromycin_-_Alfentanil_DDI/002_plotComparisonTimeProfile.png)

## 3.9 Erythromycin - Alprazolam DDI
                   

![001_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/009_3_9_Erythromycin_-_Alprazolam_DDI/001_plotComparisonTimeProfile.png)

## 3.10 Erythromycin - Midazolam DDI
                   

![001_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/010_3_10_Erythromycin_-_Midazolam_DDI/001_plotComparisonTimeProfile.png)

![002_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/010_3_10_Erythromycin_-_Midazolam_DDI/002_plotComparisonTimeProfile.png)

![003_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/010_3_10_Erythromycin_-_Midazolam_DDI/003_plotComparisonTimeProfile.png)

![004_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/010_3_10_Erythromycin_-_Midazolam_DDI/004_plotComparisonTimeProfile.png)

![005_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/010_3_10_Erythromycin_-_Midazolam_DDI/005_plotComparisonTimeProfile.png)

![006_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/010_3_10_Erythromycin_-_Midazolam_DDI/006_plotComparisonTimeProfile.png)

## 3.11 Erythromycin - Triazolam DDI
                   

![001_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/011_3_11_Erythromycin_-_Triazolam_DDI/001_plotComparisonTimeProfile.png)

![002_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/011_3_11_Erythromycin_-_Triazolam_DDI/002_plotComparisonTimeProfile.png)

## 3.12 Fluvoxamine - Alprazolam DDI
                   

![001_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/012_3_12_Fluvoxamine_-_Alprazolam_DDI/001_plotComparisonTimeProfile.png)

![002_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/012_3_12_Fluvoxamine_-_Alprazolam_DDI/002_plotComparisonTimeProfile.png)

## 3.13 Fluvoxamine - Midazolam DDI
                   

![001_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/013_3_13_Fluvoxamine_-_Midazolam_DDI/001_plotComparisonTimeProfile.png)

![002_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/013_3_13_Fluvoxamine_-_Midazolam_DDI/002_plotComparisonTimeProfile.png)

## 3.14 Itraconazole - Alprazolam DDI
                   

![001_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/014_3_14_Itraconazole_-_Alprazolam_DDI/001_plotComparisonTimeProfile.png)

## 3.15 Itraconazole - Midazolam DDI
                   

![001_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/015_3_15_Itraconazole_-_Midazolam_DDI/001_plotComparisonTimeProfile.png)

![002_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/015_3_15_Itraconazole_-_Midazolam_DDI/002_plotComparisonTimeProfile.png)

![003_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/015_3_15_Itraconazole_-_Midazolam_DDI/003_plotComparisonTimeProfile.png)

![004_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/015_3_15_Itraconazole_-_Midazolam_DDI/004_plotComparisonTimeProfile.png)

![005_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/015_3_15_Itraconazole_-_Midazolam_DDI/005_plotComparisonTimeProfile.png)

![006_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/015_3_15_Itraconazole_-_Midazolam_DDI/006_plotComparisonTimeProfile.png)

![007_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/015_3_15_Itraconazole_-_Midazolam_DDI/007_plotComparisonTimeProfile.png)

![008_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/015_3_15_Itraconazole_-_Midazolam_DDI/008_plotComparisonTimeProfile.png)

![009_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/015_3_15_Itraconazole_-_Midazolam_DDI/009_plotComparisonTimeProfile.png)

## 3.16 Itraconazole - Triazolam DDI
                   

![001_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/016_3_16_Itraconazole_-_Triazolam_DDI/001_plotComparisonTimeProfile.png)

![002_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/016_3_16_Itraconazole_-_Triazolam_DDI/002_plotComparisonTimeProfile.png)

## 3.17 Verapamil - Midazolam DDI
                   

![001_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/017_3_17_Verapamil_-_Midazolam_DDI/001_plotComparisonTimeProfile.png)

![002_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/017_3_17_Verapamil_-_Midazolam_DDI/002_plotComparisonTimeProfile.png)

![003_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/017_3_17_Verapamil_-_Midazolam_DDI/003_plotComparisonTimeProfile.png)

## 3.18 Efavirenz - Alfentanil DDI
                   

![001_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/018_3_18_Efavirenz_-_Alfentanil_DDI/001_plotComparisonTimeProfile.png)

![002_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/018_3_18_Efavirenz_-_Alfentanil_DDI/002_plotComparisonTimeProfile.png)

## 3.19 Efavirenz - Midazolam DDI
                   

![001_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/019_3_19_Efavirenz_-_Midazolam_DDI/001_plotComparisonTimeProfile.png)

![002_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/019_3_19_Efavirenz_-_Midazolam_DDI/002_plotComparisonTimeProfile.png)

![003_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/019_3_19_Efavirenz_-_Midazolam_DDI/003_plotComparisonTimeProfile.png)

## 3.20 Rifampicin - Alfentanil DDI
                   

![001_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/020_3_20_Rifampicin_-_Alfentanil_DDI/001_plotComparisonTimeProfile.png)

![002_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/020_3_20_Rifampicin_-_Alfentanil_DDI/002_plotComparisonTimeProfile.png)

![003_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/020_3_20_Rifampicin_-_Alfentanil_DDI/003_plotComparisonTimeProfile.png)

![004_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/020_3_20_Rifampicin_-_Alfentanil_DDI/004_plotComparisonTimeProfile.png)

![005_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/020_3_20_Rifampicin_-_Alfentanil_DDI/005_plotComparisonTimeProfile.png)

![006_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/020_3_20_Rifampicin_-_Alfentanil_DDI/006_plotComparisonTimeProfile.png)

![007_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/020_3_20_Rifampicin_-_Alfentanil_DDI/007_plotComparisonTimeProfile.png)

![008_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/020_3_20_Rifampicin_-_Alfentanil_DDI/008_plotComparisonTimeProfile.png)

![009_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/020_3_20_Rifampicin_-_Alfentanil_DDI/009_plotComparisonTimeProfile.png)

![010_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/020_3_20_Rifampicin_-_Alfentanil_DDI/010_plotComparisonTimeProfile.png)

## 3.21 Rifampicin - Alprazolam DDI
                   

![001_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/021_3_21_Rifampicin_-_Alprazolam_DDI/001_plotComparisonTimeProfile.png)

![002_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/021_3_21_Rifampicin_-_Alprazolam_DDI/002_plotComparisonTimeProfile.png)

![003_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/021_3_21_Rifampicin_-_Alprazolam_DDI/003_plotComparisonTimeProfile.png)

## 3.22 Rifampicin - Midazolam DDI
                   

![001_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/022_3_22_Rifampicin_-_Midazolam_DDI/001_plotComparisonTimeProfile.png)

![002_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/022_3_22_Rifampicin_-_Midazolam_DDI/002_plotComparisonTimeProfile.png)

![003_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/022_3_22_Rifampicin_-_Midazolam_DDI/003_plotComparisonTimeProfile.png)

![004_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/022_3_22_Rifampicin_-_Midazolam_DDI/004_plotComparisonTimeProfile.png)

![005_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/022_3_22_Rifampicin_-_Midazolam_DDI/005_plotComparisonTimeProfile.png)

![006_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/022_3_22_Rifampicin_-_Midazolam_DDI/006_plotComparisonTimeProfile.png)

![007_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/022_3_22_Rifampicin_-_Midazolam_DDI/007_plotComparisonTimeProfile.png)

![008_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/022_3_22_Rifampicin_-_Midazolam_DDI/008_plotComparisonTimeProfile.png)

![009_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/022_3_22_Rifampicin_-_Midazolam_DDI/009_plotComparisonTimeProfile.png)

![010_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/022_3_22_Rifampicin_-_Midazolam_DDI/010_plotComparisonTimeProfile.png)

![011_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/022_3_22_Rifampicin_-_Midazolam_DDI/011_plotComparisonTimeProfile.png)

![012_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/022_3_22_Rifampicin_-_Midazolam_DDI/012_plotComparisonTimeProfile.png)

![013_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/022_3_22_Rifampicin_-_Midazolam_DDI/013_plotComparisonTimeProfile.png)

![014_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/022_3_22_Rifampicin_-_Midazolam_DDI/014_plotComparisonTimeProfile.png)

![015_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/022_3_22_Rifampicin_-_Midazolam_DDI/015_plotComparisonTimeProfile.png)

![016_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/022_3_22_Rifampicin_-_Midazolam_DDI/016_plotComparisonTimeProfile.png)

![017_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/022_3_22_Rifampicin_-_Midazolam_DDI/017_plotComparisonTimeProfile.png)

![018_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/022_3_22_Rifampicin_-_Midazolam_DDI/018_plotComparisonTimeProfile.png)

![019_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/022_3_22_Rifampicin_-_Midazolam_DDI/019_plotComparisonTimeProfile.png)

![020_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/022_3_22_Rifampicin_-_Midazolam_DDI/020_plotComparisonTimeProfile.png)

![021_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/022_3_22_Rifampicin_-_Midazolam_DDI/021_plotComparisonTimeProfile.png)

![022_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/022_3_22_Rifampicin_-_Midazolam_DDI/022_plotComparisonTimeProfile.png)

![023_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/022_3_22_Rifampicin_-_Midazolam_DDI/023_plotComparisonTimeProfile.png)

![024_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/022_3_22_Rifampicin_-_Midazolam_DDI/024_plotComparisonTimeProfile.png)

![025_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/022_3_22_Rifampicin_-_Midazolam_DDI/025_plotComparisonTimeProfile.png)

## 3.23 Rifampicin - Triazolam DDI
                   

![001_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/023_3_23_Rifampicin_-_Triazolam_DDI/001_plotComparisonTimeProfile.png)

## 3.23 Rifampicin - Verapamil DDI
                   

![001_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/024_3_23_Rifampicin_-_Verapamil_DDI/001_plotComparisonTimeProfile.png)

![002_plotComparisonTimeProfile.png](images/003_3_Concentration-Time_Profiles/024_3_23_Rifampicin_-_Verapamil_DDI/002_plotComparisonTimeProfile.png)

# 4 References
**Almond 2016** Almond LM, Mukadam S, Gardner I, Okialda K, Wong S, Hatley O, Tay S, Rowland-Yeo K, Jamei M, Rostami-Hodjegan A, Kenny JR. Prediction of Drug-Drug Interactions Arising from CYP3A induction Using a Physiologically Based Dynamic Model. Drug Metab Dispos. 2016 Jun;44(6):821-32.

**Guest 2011** Guest EJ, Aarons L, Houston JB, Rostami-Hodjegan A, Galetin A. Critique of the two-fold measure of prediction success for ratios: application for the assessment of drug-drug interactions. Drug Metab Dispos. 2011 Feb;39(2):170-3.

**OSP PK Database** (https://github.com/Open-Systems-Pharmacology/Database-for-observed-data)



## Cimetidine-Alfentanil-DDI

**Kienlen 1993** Kienlen, J., Levron, JC., Aubas, S. *et al.* Pharmacokinetics of Alfentanil in Patients Treated with Either Cimetidine or Ranitidine.  Drug Invest **6,** 257–262 (1993).



## Cimetidine-Alprazolam-DDI

**Pourbaix 1985** Pourbaix S, Desager JP, Hulhoven R, Smith RB, Harvengt C. Pharmacokinetic consequences of  long term coadministration of cimetidine and triazolobenzodiazepines,  alprazolam and triazolam, in healthy subjects. Int J Clin Pharmacol Ther Toxicol. 1985 Aug;23(8):447-51.

**Abernethy 1983**  Abernethy DR,  Greenblatt DJ, Divoll M, Moschitto LJ, Harmatz JS, Shader RI.  Interaction of cimetidine with the triazolobenzodiazepines alprazolam  and triazolam. Psychopharmacology (Berl). 1983;80(3):275-8. doi:  10.1007/BF00436169.



## Cimetidine-Midazolam-DDI

**Elliott 1984** Elliott P, Dundee  JW, Elwood RJ, Collier PS. The influence of H2 receptor antagonists on  the plasma concentrations of midazolam and temazepam. Eur J  Anaesthesiol. 1984 Sep;1(3):245-51.

**Fee 1987** Fee JP, Collier PS, Howard PJ, Dundee JW. Cimetidine and ranitidine increase midazolam  bioavailability. Clin Pharmacol Ther. 1987 Jan;41(1):80-4.

**Greenblatt 1986** Greenblatt DJ,  Locniskar A, Scavone JM, Blyden GT, Ochs HR, Harmatz JS, Shader RI.  Absence of interaction of cimetidine and ranitidine with intravenous and oral midazolam. Anesth Analg. 1986 Feb;65(2):176-80.

**Martinez 1999** Martínez C, Albet  C, Agúndez JA, Herrero E, Carrillo JA, Márquez M, Benítez J, Ortiz JA.  Comparative in vitro and in vivo inhibition of cytochrome P450 CYP1A2,  CYP2D6, and CYP3A by H2-receptor antagonists. Clin Pharmacol Ther. 1999  Apr;65(4):369-76.

**Salonen 1986** Salonen M, Aantaa  E, Aaltonen L, Kanto J. Importance of the interaction of midazolam and  cimetidine. Acta Pharmacol Toxicol (Copenh). 1986 Feb;58(2):91-5.



## Cimetidine-Triazolam-DDI

**Pourbaix 1985** Pourbaix S, Desager JP, Hulhoven R, Smith RB, Harvengt C. Pharmacokinetic consequences of  long term coadministration of cimetidine and triazolobenzodiazepines,  alprazolam and triazolam, in healthy subjects. Int J Clin Pharmacol Ther Toxicol. 1985 Aug;23(8):447-51.

**Abernethy 1983**  Abernethy DR,  Greenblatt DJ, Divoll M, Moschitto LJ, Harmatz JS, Shader RI.  Interaction of cimetidine with the triazolobenzodiazepines alprazolam  and triazolam. Psychopharmacology (Berl). 1983;80(3):275-8.

**Cox 1986** Cox SR, Kroboth PD, Anderson PH, Smith RB. Mechanism for the interaction between triazolam  and cimetidine. Biopharm Drug Dispos. 1986 Nov-Dec;7(6):567-75.

**Friedman 1988** Friedman H,  Greenblatt DJ, Burstein ES, Scavone JM, Harmatz JS, Shader RI. Triazolam kinetics: interaction with cimetidine, propranolol, and the  combination. J Clin Pharmacol. 1988 Mar;28(3):228-33.



## Cimetidine-Verapamil-DDI

**Smith 1984** Smith MS, Benyunes  MC, Bjornsson TD, Shand DG, Pritchett EL. Influence of cimetidine on  verapamil kinetics and dynamics. Clin Pharmacol Ther. 1984  Oct;36(4):551-4. 



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

**Villikka 1997** Villikka K, Kivistö KT, Backman JT, Olkkola KT, & Neuvonen PJ. Triazolam is ineffective in patients taking rifampin. Clin Pharmacol Ther. 1997 Jan;61(1):8-14.



## Rifampicin-Verapamil-DDI

**Barbarash 1988** Barbarash RA, Bauman JL, Fischer JH, Kondos GT, Batenhorst RL. Near-total reduction in verapamil bioavailability by rifampin. Electrocardiographic correlates. Chest. 1988 Nov;94(5):954-9.


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




