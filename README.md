# UAS Program Management System

## Project Overview

I am developing a UAS Program Management System (UAS PMS) to improve how information related to a public-safety UAS program is collected, organized, maintained, and reported.

I began this project because managing a UAS program involves information spread across several areas, including aircraft, batteries, pilots, training, maintenance, equipment, flight activity, and reporting.  As the UAS Maintenance Officer, I found that locating and organizing this information could require a significant amount of administrative time.

I wanted to develop a better way to manage that information while also making routine processes as simple as practical for the pilots using the system.

The result is an evolving UAS PMS built primarily with Microsoft 365 tools.

## Why I Built It

The project started with two basic goals:

**Make routine processes easier for the pilots.**

Pilots should not have to understand the underlying data structure or navigate complicated systems simply to document normal UAS activity.

**Reduce the amount of administrative time required for me to manage the program.**

Information collected during normal operations should be structured so that I can more easily use it for maintenance, equipment management, training review, accountability, and reporting.

The overall idea is simple:

**Capture useful information once, organize it consistently, and make it easier to use later.**

## Technology

The UAS PMS is being developed within the Microsoft 365 environment using tools available for the project, including:

- Microsoft Forms
- Microsoft Lists
- Microsoft Excel
- Power Query
- Basic Power Automate workflows

Microsoft Forms provides simple user-facing data entry where appropriate.

Microsoft Lists provides structured storage for the different types of program information.

Excel and Power Query provide a way to retrieve, organize, analyze, and eventually report information maintained within the Lists.

Power Automate is being evaluated and used where appropriate to reduce repetitive manual steps.

## System Design

The UAS PMS is not one large spreadsheet or List.

I am separating information according to what it represents and then connecting related information where appropriate.

Examples include:

- Aircraft
- Batteries
- Pilots
- Individual Training
- Training Events
- Aircraft Checkouts
- Flight Logs
- Maintenance
- Support Equipment
- Vendors

This allows information to be maintained in the appropriate location without repeatedly storing the same information in every record where it may be needed.

For example, a pilot can have multiple training records, an aircraft can have multiple maintenance records, and a piece of support equipment can have its own maintenance history.

This structure also provides a better foundation for future reporting and analysis.

## Operational Workflow

The system is being designed around the way the UAS program actually operates rather than around a particular software product.

A simplified example of the data workflow is:

**Microsoft Forms → Microsoft Lists → Excel / Power Query → Reporting**

Other information sources can also support the process when appropriate.

For example, I currently use DroneSense as part of UAS operations and maintenance.  DroneSense can provide information such as battery data and maintenance information, and selected information can be exported in CSV format for use within the UAS PMS workflow.

Battery information can also be reviewed through aircraft controllers.

The UAS PMS is not dependent on DroneSense.  I designed the Microsoft 365 system so that it can operate independently while still allowing information from DroneSense or other sources to be used when that information provides value.

## Maintenance Management

Maintenance is one of the major reasons I began developing the system.

My responsibilities require me to manage information involving inspections, maintenance needed, maintenance completed, troubleshooting, battery condition, equipment status, and maintenance history.

The UAS PMS is intended to make that information easier to organize and review.

The maintenance process includes both corrective and preventive maintenance.

For example, battery discharge-cycle information can provide a maintenance indicator and help identify when an action such as battery conditioning should be considered.

A simplified process can be viewed as:

**Equipment Use → Maintenance Indicator → Inspection or Maintenance → Verification → Documentation**

The system does not make maintenance decisions for me.  It provides organized information that helps me make and document those decisions more efficiently.

## Training Management

The UAS PMS also separates overall training events from training associated with individual pilots.

A training event may involve multiple pilots and several different activities.

Individual training records document training associated with a particular pilot.

Manual flying performed during UAS training events also needs to be documented.

The UAS PMS maintains the UAS program's training information, while the Department Training Department maintains the pilot's official individual training record.

The UAS PMS is designed to support that established process rather than replace it.

## Existing Systems

One of the design principles I have followed is that the UAS PMS should work with existing systems where useful without unnecessarily depending on them.

DroneSense is an example.

I currently use DroneSense for operational functions including maintenance scheduling, documenting maintenance needed and completed, and reviewing or exporting selected equipment information.

Where that information can reduce duplicate work, I can incorporate selected data into the UAS PMS workflow.

However, the core UAS PMS remains a Microsoft 365-based system that can function without DroneSense.

This allows the system to benefit from existing tools without making those tools a requirement for the underlying design.

## Development Approach

I am developing the UAS PMS in stages.

Rather than attempting to build the entire system at one time, I work through individual components, review the fields and relationships, test the workflow, make corrections, and then move to the next area.

Some components have reached completed development milestones while other portions of the system are still being developed, reviewed, or prepared for later migration.

I am documenting the project as it actually progresses rather than presenting it as a finished system before the remaining work has been completed.

## Repository History

The UAS PMS was already under active development before I created this GitHub repository.

Because of that, several of the initial GitHub commits document development milestones that had already been completed before the repository was created.  These initial commits establish the project history up to its current development point and should not be interpreted as indicating that all of those components were originally designed and built on the dates of the GitHub commits.

Going forward, new commits will document additional development, testing, QA, migration, validation, reporting, and other milestones as that work is actually completed.

This allows the repository to begin with an accurate record of the work already performed and then continue as an ongoing development history.

## Current Development Status

The project is still in development.

Several core structures have been created, reviewed, tested, or completed in the development environment.  Other components still require additional verification or QA.

Historical information from existing Lists and spreadsheets will eventually require a controlled migration process.

That process will include reviewing field mappings, cleaning information where necessary, importing records, and validating items such as counts, identifiers, dates, statuses, and relationships.

Existing operational Lists and spreadsheets are being treated as source records and are not being modified simply for the purpose of building this portfolio.

## Documentation

The `docs` folder contains individual development milestones and design explanations.

The documentation focuses on more than what technology was used.  I am also documenting:

- The operational problem I was trying to solve
- Why I designed the component the way I did
- How the information is structured
- How different parts of the system relate to each other
- How the workflow reduces unnecessary work
- How the component was developed or tested
- What I learned while developing it
- The current status of the component

This provides a record of both the technical development and the reasoning behind the design.

## Project Goals

The long-term goals of the UAS PMS are to:

- Make routine UAS data entry easier for pilots.
- Reduce unnecessary administrative work.
- Improve organization of UAS program information.
- Support aircraft and equipment maintenance.
- Support preventive maintenance.
- Maintain useful equipment history.
- Improve training documentation.
- Support equipment accountability.
- Reduce duplicate data entry where practical.
- Make information easier to retrieve and analyze.
- Provide structured information for future reporting.
- Maintain clear boundaries with existing official Department systems.
- Create a system that can continue to evolve as program requirements change.

## Current Project Status

**Status: Active Development**

The UAS PMS is not being presented as a finished production system.

This repository documents the development work completed to date and will continue to grow as additional components are developed, tested, validated, and implemented.

## Data and Security Notice

This repository is intended to document the design and development of the UAS PMS without publishing operational or sensitive information.

No production records, pilot information, employee identification information, aircraft serial numbers, battery serial numbers, DroneSense identifiers, maintenance records, confidential employer information, restricted operational information, or other sensitive data is included in this repository.

Examples and documentation are limited to information appropriate for a public technical portfolio.
