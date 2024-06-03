# RRMV

This portal presents  RRMV ontology (Regulatory Reporting Metadata Vocabulary) for modelling and representing the Requests inside of the European Legislation.

This ontology is developed inside of the project SORTIS (Study On Regulatory reporTIng Standards) promoted by JRC of the European Commission.

## What is a Request?

A Request is a linguistic mandate addreed to some agents to other agents called addressee to do something in a given time. The Request that we are interested to model are included in legislative provisions.

An example of Request is the following.

Regulation (EU) 2016/1011 on indices used as benchmarks in financial instruments and financial contracts

>Art. 54
>2. Review the evolution of international principles applicable to benchmarks and of legal frameworks and supervisory practices in third countries concerning the provision of benchmarks and report to the European Parliament and to the Council every five years after 1 January 2018. That report shall assess in particular whether there is a need to amend this Regulation and shall be accompanied by a legislative proposal, if appropriate.

## Anatomy of a Request

A Request involve Agent(s) that should performe Action(s).  
Action(s) are events that produce ActionResult(s) in a given time.  
The Action(s) could be repetitive, for this reason we have Frequency.  
Each Request has Topic(s).
Each Agent plays a Role in a given time.  

## ELI Ontology and AKN non-Ontology

We use AKN non-Ontology and ELI ontology based on FRBR (Work, Expression, Manifestation) for fostering the ELI metadata and detect the modifications over time of the Request.  
In this way we could discover modification in the Request, in the period of time where it is valid and so to alert the legal operators. 





