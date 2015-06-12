---
layout: page
title: Open511 API specification change log
---
{% include JB/setup %}
{% include 1.0/specsnav.html %}


### Change log

(Please refer to the commit [history](https://github.com/open511/Open511API/commits/gh-pages) for detailed change log)

<table id="changelog">
	<thead>
		<tr><th>Date</th><th>Description</th></tr>
	</thead>
	<tbody>
<tr><td>Dec 6th, 2012</td><td>Initial version</td></tr>
<tr><td>Jan 9th, 2013</td><td><ul><li>Add timezone at jurisdiction level</li><li>Use snake case (underscored) for compound word in field names</li><li>Change event filtering for the <code>status</code> field</li><li>Add <code>in_effect_on</code> filtering parameter for events</li><li>Add <code>bbox</code> filtering parameter for events.</li></ul></td></tr>
<tr><td>Feb 4th, 2013</td><td><ul><li>Add crowdsourcing feature (<code>report</code> resource)</li><li>Improve severity filtering to include greater than/lesser than filtering</li><li>Define <code>geography</code> filtering parameter, including the need to support POST requests.</li><li>Include <code>tolerance</code> filtering parameter when a point or linestring is used.</li><li>Remove license conditions and generic license in the jurisdiction resource.</li><li>Add link to "road" resource in the event resource.</li><li>Change <code>attachments</code> structure using atom links.</li><li>Add <code>restriction</code> structure. Units are fixed for each type of restriction.</li><li>Specify how <code>specific_date</code> should be formatted.</li></ul></td></tr>
<tr><td>Apr 29th, 2013</td><td><ul><li>Remove the ability to filter events by polygon and the ability to POST geography filters (<a href="event.html">events</a>).</li><li>Precise when to use x-www-form and multiple/form-data to post a report (<a href="report.html">events</a>).</li><li>Limit supported authentication options to "api key" and removed the need to support HTTP Basic (<a href="guidelines.html#auth">Guidelines</a>).</li><li>Specify the requirements for cross-domain requests: CORS and JSONP (<a href="guidelines.html#cross">Guidelines</a>).</li><li>Specify how implementors can add custom fields in the data structure (<a href="guidelines.html#custom">Guidelines</a>).</li><li>Add new ressource <code>region</code> and add the region data structure in the event structure (<a href="region.html">region</a> and <a href="event.html">event</a>).</li><li>Define a new resource, jurisdiction geography, to contain the boundaries of a jurisdiction <a href="jurisdictiongeo.html">jurisdiction geometry</a> and <a href="jurisdiction.html">jurisdiction</a></li><li>Add field <code>id</code> at the jurisdiction level and use this field to field events by jurisdiction. (<a href="jurisdiction.html">jurisdiction</a>)</li></ul></td></tr>
<tr><td>May 13th, 2013</td><td><ul><li>Rename region into area</li></ul></td></tr>
<tr><td>May 22nd, 2013</td><td><ul><li>Release the specification as version 0.9</li></ul></td></tr>
<tr><td>June 5th, 2013</td><td><ul><li>Allow multi <code>event_subtype</code> values in an event</li></ul></td></tr>
<tr><td>June 12th, 2013</td><td><ul><li>Remove <code>limit</code> parameter from pagination output</li><li>Rename <code>days_of_week</code> to <code>days</code>, and use a nested-element structure rather than a space-separated list, for consistency and easier serialization rules</li><li>Description field is optional on event</li><li>Clarify that <code>supported_versions</code> is a subelement of <code>service</code> on discovery resource</li></ul></td></tr>
<tr><td>July 18th, 2013</td><td><ul><li>Bring <code>link</code> tag into main namespace</li><li>Rename <code>area_name</code> and <code>area_id</code> tags to <code>name</code> and <code>id</code></li><li>Add <code>id</code> to event</li><li>Specify that the <code>in_effect_on</code> filter may be provided either timezone-aware or naive timestamps</li><li>Added guidelines on GML geographies</li></ul></td></tr>
<tr><td>July 31st, 2013</td><td><ul><li>Change <code>severity</code> to use string values.</li><li>Accept comma-separated lists for OR queries on several event filters.</li><li>Recommend HTTP Basic in auth guidelines</li><li>Document limit querystring parameter</li></ul></td></tr>
<tr><td>Sept 13th, 2013</td><td><ul><li>Change <code>schedule</code> structure, adding a <code>schedules</code> container</li><li>Move <code>timezone</code> from <code>schedule</code> to the top level of the event</li><li>Rename <code>road_name</code> to <code>name</code></li><li>Remove <code>lane_status</code> element</li><li>Add <code>state</code>, <code>lanes_open</code>, and <code>lanes_closed</code> elements to <code>road</code></li></ul></td></tr>
<tr><td>Oct 1st, 2013</td><td><ul><li>Change <code>service_type</code> in discovery resource to a link</li><li>Simplify content-type and version negotiation</li><li>Change XML and JSON container structures</li><li>Update <code>event_subtype</code> and <code>impacted_system</code> value lists</li></ul></td></tr>
<tr><td>Oct 25th, 2013</td><td><ul><li>Add error handling section to Guidelines document</li></ul></td></tr>
<tr><td>Nov 6th, 2013</td><td><ul><li>Allow areas that don't map to GeoNames</li></ul></td></tr>
<tr><td>May 7, 2014</td><td><ul><li>Clarify that the <code>in_effect_on</code> filter on events should never return archived events</li></ul></td></tr>
<tr><td>May 14, 2014</td><td><ul><li>Document static/simple version of events resource</li></ul></td></tr>
<tr><td>February 4, 2015</td><td><ul><li>Include previously-published schedule proposal in Event documentation</li><li>Release version 1.0</li></ul></td></tr>
</tbody>
</table>
