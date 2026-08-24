# Battery Management

## Overview

Battery management is an important part of the UAS Program Management System because batteries are individual pieces of operational equipment that need to be identified, monitored, maintained, and eventually removed from service when appropriate.  I designed the battery portion of the UAS PMS to give me a more consistent and efficient way to manage battery information as part of my responsibilities as the UAS Maintenance Officer.

My goal is not simply to maintain an inventory showing which batteries the program owns.  I want the information being collected about those batteries to help me determine when maintenance may be needed, document maintenance activity, monitor battery usage, and maintain a history throughout the battery's service life.

Battery information is available to me from more than one source.  I maintain selected battery and maintenance information in DroneSense, can obtain battery information through the aircraft controllers, and can generate battery reports from DroneSense in CSV format.

Rather than manually recreating information that already exists, I developed a process that allows selected battery data to be brought into the Microsoft 365 environment and used as part of the UAS PMS.

The overall goal is to spend less time locating, entering, comparing, and reorganizing battery information and more time using that information to manage and maintain the equipment.

## Operational Problem

UAS batteries are repeatedly charged, discharged, transported, stored, and used during flight operations.  Their condition and usage can change throughout their service life.

As the UAS Maintenance Officer, I need more than a list showing that a battery exists.  I need useful information that can help me monitor battery usage, identify when maintenance may be needed, document maintenance activity, and determine the current status of the equipment.

Without a structured process, some of this information may exist in different locations or systems.  Additional time is then required to locate, compare, and organize the information before I can use it.

Some battery information already exists in DroneSense or can be obtained through the aircraft controllers.  Manually entering information that already exists somewhere else creates additional work and another opportunity for errors or inconsistent records.

I wanted the UAS PMS to make better use of information that is already available while also maintaining the additional information I need for maintenance, equipment accountability, lifecycle management, and reporting.

## Battery Information Sources

Battery information can come from multiple sources depending on what information I need and how the information is being used.

### DroneSense

DroneSense is one of the operational tools I currently use as part of the UAS maintenance process.  I maintain selected battery and maintenance information in DroneSense and can generate CSV reports containing battery information.

I also use DroneSense to help schedule monthly inspections, document maintenance that has been completed, and document maintenance that is still needed.

This provides an operational source of maintenance and equipment information that is already being used within the UAS program.

The ability to generate CSV reports also provides a practical way to use selected DroneSense battery information within the Microsoft 365-based UAS PMS without manually recreating every battery record.

### Aircraft Controllers

Battery information can also be obtained through the aircraft controllers.

This provides another source of information when I am inspecting equipment, reviewing battery usage, troubleshooting a problem, or verifying battery-related information.

The controllers provide information associated with the actual aircraft and batteries without requiring the UAS PMS itself to communicate directly with the aircraft.

Having more than one information source is also useful when information needs to be reviewed or verified.

### UAS PMS

The UAS PMS provides the structured Microsoft 365 environment where selected battery information can be organized with the other records needed to manage the UAS program.

The UAS PMS is designed to operate independently of DroneSense.  DroneSense is an additional operational tool and data source, not a requirement for the UAS PMS to function.

This distinction was intentional.  I did not want the design of the UAS PMS to depend on access to a separate commercial UAS management platform.

The core UAS PMS uses Microsoft 365 tools such as Microsoft Forms, Microsoft Lists, Excel, Power Query, and appropriate Power Automate workflows.  Where DroneSense is available, selected information from DroneSense can supplement the Microsoft 365 system.

This allows the UAS PMS design to remain useful even in an environment where DroneSense is not available.

## Relationship Between DroneSense and the UAS PMS

DroneSense and the UAS PMS have some overlapping information, but they serve different purposes.

DroneSense provides operational UAS capabilities that I currently use, including maintenance scheduling, maintenance documentation, and battery information.  The UAS PMS is being developed as a broader Microsoft 365-based system for organizing information related to aircraft, batteries, maintenance, pilots, training, equipment, operational activity, and reporting.

I am not attempting to replace DroneSense with the UAS PMS.

Instead, I designed the UAS PMS so that information from DroneSense can be used when it provides value while keeping the core system independent of DroneSense.

This avoids creating an unnecessary dependency on an external system.  If DroneSense information is available, I can use selected data rather than manually recreating it.  If DroneSense is not available, the UAS PMS can still maintain the records required for its own workflows.

This approach also makes the design more adaptable because another organization or user would not need DroneSense in order to use the basic UAS PMS design.

## Battery Data Workflow

One of the battery workflows I developed uses a DroneSense CSV report as a source for Microsoft Lists.

At a high level, the process follows this model:

**DroneSense → CSV Export → Microsoft Lists → Excel / Power Query**

Each part of the process has a specific purpose.

**DroneSense** provides selected operational battery information.

**CSV Export** provides a portable file containing selected battery records.

**Microsoft Lists** provides structured storage within the Microsoft 365 environment.

**Excel and Power Query** retrieve selected information from Microsoft Lists for review, analysis, and reporting.

