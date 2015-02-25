# Differential Prosecution

There is some speculation on the level of government or corporate involvment in various crimes againsts minors, especially sex offenders.  Though it is difficult to believe in global conspiracies, the American judicial system has shown a bias when treating famous or powerful individuals.

A group called "Operation Death Eaters" is pursuing what they deem "pedosadists" and the potential for government or institutional obfuscation of their crimes.

As a scientist (who happens to work with data, lots of it) and father, this subject is inherently interesting to me.  This repository will accumulate tools and methods to aid in legitimate (e.g. non-vigilante) law enforcement activities, from the local to the national level.  The goal of these methods is to aid in prosecution, and therefore strict data governance must be observed.

# Data Collection Program

Public data sources, legally harvested, should be collected in their raw format, including links to "related stories" or blogs.  When harvesting, the following data fields should be recorded if available.

* Date of harvest
* URL or data source
* Credentials for harvesting.  If paywalled, this should be noted.
* User or id of collector.
* Tools or feature extractors used (like ScraPy or Beautiful Soup) so that we may return for uncollected material later.
* Search terms or other inlinks leading to the source material.
* Additional labels should be developed and curated, including such things as
    * Does this article indicate conspiracy? (I suggest this as a soft measure, in the eye of the beholder)
    * Does this article involve national figures?
    * Does this article involve national figures as suspects?
    * Does this article discuss events from the last 7 / 30 / 60 / 90+ days?  (to get a sense of media attention)

I cannot at this time provide a repository for the raw data.

# Feature Extraction Program

* We will take some initial passes with the Stanford NER libraries to create an entity database.
* I will perform a variety of machine learning / deep learning techniques to the data (with public source and results) for futher feature extraction.
* More later as I think on this.

# Investigative Questions

* Can we quantify preferential treatment of pedosadists by the judciary and/or media?
* Are certain crimes or behaviors being willfully ignored by the judiciary or media?
* Are there certain crimes that are unprosecutable?

## The Notion of "Conspiracy"

My personal feeling is that this word is too vague.  I would rather avoid it as it brings unsophisticated attention.

# Tools

It is important to develop a case management tool.  There are several on the market currently.  This tools should satisfy:
* The ability to create a "case" around a topic.
* The ability to track entities from case to case
* A strict auditing capability to see which users accessed which data
* The ability to add unstructed content to the case portfolio.
* The ability to label/tag content by users for discussion.  E.g, I may suggest this article indicates prejudice or bias, but others may disagree.
    * This must include moderation.
* The ability to comment and discuss each case amongst registered users.
    * Note that having registered users is essential for data lineage and audit.

## Notes on Platforms

This system is entity-based, so may either be constructed over a Graph Database (like Titan, Neo4J, etc) or a Graph Processing System like GraphX or Dato/Graphlab.  Performance is unlikely to be the driving factor, so it may be better to use a Graph Processing tool atop a standard table structure.

Raw documents should be stored in a document store such as Solr, MongoDB or, if they are small enough, in Postgres.  Postgres enables full text search and updates, making it easier to manage meta-data within documents than Solr or Mongo.

# Victim Anonymity

Clearly, it is very important to respect the privacy of victims.  The current design is not considering a "crime reporting" tool, but rather a media or news collection tool.  We could revisit this assumption, of course.

Thus anonymity may be enforced at one of two levels.  First, the media may not report the names or identities of the victims.  Second, the hosting application may manually redact all names of potential victims.  In that latter case, an internal entity ID is easy to construct, but must be human curated. 

For the purposes of prosecution, any redacted names should be recorded (perhaps offline) but not displayed publically.  This will also be important in building social networks later.

# Anonymity of the Accused

The accused should also enjoy full judicial process. Witch hunts hurt everyone.

# Why A Secondary Database?

For the same reason we need the ACLU and the Southern Povery Law Center, it is the way democracy works. 
