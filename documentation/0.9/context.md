---
layout: page
title: Context and future plans
---
{% include JB/setup %}
{% include 0.9/specsnav.html %}

### Overview {#overview}

The goal of the Open511 project is to develop an open API for publishing road events (accidents, construction, etc) and other mobility related data. The project is led by [Open North](http://opennorth.ca) and [Metropolitan Transportation Commission](http://www.mtc.ca.gov/) in collaboration with several organizations to design Open511 (see list [below](#collaborators)).

Open511 is currently under active development. The content shared here is a draft and is published as-is. Our wish is to continue to collaborate on the design of the API; anyone that would like to provide feedback is encouraged to do so. Please refer to the "contribute" section on the menu.

### Context {#context}

The open data movement has demonstrated its value to society on many occassions, particularly with recent efforts to improve information about transit systems. This experience showed that an open data standard which improves interoperability between regions is hugely beneficial to citizens as the [GTFS](https://developers.google.com/transit/gtfs/) and [SIRI](http://www.kizoom.com/standards/siri/overview.htm) formats allowed developers to create tools for use in multiple cities at once. There is a demand for similar tools for traffic but few organizations are opening this data to the public. One of the existing barriers is that there is no relevant format for sharing traffic data. Many ITS standards exist but they lack the simplicity, openness, and interoperability demanded by the open data movement. Following the example of [Open311](http://open311.org/), this initiative will propose a specification for road event data that matches open data criteria and will also advocate for public organizations to publish traffic data.

Intially, Open511 will focus on road events (accidents, constructions, etc.) but the API is designed to support other types of data or services. Road event data has been identified as a dataset that is owned by government and has a lot of added value for developers.

Open North will also develop open source software to publish road events so that public bodies (mainly small entities) will not need to develop brand new software to publish this information.

### Funding and Collaborators {#collaborators}

Financial support for the project is provided by [GeoConnections](http://geoconnections.nrcan.gc.ca/), a national collaborative initiative led by National Resources Canada. GeoConnections supports the integration and use of Canadian Geospatial Data Infrastructure (CGDI), an on-line resource that improves the sharing, access and use of open geospatial information.

The initial collaborators on this project were the [Ministry of Transportation and Infrastruture of British Columbia](http://www.gov.bc.ca/tran/), the [City of Ottawa](http://ottawa.ca/), the [City of Montréal](http://ville.montreal.qc.ca/), the [City of Repentigny](http://www.ville.repentigny.qc.ca/), the [Living Lab of Montréal](http://www.livinglabmontreal.org/), the [International Institute of Logistics of Montréal](http://www.iilm.ca/), [InstantGeo](http://www.instantgeo.com/), [David Eaves](http://eaves.ca/) and [Nicolas Saunier](http://n.saunier.free.fr/saunier/) from [École Polytechnique de Montréal](http://www.polymtl.ca/). 

### Governance {#governance}

The specification design is led by Open North and MTC with a consensus-based decision making process to include collaborators. With the public release of the specification, any organization that would like to collaborate is encouraged to do so. Do not hesitate to contribute to the [mailing list](https://groups.google.com/forum/?fromgroups#!forum/open511) and [submit comments and issues](https://github.com/opennorth/Open511API/issues).

Once the specification is stable, we plan to submit Open511 to a relevant standardization body in order to ensure stability and evolution capabilities.
