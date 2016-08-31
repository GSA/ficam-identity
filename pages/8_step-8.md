---
layout: page_collection
title: Step 8 - Link Identity Attributes
permalink: 8_step-8/
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

Agencies should eliminate duplicate and/or redundant digital identity records to ensure that each federal user has only a single digital identity. Managing a single digital identity record for each user within the organization requires that an agency establish a process to link or bind identity attributes to the appropriate record. There are three common techniques for accomplishing this: (1) Unique Person Identifiers, (2) Multi-Attribute Keys, and (3) Manual Identity Attribute Correlation. 


## <span style="color: #0C5C89">**Checklist**</span>

> <i class="fa fa-check-square-o"></i> &nbsp;**Evaluate approaches for linking identity attributes to the appropriate record and determine which method meets your needs.**

>> **Approach #1: Unique Person Identifiers.** 

>> A unique person identifier is an alphanumeric string attribute that identifies a person’s enterprise digital identity from others, even in cases where the underlying identity attributes may be the same (e.g., two employees with the same name). If your agency chooses to implement a single enterprise system for managing identity data, unique person identifiers should be used to correlate identity data in advance of the implementation to ensure the system is populated with accurate data. Despite any changes to an individual‘s role within the organization (e.g., a contractor becomes a federal employee), these identifiers are generally assigned to an individual as part of the initial on-boarding process and persist throughout the digital identity life cycle. Agencies aren’t required to establish unique person identifiers. However, doing so can help streamline the processes required to manage digital identity and support the implementation of other ICAM programs.

>> Unique person identifiers are best used when:

>>> * Performing direct access lookups of digital identities

>>> * Reconciling collisions between identity attributes that occur as a result of automated matching processes

>>> * Limiting data discrepancies when binding identity data to an individual across multiple agency systems

<br>

| <center> Benefit </center> | <center> Description </center> |
|-------------------------------------------------------------|
| **Reduced data discrepancies** | Correlate identity data for the same individual across multiple systems. Using a unique person identifier helps to easily detect and resolve conflicts between different sources of identity attribute data and helps to ensure the uniqueness of an identity across the enterprise. |
| **Streamlined digital identity creation** | Streamline the process for reconciling attributes into a single digital identity by eliminating the need to manually correlate attributes across various source systems. |
| **Modernized access control** | Using a unique person identifier provides an agency with a greater degree of confidence when granting user access in an automated fashion because the identity attributes that are used to support authentication and authorization decisions are bound to an individual‘s digital identity through the unique identifier. |
| **Streamlined federated identity management** | In a federated environment, agencies can correlate identity data by sharing their unique person identifiers, called parallel person identifiers. Alternatively, an agency can add an agency-specific code to its unique person identifier or have its own agency-specific code added to another organization‘s unique person identifier. Doing so would extend the attribute‘s uniqueness and reciprocity across the broader Federal Government community. |
| **Visibility into identity data** | Agencies will better understand the user‘s role and entitlements across the enterprise. This data can be analyzed within an agency or between agencies for account auditing, threat identification, privilege correlation, and compliance. |

<br>

>> **Approach #2: Multi-Attribute Keys**

>> A multi-attribute key is a combination of identity attributes that can be bound to serve as an identifier for user records across multiple systems. A multi-attribute key is a combination of identity attributes that can be bound to serve as an identifier for user records across multiple systems. This approach allows your agency to take advantage of data that is already available to the agency and would likely require less modification to existing systems. Additionally, multi-attribute keys provide a layer of redundancy, which can help address an error in a single attribute that is part of the key. If an error is present, an agency can analyze the other identity attributes within the key to determine the correct individual. This may be desirable to some agencies to mitigate the risks associated with poor data quality.

<br>

>> **Approach #3: Manual Identity Attribute Correlation**

>> In cases where unique person identifiers or multi-attribute keys aren’t used, it’s likely that your agency will need to apply additional processes to bind identity attributes for an individual. This type of attribute correlation is often labor and time intensive. In addition, use of manual attribute correlation can reduce the ability to detect and resolve security and audit issues that may arise in identity records and user accounts (e.g., duplicate entries for the same individual due to status or affiliation changes). This can also result in duplicate user accounts and identity records appearing in other agency applications. Duplicate user accounts can drive up software licensing costs on some applications, and the accounts may not be detected and terminated when a user leaves the agency.

>> Despite these challenges, your agency might choose this approach, because there is only a minimal need to change business processes and upgrade or procure technology. This might also serve as a transitional approach until regular technology refresh cycles allow an agency to implement a more automated solution to achieve greater levels of efficiency.

<br>

> <i class="fa fa-check-square-o"></i> &nbsp;**Align the method with existing or planned capabilities.**

>> **Approach #1: Unique Person Identifiers**

>> When implementing a system to create and manage unique person identifiers, your agency should ensure that these attributes are randomly generated in a way the identifier cannot be easily guessed by a third party. Identifiers should be generated according to a common standard, algorithm, or naming convention. The identifier itself shouldn’t be based on commonly available information about the individual, and such information about the user shouldn’t be able to be obtained by manipulation or reverse engineering.

