# Forms and Data Entry

## Overview

I am using Microsoft Forms as part of the UAS Program Management System to provide a simple and consistent method for entering selected types of program information.  I designed this approach with two primary goals: make routine data entry easier for the pilots and reduce the amount of time required for me to perform my responsibilities as the UAS Maintenance Officer.  

The pilots should not have to understand the underlying Microsoft Lists, data structure, or reporting process simply to document routine UAS activity.  Their part of the process should be as straightforward as practical.  

At the same time, I need accurate and organized information to manage aircraft maintenance, review equipment activity, maintain program records, and support required reporting.  When information is collected consistently as part of the normal workflow, I spend less time later locating records, comparing different sources, correcting inconsistencies, and manually reorganizing information.  

The purpose of the Forms-based workflow is therefore not simply to replace one method of data entry with another.  It is to improve the process on both sides: make information easier for pilots to enter and make that information easier for me to use.  

## Operational Problem

Managing the maintenance side of a UAS program requires information from multiple areas of operation.  Aircraft usage, pilot activity, aircraft checkouts, maintenance activity, batteries, training, and other records can affect decisions I need to make as the Maintenance Officer.  

When information is stored in different locations or recorded inconsistently, additional time is required to locate and organize it before it can be useful.  That administrative work takes time away from the actual maintenance, equipment management, training support, and other responsibilities associated with the UAS program.  

I began developing the UAS PMS to reduce that workload.  My goal is to collect information in a structured and consistent manner as part of the normal operational workflow so that the information is easier to find and use when it is needed.  

## Data Entry Approach

Not every user needs direct access to the underlying Microsoft Lists.  For selected workflows, Microsoft Forms provides a straightforward user-facing method for submitting information.  

I designed the forms around the information required for each workflow.  Pilots can enter the information needed for a particular activity without having to navigate the underlying Lists or understand how the data is structured behind the form.  

This approach keeps the pilot-facing process simple while creating more consistent records behind the scenes.  Those records can then support maintenance responsibilities, equipment accountability, program administration, and reporting without requiring the same information to be collected again.  

The intent is to capture useful information once, as close as practical to when the activity occurs, and then make that information available for the other parts of the system that need it.  

## Current Workflows

Forms-based data entry has been implemented and tested for selected workflows, including:

- Pilot flight activity
- Aircraft checkout information

These workflows are currently being used to collect information through Microsoft Forms.  The submitted information is incorporated into the Microsoft 365 environment where it can be stored, reviewed, and used by other components of the UAS PMS.  

Having pilots enter information through a consistent process improves the quality and accessibility of the records available to me.  Instead of having to reconstruct activity later from multiple sources, information can be captured during the normal pilot workflow.  

This benefits both sides of the process.  Pilots have a simpler method for entering required information, while I have better organized information available for performing my Maintenance Officer responsibilities.  

## Forms, Lists, and Excel

One of the workflows I have been developing connects data collection, structured storage, and reporting.  At a high level, the process follows this model:

**Microsoft Forms → Microsoft Lists → Excel / Power Query**

Each component has a different purpose.  

**Microsoft Forms** provides the user-facing data-entry interface.  

**Microsoft Lists** provides structured storage for the information.  

**Excel and Power Query** can retrieve selected information from Microsoft Lists for analysis and reporting.  

I have tested this process and confirmed that selected List data can be refreshed in Excel using Power Query.  

This is important to the overall design because information entered during normal operations can support multiple purposes without requiring the same information to be manually entered again.  The goal is to capture useful information once, maintain it in a structured format, and then use that information where appropriate for maintenance, administration, analysis, and reporting.  

## Reducing the Maintenance Officer Workload

One of my primary reasons for developing the UAS PMS is to reduce the amount of time required to perform the administrative side of my Maintenance Officer responsibilities.  

Managing UAS maintenance involves more than physically inspecting or repairing an aircraft.  I also need information about aircraft activity, equipment status, maintenance history, pilot activity, and other program records.  

