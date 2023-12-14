## About

Forced desynchrony (FD) studies include a schedule that forces desynchrony between circadian rhythms and sleep/wake (and associated behaviors) in healthy adults. Under such conditions, the relative impact of circadian rhythms, duration of time awake or asleep, and their (non-linear) interactions on multiple physiological variables can be quantified. Outcomes include objective performance ([Psychomotor Vigilance Test](https://link.springer.com/article/10.3758/bf03200977), [Digit Symbol Substitution Test](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6291255/)), subjective alertness and mood ([Visual Analog Scale](https://pubmed.ncbi.nlm.nih.gov/4048757/), [Karolinska Sleepiness Scale](https://pubmed.ncbi.nlm.nih.gov/16679057/)), melatonin and Core Body Temperature, hormone variables, Polysomnography (PSG) signal data; electroencephalogram (EEG), electrooculography (EOG), electromyography (EMG), electrocardiogram (ECG or EKG), as well as PSG metrics; scored sleep stages, slow eye movements and [Karolinska Drowsiness Test](https://pubmed.ncbi.nlm.nih.gov/2265922/) (KDT) values.

Each study consists of a single 11-38 day inpatient visit per participant where data are collected on multiple physiological metrics across different combinations of circadian time (i.e., phase) and length of time awake or asleep. The studies shared on the NSRR took place between 2000 and 2016.

Exclusion criteria include color blindness, medication use, unstable medical conditions and personal or first degree relative with a psychiatric disorder.

**Note: All data access requests must be pre-approved by PI Dr Klerman prior to submitting a data request on sleepdata.org. Please <a href="https://redcap.link/fdcsr-pre-approval" target="_blank">complete the pre-approval survey to get started</a>.**

## Methods

Data were collected using a single-blinded parallel group randomized control trial (RCT). 

Studies were conducted in an inpatient unit at [Brigham and Women's Hospital](https://www.brighamandwomens.org/). 

All studies include Baseline (BL), Forced Desynchrony (FD) and Recovery (REC) segments.

## Data overview

Data are stored using **labtime** instead of calendar date and clock time. Labtime is a value between 0.000 and 8760.000, representing the number of hours (including fractions of hours) since midnight on January 1st of the study year. For example, 345.667 is 345h and 40 minutes since Jan 1 at midnight (0.000). Labtime is not affected by daylight savings time.

Data are time-based, not file name based. Data should be analyzed using labtime rather than by file name.  A file name including SP (Sleep Period) may include data from WP (Wake Period) before and after it; a file with name including WP may include some SP data.

For the current NSRR FD-CSR dataset, PSG, scored sleep, actigraphy, sleep schedule, circadian phase timing, and covariate information are available for 28 subjects. Other data types will be added later.

### Schedule

The FD-CSR Sleep Period times file contains 5 columns: 1) Subject; 2) SP number (includes text SP), 3) SP start time (labtime), 4) SP end (labtime), 5) Protocol section (BL, FD, REC) where Protocol section (BL, FD, REC) where BL=Baseline, FD=Forced Desynchrony, REC=Recovery.

### Polysomnography

*EDF*
[EDF signal data](:files_path:/original) (including EEG) are available for 28 subjects. The file name includes the sleep/wake period (e.g., sp2 for Scheduled Sleep Period 2). See note above about analyzing data by labtime rather than file name.

Raw data were captured using Vitaport recorders. 

A list of EDF files is in the XX file that contains 6 columns: 1) File name, 2) clock time (HH:mm:ss) of the first line, 3)  labtime of the first line, 4) number of lines in the file, 5) clock time of the last line, 6) labtime of the last line. Note: if the csv file shows clock time as a number between 0 and 1; then multiply by 24 to get the decimal time (e.g., 12.75) or have Excel reformat the cell. These data should be used to calculate labtime for each epoch of the EDF file.  EDF file data should then be linked to the Scored Sleep files (detailed below) by labtime.

*Scored Sleep*
Scoring was done manually according to the Rechtschaffen and Kales criteria (Rechtschaffen A, Kales A, editors. Los Angeles: Brain Information Service/Brain Research Institute, University of California; 1968. A manual of standardized terminology, techniques and scoring system of sleep stages in human subjects).

The Scored Sleep CSV files contain four columns: 1) Subject ID; 2) sleep/wake period number; 3) labtime; and 4) sleep staging code. Negative values in the sleep/wake period number column indicate wake periods whilst positive values indicate sleep periods. Each wake period precedes the sleep period with the same number.

<details>
  <summary>View sleep staging codes:</summary>

  <table>