I can generate a battery CSV report from DroneSense and import the selected data into the appropriate Microsoft List.  Power Query can then pull the List information into Excel.

This allows me to use existing battery information rather than manually recreating every record in another system.

## Why I Designed the Workflow This Way

One of the main goals of the UAS PMS is to reduce unnecessary manual work.

If battery information already exists in DroneSense, manually typing the same information into another system takes additional time and creates another opportunity for errors.  Using the CSV export allows me to move selected information between systems in a more structured way.

Microsoft Lists gives me a place to organize that information with the other records being developed for the UAS PMS.

Excel and Power Query provide another layer by allowing selected List information to be retrieved and refreshed for analysis and reporting.

The result is a workflow that uses the strengths of several tools rather than expecting one application to perform every function.

At the same time, I intentionally maintained the ability for the UAS PMS to operate without DroneSense.  The DroneSense connection is intended to reduce duplicate work when that information is available, not make DroneSense a requirement for the system.

## Battery Record Design

I designed the battery data structure so that each battery can be maintained as its own record rather than being treated only as an accessory attached to an aircraft.

This allows information associated with an individual battery to remain available throughout its lifecycle.

The battery structure contains information needed to identify and manage the battery along with fields that support maintenance, usage, and lifecycle tracking.

An optional DroneSense Battery ID field is included so that a UAS PMS battery record can maintain the corresponding DroneSense identifier when that information is useful.  The field remains optional because the UAS PMS should still be able to maintain a battery record when a DroneSense identifier is unavailable or unnecessary.

This is another example of keeping DroneSense integration available without making the UAS PMS dependent on it.

## Discharge Cycles and Preventive Maintenance

One of the battery data points I track is the number of discharge cycles.  The discharge-cycle count provides useful information about battery usage and can also help identify when scheduled battery maintenance may be needed.

Instead of waiting for a battery problem to occur, cycle information gives me another maintenance indicator that I can use to determine when an action such as battery conditioning should be performed.

At a basic level, the process can be viewed as:

**Battery Use → Discharge Cycles → Maintenance Trigger → Battery Conditioning or Inspection → Maintenance Documentation**

This is one of the reasons I wanted battery information maintained as structured data rather than simply keeping an inventory of batteries.  The data can help support maintenance decisions instead of only identifying which batteries the program owns.

Where available, I can obtain battery usage information from DroneSense or review battery information through the aircraft controllers.  That information can then be used as part of the maintenance process.

Tracking discharge cycles gives me a repeatable way to review battery usage and identify when preventive maintenance may be appropriate.

The goal is to make battery maintenance easier to identify, schedule, perform, document, and review while reducing the amount of manual tracking required of me as the UAS Maintenance Officer.

## Maintenance and Inspection Management

Battery management is part of the larger UAS maintenance process.

I currently use DroneSense to help schedule monthly inspections and to document both completed maintenance and maintenance that is still needed.  This gives me an existing operational source of maintenance information that I can reference while performing my Maintenance Officer responsibilities.

The UAS PMS also contains its own maintenance structure so that maintenance management is not dependent on DroneSense.

The intent is not to unnecessarily duplicate every maintenance entry across multiple systems.  The objective is to maintain the information required by the UAS PMS while using information from existing operational systems when it can reduce manual work or assist with verification.

The combination of scheduled inspections, maintenance-needed records, completed-maintenance records, and battery usage information provides a more complete view of the equipment than an inventory list alone.

## Preventive Rather Than Only Reactive Maintenance

An important goal of tracking battery information is to help identify maintenance needs before they become equipment problems.

Discharge-cycle information, scheduled inspections, controller information, DroneSense records, and maintenance history can provide indicators that a battery needs attention.

This allows maintenance to be based on equipment information and usage rather than relying only on a reported failure.

The UAS PMS does not make the maintenance decision for me.  It organizes information that can help me recognize when maintenance may be needed and provides a structure for documenting what was done.

This keeps the Maintenance Officer involved in reviewing the actual equipment and making the maintenance decision while using the available data to make that process more efficient.

## Lifecycle Management

I included lifecycle information in the battery design because a battery record should not simply disappear when the battery is no longer being used.

A battery may eventually be removed from service, replaced, damaged, retired, or otherwise reach the end of its useful lifecycle.  Maintaining lifecycle disposition information allows the record to show what happened to the equipment rather than requiring the record to be deleted.

Preserving this history supports equipment accountability and provides a more complete record of the battery throughout its service life.

The battery record therefore represents more than the current condition of the equipment.  It can maintain useful information from active service through eventual disposition.

## Reducing the Maintenance Officer Workload

One of my primary reasons for developing the battery-management process is to reduce the amount of time required for me to perform the administrative side of my Maintenance Officer responsibilities.

The information I need may already exist in DroneSense, on an aircraft controller, in Microsoft Lists, or in other maintenance records.  The challenge is making that information useful without spending unnecessary time repeatedly entering, locating, comparing, and reorganizing it.

The CSV import and Power Query workflow helps reduce some of that manual work.

