## About

Forced desynchrony (FD) studies are designed to force desynchrony between circadian rhythms and sleep/wake (and associated behaviors) in healthy adults. Under such conditions, the relative impact of circadian rhythms, duration of time awake or asleep, and their (non-linear) interactions on multiple physiological variables can be quantified. Primary outcomes are objective performance (PVT, DSST), subjective alertness and mood (VAS, KSS), melatonin and Core Body Temperature. Secondary metrics include hormone variables, as well as PSG signal data (EEG, EOG, EMG, ECG) and metrics (scored sleep, KDTs, SEMs)

Each study consists of a single 20-75 day inpatient visit where data is collected on multiple physiological metrics across different combinations of circadian time (i.e., phase) and length of time awake or asleep. 

Exclusion criteria include color blindness, medication use, medical instability and personal or first degree relative with a psychiatric disorder.

## Methods

Data were collected using a single-blinded parallel group randomized control trial (RCT). 

Validated instruments used include:
* Karolinska Sleepiness Scale
* Psychomotor Vigilance Task 
* Digit Symbol Substitution Task
* Visual Analog Scale

## Data overview

### Polysomnography
EDF signal data (including EEG) are available for 37 subjects, with separate files for each sleep/wake period. Raw data was captured using Vitaport recorders. Scored Sleep files, scored by hand according to the Rechtschaffen and Kales criteria, are available for 28 subjects.

### Actigraphy
Raw actigraphy data is available for 36 subjects (all except *2173DX*) and covers a period of up to 90 days. Each participant's actigraphy csv has an activity level and light level score per 1-minute epoch.

### Covariate/phenotype datasets
Covariate CSV files contain data on 37 subjects. The [subject](:variables_path:/subject) column is the unique FD-CSR identifier. The [study](:variables_path:/study) variable identifies the full name of the particular study a participant was involved in, and [study2](:variables_path:/study2) provides the study nickname.

The dataset columns are described in the accompanying data dictionary files. The **variables** data dictionary file includes column names (id), labels (display names), descriptions, and other metadata. Categorical variables also include an associated “domain” (e.g., 1=Female, 0=Male), which are described in the **domains** data dictionary file.

The history of the covariate dataset and data dictionary files have been tracked on GitHub (https://github.com/nsrr/apples-data-dictionary). 

## Access and usage restrictions

All data access requests must be approved by PI Dr Klerman. The FD-CSR dataset is only available for non-commercial use.

## Citation and acknowledgement

When using this dataset, users must cite the following:

> [Zhang GQ, Cui L, Mueller R, Tao S, Kim M, Rueschman M, Mariani S, Mobley D, Redline S. The National Sleep Research Resource: towards a sleep data commons. J Am Med Inform Assoc. 2018 Oct 1;25(10):1351-1358. doi: 10.1093/jamia/ocy064. PMID: 29860441; PMCID: PMC6188513.](https://pubmed.ncbi.nlm.nih.gov/29860441/)
>
>[]()

Users must include the following text in any Acknowledgements:

> The National Sleep Research Resource was supported by the U.S. National Institutes of Health, National Heart Lung and Blood Institute (R24 HL114473, 75N92019R002).

## Changelog

*July 2023*

- Make FD-CSR dataset available for data requests

## References

- NSRR FD-CSR GitHub Documentation: https://github.com/nsrr/fdcsr-documentation

## Questions?

Please reach out to us at support@sleepdata.org or in the [Forum](https://sleepdata.org/forum) if you have questions.

