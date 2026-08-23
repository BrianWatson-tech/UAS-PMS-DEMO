# System Architecture

## Architecture Overview

The UAS Program Management System (UAS PMS) is being developed as a connected Microsoft 365-based information management system.

The architecture is designed to separate data collection, structured data storage, reporting, and workflow automation while allowing information to move between these components.

The current architecture uses Microsoft Lists as the primary structured data layer, Microsoft Forms for selected data-entry processes, Microsoft Excel and Power Query for data retrieval and analysis, and Power Automate for workflow automation.

## Core Components

### Microsoft Lists

Microsoft Lists serves as the primary structured data layer of the system.

Separate lists are used to manage different categories of UAS program information. Fields and relationships are designed so related records can be connected while reducing unnecessary duplication of data.

### Microsoft Forms

Microsoft Forms is used for selected data-entry workflows where a simplified interface is appropriate.

Forms provide users with a controlled method of submitting information without requiring direct interaction with the underlying Microsoft Lists.

### Microsoft Excel and Power Query

Microsoft Excel is used for portions of the reporting and analysis environment.

Power Query allows data stored in Microsoft Lists to be retrieved and refreshed in Excel. This reduces the need to manually copy information between systems and provides a foundation for repeatable reporting processes.

### Power Automate

Power Automate is being incorporated to automate selected workflows between system components.

Automation capabilities are still under development and will be expanded as the underlying data structure and business processes are finalized.

## Current Data Flow

At a high level, the developing system follows this model:

**Data Entry → Structured Storage → Data Retrieval → Reporting and Analysis**

Depending on the workflow, information may be entered through Microsoft Forms or directly into an appropriate Microsoft List.

Microsoft Lists provides the structured storage layer.

Power Query can then retrieve information from Lists into Excel for analysis and reporting.

Power Automate can support workflows and movement of information between components where automation is appropriate.

## Design Considerations

The architecture is being developed around several principles:

- Reduce repetitive data entry.
- Maintain structured and consistent records.
- Connect related information through defined relationships.
- Separate data storage from reporting where practical.
- Create repeatable reporting processes.
- Automate appropriate administrative workflows.
- Allow the system to expand as program requirements change.
- Use tools available within the Microsoft 365 environment.

## Development Status

The architecture continues to evolve as individual components are built and tested.

Several Microsoft Lists and their associated fields and relationships have been implemented. Portions of the Forms, Lists, Excel, and Power Query workflow have also been tested.

Additional workflow automation, reporting capabilities, data relationships, and legacy-data migration processes remain under development.

This document will be updated as the architecture changes and additional components are implemented.

## Data and Security Notice

This repository is intended as professional portfolio and technical documentation.

It does not contain confidential employer information, personally identifiable information, restricted operational information, or production data.

Any examples, screenshots, diagrams, or sample records published in this repository will be sanitized, recreated, or fictionalized as necessary to protect operational information.
