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

## Theses

The Digital Humanities is based on data exchange, standardisation and openness. 

But Publishing Digital Humanities Data may be problematic from an ethical or deontologic point of view.

A journey from the sunny dreams of openness to the difficulties of open data.  

1) Putting Data in Open Access requires a series of technical steps 

2) A special attention should be paid to personal data 

3) Among the users rights, the right to be forgotten / erased is one of the most complex. 

## Open Data Repositories

### FAIR Principle

Findable Accessible Interropeable and Reusable 

### Case Study : Zenodo

- research is stored safely for the future in CERN’s Data Centre for as long as CERN exists.

- built and operated by CERN and OpenAIRE to ensure that everyone can join in Open Science.
- every upload is assigned a Digital Object Identifier (DOI), to make them citable and trackable.
- Uploads are made available online as soon as you hit publish, and your DOI is registered within seconds.
- Share e.g. anonymized clinical trial data with only medical professionals via our restricted access mode.
- Easily update your dataset with our versioning feature
- All uploads display standards compliant usage statistics

### Other platforms

- Re3data.org
- Dryad
- figshare

### Case Study : Using Dataverse

Dataverse was created in 2015. It developed in Europe. 

The **Dataverse** is an open source web application to share, preserve, cite, explore and analyze research data. Researchers, data authors, publishers, data distributors, and affiliated institutions all receive appropriate credit via a data citation with a persistent identifier (e.g., DOI, or Handle).

The strenght of Dataverse is versionning. 

 https://dataverse.org

### Open Source Licenses

(See part I)

## Data Management Plan

Not all data are sharable, but all projects must have a Data Management Plan (DMP)

Data collection and documentation

1.1 What data will you collect, observe, generate or re-use?

1.2 How will the data be collected, observed or generated?

1.3 What documentation and metadata will you provide with the data?

Ethics, legal and security issues

2.1 How will ethical issues be addressed and handled?

2.2 How will data access and security be managed?

2.3 How will you handle copyright and Intellectual Property Rights issues?

Data storage and preservation

3.1 How will your data be stored and backed-up during the research?

3.2 What is your data preservation plan?

4. Data sharing and reuse

4.1 How and where will the data be shared?

4.2 Are there any necessary limitations to protect sensitive data?

## Data Sustainability

What is the point of digitising the whole history of the world if we cannot reliability store it. 

#### Lifetime of memory supports

Stone : 10 000 years

Parchment : 1000 years

Film : 100 years

CD-Rom : 20 years 

#### Data preservation paradox

As volume of data increases, lifetime of memory support decreases. 

#### Case Study : DNA storage

Richard P. Feynman: "There's Plenty of Room at the Bottom”

In June 2019, all 16 GB of Wikipedia have been encoded into synthetic DNA.

#### Living archives

All archives are like theatre play. They need to be perform for surviving. 

## Personal Data

(Source Thouvenin et al 2020) 

### Personal Data

Personal data is any data that relates to an identified or an identifiable natural person, called data subject. This is the case if it is possible to distinguish an individual from others.

Identifiers may for example be the name, the birth date, an identification number, or an IP address.

When assessing whether an identification is possible, the possibility to combine data with other data must be taken into account.

### Sensitive Personal Data

Within personal data, “sensitive personal data” constitutes a special category. The processing of this sensitive personal data requires the compliance with additional requirements, such as higher standards with regard to consent by the data subject.

What kind of data is considered sensitive?

Comparison revDPA (CH) and GDPR (EU)

### Anonymized Data

Personal data can be pseudonymized or anonymized. A pseudonymization process leads to a state where “personal data can no longer be attributed to a specific data subject without the use of additional information” (Article 4 Paragraph 5 of the GDPR)

Unlike with pseudonymization, anonymization results in data where an attribution to a natural person is not possible anymore. In case personal data is anonymized, it is not considered to be personal data and falls out of the scope of data protection laws

### Case Study : Using Amnesia (Anonymisation)

https://amnesia.openaire.eu/amnesiaInfo.html

