---
layout: page
title: Introduction to the Open511 API (draft)
---
{% include JB/setup %}
{% include specsnav.html %}


## Getting started {#started}

This document describes the specifications of the Open511 API. It will provide an open data standard for road event information. The API is currently under development and we are looking for comments and feedback before it is implemented. You can read more about the [context](context.html) of the API or jump directly to the technical stuff (see below). If you are interested in contributing, you can start by joining the mailing list and consulting the "contribute" panel on the right.


## How it works {#techdocuments}

* The [technical guidelines](guidelines.html) provide specifics about encoding, formats, architecture and content negotiation.

**Main Resources:**

* [Root (aka discovery)](root.html): this resource is the single entry point for the entire framework. It provides links to all the other resources.   
* [Jurisdictions](jurisdiction.html): represent a specific government with some metadata (contact info, geographical coverage and other options). 
* [Events](event.html): represent events (construction, accident, etc.) that are published by jurisdictions. 
* [Reports](report.html): The report is the crowdsourcing feature of Open511. A road user can submit a report to notify the jurisdiction that something is ongoing (e.g an accident). Other clients can also retrieve reports submitted to a jurisdiction.

**Support resources:**
* [Area](area.html): Open511 contains the concept of area that can be attached to events. An area can be any location with a name: city, county, district, etc. It allows jurisdiction to provide additional location data without providing other geospatial data.
* [Jurisdiction geography](jurisdictiongeo.html): Contain the geographical boundaries of a jurisdiction.

## Status {#status}

This specification is a second draft. The format is expected to evolve in the coming weeks. Therefore, the present specifications should not be used to develop tools.

## Roadmap and Timeline {#timeline}

The first draft of the specification was released to collaborators in October 2012 and the second iteration  released in January 2013. The first official release (ready for implementation) is expected in May 2013.
