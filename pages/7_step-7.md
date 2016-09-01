---
layout: page_collection
title: Step 7 - Address Your Attribute Exchange Elements
permalink: 7_step-7/
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
--------------------------------------

When seeking to electronically share attribute data between authoritative source systems and relying parties, you must be address protocols, payload, and agency policies to support the attribute exchange.

> * **Identity a common exchange protocol.** This allows the involved parties to communicate using the same language and set of rules. Your agency should select a protocol that meets the technical needs of both the Identity Provider and Relying Party when establishing an attribute sharing capability. The selection of a protocol that meets your agency’s need also depends on the type of connection that is preferred between the parties. You should also be aware that different types of connections might not be equally supported by all approved protocols.

The table below describes several common protocols used for exchanging identity data.

<br>

| <center> Protocol </center> | <center> Description </center> |
|:---------------------------:|------------------------------------------|
| **LDAP/s** | Lightweight Directory Access Protocol is used to read and/or edit directories. Traffic to and from the directory should be encrypted (i.e., TLS, SSL, Internet Protocol Security). Access control should be in place to ensure data is provided to only those authorized to view it. |
| **DSML** | Directory Service Markup Language provides directory service information in an XML syntax. Data traverses across HTTP/s. |
| **SAML**| Security Assertion Markup Language is used to exchange authentication and authorization data in XML. |
| **SPML**| Service Provisioning Markup Language is an open standard that uses an XML-based framework for the integration and interoperation of service provisioning requests. |

<br>

> * **Define which attributes will be exchanged and how they will be formatted.** Defining attribute syntax (e.g., format) helps ensure that identity attributes are received in such a manner that they are usable within a relying party application. This is typically accomplished by establishing an attribute contract (Definition - A document that extensively describes the agreement on the set of, and syntax of, attributes that members of a federation have to abide by on the payload.) When streamlining the exchange and management of identity data within an agency, it’s expected that the payload will align with the government-wide Core Person Model. However, an agency may opt to include additional attributes based on its specific mission and business needs.

> * **Establish an exchange policy.** Establishing governance is important to maintain the ongoing operation of identity attribute sharing arrangements and to provide a framework ensuring both the Identity Provider and Relying Party(s) operate within the boundaries of the arrangement. An agency implementing an internally-focused attribute sharing capability should establish agency policies governing the appropriate use of identity data that is made available through the solution. This can often lessen the need for point-to-point agreements between groups within the organization.

<br>

<div style="background-color: #edf1f3;color: black;margin: 10px;padding: 10px">
<h3><span>Privacy Tip</span></h3>
<p><span>Implementing an attribute sharing capability provides an agency with a number of benefits and process efficiencies. However, one goal of this effort is to avoid collecting and/or sharing more Personally Identifiable Information (PII) than is necessary for the intended use. Therefore, only collect the attributes necessary to share with a relying party. To achieve this, agencies should consider establishing attribute agreements or attribute practice statements to address which attributes will be shared and the manner in which they will be conveyed, to ensure privacy and security.</span></p>

</div>
















