---
layout: page
title: Introduction to the Open511 API (draft)
---
{% include JB/setup %}


Open511 is the specification of an API designed publish open data format for road events (accidents, construction, etc) and potentially many other road and mobility related data. The project is developed by [Open North](http://opennorth.ca) and funded by [GeoConnections](http://geoconnections.nrcan.gc.ca/), an program of the Government of Canada.

Open511 is currently under development. The specifications presented are only a first draft version designed by Open North with the initial collaborators of the project. The remaining of the process will be open to any organization or person willing to participate. The format will go through one or two other iterations in order to get a final version for the summer 2013. If you want to join the effort, please join the mailing list. In order to manage comments, request for change and other remarks related to the open511 API, you can submit an issue.

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


