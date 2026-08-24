# Vendor Management

## Overview

I created the Vendor Management portion of the UAS PMS to provide a structured location for information about vendors that support the UAS program.

The program may need vendors for aircraft repairs, replacement parts, batteries, accessories, support equipment, training, or other UAS-related services.  Instead of repeatedly entering the same vendor information in different records, I wanted a central location where vendor information could be maintained and referenced when needed.

The purpose is not to create a purchasing or procurement system.  The Vendor structure provides supporting information that can be used by the UAS PMS while existing Department purchasing and procurement processes remain separate.

## Operational Problem

Maintenance and equipment management sometimes require outside vendors.

When an aircraft or another piece of equipment needs repair, I may need to determine which vendor can provide the required service.  The same issue applies when replacement parts, batteries, accessories, or other equipment are needed.

If vendor information is maintained only in emails, previous quotes, individual documents, or personal notes, additional time may be required to locate the information again.

I wanted a structured way to maintain useful vendor information so that I do not have to repeatedly search for the same information when a maintenance or equipment need occurs.

## Vendor Record Design

I designed the Vendors structure so that each vendor can have its own record.

The vendor record provides a central location for information needed to identify and work with that vendor.

This creates a reusable record instead of entering the same vendor information repeatedly in unrelated areas of the UAS PMS.

At a high level, the concept is:

**Vendor → Parts / Services / Repairs / Support**

The vendor record does not represent a purchase or maintenance action by itself.  It represents the organization that may provide a product or service needed by the UAS program.

## Supporting Maintenance

Vendor information can be useful when maintenance requires outside support.

Some maintenance can be handled internally, while other work may require a repair facility, manufacturer support, replacement components, or another outside service.

Having vendor information organized gives me a faster way to identify a potential source when outside maintenance support is required.

This supports the maintenance process without making vendor information part of the maintenance record itself.

The maintenance record documents the maintenance activity.  The vendor record identifies the outside organization that may provide the required service or support.

## Supporting Parts and Equipment

Vendor information can also support equipment and replacement-part needs.

UAS equipment includes aircraft, batteries, propellers, accessories, support equipment, and other components that may eventually require replacement or repair.

Maintaining vendor information provides a structured reference when I need to determine where a particular item or service may be available.

This does not replace the Department's purchasing process.  It provides information that can help me identify what may be needed and where the appropriate product or service may be available before the established purchasing process is used.

## OEM and Manufacturer-Approved Parts

Safety is an important consideration when selecting parts used on aircraft.

UAS aircraft operate in the air, and a component failure can potentially result in equipment damage, property damage, or injury.  For that reason, the source and quality of replacement parts can be important when maintenance is performed.

Where appropriate, I consider OEM or manufacturer-approved parts when identifying repair and replacement options.

The Vendor structure can help maintain information about sources that provide the appropriate parts or services needed to support the equipment.

The UAS PMS does not make procurement decisions or replace required purchasing procedures.  It provides organized information that can support the maintenance and equipment-management process.

## Relationship to Department Procurement

The Department has established purchasing and procurement processes that remain responsible for official purchasing activity.

The UAS PMS is not intended to replace those processes.

My role may require me to identify an equipment problem, determine what repair or replacement may be needed, identify an appropriate vendor or manufacturer source, and provide technical information that supports the purchasing process.

At a high level:

**Maintenance or Equipment Need → Identify Requirement → Identify Potential Vendor → Department Procurement Process**

Keeping those responsibilities separate is important.

The UAS PMS helps organize the technical and operational information I need to manage the program.  Official purchasing actions continue through the Department's established process.

## Why I Designed It This Way

I did not want vendor information repeatedly entered into maintenance records, equipment records, spreadsheets, or other documents whenever the same vendor was used.

A vendor is its own type of information.

A maintenance record describes maintenance activity.

An equipment record describes the equipment.

A vendor record describes the organization providing a product or service.

These records can be related without treating them as the same thing.

Maintaining vendors separately provides a cleaner structure and allows the vendor information to be reused when needed.

## Reducing Administrative Work

One of the overall goals of the UAS PMS is to reduce the time I spend searching for and reorganizing information.

Vendor information is another example of information that may be needed repeatedly.

If I have already identified a vendor that provides a particular type of repair, part, or service, I should not have to start the search from the beginning every time the same need occurs.

Maintaining structured vendor records gives me a reference point for information I have already collected.

This can make the early stages of maintenance and equipment planning more efficient while still following the Department's required procurement process.

## Supporting Equipment Planning

Vendor information can also help when evaluating future equipment or replacement needs.

Maintenance history may identify equipment that requires repair or replacement.  Vendor information can then help identify possible sources for the required service or equipment.

This creates a connection between identifying an operational need and gathering the information required to address that need.

The UAS PMS does not authorize the purchase.  It helps me organize the information needed to support the process.

## Design Considerations

When creating the Vendor structure, I considered several factors:

- Maintain each vendor as its own record.
- Avoid repeatedly entering the same vendor information.
- Support aircraft and equipment repair needs.
- Support replacement-part and equipment needs.
- Maintain information useful for locating outside services.
- Support the use of appropriate OEM or manufacturer-approved parts when required.
- Keep vendor information separate from maintenance records.
- Keep vendor information separate from equipment records.
- Recognize the Department's existing procurement process.
- Avoid attempting to create a purchasing system inside the UAS PMS.
- Make previously identified vendor information easier to locate.
- Reduce the administrative time required to research recurring needs.
- Allow the structure to support additional vendors as program needs change.

These decisions were based on how vendor information supports my maintenance and equipment responsibilities rather than simply creating an address book.

## Development Approach

I created the Vendors structure as another component of the larger UAS PMS.

The structure was developed to provide a reusable location for vendor information that may support maintenance, repairs, parts, equipment, and other program needs.

I also considered the boundary between the UAS PMS and the Department's official procurement process.

The UAS PMS needs enough information to help me identify and research a vendor, but it does not need to duplicate the Department's purchasing system.

Maintaining that distinction keeps the UAS PMS focused on the operational and maintenance information it is intended to manage.

## Current Status

The Vendors structure has been created in the development environment.

Formal QA of this component has not yet been completed.

For that reason, I consider this a development milestone rather than a completed and locked component of the UAS PMS.

The structure may still be refined as QA is performed and as its relationships with other portions of the system are reviewed.

Historical vendor information, final migration, production deployment, and system-wide validation remain future phases and are not represented as complete.

## What I Learned

Creating the Vendor Management component reinforced the importance of defining where one system should stop and another established process should begin.

The UAS PMS can help me identify vendors, organize technical information, and support maintenance or equipment needs without becoming a procurement system.

It also reinforced the value of separating different types of information.

A vendor, an aircraft, a maintenance action, and a purchase are related in some situations, but they represent different things.  Maintaining them appropriately makes the information easier to understand and manage.

This component also supports the larger reason I am developing the UAS PMS: organize information I repeatedly need, reduce unnecessary administrative work, and make it easier for me to perform my responsibilities without attempting to replace existing Department systems that already have an established purpose.

## Data and Security Notice

This documentation describes the Vendor Management design at a portfolio level.  No production vendor records, quotes, pricing, account information, procurement records, confidential employer information, restricted operational information, or other sensitive information is included in this repository.
