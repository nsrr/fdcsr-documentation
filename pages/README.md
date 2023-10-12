## About

Forced desynchrony (FD) studies are designed to force desynchrony between circadian rhythms and sleep/wake (and associated behaviors) in healthy adults. Under such conditions, the relative impact of circadian rhythms, duration of time awake or asleep, and their (non-linear) interactions on multiple physiological variables can be quantified. Outcomes include objective performance ([Psychomotor Vigilance Test](https://link.springer.com/article/10.3758/bf03200977), [Digit Symbol Substitution Test](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6291255/)), subjective alertness and mood ([Visual Analog Scale](https://pubmed.ncbi.nlm.nih.gov/4048757/), [Karolinska Sleepiness Scale](https://pubmed.ncbi.nlm.nih.gov/16679057/)), melatonin and Core Body Temperature, hormone variables, Polysomnography (PSG) signal data; electroencephalogram (EEG), electrooculography (EOG), electromyography (EMG), electrocardiogram (ECG or EKG), as well as PSG metrics; scored sleep stages, slow eye movements and [Karolinska Drowsiness Test](https://pubmed.ncbi.nlm.nih.gov/2265922/) (KDT) values.

Each study consists of a single 20-75 day inpatient visit where data are collected on multiple physiological metrics across different combinations of circadian time (i.e., phase) and length of time awake or asleep. 

Exclusion criteria include color blindness, medication use, unstable medical conditions and personal or first degree relative with a psychiatric disorder.

## Methods

Data were collected using a single-blinded parallel group randomized control trial (RCT). 

Validated instruments used include:
* Karolinska Sleepiness Scale
* Psychomotor Vigilance Task 
* Digit Symbol Substitution Task
* Visual Analog Scale

Date and time of recordings are presented using **labtime**, which is a value between 0 and 8760, representing the number of hours since midnight on January 1st of the study year. Labtime is not affected by daylight savings time. 

## Data overview

### Polysomnography
EDF signal data (including EEG) are available for 28 subjects, with files named by the sleep/wake period (e.g., sp2 for Scheduled Sleep Period 2). Raw data were captured using Vitaport recorders. Scored Sleep files are available for all subjects, with scoring completed by hand according to the Rechtschaffen and Kales criteria (Rechtschaffen A, Kales A, editors. Los Angeles: Brain Information Service/Brain Research Institute, University of California; 1968. A manual of standardized terminology, techniques and scoring system of sleep stages in human subjects). EDF files can be linked to the Scored Sleep files by sleep/wake period number; negative values indicate wake periods whilst positive values indicate sleep periods. Each wake period precedes the sleep period with the same index.

The Scored Sleep CSV files contain four columns: 1) Subject ID; 2) sleep/wake period number; 3) labtime; and 4) sleep staging code. These files describe the **scheduled sleep and wake periods**. The actual start and end labtime for each EDF file can be found in the [EDF labtimes CSV file](:files_path:/original).

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
Raw actigraphy data is available for each of the 28 recordings and each covers a period of up to 90 days. All actigraphy CSV files have an activity level and light level score per 1-minute epoch.

### Covariate/phenotype datasets
Covariate CSV files contain data on all 28 subjects. The [subject](:variables_path:/subject) column is the unique FD-CSR identifier. The [study](:variables_path:/study) variable identifies the full name of the particular study a participant was involved in, and [study2](:variables_path:/study2) provides the study nickname.

The dataset columns are described in the accompanying data dictionary files. The **variables** data dictionary file includes column names (id), labels (display names), descriptions, and other metadata. Categorical variables also include an associated “domain” (e.g., F=Female, M=Male), which are described in the **domains** data dictionary file.

The history of the covariate dataset and data dictionary files have been tracked on GitHub (https://github.com/nsrr/fdcsr-data-dictionary). 

## Access and usage restrictions

All data access requests must be pre-approved by PI Dr Klerman (ebklerman@mgh.harvard.edu) prior to submitting a data request with sleepdata.org. The FD-CSR dataset is only available for non-commercial use.

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

*October 2023*

- Make FD-CSR dataset available for data requests

## References

- NSRR FD-CSR GitHub Documentation: https://github.com/nsrr/fdcsr-documentation
- FD-CSR GitHub Data Dictionary: https://github.com/nsrr/fdcsr-data-dictionary

## Questions?

Please reach out to us at support@sleepdata.org or in the [Forum](https://sleepdata.org/forum) if you have questions.