<tr><td><b>Value</b></td><td><b>Meaning</b></td></tr>
<tr><td>0</td><td>Unknown</td></tr>
<tr><td>1</td><td>NREM 1</td></tr>
<tr><td>2</td><td>NREM 2</td></tr>
<tr><td>3</td><td>NREM 3</td></tr>
<tr><td>4</td><td>NREM 4</td></tr>
<tr><td>5</td><td>Wake</td></tr>
<tr><td>6</td><td>REM</td></tr>
<tr><td>7</td><td>Movement</td></tr>
<tr><td>8</td><td>Lights Out</td></tr>
<tr><td>9</td><td>Lights On</td></tr>


</table>

</details>    


### Actigraphy
[Raw actigraphy data](:files_path:/original) are available. For each subject, data are available for 1-2 weeks prior to the inpatient study through the immediately following inpatient study. All actigraphy CSV files have an activity level and light level score per 1-minute epoch.

### Objective Performance and Subjective Alertness
Validated instruments used include:

- Karolinska Sleepiness Scale
- Psychomotor Vigilance Task
- Digit Symbol Substitution Task
- Visual Analog Scale

Note: These will be made available on NSRR later.

### Covariate/phenotype datasets
[Covariate CSV files](:files_path:/datasets) contain data on all subjects. The [subject](:variables_path:/subject) column is the unique FD-CSR identifier. The [study](:variables_path:/study) variable identifies the full name of the particular study a participant was involved in, and [study2](:variables_path:/study2) provides the study nickname.

The dataset columns are described in the accompanying data dictionary files. The **variables** data dictionary file includes column names (id), labels (display names), descriptions, and other metadata. Categorical variables also include an associated “domain” (e.g., F=Female, M=Male), which are described in the **domains** data dictionary file.

The history of the covariate dataset and data dictionary files have been tracked on GitHub (https://github.com/nsrr/fdcsr-data-dictionary). 

## Access and usage restrictions

The FD-CSR dataset is only available for non-commercial use.

## Citation and acknowledgement

When using this dataset, users must cite the following:

>[Zhang GQ, Cui L, Mueller R, Tao S, Kim M, Rueschman M, Mariani S, Mobley D, Redline S. The National Sleep Research Resource: towards a sleep data commons. J Am Med Inform Assoc. 2018 Oct 1;25(10):1351-1358. doi: 10.1093/jamia/ocy064. PMID: 29860441; PMCID: PMC6188513.](https://pubmed.ncbi.nlm.nih.gov/29860441/)

>[Grady S, Aeschbach D, Wright KP Jr, Czeisler CA. Effect of modafinil on impairments in neurobehavioral performance and learning associated with extended wakefulness and circadian misalignment. Neuropsychopharmacology. 2010 Aug;35(9):1910-20. doi: 10.1038/npp.2010.63. Epub 2010 May 26. PMID: 20505660; PMCID: PMC2904872.](https://pubmed.ncbi.nlm.nih.gov/20505660/)

>[Cohen DA, Wang W, Wyatt JK, Kronauer RE, Dijk DJ, Czeisler CA, Klerman EB. Uncovering residual effects of chronic sleep loss on human performance. Sci Transl Med. 2010 Jan 13;2(14):14ra3. doi: 10.1126/scitranslmed.3000458. PMID: 20371466; PMCID: PMC2892834.](https://pubmed.ncbi.nlm.nih.gov/20371466/)
 
>[McHill AW, Hull JT, Wang W, Czeisler CA, Klerman EB. Chronic sleep curtailment, even without extended (>16-h) wakefulness, degrades human vigilance performance. Proc Natl Acad Sci U S A. 2018 Jun 5;115(23):6070-6075. doi: 10.1073/pnas.1706694115. Epub 2018 May 21. PMID: 29784810; PMCID: PMC6003377.](https://pubmed.ncbi.nlm.nih.gov/29784810/)

>[McHill AW, Hull JT, Cohen DA, Wang W, Czeisler CA, Klerman EB. Chronic sleep restriction greatly magnifies performance decrements immediately after awakening. Sleep. 2019 May 1;42(5):zsz032. doi: 10.1093/sleep/zsz032. PMID: 30722039; PMCID: PMC6519907.](https://pubmed.ncbi.nlm.nih.gov/30722039/)

Users must include the following text in any Acknowledgements:

> The National Sleep Research Resource was supported by the U.S. National Institutes of Health, National Heart Lung and Blood Institute (R24 HL114473, 75N92019R002).

## Changelog

*December 2023*

- Revise README to make descriptions of data types and analysis tips clearer

*November 2023*

- Add link to  <a href="https://redcap.link/fdcsr-pre-approval" target="_blank">pre-approval survey</a> for users wishing to access FD-CSR data

*October 2023*

- Make FD-CSR dataset available for data requests

## References

- NSRR FD-CSR GitHub Documentation: https://github.com/nsrr/fdcsr-documentation
- FD-CSR GitHub Data Dictionary: https://github.com/nsrr/fdcsr-data-dictionary

## Questions?

Please reach out to us at support@sleepdata.org or in the [Forum](https://sleepdata.org/forum) if you have questions.
