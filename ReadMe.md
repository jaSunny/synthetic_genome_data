
# MA-enriched-Health-Data

> This repo holds an enriched genome data composed of multiple dataset publications enriched with profile data in close alignment with learned distributions.

Nowadays, data processing becomes more and more common. To enable testing, evaluation and development of data driven applications, this repository holds a script to generate large scale and high dimensional data sets which are created in close alignment with public data sets esp. their data distribution.

An examplary usage can be to evaluate new anonymization techniques which rely on non-anonymized data. Since nobody wants his PII data published, this fake but realistic data may be used to assess and evaluate such use cases.

## Table of Contents
- Composition
  - CRM Attributes
    - CRM Attributes
    - Example Values
  - Behavioral/Medical Attributes
    - CRM Attributes
    - Example Values
    - Sources
- Related Links & Other Datasets
- Distributions
  - Structural Overview
  - Attribute Value Distributions

## Composition
The following chapter shall briefly list and describe the include attributes for a single data record, including its source, type and distribution. All attributes shall be presented with examples.

### CRM Attributes

The CRM attribute values originate from [fakenamegenerator.com](http://www.fakenamegenerator.com/), which provides
* in sum 487 million different region-sensitive names (108 million male names, 379 million female names)
* addresses and its geocoordinates (latitude & longitude) for 31 countries
* local telephone numbers
* national identification numbers
* birthday and age
* email addresses, usernames, passwords, websites and browser user agents
* (fake but consistent) Visa numbers, expiring dates, CVV2s
* employment details including company and Occupation
* height and weight

Further details regarding the statistics, the reader is kindly referred to the [original source](http://www.fakenamegenerator.com/statistics.php).

#### Example Values

| Attribute        | Type           | Example value |
| ------------- |:-------------:| -----:|
| Firstname | String | Shirley |
| Middlename | String | Time |
| Lastname | String | Coffey |
| Address | String | Sömmeringstr. 93 |
| ZIP | Integer | 75172  |
| City | String | Pforzheim Weststadt |
| GeoCoordinates | String | 48.884783, 8.690593 |
| Phone | String | 07231 69 44 49 |
| County Code | Integer | 49 |
| Birthday | Date | August 2, 1941 |
| Age | Integer | 75 |
| Email Address | String | SebastianGottlieb@dayrep.com  |
| Username | String | Topas1941  |
| Password | String | vaiFaoz4  |
| Browser user agent | String | Mozilla/5.0 (Windows NT 10.0; Win64; x64)   |
| Visa Nr. | String | 4929 0844 9315 7600  |
| Expiring Date | Date | 5/2019 |
| CVV2 | Integer | 666 |
| Company | Integer | Schaak Electronics |
| Occupation | Integer | Financial examiner |
| Height (in cm)| Integer | 173  |
| Weight (in kg) | Float | 68.2  |

### Behavioral/Medical Attributes
The behavior attribute values include, but may not be limited to
* blood type
* drug usage
* disease-gene relations
* disease-disease relations
* disease diagnosis
* single-nucleotide polymorphis (SNP)
* color

The raw data can be found in ```/2_behavior_medical_attribute_values``` .


#### Example Values

| Attribute        | Type           | Example  value |
| ------------- |:-------------:| -----:|
| Blood Type | String | B+ |
| Color | String | Purple |

For drugs:

| Attribute        | Type           | Example  value |
| ------------- |:-------------:| -----:|
| PRODUCTID | String | 0002-1200_e62214a4-82fd-4e06-90a0-577a32fea93f |
| PRODUCTTYPENAME | String | HUMAN PRESCRIPTION DRUG	|
| PROPRIETARYNAME | String | Amyvid |
| PRODUCTNDC | String | 0002-1200 |
| NONPROPRIETARYNAME | String | Florbetapir F 18 |
| DOSAGEFORMNAME | String | INJECTION, SOLUTION |
| ROUTENAME | String | INTRAVENOUS |
| STARTMARKETINGDATE | Date | 20120601 |
| MARKETINGCATEGORYNAME | String | NDA |
| APPLICATIONNUMBER | String | NDA202008 |
| ACTIVE_NUMERATOR_STRENGTH | Integer | 51 |
| ACTIVE_INGRED_UNIT | String | mCi/mL |
| PHARM_CLASSES | String | Radioactive Diagnostic Agent [EPC],Positron Emitting Activity [MoA] |


For drug packages:

| Attribute        | Type           | Example value |
| ------------- |:-------------:| -----:|
| PRODUCTNDC | String | 0002-1200 |
| NDCPACKAGECODE | String | 0002-1200-30 |
| PACKAGEDESCRIPTION | String | 1 VIAL, MULTI-DOSE in 1 CAN (0002-1200-30)  > 30 mL in 1 VIAL, MULTI-DOSE |

For disease-disease relations:

| Attribute        | Type           | Example value |
| ------------- |:-------------:| -----:|
| Disease_1 | String | Yohimbine  |
| Disease_2 | String | Disorder Of Male Reproductive System |
| relation | Double | 0 |

For disease-gene relations:

| Attribute        | Type           | Example value |
| ------------- |:-------------:| -----:|
| Concept ID | String | C0035243  |
| Disease | String | Respiratory Tract Infections |
| Type | String | DEG |
| Gene | String | RNFT1 |

For symptoms:

| Attribute        | Type           | Example value |
| ------------- |:-------------:| -----:|
| symptom_name | String | Aging, Premature  |
| disease_name | String | Acquired Immunodeficiency Syndrome  |
| cooccurs | Integer | C0035243  |
| tfidf_score | Integer | 3  |
| disease_id | Float | 10.3936544686139  |
| symptom_id | String | D000163  |
| doid_code | String | DOID:635  |
| doid_name | String | acquired immunodeficiency syndrome  |

For SNPs:

| Attribute        | Type           | Example value |
| ------------- |:-------------:| -----:|
| snpId | String | rs10004195  |
| pubmedId | Integer | 25687912 |
| geneId | String | 81793  |
| TEST | String | TLR10  |
| geneSymbol | String | umls:C0679408  |
| sourceId | String | BeFree |
| diseaseName | String | Lesion of stomach	|
| sentence | String | Three single-nucleotide polymorphisms, TLR1 rs4833095, TLR10 rs10004195, and TLR10 rs4129009 were genotyped by TaqMan SNP genotyping assay in 2553 participants with diverse gastric lesions.  |
| score | Float | 0.000271441872080303  |
| year | Date | 2015  |
| geneSymbol_dbSNP | String | TLR10  |
| CHROMOSOME | String | 4  |
| POS | String | 38783103  |
| REF | String | T  |
| ALT | String | A  |


#### Sources

Genome data:
* http://www.1000genomes.org/data
* http://www.completegenomics.com/public-data/69-genomes/
* http://www.ebi.ac.uk/pdbe/emdb/index.html/
* http://www.hagsc.org/hgdp/files.html
* http://geneontology.org/docs/download-go-annotations/
Disease relations:
* http://disease-connect.org/
* [Suthram S, Dudley JT, Chiang AP, Chen R, Hastie TJ, Butte AJ: Network-based elucidation of human disease similarities reveals common functional modules enriched for pluripotent drug targets. PLoS Comput Biol 2010, 6:1–10.](http://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1000662)
* http://www.disgenet.org/web/DisGeNET/menu/downloads#r

Blood type distribution per country:
* https://en.wikipedia.org/wiki/Blood_type_distribution_by_country

Diseases:
* [Rzhetsky, A., Wajngurt, D., Park, N., & Zheng, T. (2007). Probing genetic overlap among complex human phenotypes. Proceedings of the National Academy of Sciences of the United States of America, 104, 11694–11699. doi:10.1073/pnas.0704820104](http://www.pnas.org/content/104/28/11694.full.pdf)
* [Supplementary data from the disease network](https://www.nature.com/articles/ncomms5212)

Drugs:
* [US Food & Drug Administration](https://www.fda.gov/drugs/informationondrugs/ucm142438.htm)
* https://www.medicare.gov/download/downloaddb.asp
Genes:
* https://github.com/macarthur-lab/gene_lists
* http://www.disgenet.org/web/DisGeNET/menu/downloads#r
* http://www2.gov.bc.ca/gov/content/health/practitioner-professional-resources/pharmacare/health-industry-professionals/downloadable-drug-data-files

A Bundle of disease, SNP and genomic data:
* https://github.com/mdozmorov/gwas2bed

ICD-9-CM Diagnosis and Procedure Codes:
* https://www.cms.gov/Medicare/Coding/ICD9ProviderDiagnosticCodes/codes.html

Other:
* https://github.com/awesomedata/awesome-public-datasets

## Composed Data set

A composed data set with 107 columns and nearly 1M rows can be found at [here](https://hpi.framsteg.de/data/epic/MA_enriched_Health_Data.csv.gz).


## Related Links & Other Datasets

Aggregated & statistics:
* https://www.cms.gov/OpenPayments/Explore-the-Data/Dataset-Downloads.html
* https://dev.pbs.gov.au/readme.html
* [Million Hearts](https://millionhearts.hhs.gov/data-reports/data.html)
* [Health Data NY](https://health.data.ny.gov/browse?limitTo=datasets&sortBy=alpha)
* [HHS 2013 Year in Health Data Highlights](https://www.data.gov/health/hhs-2013-year-in-health-data-highlights)
* [MHEALTH Dataset Data Set](https://archive.ics.uci.edu/ml/datasets/MHEALTH+Dataset)
* https://hcup-us.ahrq.gov/databases.jsp


## Distributions

### Structural Overview

![alt tag](docs/distribution_overview.png?raw=true)

Image Source: http://people.stern.nyu.edu/adamodar/pdfiles/papers/probabilistic.pdf

### Attribute Value Distributions

![alt tag](docs/barplot_BloodType_distribution.png?raw=true)
![alt tag](docs/barplot_Centimeters_distribution.png)
![alt tag](docs/barplot_Color_distribution.png?raw=true)
![alt tag](docs/vioplot_Age_distribution.png?raw=true)
![alt tag](docs/Density_Rug_Birthday_distribution.png?raw=true)
![alt tag](docs/Density_Rug_disease_date_0_distribution.png?raw=true)
![alt tag](docs/Density_Rug_drug_0_distribution.png?raw=true)
![alt tag](docs/Density_Rug_drug_date_0_distribution.png?raw=true)

more statistics can be found in ```docs/```
