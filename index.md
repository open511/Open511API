---
layout: page
title: Introduction to the Open511 API (draft)
---
{% include JB/setup %}
{% include specsnav.html %}

Open511 is a initiative to develop an API designed to publish road events (accidents, construction, etc) and potentially many other road and mobility related data and following the principles of open data. The project is lead by [Open North](http://opennorth.ca) and funded by [GeoConnections](http://geoconnections.nrcan.gc.ca/), an program of Naturel Resources Canada. Open North already works with several organizations to design the API (see list [below](#collaborators)).

Open511 is currently under active development. The content shared here is the result of the first draft and is published as-is. Our wish is to follow a collaborative path to design this API; consequently any organization that would like to provide some feedback is welcome. Please refer to the "contribute" section in the right menu.


### Collaborators {#collaborators}

The initial collaborators on the projet are the [Ministry of Transportation and Infrastruture of British Columbia](http://www.gov.bc.ca/tran/), the [City of Ottawa](http://ottawa.ca/), the [City of Montréal](http://ville.montreal.qc.ca/), the [City of Repentigny](http://www.ville.repentigny.qc.ca/), the [Living Lab of Montréal](http://www.livinglabmontreal.org/), the [International Institute of Logistics of Montréal](http://www.iilm.ca/), [InstantGeo](http://www.instantgeo.com/), [David Eaves](http://eaves.ca/) and [Nicolas Saunier](http://n.saunier.free.fr/saunier/) from [École Polytechnique de Montréal](http://www.polymtl.ca/). 

We are also working closely with the [Metropolitan Transportation Commission](http://www.mtc.ca.gov/) of San Francisco Bay Area which is coordinating the [511.org](http://511.org/) initiative and we are in communication with other actors in the 511 and transportation world.

## Overview {#overview}

Open data is currently a leading movement that demonstrated its strengths in many occassion, for example to improve information about transit systems. The experience with transit data proved that having an open data standard to improve interoperability is a major step and the GTFS and SIRI formats provided what was needed. Many people would like similar data for traffic but few organization are opening their traffic data and no relevant format exists. Many ITS standards exist by they lack the simplicity, openess and the interoperability needed for open data. Using the same philosophy as Open311, the current initiative will propose a specification for traffic data that matches open data criteria and will also include advocacy toward public organization to publish traffic data.

For the moment, the initiative will focus on the road events (accidents, constructions, etc.) but the API is designed to support other types of data/services. This set of data have been identified as the one that is owned by government and with a lot of added values.

Added to that, Open North will also develop an open source software to publish road events so that public bodies (mainly small cities) will not need to develop brand new software to publish this information.


## Technical overview {#techoverview}

Open511 will follow best practices in terms of open data API, following the guidelines of the REST style. As a consequence, the API will rely on the HTTP protocol and its regular features and most of the resources will be accessible via clearly identified URLs.

The API and data format is designed to allow agregation. In other words, one server/endpoint can provide data for several cities/states (called jurisdictions). Added to that, a third party could retrieve data from several endpoint and provide a unified feed for potential user. For example a regional agency could agregate and republish data from all the jurisdiction within it geographical coverage.

The format contain geospatial metadata that allows client software to evalute the coverage of an endpoint. 

### Technical documents {#techdocuments}

Before looking at the format structure, please have a look to the common rules that apply to all resources:
* [The general guidelines](general.html) provides information about encoding, formats, external standards used, languages, etc.
* [HTTP headers and features](headers.html) describes all the HTTP features an Open511 endpoint should respect
* [Common URL parameters](parameters.html) lists all the URL parameters a client can apply to any resource within the open511 framework.

Here are the resource supported by Open511
* [Root (aka discovery)](root.html): This resource is the single entry point for the entire framework. It provides links to all the other resources, 
* [Jurisdictions](jurisdiction.html): represent a specific governement with some metadata (contact info, geographical coverage and other options)
* [Events](event.html): represent events that are published by the jurisdictions.

Following the REST style guideline, there is no predefined URL schema. Each implementation can have its own schema, the client should follow the links from the root resource to access relevant data.

## Status {#status}

The open511 specification is the first draft designed. The format is expected to evolve in the coming. As a consequence, the present specifications should not be used to develop tools.

## Timeline {#timeline}

The first draft of the specification released to collaborators in october 2012 and made public in nov 2012. A second iteration is due for Jan 2013 and a third and last one for April 2013. At that point, the specification should be considered stable enough for general implementation.

In order to test the specification, a leading implementation might take place beginning of 2013 with one of the collaborators of the initiative.

## Governance {#governance}

For the moment, the specification design is lead by Open North on a consensus based process with collaborators. With the public release of the specification, any organization that would like to collaborate can do so. Do not hesitate to [contact](mailto:open511@opennorth.ca) Open North and to contribute to the [mailing list](https://groups.google.com/forum/?fromgroups#!forum/open511) and [submit comments and issues](https://github.com/opennorth/Open511API/issues).

Once the specification is stable, Open North plans to submit it to a standardization body in order to ensure stability and evolution capabilities.