Instead of manually recreating selected DroneSense battery records, I can export the information to CSV and import it into Microsoft Lists.  Once the information is in Lists, Excel and Power Query can retrieve the data for additional review and reporting.

Tracking information such as discharge cycles also gives the data an operational purpose.  Instead of manually trying to remember which batteries may be approaching a maintenance point, structured information can help identify when I need to take a closer look at a battery.

The objective is to create a repeatable process in which information can move through the system with fewer unnecessary manual steps and provide useful maintenance information when I need it.

## Data Verification

Using information from another system does not eliminate the need to verify the data.

DroneSense reports, aircraft controller information, and UAS PMS records can provide different views of battery information.  When necessary, I can use these sources to review or verify information before making maintenance or equipment-management decisions.

Imported data should not automatically be assumed to be correct simply because it came from another system.  Part of the maintenance process is determining whether the information available from different sources is consistent with the actual equipment being managed.

The system is intended to support my maintenance decisions, not replace inspection, verification, or professional judgment.

## Design Considerations

When designing the battery-management process, I considered several factors:

- Maintain a separate record for each battery.
- Track battery usage information such as discharge cycles.
- Use battery usage as an indicator for preventive maintenance.
- Support battery conditioning and other scheduled maintenance activities.
- Use existing battery information when practical instead of entering the same information repeatedly.
- Use DroneSense CSV reports as a structured source of selected battery data.
- Maintain the ability to review battery information through aircraft controllers.
- Import selected battery information into Microsoft Lists.
- Use Excel and Power Query to retrieve List data for analysis and reporting.
- Support monthly inspection and maintenance responsibilities.
- Document maintenance needed and maintenance completed.
- Maintain lifecycle and disposition information.
- Preserve historical records when equipment leaves service.
- Avoid depending entirely on a single application or data source.
- Keep DroneSense integration optional rather than required.
- Reduce unnecessary duplicate data entry.
- Make battery information easier for me to locate and use.
- Support maintenance and equipment accountability.
- Maintain the ability to verify information from multiple sources.
- Keep the UAS PMS functional without DroneSense.

These decisions are based on how I actually need to manage and maintain the equipment rather than simply collecting information because the data is available.

## Development and Testing Approach

I developed the battery structure and supporting workflow as one component of the larger UAS PMS.

I tested the process of moving selected data into Microsoft Lists and confirmed that List information can be retrieved and refreshed in Excel using Power Query.

The battery structure itself was reviewed and refined during development so that the record contained information useful for maintenance, usage, and lifecycle management without becoming unnecessarily complicated.

Once the battery structure reached the point where the required design had been completed and reviewed, I treated the DEV structure as locked.  This helps prevent unnecessary changes to a component that has already gone through development and review while other portions of the UAS PMS continue to be developed.

Locking the battery structure does not mean that the entire UAS PMS is complete.  It means that this individual component reached its current completed development milestone.

## Current Status

The battery structure has been completed and locked in the development environment.

The DroneSense CSV, Microsoft Lists, Excel, and Power Query workflow has also been tested as part of the development process.

DroneSense continues to be used operationally for functions including monthly inspection scheduling, maintenance documentation, and battery information.  Aircraft controllers provide another source for reviewing battery information.

The UAS PMS remains capable of operating independently of DroneSense.

This milestone represents the completed battery data structure and the battery-related workflow that has been developed and tested to this point.  Historical data migration, production deployment, and final system-wide validation remain separate phases and are not represented as complete.

Legacy Lists and spreadsheets remain source records for future controlled migration.  Those original sources are not being modified as part of this portfolio documentation.

## What I Learned

Developing the battery-management portion of the UAS PMS reinforced that collecting data has limited value unless I understand why I am collecting it and how I intend to use it.

A discharge-cycle count is not useful simply because it is another number that can be stored.  It becomes useful when I can use that information as an indicator that a battery may have reached a point where conditioning, inspection, or another maintenance action should be considered.

I also learned that building a useful system does not always mean replacing systems that already exist.

DroneSense, aircraft controllers, Microsoft Lists, Excel, and Power Query each provide different capabilities.  The better solution is often to determine what each tool does well and develop a process that makes appropriate use of the information already available.

This portion of the project also reinforced the importance of distinguishing between integration and dependency.  Connecting the UAS PMS to information available from DroneSense can reduce duplicate work, but requiring DroneSense would unnecessarily limit the system.

By keeping the DroneSense connection optional, I can take advantage of existing operational information while maintaining a Microsoft 365-based UAS PMS that can function independently.

Most importantly, this part of the project reinforced the reason I started developing the UAS PMS in the first place: use information and technology to make routine processes easier, reduce unnecessary administrative work, and give me better organized information to perform my Maintenance Officer responsibilities.

## Data and Security Notice

This documentation describes the battery-management process at a portfolio level.  No production battery records, serial numbers, DroneSense identifiers, confidential employer information, restricted operational information, CSV files containing operational data, or other sensitive information is included in this repository.
