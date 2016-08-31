---
layout: page_collection
title: Step 2 - Identify Authoritative Data Source(s)
permalink: 2_step-2/
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
-----------------------------------------------

An authoritative data source for identity is a repository or system that contains attributes about an individual and is considered to be the primary or most reliable source for this information. In the case that two or more systems have mismatched or have conflicting data, the data within the authoritative data source is considered the most accurate.

Within many federal agencies, authoritative identity data is dispersed across a number of different systems that are often independently managed. Some agencies, however, may operate a single centralized repository of identity data, such as an Identity Management System (IDMS). While your agency is not required to have a single repository of identity data, it’s expected your agency designate an authoritative data source for each data element in the Core Person Model and work to minimize the number of data sources used to collect and maintain the same identity information. In cases where an agency houses identity data elements across several authoritative data sources, it’s recommended that it share or map identifiers between the data sources to avoid collisions and errors.


## <span style="color: #0C5C89">**Checklist**</span>

> <i class="fa fa-check-square-o"></i> &nbsp;**Determine where identity data is stored.** Identifying which systems/resources are authoritative for specific identity attributes involves determining where identity attributes are first recorded and updated. 

> <i class="fa fa-check-square-o"></i> &nbsp;**Perform an analysis to identify which of those source systems should be designated as authoritative.** To comply with HSPD-12, many agencies have already identified authoritative data sources for the data elements that are required as part of the PIV enrollment and issuance process. It’s likely, however, that your agency will need to conduct added authoritative source discovery to identify an authoritative source for each data element contained in the Core Person Model.

> <i class="fa fa-check-square-o"></i> &nbsp;**Document and map digital identity data elements.** Mapping should be done based on how the data is originated, types of transformations that occur to the data, and where the data is stored. It’s possible for one system to be authoritative for data element creation and a second system to be authoritative for data element modification. For example, an employee’s initial building and room number may be created in the PACS, whereas subsequent changes to building and room may be handled in an employee locator system. It’s still important to ensure that there is only one authoritative source for data creation and only one for data modification.

The table below provides a number of common characteristics that you should look for as part of the discover process:

<br>

| <center> Characteristic </center>        | <center> Description </center> |
|------------------------------------------|--------------------------|
| **Primary Source** | Where an identity data element originates. The data is not received from another system or resource. |
| **Legal Authority to Collect** | Generally operates with a legal authority to collect certain data elements as part of the organization's mission (e.g., HR has the legal authority to collect identity data within federal agencies). |
| **Data Accuracy** | Considered to be accurate and reliable for a specific attribute(s) at any given time. |
| **Data Freshness** | Contains the most up-to-date data available and is generally the first system to be updated when data changes. |
| **Data Accessibility** | Limits the availability of certain data elements to those individuals or groups that have a need to know. |
| **Data Protection** | Has restrictions in place that limit the ability to change stored data to a select group of users. |
| **Data Ownership** | Generally owned and maintained by groups that own the data itself and can vouch for its authenticity. |
| **Data Modification** | Performs modification of data originated elsewhere (e.g., updating identity attributes for use in downstream processes, data normalization) and becomes authoritative by virtue of performing the modification. |

<br>

> <i class="fa fa-check-square-o"></i> &nbsp;**Prepare Authoritative Data Source.** Data preparation and cleanup is needed to remove redundancies and discrepancies in the data housed within authoritative data sources. If your agency has multiple authoritative sources, it should evaluate the merits of consolidating data sources where appropriate. As identity data from authoritative data sources is shared with downstream processes, further data preparation requirements will evolve (e.g., ensuring employment status information can be read by both logical access control systems (LACS) and physical access control systems (PACS) to trigger de-provisioning workflows).

> <i class="fa fa-check-square-o"></i> &nbsp;**Perform real-time or periodic synchronization.** Synchronization should occur in the authoritative data source as well as areas where the data is shared to ensure that identity data is current. For example, if the data attribute for an employee’s bureau/component affiliation changes in the authoritative data source, the change should be synchronized in other systems that use this data element. This is an important step in cases where identity attributes are used to determine access privileges on a resource.

