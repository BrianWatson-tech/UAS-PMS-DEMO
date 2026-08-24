# Pilot Management

## Overview

Pilot management is another core component of the UAS Program Management System.  Aircraft and equipment records are important, but the system also needs a structured way to maintain information about the personnel authorized to participate in the UAS program.

I designed the pilot portion of the UAS PMS to provide a consistent record for each pilot and to support other parts of the system that need pilot information.

The goal is to maintain pilot information once and allow that information to support other UAS PMS processes rather than repeatedly entering the same pilot information into separate records.

## Operational Problem

A UAS program generates records involving pilots across multiple activities.  Pilot information may be needed for aircraft checkouts, flight activity, training, qualifications, and other program functions.

If pilot information is entered independently every time one of those activities occurs, names and other information can be entered differently across records.  It also creates unnecessary repetitive data entry.

I wanted the UAS PMS to maintain a structured pilot record that could serve as a consistent reference for other parts of the system.

This reduces duplicate information and helps create more consistent records throughout the UAS PMS.

## Pilot Record Design

I designed the Pilots list so that each pilot has an individual record.

The pilot record provides a central location for information needed by the UAS PMS and creates a consistent identity that can be referenced by other components of the system.

I use a **Pilot ID** as the primary identifying value within the pilot structure.

Using a consistent identifier helps distinguish the pilot record from the pilot's name alone and provides a more reliable way to associate information across different areas of the system.

## Connecting Pilots to Other Records

One of the reasons for creating a separate Pilots structure is that pilot information is used in several other parts of the UAS program.

At a high level, pilot information can support relationships such as:

**Pilot → Aircraft Checkout**

**Pilot → Flight Activity**

**Pilot → Individual Training**

**Pilot → Training Events**

Rather than creating a completely new pilot record for each activity, the system can reference the existing pilot information.

This is part of the larger data-design approach I am using throughout the UAS PMS.  Information that represents a unique person, aircraft, battery, or other program asset should be maintained in an appropriate structured record and then referenced where that information is needed.

## Reducing Duplicate Data Entry

Reducing duplicate entry is an important design goal of the UAS PMS.

If a pilot's information already exists in the Pilots list, I do not want that information recreated manually every time the pilot completes training, checks out an aircraft, or performs another activity.

Repeated manual entry takes additional time and increases the possibility of inconsistent information.

Maintaining a structured pilot record provides a more reliable source for information that can be reused by other workflows.

This makes the system easier to maintain and supports more consistent reporting later.

## Supporting Pilot Workflows

The pilot structure is also intended to support workflows that should remain simple for the pilots themselves.

Pilots should not need to understand how the underlying Microsoft Lists are structured in order to complete routine activities.

Where appropriate, Microsoft Forms can provide the user-facing interface while the underlying Lists maintain the structured records.

This allows me to separate the user experience from the underlying data structure.

The pilot sees the information needed to complete the task.  The UAS PMS maintains the structured information needed behind the scenes.

## Training Relationship

Training is an important part of maintaining a qualified UAS program.

The pilot structure provides the foundation for associating training information with individual pilots.

Rather than placing all training information directly inside the pilot record, training can be maintained as its own structured information and associated with the appropriate pilot.

This provides greater flexibility because one pilot can have multiple training records over time.

It also prevents the pilot record from becoming unnecessarily large or difficult to maintain as additional training is completed.

## Why I Designed It This Way

I wanted the UAS PMS to separate information based on what that information represents.

A pilot is a person participating in the program.  A training record represents an event or qualification associated with that pilot.  A flight record represents operational activity.  An aircraft checkout represents another type of activity.

Although these records are related, they are not the same thing.

Separating them into appropriate structures makes the information easier to maintain and allows the relationships between the records to be used without repeatedly storing the same information.

This was an important part of learning how to think about structured data rather than simply creating individual spreadsheets for every task.

## Reducing Administrative Work

The pilot-management structure supports the larger goal of reducing unnecessary administrative work.

Maintaining consistent pilot information makes it easier for me to review records associated with pilots without repeatedly reconciling different versions of the same information.

It also creates a better foundation for future reporting because pilot activity, training, and other records can be associated with a consistent pilot identity.

The goal is to organize the information at the beginning of the process so that less time is required to correct or reorganize it later.

## Design Considerations

When developing the pilot-management structure, I considered several factors:

- Maintain an individual record for each pilot.
- Use a consistent Pilot ID.
- Reduce repeated entry of pilot information.
- Support relationships with flight activity.
- Support relationships with aircraft checkout records.
- Support individual training records.
- Support training-event information.
- Keep pilot-facing workflows as simple as practical.
- Separate user-facing Forms from the underlying data structure where appropriate.
- Maintain consistent information for future reporting.
- Make pilot information easier to manage as the UAS program changes.
- Avoid placing unrelated information into a single large record.

These decisions support the larger design of the UAS PMS and allow pilot information to work with other components rather than existing as an isolated list.

## Development and QA Approach

I developed the Pilots structure as one component of the larger UAS PMS.

The fields and structure were reviewed during development to determine whether the information being collected supported the other workflows that depend on pilot information.

The Pilots component has progressed through development and into QA.

QA provides an opportunity to review the structure and confirm that the information works as intended before the system progresses toward later migration and production phases.

This approach allows problems to be identified while the system is still being developed rather than after historical information has already been migrated into the new structure.

## Current Status

The Pilots component has reached the QA stage.

This milestone represents completion of the current pilot data structure and its progression into quality review.  It does not represent completion of the entire UAS PMS.

Historical data migration, final production deployment, and system-wide validation remain separate phases.

Existing operational Lists and spreadsheets remain source records for the future controlled migration process.

## What I Learned

Developing the pilot-management portion of the UAS PMS reinforced the importance of maintaining information according to what it represents rather than repeatedly storing the same information in every record where it is needed.

A pilot, a flight, a checkout, and a training record are related, but they represent different things.

Separating those records while maintaining relationships between them creates a structure that is easier to maintain and expand.

It also reinforced why consistent identifiers matter.  Names alone may not always provide the best way to associate information across multiple records, while a consistent Pilot ID provides another way to maintain those relationships.

This component helped me better understand how structured information can reduce duplicate work while improving consistency throughout a larger system.

## Data and Security Notice

This documentation describes the pilot-management design at a portfolio level.  No pilot names, employee identification numbers, contact information, personnel records, confidential employer information, restricted operational information, or other sensitive information is included in this repository.
