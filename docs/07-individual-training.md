# Individual Training Management

## Overview

Training is an important part of maintaining a qualified UAS program.  I designed the Individual Training portion of the UAS PMS to provide a structured way to document training completed by individual pilots and maintain that information as part of the UAS program.

UAS training can include classroom instruction, specialized training, equipment-related training, mapping instruction, and actual manual flight training.  Manual flying conducted during training events must be documented within the UAS program and also documented in the pilot's official individual training record maintained by the Department Training Department.

These records serve different purposes.  The UAS PMS maintains information needed to manage and review training within the UAS program, while the Department Training Department maintains the official individual training record for the pilot.

I designed the UAS PMS to support that existing process rather than attempt to replace it.

## Operational Problem

UAS pilots can complete many different types of training throughout their participation in the program.  A single pilot may accumulate numerous training activities over time.

Some training also includes actual manual flight time that needs to be documented.

If training information is scattered across spreadsheets, emails, certificates, flight records, and other sources, it becomes more difficult to determine what training has been completed and whether the required information has been documented.

At the same time, I did not want to create another system that attempted to replace the Department's established training records.

I needed a structure that could document UAS-specific training information while still recognizing that the Department Training Department maintains the pilot's official individual training record.

## Separating Pilots From Training Records

I designed the system so that the pilot and the training record represent two different types of information.

The **Pilots** structure identifies the person.

The **Individual Training** structure documents training completed by that person.

At a high level, the relationship can be viewed as:

**Pilot → Individual Training Records**

One pilot can therefore be associated with multiple individual training records.

This prevents me from repeatedly recreating the pilot's primary information every time new training is completed.  It also allows the pilot's UAS training history to grow over time without requiring the structure of the pilot record itself to change.

## Individual Training Record

Each Individual Training entry represents a specific training activity associated with a pilot.

The record can maintain information needed to identify the training, when it occurred, the type of training, the organization providing the training, and other information needed to document the activity.

I included **Pix4D / Mapping** as a training type because mapping and related UAS capabilities are among the types of training that may need to be documented.

The training organization can also be maintained as part of the record.  For the current environment, DART PD is the default training organization while still allowing training provided by another organization to be documented when appropriate.

The goal is to maintain a consistent UAS training history rather than using a different method to document each type of training.

## Manual Flight Training

Manual flight training is an important part of UAS training and needs to be documented.

When pilots perform manual flying during UAS training events, that activity needs to become part of the training record rather than simply being considered part of the event and then forgotten.

The UAS PMS provides a way to maintain that information within the UAS program.

Documenting the actual training activity provides a better record of what occurred during the training event and helps distinguish attendance at an event from actual hands-on flight training.

This is important because attending a training event and actually performing manual flight training are not necessarily the same thing.

## Department Training Records

Manual flight training conducted during UAS training events must also be documented in the pilot's official individual training record, which is maintained by the Department Training Department.

The UAS PMS and the Department's official training records have different responsibilities.

The **UAS PMS** maintains the UAS program's structured record of the training activity.

The **Department Training Department** maintains the pilot's official individual training record.

At a high level, the process can be viewed as:

**UAS Training Event → Manual Flight Training → UAS PMS Training Documentation → Department Individual Training Record**

The UAS PMS is not intended to replace the Department's official training record system.  It provides the UAS program with the information needed to document, manage, and review UAS training while working within the Department's established training process.

This distinction was important when I designed the system.  I wanted the UAS PMS to improve UAS program recordkeeping without creating a competing official personnel training record.

## Training Events and Individual Training

A training event and an individual pilot's training record are also different types of information.

The training event describes the overall event.  Individual Training documents training associated with a particular pilot.

At a high level:

**Training Event → Participating Pilots → Individual Training Records**

This allows information about the overall event to be maintained without placing every pilot's individual training history directly into the event record.

It also allows an individual pilot's UAS training history to remain associated with that pilot even though the training may have occurred during a larger event involving multiple pilots.

## Why I Designed It This Way

I wanted the UAS PMS to separate information based on what the information actually represents.

A pilot is a person.

A training event represents an organized training activity.

An individual training record represents training associated with a particular pilot.

Manual flight training represents actual hands-on flying performed as part of that training.

The Department's individual training record is the official departmental record maintained through the Department Training Department.

These pieces of information are related, but they are not the same thing.

Separating them allows the UAS PMS to maintain useful UAS program information without trying to force everything into one large record or replace an established Department process.

## Supporting Qualifications and Readiness

Training records can help provide information about pilot experience, qualifications, and program readiness.

The Individual Training structure is not intended to automatically determine whether a pilot is qualified for a particular assignment.  It provides organized information that can support that review.

For example, being able to review training history and documented manual flight training can provide useful information when determining what training a pilot has completed.

The system supports the decision by organizing the information.  It does not replace the person responsible for reviewing the pilot's qualifications.

