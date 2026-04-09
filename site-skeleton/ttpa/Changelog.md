# TTPA Changelog

## Introduction

This document describes the (major) changes to [the current version 0.0.2](https://model-001a02.pages.code.europa.eu/) of the TTPA model.

## Detailed changes from v0.0.1 to v0.0.2

The table below gives an overview of the classes (and their definitions) within both data models. Classes that are related are juxta-positioned.

**C** stands for changes in classes

**R** stands for changes in relationships

**P** stands for changes in properties

**D** stands for changes in data types

# TTPA Changelog

| Nr | TTPA v0.0.1 | TTPA v0.0.2 | Rationale |
| --- | --- | --- | --- | 
| C | Targeting | Targeting Technique | renamed and restructured as subclass of Technique to separate targeting from ad delivery |
| C | - | Technique | addition of this generic superclass for Targeting Technique and Ad Delivery Technique |
| C | - | Ad Delivery Technique | addition of this class as subclass of Technique to model ad delivery separately from targeting |
| C | - | Identifier | addition of this class to provide structured identification references for agents |
| C | Campaign Financial Information | - | removal of this class; financial information now consolidated under Funding |
| C | Funding | Funding | definition changed from "Financial support provided for a project..." to "An amount of money available to finance some project or activity"; addition of Reference field |
| R | Funding / has campaign financial info | - | removal following consolidation of Campaign Financial Information into Funding |
| P | - | Funding / currency | addition of this property, moved from Campaign Financial Information and Political Advertisement Information |
| P | - | Funding / has value | addition of this property with range Decimal, moved from Campaign Financial Information and Political Advertisement Information |
| R | - | Funding / has political advertisement | addition of this relation to link funding directly to the political advertisement |
| P | Political Advertisement / hasEnd | Political Advertisement / has end | property renamed for consistent naming convention |
| R | Political Advertisement / has Initiative | Political Advertisement / has initiative | relation renamed for consistent casing convention |
| R | - | Political Advertisement / has technique | addition of this relation to link the political advertisement to its targeting and ad-delivery techniques |
| P | - | Political Advertisement / identifier | addition of this property to provide a persistent unique identifier for the political advertisement |
| R | - | Political Advertisement / is funded by | addition of this relation to link the political advertisement to its funding |
| P | Political Advertisement / is linked to election | - | removal of this boolean property; linkage now expressed via has election relation |
| P | Political Advertisement / is linked to legislative process | - | removal of this boolean property; linkage now expressed via has initiative relation |
| P | Political Advertisement / previous non-compliance exists | - | removal of this property; non-compliance now covered by status property |
| P | Political Advertisement / has beginning (def: "The beginning of a period or interval") | Political Advertisement / has beginning (def: "The start of the period") | definition simplified |
| P | - | Targeting Technique / use targeting techniques | addition of this property for a description of the targeting technique(s) used |
| P | Targeting / ad delivery technique description | Ad Delivery Technique / use ad delivery techniques | property moved and renamed following separation of ad delivery from targeting |
| P | Targeting / usage of AI systems | Ad Delivery Technique / use of AI systems | property moved following separation of ad delivery from targeting |
| P | Targeting / analytics | - | removal of this property |
| P | Targeting / consent notice | Technique / consent notice | property moved to Technique superclass |
| P | Targeting / has personal data | Technique / has personal data | property moved to Technique superclass |
| P | Targeting / hasBeginning | Technique / has beginning | property renamed and moved to Technique superclass for consistent naming convention |
| R | Targeting / hasController | Technique / has controlling entity | relation renamed and moved to Technique superclass |
| P | Targeting / hasEnd | Technique / has end | property renamed and moved to Technique superclass for consistent naming convention |
| P | Targeting / hasPolicy | Technique / has policy | property renamed and moved to Technique superclass for consistent naming convention |
| P | Targeting / internal policy URL | - | removal of this property; now covered by Technique / has policy |
| P | Targeting / number of clicks, likes, or comments | Technique / number of comments | property split into separate properties for comments and likes |
| P | Targeting / number of clicks, likes, or comments | Technique / number of likes | property split into separate properties for comments and likes |
| P | Targeting / number of views | Technique / number of views | property moved to Technique superclass |
| P | Targeting / other relevant information | Technique / other relevant information | property moved to Technique superclass |
| P | Targeting / use ad delivery techniques based on personal data | - | removal of this boolean property; ad delivery now modelled as separate class |
| P | Targeting / user rights support URL | Technique / user rights support URL | property moved to Technique superclass |
| R | Transparency Notice / has political advertisement | - | removal of this relation; link now expressed via Political Advertisement / is funded by and Funding / has political advertisement |
| R | Transparency Notice / has targeting | - | removal of this relation; targeting now linked from Political Advertisement / has technique |
| R | Transparency Notice / paying entity | - | removal of this relation; paying entity now modelled under Funding / has paying entity |
| R | Transparency Notice / sponsor | Transparency Notice / has sponsor | relation renamed for consistent naming convention |
| P | Transparency Notice / modified (range: Literal) | Transparency Notice / modified (range: Date) | range changed from Literal to Date for type consistency |
| P | - | Address / full address | addition of this property to provide the complete address as a single text string |
| P | Person / has email, Legal Entity / has email | Agent / has email | property moved to Agent superclass to avoid duplication |
| R | - | Agent / identifier (range: Identifier) | addition of this relation to link an agent to a structured Identifier |
| P | Legal Entity / alternativeTitle | Legal Entity / alternative title | property renamed for consistent naming convention |
| P | Legal Entity / has email | - | removal from Legal Entity; property moved to Agent superclass |
| P | Legal Entity / is postal address different than establishment | - | removal from Legal Entity; property already exists on Agent superclass |
| P | Legal Entity / notation | - | removal from Legal Entity; notation now modelled under the new Identifier class |
| P | Person / has email | - | removal from Person; property moved to Agent superclass |
| P | - | Identifier / notation | addition of this property, moved from Legal Entity to the new Identifier class |