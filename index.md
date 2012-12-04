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

**Supported Resources:**
* [Root (aka discovery)](root.html): this resource is the single entry point for the entire framework. It provides links to all the other resources. 
Below is an example of the discovery resource. This example demonstrates an aggregator (open511.info) which gathers information from two different jurisdictions (My City and My Region). The jurisdiction link points to the original jurisdiction resource while the events are aggregated and served locally.  
* [Jurisdictions](jurisdiction.html): represent a specific government with some metadata (contact info, geographical coverage and other options). 
Below is a example of the jurisdiction resource. The resource presents the data of the "My City" jurisdiction including the geographical coverage of the jurisdiction, the license applied to the content, and the languages supported.
* [Events](event.html): represent events that are published by jurisdictions. 
Below is an example of the events resource. The example demonstrates how an event from juridiction "My City" is served by an aggregator (open511.info). The jurisdiction link still points to the original jurisdiction, but the self resource of the event is local (as well as the collection of events).

## Status {#status}

This specification is a first draft. The format is expected to evolve in the coming months. Therefore, the present specifications should not be used to develop tools.

## Roadmap and Timeline {#timeline}

The first draft of the specification was released to collaborators in October 2012 and will be made public in December 2012. A second iteration will be released in January 2013 with the final version expected in April 2013. At that point, the specification should be stable enough for general implementation.

The second iteration will provide improvements to architecture and data formatting. It may also include two new services:
* Crowdsourcing: the ability for citizens to submit reports like in the open311 framework.
* Network data: with the first release, we noticed a need for linking an event with the road network. Also, some transportation agencies would like to publish their road network so a new resource might be added to support this feature but it is still under discussion. [(Issue 11)](https://github.com/opennorth/Open511API/issues/11)
