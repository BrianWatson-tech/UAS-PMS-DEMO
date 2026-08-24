# Maintenance Management

## Overview

Maintenance management is one of the primary reasons I began developing the UAS Program Management System.  As the UAS Maintenance Officer, I need a reliable way to identify maintenance that is needed, document maintenance that has been completed, review equipment history, and keep track of the overall condition of the equipment I am responsible for.

The maintenance process involves more than repairing an aircraft after something fails.  It also includes inspections, preventive maintenance, battery maintenance, troubleshooting, documenting problems, tracking work that still needs to be completed, and maintaining a history of what has been done.

I designed the Maintenance portion of the UAS PMS to organize that information in a structured Microsoft 365 environment and reduce the amount of time I spend locating and managing maintenance information.

The goal is to give me better information to manage maintenance while reducing unnecessary administrative work.

## Operational Problem

Maintenance information can originate from several different places.

A problem may be reported by a pilot.  I may identify an issue during an inspection.  Battery information may indicate that maintenance such as conditioning should be performed.  Information may also be available through DroneSense, an aircraft controller, or other operational records.

Without a structured process, maintenance information can become scattered across different systems, notes, emails, spreadsheets, or individual records.

That makes it more difficult to answer basic maintenance questions:

- What equipment currently needs maintenance?
- What problem was reported?
- What maintenance has already been completed?
- When was the equipment last inspected?
- Does additional work still need to be performed?
- What maintenance history exists for a particular piece of equipment?

I wanted the UAS PMS to provide a consistent place to maintain this information so that I do not have to reconstruct the maintenance history each time I need it.

## Maintenance Record Design

I designed the Maintenance structure so that maintenance activity can be maintained as its own record.

A maintenance record represents a maintenance issue, inspection, repair, preventive-maintenance action, or other maintenance-related activity.

Keeping maintenance records separate from the equipment records allows an individual aircraft, battery, or piece of support equipment to accumulate multiple maintenance records over time.

At a high level, the concept can be viewed as:

**Equipment → Maintenance Records**

This provides a maintenance history without requiring all maintenance information to be stored directly inside the equipment's primary record.

## Maintenance Needed and Maintenance Completed

An important part of the maintenance process is distinguishing between work that needs to be performed and work that has already been completed.

Identifying a problem does not mean the maintenance has been completed.

I need to be able to document that maintenance is needed, review the outstanding issue, perform or coordinate the appropriate work, and then document what was completed.

At a basic level, the process can be viewed as:

**Issue Identified → Maintenance Needed → Maintenance Action → Maintenance Completed → Verification**

This provides a clearer maintenance history than simply changing an equipment status without documenting what occurred.

It also gives me a way to identify work that may still require attention.

## Monthly Inspections

Scheduled inspections are part of my maintenance responsibilities.

I currently use DroneSense to help schedule monthly inspections and document maintenance activity.  This includes documenting maintenance that is needed and maintenance that has been completed.

The UAS PMS provides its own maintenance structure so that the Microsoft 365-based system is not dependent on DroneSense.

DroneSense can therefore support my current operational workflow while the UAS PMS maintains the structured information needed for its own maintenance-management process.

The intent is not to recreate every DroneSense function.  The intent is to use existing information when it is useful while maintaining a UAS PMS that can operate independently.

## Preventive Maintenance

I wanted the Maintenance portion of the UAS PMS to support preventive maintenance as well as repairs.

Waiting for equipment to fail is not the only way a maintenance need can be identified.

Inspection schedules, equipment usage, battery discharge cycles, controller information, maintenance history, and other available information can provide indicators that equipment needs attention.

Battery discharge cycles are one example.  Cycle information can help identify when a battery may have reached a point where conditioning or another maintenance action should be considered.

At a basic level:

**Equipment Use → Maintenance Indicator → Inspection or Preventive Maintenance → Documentation**