## Reducing Duplicate Data Entry

Reducing unnecessary duplicate data entry is one of the overall goals of the UAS PMS.

The pilot's primary information should not have to be recreated every time the pilot completes another training activity.

Instead, the training record can be associated with the existing pilot record.

At the same time, some information must exist in more than one system because the records serve different purposes.  UAS program documentation and the Department's official individual training record are an example of this.

That is different from unnecessary duplication.

The goal is to eliminate duplicate work where practical while still maintaining information in the official systems where it is required.

## Reducing Administrative Work

A structured Individual Training system gives me a consistent place to locate UAS training information instead of having to reconstruct a pilot's UAS training history from multiple unrelated sources.

It also helps me identify the information that needs to be documented through the Department's established training process.

This makes the distinction between UAS program records and official Department training records clearer.

The goal is to organize the information at the time the training occurs so that less time is required later to determine who participated, what training was completed, and what information needs to be documented.

## Supporting Future Reporting

Structured training records also provide a foundation for future reporting.

Because individual training is maintained separately from the pilot record and training event, the information can eventually be filtered, grouped, and reviewed in different ways.

For example, the structure can support questions such as:

- What UAS training has a particular pilot completed?
- Which pilots participated in a particular training event?
- What type of training was conducted?
- When was the training completed?
- Which organization provided the training?
- Was manual flight training performed?
- What types of UAS training have been documented within the program?

The purpose is to make these questions easier to answer from organized information rather than manually reviewing multiple unrelated sources.

## Design Considerations

When developing the Individual Training structure, I considered several factors:

- Maintain each training activity as its own record.
- Associate training with the appropriate pilot.
- Allow one pilot to have multiple training records.
- Separate individual training from the overall training event.
- Document manual flight training performed during training events.
- Maintain information needed to support Department training documentation.
- Recognize the Department Training Department as the manager of the official individual training record.
- Avoid attempting to replace the Department's official training record system.
- Avoid repeatedly entering the same pilot information.
- Maintain consistent training types where practical.
- Include Pix4D / Mapping as a training type.
- Maintain the organization providing the training.
- Use DART PD as the current default training organization while allowing other organizations when needed.
- Make UAS training history easier to locate and review.
- Support qualification and readiness reviews.
- Maintain information that can support future reporting.
- Allow a pilot's training history to grow without redesigning the pilot record.
- Reduce unnecessary administrative work while maintaining required records.

These decisions were based on how the training information actually needs to be used rather than simply creating another list of courses and names.

## Development and Testing Approach

I developed the Individual Training structure as a separate component of the UAS PMS and reviewed how it would connect with the Pilots and Training Events structures.

The design was refined so that individual training could be associated with the correct pilot while remaining separate from the overall training event.

I also considered how manual flight training needs to be documented and how the UAS PMS fits into the Department's existing training-record process.

This allowed me to design the UAS PMS around an existing operational requirement instead of creating a separate process that did not account for the Department's official records.

After development and review, the Individual Training structure reached the point where I considered the current DEV design complete and locked.

Locking the structure does not mean that every historical training record has been migrated or that the entire UAS PMS is complete.  It means that this component reached its current completed development milestone.

## Current Status

The Individual Training structure has been completed and locked in the development environment.

The structure supports individual pilot training records, including the documentation of manual flight training associated with UAS training activities.

The Department Training Department remains responsible for maintaining the pilot's official individual training record.  The UAS PMS does not replace that official record.

This milestone represents completion of the current Individual Training data structure.  Historical training information still requires controlled migration and validation before the overall UAS PMS can be considered complete.

Existing Lists, spreadsheets, training records, and other source information remain sources for that later process and are not being altered as part of this portfolio documentation.

## What I Learned

Developing the Individual Training component reinforced the importance of understanding which system is responsible for which information.

The UAS PMS needs enough information to manage and document UAS training, but that does not mean it should replace every existing Department system.

The Department already has an established process for maintaining official individual training records.  My job in designing the UAS PMS was to determine how the UAS program's training information fits into that process.

It also reinforced the importance of separating related information into appropriate records.

A pilot, a training event, an individual training activity, and manual flight training are related, but they represent different things.  Structuring those records appropriately makes the information easier to maintain and review.

I also learned that eliminating duplicate work does not necessarily mean that information should exist in only one place.  Sometimes information must be documented in separate systems because those systems serve different official purposes.

The goal is to eliminate unnecessary duplication while making sure required records are still maintained.

This is the same approach I am using throughout the UAS PMS: understand the operational requirement first, determine where the information belongs, connect related information where appropriate, and use technology to make the process easier without interfering with established responsibilities.

## Data and Security Notice

This documentation describes the Individual Training design at a portfolio level.  No pilot names, employee identification numbers, official training records, training certificates, personnel information, confidential employer information, restricted operational information, or other sensitive information is included in this repository.
