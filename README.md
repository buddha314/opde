# Differential Prosecution

There is some speculation on the level of government or corporate involvment in various crimes againsts minors, especially sex offenders.  Though it is difficult to believe in global conspiracies, the American judicial system has shown a bias when treating famous or powerful individuals.

A group called "Operation Death Eaters" is pursuing what they deem "pedosadists" and the potential for government or institutional obfuscation of their crimes.

As a scientist (who happens to work with data, lots of it) and father, this subject is inherently interesting to me.  This repository will accumulate tools and methods to aid in legitimate (e.g. non-vigilante) law enforcement activities, from the local to the national level.

# Data Collection Program

Public data sources, legally harvested, should be collected in their raw format, including links to "related stories" or blogs.  When harvesting, the following data fields should be recorded if available.

* Date of harvest
* URL or data source
* Credentials for harvesting.  If paywalled, this should be noted.
* User or id of collector.
* Tools or feature extractors used (like ScraPy or Beautiful Soup) so that we may return for uncollected material later.
* Search terms or other inlinks leading to the source material.
* Additional labels should be developed and curated, including such things as
    * Does this article indicate conspiracy?
    * Does this article involve national figures?
    * Does this article involve national figures as suspects?
    * Does this article discuss events from the last 7 / 30 / 60 / 90+ days?  (to get a sense of media attention)

I cannot at this time provide a repository for the raw data.

# Feature Extraction Program

* We will take some initial passes with the Stanford NER libraries to create an entity database.
* I will perform a variety of machine learning / deep learning techniques to the data (with public source and results) for futher feature extraction.
* More later as I think on this.

# Tools

It is important to develop a case management tool.  There are several on the market currently.  This tools should satisfy
* The ability to create a "case" around a topic.
* The ability to track entities from case to case
* A strict auditing capability to see which users accessed which data
* The ability to add unstructed content to the case portfolio
* The ability to comment and discuss each case amongst registered users.
