<?xml version="1.0" encoding="utf-8"?>
<schema    
  xmlns="http://purl.oclc.org/dsdl/schematron"  
  xmlns:gml="http://www.opengis.net/gml">                  
  <title>Open511 Schematron</title>
	<ns prefix='gml' uri='http://www.opengis.net/gml'/> 

	<pattern>
		<rule context="open511">
			<assert test="link[@rel='self']">Every document must have a self link</assert>
			<assert test="(services) or (link[@rel='up'])">Every non-root document must have an up link</assert>
		</rule>
		<rule context="open511/link">
			<assert test="@rel = 'self' or @rel = 'up'">Only the 'self' and 'up' links can appear inside open511</assert>
		</rule>
		<rule context="area|jurisdiction|event">
			<assert test="link[@rel='self']">A self link is required</assert>
		</rule>
		<rule context="open511/jurisdiction">
			<assert test="link[@rel='geography']">Jurisdictions require a geography link</assert>
			<assert test="link[@rel='license']">Jurisdictions require a license link</assert>
			<assert test="count(link) = 3 or count(link) = 4">A jurisdiction must have three or four links</assert>
		</rule>
		<rule context="open511/jurisdiction/link">
			<assert test="@rel = 'self' or @rel = 'geography' or @rel = 'license' or @rel = 'description'">Valid link types with jurisdiction are self, geography, license, and description</assert>
		</rule>
		<rule context="event">
			<assert test="link[@rel='jurisdiction']">Events require a jurisdiction link</assert>
			<assert test="count(link) = 2">Events must have a self and jurisdiction link, and no others</assert>
		</rule>
		<rule context="event/roads/road">
			<assert test="not(lane_status) or (direction and not(direction/text() = 'BOTH'))">If lane_status is set, direction must be too, and direction cannot be BOTH.</assert>
		</rule>
		<rule context="pagination">
			<assert test="link[@rel = 'next'] or link[@rel = 'previous'] or not(link)">Pagination links must be next or previous</assert>
			<assert test="count(link[@rel = 'next']) &lt; 2 and count(link[@rel = 'previous']) &lt; 2">No more than one next or previous link</assert>
		</rule>
	</pattern>


</schema>