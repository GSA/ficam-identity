---
layout: page_collection
title: Step 1 - Core Identity Attribute Collection
permalink: /1_step-1/
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
-----------------------------------------------------

An agency typically collects a wide variety of data elements about its employees, contractors, and other support staff who have access to agency resources. Within this data set, smaller subsets of attributes enable an agency to uniquely identify an individual within the organization and support the execution of meaningful access control decisions. This data set is known as the core digital identity. 

The ICAM Subcommittee developed the government-wide Core Person Model for agencies working to align with the FICAM Architecture, which will assist in the management and sharing of digital identity records.  As shown in the table below, the Core Person Model provides a common definition for the attributes that contain a digital identity record within the Federal Government. 

<br>

| <center> Attribute </center> | <center> Description </center> |
| :---------------------------:|--------------------------------|
| **Person Identifier** | Uniquely identifies an individual within a specified domain in which the person exists (e.g., Locally Unique Identifier [LUID] associated with the Backend Attribute Exchange [BAE]) |
| **Name** | An individual's name, typically including first, middle, last, and display names |
| **_Set of_ Biometrics** | A measured biological or behavioral characteristic of an individual (e.g., electronic fingerprint template, facial image) |
| **Physical Description** | An individual's physical characteristics (e.g., height, eye color, hair color, sex) |
| **Birth Record** | Pertains to the place (city, state, and country) and date of a person's birth record |
| **Contact Information** | Includes an individual's phone number(s) and work mailing address |
| **_Set of_ Credentials** | Relates to one or more identity credentials possessed by an individual (e.g., credential sponsor, FASC-N, serial number(s), issuer, revocation uniform resource identifier [URI], etc.) |
| **_Set of_ Citizenships** | An individual's country or countries of citizenship, commonly expressed as a digraph or trigraph |
| **_Set of_ Email Addresses** | An individual's current and historical email addresses |
| **_Set of_ Clearances** | An individual's background investigation and/or clearance history (e.g., investigation type, completion date, status, etc.)|
| **_Set of_ Affiliates** | An individual's affiliation with an organization (e.g., employee status, business relationship, etc.)|
| **Social Security Number (SSN)** | An individual's SSN or other national ID with a corresponding country code for foreign nationals |

<br>

## <span style="color: #0C5C89">**Checklist**</span>

> <i class="fa fa-check-square-o"></i> &nbsp;**Identify where each data element is collected and stored.** It’s important to know the location of each attribute and the responsible office or group(s) that collect and maintain data elements. 

> <i class="fa fa-check-square-o"></i> &nbsp;**Map agency data to the model.** After you’ve identified the location of each data element, you should map the data model to the Core Person Model to tailor it for agency use. 

> <i class="fa fa-check-square-o"></i> &nbsp;**Determine additional core data elements, if necessary.** If  more attributes are necessary to support the implementation of the Core Person Model, they should be limited to the elements needed to uniquely identify an individual within the organization and that support your agency’s specific mission needs. Other identity attributes may be collected to support enhanced access control scenarios, but these are considered entitlement attributes, not part of the basic digital identity record. 

> <i class="fa fa-check-square-o"></i> &nbsp;**Identify opportunities for process integration.** You should identify redundancies in data collection associated with the Core Person Model and determine opportunities to integrate and streamline these business processes by referencing existing identity data. 


## <span style="color: #0C5C89">**Benefits**</span>

> <i class="fa fa-thumbs-o-up" aria-hidden="true"></i> &nbsp;**Eliminate redundant identity data creation.** Your agency will be able to reduce or eliminate the need for extra business processes that may collect redundant identity data for specific application use. 

> <i class="fa fa-thumbs-o-up" aria-hidden="true"></i> &nbsp;**Enable interoperability and more robust identity attribute sharing.** Your agency is provided a common basis for sharing identity attributes internally. When combined with the establishment of attribute management and distribution services, agencies are able to offer enhanced attribute sharing capabilities for use by programs and applications across the organization. 

> <i class="fa fa-thumbs-o-up" aria-hidden="true"></i> &nbsp;**Streamline identity life cycle management.** The administrative burden associated with identity life cycle management will be greatly reduced, while improving data quality and accuracy. 

> <i class="fa fa-thumbs-o-up" aria-hidden="true"></i> &nbsp;**Increase the accuracy and reliability of provisioned identities.** This will provide consistency across enterprise identities and improve the accuracy of user account data established through automated provisioning workflows.