Without a structured system, time can be spent locating information, checking multiple sources, comparing records, and reorganizing information before I can use it.  

The Forms-based workflow helps address that problem by moving structured data collection closer to the point where the activity actually occurs.  Pilots enter information as part of their normal workflow, and that information becomes part of the supporting data structure.  

The objective is not to eliminate my responsibility for reviewing and verifying information.  The objective is to reduce unnecessary administrative work so that more of my time can be spent actually managing maintenance, equipment, training support, and other UAS program responsibilities.  

## Designing for the Pilots

Reducing my workload cannot come at the expense of creating additional unnecessary work for the pilots.  

For that reason, I try to keep the pilot-facing portion of the system as simple as practical.  Pilots should be able to enter the required information without having to understand the structure of the underlying Lists or perform unnecessary administrative steps.  

When designing the Forms, I consider what information is actually required, how the questions should be presented, and how many steps the pilot must complete.  

A technically sophisticated system provides little operational value if users find it unnecessarily difficult or time-consuming to use.  The goal is therefore to make the pilot experience simple while maintaining useful structure behind the scenes.  

## Design Considerations

When developing Forms and data-entry processes, I consider several factors:

- Keep the user-facing process simple.
- Collect only information needed for the workflow.
- Use consistent fields and values where practical.
- Reduce duplicate entry of the same information.
- Capture information as part of the normal operational workflow.
- Maintain structured records for future use and reporting.
- Make information easier to locate and review.
- Reduce unnecessary administrative work for pilots.
- Reduce the time required for me to perform Maintenance Officer responsibilities.
- Support maintenance and equipment decisions with better organized information.
- Design workflows that can be expanded or automated later.

These decisions are based on how the system will actually be used.  I try to consider both the person entering the information and the person who will eventually need to use that information.  

## Development and Testing Approach

I have been developing the UAS PMS in stages rather than attempting to build the entire system at one time.  

Individual areas are designed, built, reviewed, and tested before I consider them ready to move forward.  This allows me to identify problems with fields, workflows, or data structure before additional parts of the system depend on them.  

As I work with the system, I also evaluate whether the design actually improves the operational process.  A feature that technically works is not necessarily useful if it creates unnecessary work or does not provide information that is needed later.  

This development process allows me to make changes while the system is still being developed rather than waiting until the entire system is completed.  

## Development Status

The Forms and data-entry portion of the UAS PMS is still evolving.  Selected workflows have been implemented and tested, while additional Forms, integration, automation, and validation processes will be developed as the overall system progresses.  

The current process has already demonstrated that Microsoft Forms, Microsoft Lists, Excel, and Power Query can work together to collect operational information and make selected records available for review and reporting.  

Future work will include evaluating where Power Automate can appropriately reduce additional manual steps between data collection, storage, notification, and reporting.  

The overall UAS PMS remains a work in progress.  I am documenting completed development milestones as they occur rather than presenting the system as a finished product.  

## What I Learned

Developing this portion of the UAS PMS reinforced that the user-facing form is only one part of the solution.  The questions being asked, the way information is structured behind the form, and how that information will eventually be used all have to be considered together.  

I also learned that making a process easier for the user can simultaneously make the administrative side more efficient.  When information is collected consistently at the beginning of a workflow, less effort is required to locate, interpret, and reorganize it later.  

This has influenced how I approach other parts of the UAS PMS.  Instead of starting with a particular Microsoft tool and looking for a reason to use it, I try to start with the operational problem and determine how the available tools can help solve it.  

For me, the value of the system is not simply that it uses Microsoft Forms, Lists, Excel, Power Query, or Power Automate.  The value is whether those tools can make the pilots' responsibilities easier, reduce the amount of time required for me to manage the program, and provide better organized information when it is needed.  

## Data and Security Notice

This documentation describes the design and functionality of the data-entry process at a portfolio level.  No production records, personally identifiable information, confidential employer information, restricted operational information, or other sensitive data is included in this repository.  
