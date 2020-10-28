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

## Processing power

Economies of scale. 

Designing a planetary-scale map processing is a difficult task. 

It is important to separate it in submodules, with well defined interface. This enables to have potentially more than one implementation for module (e.g. automatic vs. Manual processes)

Scaling up : Adding more resource to a node (CPU, Memory, Disk)

Scaling out : Adding more nodes (e.g. virtual machines)

### Hardware as a Service

Hardware rented on a daily a basis

### Infrastructure as a Service

Virtual machines, container, storage, load balancer

### Scientific Computing as a Service

Parallel computing environment, HPC distribbuted clusters, GPGPUs management layers, dynamic scheduling, dedicated programming environment, optimization services. 

### Cloud

Cloud Burst : seamless burst into public clouds in a safe and secure manner. Cloud bursting is an application deployment model in which an application runs in a [private cloud](https://searchcloudcomputing.techtarget.com/definition/private-cloud) or data center and [bursts](https://searchnetworking.techtarget.com/definition/burst) into a [public cloud](https://searchcloudcomputing.techtarget.com/definition/public-cloud) when the demand for computing capacity spikes. An organization only pays for extra compute resources when they are needed. An application can be deployed locally and then burst to the cloud to meet peak demands, or the application can be moved to the public cloud to free up local resources for business-critical applications. Cloud bursting works best for applications that don’t depend on a complex application delivery infrastructure or integration with other applications, components and systems internal to the data center. 



## Practice

### Using Zenodo

- research is stored safely for the future in CERN’s Data Centre for as long as CERN exists.

- built and operated by CERN and OpenAIRE to ensure that everyone can join in Open Science.
- every upload is assigned a Digital Object Identifier (DOI), to make them citable and trackable.
- Uploads are made available online as soon as you hit publish, and your DOI is registered within seconds.
- Share e.g. anonymized clinical trial data with only medical professionals via our restricted access mode.
- Easily update your dataset with our versioning feature
- All uploads display standards compliant usage statistics

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