"Amnesia implements data anonymization techniques from the field of Privacy Preserving Data Publishing (PPDP). The key idea in anonymization is that identifying information is removed from the published data, so no sensitive information can be attributed to a person. The anonymization procedure is not limited to the removal of direct identifiers that might exist in a dataset, e.g. the name or the Social Security Number of a person; it also includes removing secondary information, e.g. like age, zipcode that might lead indirectly to the true identity of an individual. This secondary information is referred to as quasi-identifiers. To better understand how secondary information can be used to re-identify a person, consider the following example. A publisher that owns medical data of patients wants to publish an anonymized version of the data she owns. The data are superficially anonymized by removing direct identifiers e.g., names and social security numbers, but descriptive information like the zip code of the patient’s residence and her/his age remain. An adversary who wants to identify the patients that are related to the anonymized data, may have access to such descriptive information from other sources, e.g., a voter’s registry. The re-identification can be achieved by matching the descriptive information (Zip code, Age) of the anonymized data to the public registry. If a single match is produced for a given combination, then a patient can be accurately identified. The sparser the data are, the more unique combinations exist, and the easier it is for an adversary to locate unique records that correspond to specific users."

### Principle of purpose limitation

According to the principle of purpose limitation, personal data may only be processed for the purpose defined beforehand and communicated to the data subjects. This means that the purpose of the data processing must be defined first and it is not allowed to collect personal data for yet to define purposes.

### Principle of transparency

The principle of transparency prescribes that the data processing is clear to the data subject and that they are informed openly and clearly about the means and purposes of the processing

### Principle of proportionality

The principle of proportionality requires that personal data may only be processed to the extent it is objectively suitable and necessary to achieve a specific purpose

### Data subject rights 

Comparison swiss vs Europe. 

Right to be informed: Data subjects have the right to be informed about what personal data concerning them is processed, as well as the means and purposes of the processing.

\- Right of access: Data subjects may request access to the personal data concerning them.

\- Right to rectification: In case personal data is inaccurate, data subjects may request the data to be rectified.

\- Right to erasure: Data subjects may request that their personal data is erased.

\- Right to restrict processing: Data subjects have the right to request the restriction of processing of their personal data.

\- Right to data portability: Individuals may request a copy of their personal data in order to reuse it for their own purposes on a different service without affecting its usability. This right has to be seen in the context of making sure that people may switch to another service provider.

\- Right to object: Data subjects have the right to object the processing of their personal data.

## Right to be forgotten

The right to be forgotten is the right of persons to “determine the development of their life in an autonomous way, without being perpetually or periodically stigmatized as a consequence of a specific action performed in the past.”

**Rehabilitation of Offenders Act (UK)** : Its purpose is that people do not have a lifelong blot on their records because of a relatively minor offence in their past. The rehabilitation period is automatically determined by the sentence

**Droit à l’oubli (France)** : “Droit à l’oubli” officially recognized in French Law in 2010.

**Right to know (US):** the right of free speech according to the First Amendment, and the right to know.

**Costeja case (2014)**: May 13, 2014 the European Court of Justice legally solidified that the "right to be forgotten” is a human right when they ruled against Google in the Costeja case.

**Right to be forgotten -> Right to erasure**. As of May 2014, Google had removed 1,390,838 URLs. Incl Facebook (11,973 URLs) YouTube (5,999 removed), Twitter (4,588 removed). However, you can access them from outside Europe. 

**Right to be forgotten vs Right to privacy.** Right to privacy constitutes information that is not publicly known, whereas the right to be forgotten involves removing information that was publicly known at a certain time and not allowing third parties to access the information.

Weighting the individual's right to privacy against the public's right to know

Associated Businesses : Businesses which focus on protecting their client’s online reputation have jumped on the European Court ruling as a potentially profiting business.

**Right to be forgotten vs Right to inform.** Is RTBF is a form of censorship, against Freedom of Speech? Should journalism be protected ?

Wikipedia co-founder Jimmy Wales "described the EU's Right to be Forgotten as deeply immoral, as the organisation that operates the online encyclopedia warned the ruling will result in an internet riddled with memory holes"

But other commentators cite the example of particular practices like, revange porn. 

**Development of Jurisprudence at the Strasbourg court.**

A geopolitical question.

A complex debate between the risk for individuals and risk for society. 



## Summary 

Data management is associated with a larger number of difficulties and obligations. 

## In the next chapter

We will deal with user management 

## Further Reading

## To be developped  

- Uncertainty management. Visualisation and Paradata 



## To be put somewhere else : Processing power

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