>> Unique identifiers shouldn’t be derived from or linked to data that is subject to change, such as user biographic data or credential-specific numbers. For example, the Federal Agency Smart Credential Number (FASC-N) or optional Universally Unique Identifier (UUID) of the PIV card shouldn’t be used as a person’s enterprise unique identifier if the intended use is to link the identity record to the user‘s active credential. These numbers are linked to a specific credential and change with each consecutive card issued to that person. If your agency is only seeking an authoritative originator for its unique numbers and the identifier can persist across the user’s digital identity life cycle, a card identifier may be a viable option. As an alternative, an agency should establish a separate unique person identifier attribute (i.e., not linked to a credential) that is intended to support digital identity management for managed identities that will span multiple credentials.

>> Although there may be multiple authoritative sources containing different sets of data about an individual, the unique identifier should be generated from one originator. Doing so eliminates the possibility of collision or conflict between identifiers issued from different sources. In some cases, it may make sense for your agency to generate a unique identifier with an existing system that houses digital identity data (e.g., HR or PIV card enrollment). Some of these systems, however, only contain identity data for a portion of the total user population and should be extended to include the entire intended user population if they will be used to create unique identifiers.

>> It’s also important that unique identifiers be reconciled on a regular basis to ensure there’s neither redundant identifiers nor the same identities with different identifiers. If fraudulent enrollment is a concern, your agency can leverage one-to-many biometric matching against the entire enrolled community to detect duplicate enrollments and reconcile individuals who may have more than one identifier.

>> Your agency should consider the life cycle of unique person identifiers and establish a policy to govern if identifiers for identities that are no longer valid can be recycled and reused. Your agency‘s policy for the life cycle of unique person identifiers should seek to address the following:

>>> * **Identifier Longevity.** Your agency should set a life span (years) that must expire before an identifier could be recycled, which should be at least as long as the potential life span of any archived records associated with the user.
>>> * **Management of identifiers.** Your agency should determine how identifiers will be managed for a user that has become inactive, but may reinitiate his/her affiliation with the agency in the future. Doing so ensures that an identifier is not made available for re-use during the defined life span.
>>> * **Temporary users.** Your agency should determine if temporary users not expected to return in the future will obtain unique identifiers from the same system/process as other users, or if a secondary namespace with lower longevity is needed.

<br>

>> **Approach #2: Multi-Attribute Keys**

>> To establish a multi-attribute key, your agency must designate an attribute set (two or more identity attributes) to serve as key fields within its relational database system(s). Your agency should choose attributes which, when combined, are sufficient to tell the difference among users within their agency community. For example, combining name, date of birth (DOB), entrance on duty date, and home telephone number is likely to be enough to tell the difference between individuals that might share a common attribute (e.g., the same name). Once a multi-attribute key has been established, the database system will then enforce this property as new records are added across the database. When duplicate identifiers are compared, these key fields will be analyzed to further refine the search and identify the correct record.

>> When selecting attributes to form a multi-attribute key, your agency should evaluate the use of attributes that are considered PII. PII is generally subject to use restrictions, which could affect the availability of a multi-attribute key that includes a PII data element.

<br>

>> **Approach #3: Manual Identity Attribute Correlation**

>> Correlating identity attributes can typically be accomplished in two ways:

>>> * Develop a correlation algorithm that must be manually applied by an administrator through a batch process; or

>>> * Manual linking by an administrator using a pre-defined rule set

>> Within your agency or organization, each application may have different naming standards for user account creation. Without a unique identifier or multi-attribute key to serve as the primary key, it may be necessary to develop unique correlation algorithms for every application in the enterprise. In addition to requiring additional development time, this process may also introduce additional risk in successfully identifying related records during correlation activities. To resolve these errors, administrators would then spend additional time manually verifying identities, attributes, and entitlements and reconciling each account within the application.

<br>

<div style="background-color: #edf1f3;color: black;margin: 10px;padding: 10px">

<h3><span>Implementation Tip #3</span></h3>
<p><span>Request for Comments (RFC) 4122, A Universally Unique Identifier (UUID) Uniform Resource Namespace, offers agencies a standardized approach for creating unique person identifiers using time-based, name-based, or random number algorithms. Leveraging an approach like RFC 4122 is the preferred approach to creating identifiers, as it results in an infinitesimally small chance of collision, without the need for a managed identifier namespace.</span></p>

</div>

<br>

<div style="background-color: #edf1f3;color: black;margin: 10px;padding: 10px">

<h3><span>Implementation Tip #4</span></h3>
<p><span>Treasury’s HRConnect has been identified as the authoritative source of core identity data for employees and contractors within Treasury. As a result, HRConnect is the originator of the Treasury Unique Identifier (TrUID), which is used to link users in USAccess, Treasury Enterprise Directory, and bureau Identity Management Systems (IDMS) through the user’s lifecycle. This approach dramatically improves data quality and reduces redundant collection of data.</span></p>

</div>

<br>

<div style="background-color: #edf1f3;color: black;margin: 10px;padding: 10px">
<h3><span>Lessons Learned</span></h3>
<p><span>A federal agency with a large user base began a logical access control system (LACS) modernization effort, initially relying on manual attribute correlation techniques to bind identity attributes to digital identities. Early in the implementation, the agency determined that the time and effort associated with manually resolving data collisions had significant impacts to the cost and schedule of the overall effort. To mitigate this, the agency implemented a unique person identifier system, which offered a more efficient approach to identity correlation.</span></p> 

</div>