---
layout: page
title: Introduction to the Open511 API
redirect_from:
- /documentation.html
---
{% include JB/setup %}
{% include 1.0/specsnav.html %}


### Getting started {#started}

This document describes the specifications of the Open511 API, an open data standard for road event information. You can read more about the [context](context.html) of the API or jump directly to the [technical stuff](#techdocuments). If you are interested in contributing, you can start by joining the mailing list and consulting the "contribute" panel on the right.

We've provided some getting-started tips for [data consumers](consumer_guide.html) and [data providers](implementor_guide.html).


### How it works {#techdocuments}

* The [technical guidelines](guidelines.html) provide specifics about encoding, formats, architecture and content negotiation.

#### Main Resources:

* [Root (aka discovery)](root.html): this resource is the single entry point for the entire framework. It provides links to all the other resources.   
* [Jurisdictions](jurisdiction.html): represent a specific government with some metadata (contact info, geographical coverage and other options). 
* [Events](event.html): represent events (construction, accident, etc.) that are published by jurisdictions. 


#### Support resources:
* [Area](area.html): Open511 contains the concept of area that can be attached to events. An area can be any location with a name: city, county, district, etc. It allows jurisdiction to provide additional location data without providing other geospatial data.
* [Jurisdiction geography](jurisdictiongeo.html): Contain the geographical boundaries of a jurisdiction.


#### Draft resources

Drafts are resources that have been proposed or requested by adopters and that are still under development.

* [Reports](report.html): The report is the crowdsourcing feature of Open511. A road user can submit a report to notify the jurisdiction that something is ongoing (e.g an accident). Other clients can also retrieve reports submitted to a jurisdiction.
* [Traffic Cameras](camera.html): Provide information about the traffic cameras managed by a given jurisdiction.
* [Roads](road.html): List the road names under a given jurisdiction.
* [Traffic segments](traffic_segment.html): Provide geospatial information about road segments as well as real-time information (speed) if available.
* [Traffic historical conditions](historical_traffic_condition.html): Sub-resource of the traffic segments that provide access to historical data of the speed if available.


### Status {#status}

**The open511 specification has reached version 1.0**. We believe the specification is ready to implement.

Several jurisdictions have either implemented or are in the process of implementing Open511 Events services. Two examples are [the province of British Columbia](http://api.open511.gov.bc.ca/help) and the city of <a href="https://info-travaux.ville.repentigny.qc.ca/api/">Repentigny, Québec</a>. Please <a href="mailto:open511@opennorth.ca">get in touch with us</a> if you're considering implementing, or would just like more information on other existing and in-progress implementations. We also recommend joining the [mailing list](https://groups.google.com/forum/?fromgroups#!forum/open511).

It may be helpful to [browse](http://demo.open511.org/) the output of Open North's in-progress implementation of this API.


