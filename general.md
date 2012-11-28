---
layout: page
title: General Guidelines
---
{% include JB/setup %}

{% include specsnav.html %}

Open511 follows some general guideline that are applied to all the resources available within the API. 

## RESTFul {#restful}

Althougth the REST style does not provide direct constains, the Open511 applies most of its best practices. It includes:
* Use of HTTP as a uniform way to interact with resources.
* Access to the resource via stable URLs.
* hypermedia structure: the resources are linked together to allow a client to jump from one resource to another.

### Representations {#representations}

In order to ease access, the open511 API will provide two types of representations: XML and JSON. Both representation will provide that same information except some minor differences (for example JSON will not support [multiple language](#language) in a single response)

In the current status of the specification, most of the examples provided are in XML, the detail of the JSON representations should come soon.

For the XML representation, a schema (XSD) will be provided once the design is stabilized. In the meantime, please refer to the data structure and examples.

Format (XML or JSON) negociation will be done by [HTTP header](header.html#parameters-Accept) with an override with a [URL parameter](parameters.html#parameters-format).

### Language {#language}

The API is designed to support multiple language. The XML representation will be able to contain multiple languages per request thanks to the <code>xml:lang</code> attribute. Since this feature adds some complexity in JSON, JSON will be able to contain a single language per request.

Language negociation will be done with the use of a [HTTP header](header.html#parameters-Accept-Language) with an override with a [URL parameter](parameters.html#parameters-lang).

If a requested language is not available, the API will fall back on the default language of the endpoint.

### Authentication {#authentication}

In order to request the data, it is advised not to request any authentication. In order to submit data, usual HTTP basic authentication will be the only method accepted.

### Encoding and other formatting elements {#encoding}

The data will be served with the UTF-8 encoding.

Date and time will follow the ISO 8601 subset as per the [w3c note](http://www.w3.org/TR/NOTE-datetime) except when specified otherwise.

Geospatial data will use the [GML notation](http://en.wikipedia.org/wiki/Geography_Markup_Language) for the XML notation and [GeoJSON](http://www.geojson.org/) for the JSON representation.

Links will use the [ATOM link structure](http://tools.ietf.org/html/rfc4287) using as much as possible the IANA [link relations list](http://www.iana.org/assignments/link-relations/link-relations.xml). 
