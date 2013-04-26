---
layout: page
title: Open511 API specification change log
---
{% include JB/setup %}
{% include specsnav.html %}


## Change log

(Please refer to the commit [history](https://github.com/opennorth/Open511API/commits/gh-pages) for detailed change log)

Date | Description                                               |
-----|-----------------------------------------------------------|
Dec 6th, 2012 | Initial version |
Jan 9th, 2013 | <ul><li>Add timezone at jurisdiction level</li><li>Use snake case (underscored) for compound word in field names</li><li>Change event filtering for the <code>status</code> field</li><li>Add <code>in_effect_on</code> filtering parameter for events</li><li>Add <code>bbox</code> filtering parameter for events.</li></ul> |
Feb 4th, 2013 | <ul><li>Add crowdsourcing feature (<code>report</code> resource)</li><li>Improve severity filtering to include greater than/lesser than filtering</li><li>Define <code>geography</code> filtering parameter, including the need to support POST requests.</li><li>Include <code>tolerance</code> filtering parameter when a point or linestring is used.</li><li>Remove license conditions and generic license in the jurisdiction resource.</li><li>Add link to "road" resource in the event resource.</li><li>Change <code>attachments</code> structure using atom links.</li><li>Add <code>restriction</code> structure. Units are fixed for each type of restriction.</li><li>Specify how <code>specific_date</code> should be formatted.</li></ul> |
Apr 29th, 2013 | <ul><li>Remove the ability to filter events by polygon and the ability to POST geography filters (<a href="event.html">events</a>).</li><li>Precise when to use x-www-form and multiple/form-data to post a report (<a href="report.html">events</a>).</li><li>Limit supported authentication options to "api key" and removed the need to support HTTP Basic (<a href="guidelines.html#auth">Guidelines</a>).</li><li>Specify the requirements for cross-domain requests: CORS and JSONP (<a href="guidelines.html#cross">Guidelines</a>).</li><li>Specify how implementors can add custom fields in the data structure (<a href="guidelines.html#custom">Guidelines</a>).</li><li>Add new ressource <code>region</code> and add the region data structure in the event structure (<a href="region.html">region</a> and <a href="event.html">event</a>).</li><li>Define a new resource, jurisdiction geography, to contain the boundaries of a jurisdiction <a href="jurisdictiongeo.html">jurisdiction geometry</a> and <a href="jurisdiction.html">jurisdiction</a></li></ul> |
{#changelog}