> <i class="fa fa-check-square-o"></i> &nbsp;**Ideally, only modify Core identity data in one place.** Applications and processes reliant on authoritative data shouldn’t have the capability to manipulate authoritative data. Instead, they should only consume data and make business decisions based on them. Your agency should determine the logical place for updating each data attribute based upon the business processes that typically initiate the change (e.g., an agency personnel security system is a logical place for updates to background investigation status data).

> <i class="fa fa-check-square-o"></i> &nbsp;**Define processes that ensure the most accurate and recent identity data resides in the authoritative source.** There may be cases in which a downstream application has more recent data than the data housed in the authoritative source. In such cases, your agency should be capable of processing and approving out-of-band change requests to ensure the data in the authoritative data source is appropriately updated.


### Security and Privacy Considerations

Authoritative data sources are subject to the security and privacy requirements in accordance with the Federal Information Security Management Act (FISMA) of 2002 and the Privacy Act of 1974. Given the sensitive nature of the information contained within authoritative identity data sources, your agency should closely observe the requirements outlined in FISMA and consider implementing optional enhancements to provide an additional measure of security, if justified based on the information system risk classification. Potential enhancements include:

> <i class="fa fa-lock" aria-hidden="true"></i> &nbsp;**Enforcement of strict access permissions.** To maximize data integrity within authoritative data sources, agencies should take steps to ensure that the information contained within authoritative data sources cannot be manipulated or changed without strict rules and enforcement mechanisms.

> <i class="fa fa-database" aria-hidden="true"></i> &nbsp;**Appropriateness of data usage.** Agencies should take additional measures beyond the FISMA requirements to ensure that data usage or exchange stemming from authoritative data sources can be recorded and audited to ensure that data is accessed, used, and shared in accordance with security and privacy policies.

> <i class="fa fa-users" aria-hidden="true"></i> &nbsp;**Employee security enhancements.** Agencies should consider applying the security enhancements associated with high-impact systems, outlined in SP-800-53, to authoritative data sources. Doing so requires that additional security controls are put in place to protect the system and its data.

> <i class="fa fa-check-circle-o" aria-hidden="true"></i> &nbsp;**Verify authoritative source authenticity.** It may be desirable for downstream applications that rely on identity data from authoritative sources to validate the attributes provided by the source. This typically includes verifying the identity of the source and the time at which it validated the attribute values. This can be accomplished by verifying a digital signature placed by the authoritative source around selected groups of attribute- value pairs or by a real-time verification service.

> <i class="fa fa-user-times" aria-hidden="true"></i> &nbsp;**Provide redress capability.** In accordance with the Privacy Act of 1974, your agency should ensure that users have redress capabilities to rectify errors associated with identity records. This capability improves the accuracy and freshness of authoritative data, while also providing a level of transparency for end-users and consumers of identity data.

<br>

<div style="background-color: #edf1f3;color: black;margin: 10px;padding: 10px">

<h3><span>Case Study</span></h3>
<p><span>Sometimes identifying an authoritative source can lead to other efficiencies. Treasury identified HRConnect as its authoritative source of core identity data for employees and contractors. As a result, Treasury was able to establish HRConnect as the originator of the Treasury Unique Identifier (TrUID), which is used to link users in USAccess, Treasury Enterprise Director, and bureau Identity Management Systems (IDMS) through the user’s lifecycle. As a result, data quality is dramatically improved, while reducing redundant data collection.</span></p>

</div>

<br>

<div style="background-color: #edf1f3;color: black;margin: 10px;padding: 10px">

<h3><span>Implementation Tip #1</span></h3>
<p><span>Many agencies maintain an inventory of systems and applications that house Personally Identifiable Information (PII), often referenced in Systems of Record Notices (SORNs). This inventory can provide a starting point for determining which agency systems can serve as authoritative data sources for identity attributes. As a SORN specifies the permissible, or routine, use of the data in a particular system of records, modification will be necessary if the information will be used in a different way than anticipated.</span></p>

</div>

<br>

<div style="background-color: #edf1f3;color: black;margin: 10px;padding: 10px">
<h3><span>Implementation Tip #2</span></h3>
<p><span>Partially automating requests for redress within the standard IT environment can help speed up the processing time and improve data quality. However, requests for redress should never be processed without human review, because of the risk of falsification of identity details.</span></p>

</div>

<br>
