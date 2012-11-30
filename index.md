---
layout: page
title: Introduction to the Open511 API (draft)
---
{% include JB/setup %}
{% include specsnav.html %}


## Getting started {#started}

The present document describes the specifications of the Open511 API. This API is currently under design and aims at providing open data for traffic information. The API is currently not implemented, at that stage we are more looking for comments. You can read more about the [context](context.html) of the API or directly jump to the technical stuff (see below). If you are interesting in participating, you can start by joining the mailing list and have a look to the "contribute" right-hand panel.


## How it works {#techdocuments}

* The [technical guidelines](guidelines.html) provide several important technical information about encoding, formats, architecture and content negociation.

Below is the list of resources supported:
* [Root (aka discovery)](root.html): This resource is the single entry point for the entire framework. It provides links to all the other resources, 
* [Jurisdictions](jurisdiction.html): represent a specific governement with some metadata (contact info, geographical coverage and other options)
* [Events](event.html): represent events that are published by the jurisdictions.

## Status {#status}

The open511 specification is the first draft designed. The format is expected to evolve in the coming months. As a consequence, the present specifications should not be used to develop tools.

## Roadmap and timeline {#timeline}

The first draft of the specification released to collaborators in october 2012 and made public in dec 2012. A second iteration is due for Jan 2013 and a third and last one for April 2013. At that point, the specification should be considered stable enough for general implementation.

The next iteration should provide some improvements concerning the architecture and the data format. I might also include two news services:
* Crowdsourcing: the ability for citizen to submit reports will be supported in the second iteration,
* Network data: The release of the first draft raised the need to link an event with some the road network. Added to that some transportation would like to publish their road network. As a consequence, a news resource might be added to support this feature although it is still under discussion. [(Issue 11)](https://github.com/opennorth/Open511API/issues/11)

In order to test the specification, a leading implementation should take place beginning of 2013 with one of the collaborators of the initiative.
