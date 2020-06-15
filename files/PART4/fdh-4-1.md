---
title: 'Foundations in Digital Humanities 4.1'
subtitle: 'Data Management'
author:
 - Frederic Kaplan

# Don't change the following lines
header-includes:
- \usepackage{fancyhdr}
- \pagestyle{fancy}
- \fancyfoot[L]{-release-version-}
output: pdf_document

---

# Data Management

## Concepts

FAIR principle, Creative Commons, Data Management models, Sustainability, Right to Forgotten. Management of uncertainty, incoherence and errors. Iconographic principle of precaution

Anonymisation and privacy protection



## Practice

### Using Zenodo

### Using Dataverse

Dataverse was created in 2015. It developed in Europe. 

The **Dataverse** is an open source web application to share, preserve, cite, explore and analyze research data.[[1\]](https://en.wikipedia.org/wiki/Dataverse#cite_note-1)[[2\]](https://en.wikipedia.org/wiki/Dataverse#cite_note-2) Researchers, data authors, publishers, data distributors, and affiliated institutions all receive appropriate credit via a data citation with a persistent identifier (e.g., DOI, or Handle).

The strenght of Dataverse is versionning. 

 https://dataverse.org

### Using Amnesia (Anonymisation)

https://amnesia.openaire.eu/amnesiaInfo.html

Amnesia implements data anonymization techniques from the field of Privacy Preserving Data Publishing (PPDP). The key idea in anonymization is that identifying information is removed from the published data, so no sensitive information can be attributed to a person. The anonymization procedure is not limited to the removal of direct identifiers that might exist in a dataset, e.g. the name or the Social Security Number of a person; it also includes removing secondary information, e.g. like age, zipcode that might lead indirectly to the true identity of an individual. This secondary information is referred to as quasi-identifiers. To better understand how secondary information can be used to re-identify a person, consider the following example. A publisher that owns medical data of patients wants to publish an anonymized version of the data she owns. The data are superficially anonymized by removing direct identifiers e.g., names and social security numbers, but descriptive information like the zip code of the patient’s residence and her/his age remain. An adversary who wants to identify the patients that are related to the anonymized data, may have access to such descriptive information from other sources, e.g., a voter’s registry. The re-identification can be achieved by matching the descriptive information (Zip code, Age) of the anonymized data to the public registry. If a single match is produced for a given combination, then a patient can be accurately identified. The sparser the data are, the more unique combinations exist, and the easier it is for an adversary to locate unique records that correspond to specific users.

## Question and Answers 

## Further Reading
