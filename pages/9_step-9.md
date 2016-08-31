---
layout: page_collection
title: Step 9 - Integrate Your AAES With Your IT infrastructure
permalink: 9_step-9/
---
<script>
$(function() {
  $( "#accordion" ).accordion({
    heightStyle: "content",
    collapsible: "true",
    active: "false"
  });
});
</script>

<script src="https://use.fontawesome.com/e20c671b68.js"></script>
---------------------------------------------------------

Designing an AAES solution architecture requires agencies to consider the capabilities presented in the FICAM Architecture, existing ICAM investments (e.g., logical access solutions), and your agency’s overall IT infrastructure. The goal of this step is to find how an AAES capability will integrate with your agency’s IT infrastructure and provide digital identity attribute sharing services.

An AAES provides a consolidated system for securely and electronically exchanging digital identity attributes between authoritative data sources and your agency applications that consume those attributes. In many cases, this data is spread across multiple authoritative sources within your agency, which complicates the challenge of exchanging attributes between sources and consumers. The AAES should be primarily comprised of two specific solution components:

> * Authoritative Attribute Manager. Provides the capability to present a single, authoritative view of that data by reconciling and aggregating attributes from the various sources.

> * Authoritative Distributor. The component that integrates with attribute consumers and conducts the data exchange.

The FICAM Architecture [Applications View](http://gsa.github.io/ficam-arch/applications/) provides a view of general enterprise ICAM applications and systems. It represents multiple solutions that your agency may choose to use. The solution components are represented generically and could be implemented using a variety of Commercial Off-The-Shelf (COTS) or purpose-built products. Your agency should evaluate its existing ICAM and infrastructure investments and select the approach that best meets their needs.

<br>

| AAES Characteristic ID | <center> AAES Solution Characteristics </center> |
|:-----------------------------------------:|------------------------|
| **AAES 1** | Provides aggregation of identity attributes |
| **AAES 2** | Supports deployment of connectors and service interfaces to retrieve identity attributes for distributed sources |
| **AAES 3** | Uses a unique person identifier to distinguish between identities |
| **AAES 4** | Provides transformation of identity attributes from authoritative source data storage format to a standardized format to present data externally |
| **AAES 5** | Provides correlation of identity attributes from distributed sources of identity information |
| **AAES 6** | Provides the capabiltiy to reconcile differences between different sources of identity attributes | 
| **AAES 7** | Provides an interface to request identity attributes over common protocols, such as LDAP/s, DSML, SAML, and SPML |
| **AAES 8** | Provides security to protect data against unauthorized access and logging to facilitate audits |
| **AAES 9** | Provides various views of identity attributes and display them only to users or systems that are authorized to view those attributes |
| **AAES 10** | Provides the ability to request identity data based on a variety of methods (name, globally unique identifier, email, DOB) |
| **AAES 11** | Provides reports of identity attributes | 
| **AAES 12** | Provides the capability to push or pull identity attributes, including the ability to distribute new identities and updates to existing identity attributes |
| **AAES 13** | Provides the capability to protect data at rest |
| **AAES 14** | Provides the capability to sign attribute assertions |