The system does not make the maintenance decision for me.  It organizes information that can help me determine when maintenance may be appropriate.

## Aircraft Maintenance

Aircraft are one of the primary types of equipment that may require maintenance.

An aircraft can experience different types of issues during its service life.  These may be identified during normal operations, pilot reports, scheduled inspections, troubleshooting, or other maintenance activities.

The Maintenance structure provides a way to document those activities separately from the aircraft's primary inventory record.

This allows an aircraft to maintain a history of multiple maintenance activities over time rather than having the current aircraft record overwrite the history of previous problems and repairs.

## Battery Maintenance

Batteries also require maintenance and monitoring.

Battery information such as discharge cycles can provide useful information about usage and can help identify when maintenance such as conditioning should be considered.

Battery information may be available through DroneSense, aircraft controllers, or UAS PMS records.

The maintenance process can use that information as another indicator when reviewing battery condition.

Maintaining battery-related maintenance history also allows me to see more than the battery's current status.  I can maintain information about maintenance activity that occurred during the battery's service life.

## Support Equipment Maintenance

Maintenance is not limited to aircraft and batteries.

Support equipment used by the UAS program can also require inspection, troubleshooting, repair, replacement, or other maintenance activity.

For that reason, I added a Support Equipment ID lookup to the Maintenance structure.

At a high level:

**Support Equipment → Maintenance Record**

This allows a maintenance record to identify the support equipment involved without requiring support-equipment maintenance to be maintained in a completely separate system.

This was an important design decision because I wanted the maintenance process to support the equipment I am responsible for rather than assuming every maintenance issue involves an aircraft.

## Relationship With DroneSense

DroneSense is an important operational tool in my current maintenance workflow.

I use it to schedule monthly inspections, document maintenance that is needed, and document maintenance that has been completed.

However, I intentionally designed the UAS PMS so that DroneSense is not required for the maintenance structure to function.

Where information from DroneSense is useful, it can support the maintenance process.  Where DroneSense is not available, the Microsoft 365-based UAS PMS can still maintain its own maintenance records.

This is the same approach I used with battery information.

I want to take advantage of useful information and capabilities that already exist without creating a system that stops functioning if access to another application changes.

## Troubleshooting and Verification

Maintenance sometimes begins with a reported problem rather than an obvious equipment failure.

In those situations, the maintenance process may involve reviewing available information, checking equipment, examining logs or other records, identifying possible causes, taking corrective action, and then testing the equipment to determine whether the issue has been resolved.

Documenting the result is an important part of that process.

A maintenance action should not automatically be considered successful simply because a change was made.

The basic troubleshooting process I try to follow is:

**Problem Reported → Information Reviewed → Possible Cause Identified → Corrective Action → Operational Test → Result Documented**

This provides a better maintenance history and helps distinguish between an attempted corrective action and a verified resolution.

## Maintaining History

I do not want completed maintenance information to disappear simply because an equipment item is currently operational.

Historical maintenance information can provide useful context when another problem occurs later.

For example, repeated issues involving the same equipment may be easier to recognize when previous maintenance activity remains available for review.

Maintaining separate maintenance records allows the history to grow over time without replacing previous entries.

This supports both equipment management and troubleshooting.

## Reducing the Maintenance Officer Workload

Reducing the amount of administrative time required to manage maintenance is one of the main goals of the UAS PMS.

The information I need may originate from pilots, DroneSense, aircraft controllers, inspections, battery records, maintenance records, or other program information.

Without a structured process, I can spend unnecessary time locating and comparing information before I can act on it.

The UAS PMS is intended to make that information easier to organize and retrieve.

The goal is not to eliminate the need for me to inspect equipment, troubleshoot problems, verify information, or make maintenance decisions.

The goal is to reduce the administrative work surrounding those responsibilities so that more of my time can be spent actually managing and maintaining the equipment.

## Maintenance Workflow

At a high level, the maintenance process I am supporting with the UAS PMS can be viewed as:

**Problem or Maintenance Need Identified**

↓

**Equipment Identified**

↓

**Maintenance Need Documented**

↓

**Inspection / Troubleshooting**

↓

**Corrective or Preventive Action**

↓

**Operational Verification**

↓

**Maintenance Completed**

↓

**Maintenance History Retained**

Not every maintenance activity will require every step.  The workflow provides a general structure for thinking about how maintenance information moves from identifying a need through documenting the final result.

## Design Considerations

When developing the Maintenance structure, I considered several factors:

- Maintain maintenance activity as separate records.
- Associate maintenance with the appropriate equipment.
- Support aircraft maintenance.
- Support battery maintenance.
- Support support-equipment maintenance.
- Distinguish maintenance needed from maintenance completed.
- Support scheduled monthly inspections.
- Support preventive as well as corrective maintenance.
- Use equipment information such as battery discharge cycles when appropriate.
- Maintain maintenance history rather than overwriting previous activity.
- Support troubleshooting and verification.
- Document the result of maintenance activity.
- Use DroneSense information where it provides value.
- Keep DroneSense optional rather than making it a dependency.
- Reduce unnecessary duplicate data entry.
- Make outstanding maintenance easier to identify.
- Make maintenance history easier to locate and review.
- Reduce the administrative time required for me to perform Maintenance Officer responsibilities.

These decisions were based on how I actually manage maintenance rather than simply creating a list of repair records.

## Development and Testing Approach

I developed the Maintenance structure as a core component of the larger UAS PMS.

During development, I considered the different types of equipment that may require maintenance and how those maintenance records should relate to the equipment being managed.

The structure was expanded to include a Support Equipment ID lookup so that maintenance could be associated with support equipment as well as the other equipment managed by the system.

I also considered how maintenance-needed information, completed maintenance, scheduled inspections, preventive maintenance, and historical records fit into the overall process.

The Maintenance structure was reviewed and refined as these requirements were identified.

This allowed me to build the structure around actual maintenance responsibilities rather than designing the entire system first and trying to fit the maintenance process into it afterward.

## Current Status

The current Maintenance structure has been created and reviewed in the development environment.

The structure supports maintenance records and includes the ability to associate applicable maintenance activity with support equipment.

DroneSense continues to be used as part of my operational maintenance workflow for monthly inspection scheduling and maintenance documentation.  The UAS PMS maintenance structure remains designed to operate independently of DroneSense.

This milestone represents the Maintenance structure developed and confirmed to this point.

Historical maintenance migration, final production deployment, and system-wide validation remain separate phases and are not represented as complete.

Existing operational Lists, spreadsheets, DroneSense records, and other maintenance information remain source records for later controlled migration or reference and are not being altered as part of this portfolio documentation.

## What I Learned

Developing the Maintenance component reinforced that maintenance management is not simply a record of repairs.

A useful maintenance process needs to account for how a problem is identified, what equipment is involved, what work is needed, what action was taken, whether the action resolved the problem, and what history should be retained.

It also reinforced the value of preventive maintenance.

Information such as inspection schedules and battery discharge cycles can provide a reason to inspect or maintain equipment before a failure occurs.

I also learned that maintenance information can come from several systems and sources.  The challenge is not necessarily collecting more data.  The challenge is organizing the useful information so that I can make better and faster maintenance decisions.

The system does not replace my responsibility as the Maintenance Officer.  It is intended to give me a better way to manage the information I need to perform that responsibility.

That is the larger purpose of this portion of the UAS PMS: reduce unnecessary administrative work, maintain useful equipment history, and make it easier for me to identify, perform, document, and verify maintenance.

## Data and Security Notice

This documentation describes the Maintenance design and workflow at a portfolio level.  No production aircraft identifiers, battery identifiers, serial numbers, maintenance records, DroneSense information, confidential employer information, restricted operational information, or other sensitive information is included in this repository.
