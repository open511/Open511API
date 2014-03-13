---
layout: page
title: Introduction to the Open511 API
---
{% include JB/setup %}
{% include specsnav.html %}


### Getting started {#started}

This document describes the specifications of the Open511 API, an open data standard for road event information. The specification is almost completed and should be [released soon](#timeline). You can read more about the [context](context.html) of the API or jump directly to the [technical stuff](#techdocuments). If you are interested in contributing, you can start by joining the mailing list and consulting the "contribute" panel on the right.


### How it works {#techdocuments}

* The [technical guidelines](guidelines.html) provide specifics about encoding, formats, architecture and content negotiation.

####Main Resources:

* [Root (aka discovery)](root.html): this resource is the single entry point for the entire framework. It provides links to all the other resources.   
* [Jurisdictions](jurisdiction.html): represent a specific government with some metadata (contact info, geographical coverage and other options). 
* [Events](event.html): represent events (construction, accident, etc.) that are published by jurisdictions. 


####Support resources:
* [Area](area.html): Open511 contains the concept of area that can be attached to events. An area can be any location with a name: city, county, district, etc. It allows jurisdiction to provide additional location data without providing other geospatial data.
* [Jurisdiction geography](jurisdictiongeo.html): Contain the geographical boundaries of a jurisdiction.


####Draft resources

Drafts are resources that have been proposed or requested by adopters and that are still under development.

* [Reports](report.html): The report is the crowdsourcing feature of Open511. A road user can submit a report to notify the jurisdiction that something is ongoing (e.g an accident). Other clients can also retrieve reports submitted to a jurisdiction.
* [Traffic Cameras](camera.html): Provide information about the traffic cameras managed by a given jurisdiction.
* [Roads](road.html): List the road names under a given jurisdiction.
* [Traffic segments](traffic_segment.html): Provide geospatial information about road segments as well as real-time information (speed) if available.
* [Traffic historical conditions](historical_traffic_condition.html): Sub-resource of the traffic segments that provide access to historical data of the speed if available.


### Status {#status}

**The open511 specification has reached version 0.9**. This first official version is also the first "implementation ready" specification. 

Why not version 1.0? We expect that while developing the first implementations we'll some discrepancies and possible improvements. As a consequence, version 1.0 will be the result of the first implementations.

Who will be the first implementers? [MTC](http://511.org/), the [Ministry of Transportation of British Columbia](http://www.gov.bc.ca/tran/) and [OpenNorth](https://github.com/opennorth/open511) will work in parallel to build the two first implementations. Any other organization can start implementing this specification but it should be done in collaboration with MTC and OpenNorth since some minor changes could still occur. If your organization wants to build software based on open511, please join the [mailing list](https://groups.google.com/forum/?fromgroups#!forum/open511).

It may be helpful to [browse](http://demo.open511.org/) the output of Open North's in-progress implementation of this API.

### Roadmap and Timeline {#timeline}

The first draft of the specification was released to collaborators in October 2012 and the second iteration released publicly in January 2013. The current version (0.9) is the result of the third iteration and is used to develop the first implementations. The version will switch to version 1.0 when the first implementations are live (target date: spring 2014).

