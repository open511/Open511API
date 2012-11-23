---
layout: page
title: Introduction to the Open511 API (draft)
---
{% include JB/setup %}
{% include specsnav.html %}

Open511 is a initiative to develop an API designed to publish road events (accidents, construction, etc) and potentially many other road and mobility related data and following the principles of open data. The project is lead by [Open North](http://opennorth.ca) and funded by [GeoConnections](http://geoconnections.nrcan.gc.ca/), an program of Naturel Resources Canada. Open North already works with several organizations to design the API (see list [below](#collaborators)).

Open511 is currently under active development. The content shared here is the result of the first draft and is published as-is. Our wish is to follow a collaborative path to design this API; consequently any organization that would like to provide some feedback is welcome. Please refer to the "contribute" section in the right menu.


### Collaborators {#collaborators}


## Overview

Open511 follows the path of the open311 initiative as well as the general move toward making data open and easily accessible.

For the moment, the initiative will focus on the road events (accidents, constructions, etc.) but the API is designed to support other types of data. This set of data have been identified as the one that is owned by government and with a lot of added values.


## Technical overview

Many standards already exist to share road related data. These standards are usually designed for the communication of control centers or specialized devices; as a consequence the format tend to be complex and difficult to use. In order to make the data as easily accessible as possible, the Open511 API will stick to the following technical elements:

- Standard web technologies. The current design works using the HTTP protocol (the foundation of the web). All modern development languages have powerful HTTP libraries.
- URL based. All data is accessible through simple URLs (like any web page). Each individual URL corresponds to a specific resource.
- Discoverable. The content of the API is easy for clients to discover, largely via hypertext links between items.
- Stateless. Each request is independant from the previous/following request, which makes implementation easier both on the client and server side.
- On request. The client has to send a request to get the data.


## Overview

The Open511 API will allow governements (cities as well as states) publishing road events (accidents, constructions, etc) and potentially other types off data. As a consequence, developers and third parties will have the opportunity to access this data from several jurisdictions to offer services to citizen or governments.

Currently, the API contain two central resources: 
* Jurisdiction: represent a specific governement with some metadata (contact info, geographical coverage and other options)
* Events: represent events that are published by the jurisdictions.

Any jurisdiction can publish events and many jurisdictions can publish events from one endpoint (a endpoint is the server providing the data). Morevoer, the open511 API is designed to allow agregation from multiple source to simplify the access to the data.

Since Open511 follows the REST architecture, the data can be obtained thanks to a GET request on a target URL.

## Status 

The open511 specification is the first draft designed. The format is expected to evolve in the coming. As a consequence, the present specifications should not be used to develop tools.

## Guidelines

Before reading the message structure, have a look to the following elements.

* Using some REST best practices, the open511 API will provide for each endpoint a discovery point. The discovery will contain links pointing other resources (like jurisdictions and events). As a consequence, a server implementation or a client should not consider the URLs a fixed. URLs are dynamic and should be retrieved by following the internal links of the API.

* Open511 makes use of some HTTP headers for various needs. Please, refer to the HTTP headers section.

### Representations: XML and JSON

The API will support representation of the data both in XML and JSON. While the API design is in draft, only the XML representation will be documented. The JSON representation will come later.

An schema (XSD) will be provided for the XML representation once the design is stabilized. In the meantime, please refer to the data structure and examples.

Format negociation will be done by HTTP header with an override in URL parameters.

### Language support

The API is designed to support multiple language. The XML representation will be able to contain multiple languages per request thanks to the xml:lang attribute. Since this feature adds some complexity in JSON, JSON will be able to contain a single language per request.

Language negociation will be by HTTP header with an override in URL parameters.

If a requested language is not available, the API will fall back on the default language of the endpoint.

### Authentication

In order to request the data, it is advised not to request any authentication. In order to submit data, usual HTTP basic authentication will be the only method accepted.

### Encoding and other formatting elements

The data will be served with the UTF-8 encoding.

Date and time will follow the ISO 8601 subset except when specified otherwise.

### Agregation

!!!!

## Resources 

* Jurisdictions
* Events

HTTP Headers

## Specification license and governance

Once stabilized, the licence will be released in creative common and will be manager by a committee based organization (either ad-hoc or an existing structure)
