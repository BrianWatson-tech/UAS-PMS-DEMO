# Training Event Management

## Overview

I designed the Training Events portion of the UAS PMS to document organized UAS training activities separately from the individual training records maintained for each pilot.

A training event may involve multiple pilots, instructors, aircraft, and different types of training.  Instead of entering the same event information separately for every pilot who attends, the Training Events structure provides a record of the overall event.

Individual pilot training can then be documented separately and associated with the appropriate pilot.

This allows me to maintain information about both the event itself and the training completed by individual pilots without treating them as the same type of record.

## Operational Problem

UAS training can involve more than simply recording that a pilot attended a class.

A training event may include classroom instruction, equipment familiarization, scenario-based exercises, manual flight training, mapping instruction, or other hands-on activities.

Multiple pilots may participate in the same event.

If the complete event information has to be recreated separately for every pilot, the same information is entered repeatedly.  This takes additional time and increases the possibility that records from the same event will contain inconsistent information.

At the same time, simply recording that a training event occurred does not provide a complete individual training history for each pilot.

I needed a way to document the overall event while still maintaining individual pilot training information where it belongs.

## Separating Training Events From Individual Training

I designed Training Events and Individual Training as related but separate parts of the UAS PMS.

The **Training Event** represents the overall organized activity.

The **Individual Training** record represents training associated with a particular pilot.

At a high level:

**Training Event → Participating Pilots → Individual Training Records**

This structure allows information that applies to the entire event to be maintained at the event level while pilot-specific information can be maintained with the individual pilot.

The separation also makes it easier to understand what actually occurred during an event without placing all information into one large record.

## Manual Flight Training

Manual flight training performed during a training event needs to be documented.

A pilot attending an event does not necessarily mean that the pilot performed manual flight training.  I wanted the system to preserve that distinction.

When manual flying occurs, the activity needs to be documented as part of the UAS training information and also included in the pilot's individual training documentation as required.

This provides a better record of actual hands-on training rather than relying only on attendance at an event.

At a high level, the process can be viewed as:

**Training Event → Pilot Participation → Manual Flight Training → Individual Training Documentation**

The UAS PMS provides the UAS program record of this activity.

## Department Training Records

The Department Training Department maintains the pilot's official individual training record.

The UAS PMS does not replace that official record.

When UAS training requires information to be entered into a pilot's official individual training record, the UAS PMS provides organized information that supports that process.

This means the two systems serve different purposes.

The UAS PMS documents and organizes training information needed by the UAS program.  The Department Training Department maintains the official individual training record.

I designed the UAS PMS around that existing responsibility rather than attempting to create a competing official training system.

## Event-Level Information

The Training Events structure allows information that applies to the overall event to be maintained together.

This can include information such as the type of training, date of the event, training organization, and other information needed to describe the training activity.

Keeping event-level information separate prevents the same basic event information from having to be recreated for every participating pilot.

It also provides a record that can be reviewed later to understand what training activities were conducted by the UAS program.

## Pilot Participation

A training event may involve multiple pilots.

The structure therefore needs to account for the relationship between an event and the people who participated in it.

The event record answers the question:

**What training activity occurred?**

The individual training information helps answer:

**What training did this particular pilot complete?**

Keeping those questions separate makes the records easier to understand and maintain.

It also provides more flexibility as the amount of training information grows over time.

## Why I Designed It This Way

I did not want the training portion of the UAS PMS to become one large list containing pilots, events, flight activity, and every other piece of training information.

Those items are related, but they represent different things.

Separating Training Events from Individual Training allows the system to maintain the event once and associate the appropriate individual training information with the pilots who participated.

This reduces unnecessary duplicate entry while preserving the information needed at both the program and individual level.

It also gives me a clearer picture of the UAS program's training activities without requiring me to reconstruct that information from individual personnel records.

## Reducing Administrative Work

Training documentation can create a significant amount of administrative work when information has to be entered or reconstructed from multiple sources.

By maintaining a structured Training Events record, I can document information about the event once rather than repeatedly recreating the same information for each participant.

The individual pilot information can then be handled through the appropriate Individual Training process.

This allows the information to be organized closer to when the training occurs and makes it easier to review later.

The goal is to reduce the amount of time required to determine what training occurred, who participated, what hands-on training was performed, and what information needs to be documented elsewhere.

## Supporting Program Oversight

Training Events also provide information about the training activity of the UAS program as a whole.

Individual Training tells me about a particular pilot.

Training Events provide another view by showing the organized training activities being conducted by the program.

Both views are useful.

Together they provide a better picture of training activity than either type of record could provide by itself.

## Supporting Future Reporting

Maintaining Training Events as structured records provides a foundation for future reporting.

The information can eventually support questions such as:

- What UAS training events were conducted?
- When did the events occur?
- What type of training was provided?
- Which pilots participated?
- Was manual flight training conducted?
- Which organization provided the training?
- How much training activity occurred during a particular period?

The goal is to collect information in a structured way so that it can later support reporting without requiring the records to be manually rebuilt each time the information is needed.

## Design Considerations

When developing the Training Events structure, I considered several factors:

- Maintain the overall training event as its own record.
- Separate event information from individual pilot training records.
- Support multiple pilots participating in the same event.
- Document manual flight training when it occurs.
- Distinguish event attendance from actual hands-on flight training.
- Support the documentation needed for individual pilot training records.
- Recognize the Department Training Department as the manager of the official individual training record.
- Avoid replacing an established Department training process.
- Reduce repeated entry of the same event information.
- Maintain consistent training types where practical.
- Support different training organizations.
- Include specialized UAS training such as Pix4D / Mapping where appropriate.
- Make training activity easier to review.
- Support future reporting.
- Reduce unnecessary administrative work.

These decisions were based on how UAS training actually needs to be documented and managed rather than simply creating another list of training dates.

## Development and QA Approach

I developed the Training Events structure as a separate component of the UAS PMS and reviewed how it relates to Pilots and Individual Training.

During development, I considered the difference between documenting an overall event and documenting what an individual pilot actually completed.

I also accounted for manual flight training and the requirement for applicable training to be documented through the Department's established individual training process.

The Training Events structure went through development and QA to review the fields, relationships, and intended workflow.

Completing QA on this component does not mean that the entire UAS PMS is complete.  It means that this portion of the system reached its completed development milestone.

## Current Status

The Training Events structure has completed its current development and QA milestone.

This milestone represents the Training Events structure that has been developed and reviewed to this point.

Historical training information still requires controlled migration and validation before the overall UAS PMS can be considered complete.

Existing Lists, spreadsheets, training records, and other source information remain sources for that later migration process and are not being altered as part of this portfolio documentation.

## What I Learned

Developing the Training Events component helped reinforce the difference between recording an activity and recording how that activity applies to an individual person.

A training event may involve many pilots, but each pilot may have a different training experience during that event.

Someone may attend an event while another pilot performs actual manual flight training.  Those differences matter when the information is later reviewed.

Separating the overall event from the individual training records gives me a better way to represent those differences.

It also reinforced the importance of designing around existing Department processes.  The UAS PMS can organize UAS training information and make the administrative process easier without trying to replace the Department Training Department's responsibility for official individual training records.

The larger lesson for me was that a useful system needs to reflect how the work actually happens.  Understanding the process first makes it easier to decide what information needs to be collected, where it belongs, and how the different records should relate to each other.

## Data and Security Notice

This documentation describes the Training Events design at a portfolio level.  No pilot names, employee identification numbers, official training records, training certificates, confidential employer information, restricted operational information, or other sensitive information is included in this repository.
