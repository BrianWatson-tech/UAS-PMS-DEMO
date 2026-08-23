# Data Structure

## Overview

I designed the UAS Program Management System around multiple Microsoft Lists rather than storing all program information in a single large dataset.

Each list represents a specific category of information. Related records can then be connected through lookup fields and other defined relationships.

This approach allows me to organize information consistently, reduce duplicate data entry, and build reporting and workflow processes around structured records.

## Core Data Areas

The system is being developed to manage several categories of UAS program information, including:

- Aircraft
- Batteries
- Equipment
- Pilot information and qualifications
- Training records
- Flight activity
- Aircraft checkout information
- Maintenance records
- Support equipment
- Vendor information
- Other supporting program records

The exact structure continues to evolve as I develop and test the system.

## Microsoft Lists

Microsoft Lists serves as the primary structured data layer.

Instead of placing unrelated information into one list, I use separate lists for different types of records. Each list contains fields appropriate to the information being managed.

This makes individual lists easier to maintain while still allowing information to be connected across the system.

## Relationships Between Records

Where information is related, I use lookup fields and other relationships to connect records between Microsoft Lists.

For example, a record associated with an aircraft can reference the appropriate aircraft record rather than requiring the same aircraft information to be entered repeatedly.

My goal is to create relationships that allow information to be entered once and reused wherever it is needed.

## Data Consistency

A major design goal is improving consistency across the program's information.

Where practical, I use defined fields, controlled selections, lookup values, and Microsoft Forms to reduce inconsistent or repetitive manual entry.

This provides a more structured foundation for reporting, analysis, and future workflow automation.

## Reporting and Data Retrieval

The structured Microsoft Lists environment also provides the source data for reporting.

I use Power Query to retrieve and refresh selected Microsoft Lists data in Excel. This allows reporting and analysis to use the structured records without manually recreating the same information in separate spreadsheets.

Additional reporting capabilities are still under development.

## Development Status

The data structure is still evolving as additional components of the UAS PMS are designed and tested.

Multiple Microsoft Lists, fields, and relationships have already been created. I will continue refining the structure as I test workflows, reporting requirements, and relationships between different types of program information.

## Data and Security Notice

This documentation describes the structure and design of the system without publishing production data.

Any examples or screenshots added to this repository will be sanitized, recreated, or fictionalized as necessary to prevent disclosure of confidential, personally identifiable, restricted, or operational information.
