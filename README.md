# OGC API - Joins

This GitHub repository contains a **draft** of the [OGC](https://www.ogc.org)'s
multi-part standard for Web APIs that join data from input files either with feature collections that are available on the server or directly with other input files.

[OGC API standards](https://ogcapi.ogc.org/) define modular API building blocks to spatially enable Web APIs in a consistent way. [OpenAPI](https://openapis.org) is used to define the reusable
API building blocks with responses in JSON and HTML.

The OGC API family of standards is organized by resource type. OGC API - Joins specifies the behavior of Web APIs that join data from input files either with feature collections that are available on the server or directly with other input files. The core module contains 3 operation sets: discovery operations, data joining operations and file joining operations.

## Overview

The OGC API - Joins draft standard is an extension of the OGC API - Common standard.

```
GET /collections
```
Returns metadata on the collections available on the server

```
GET /collections/{collectionId}
```
Returns metadata on a specific collection available on the server

```
GET /collections/{collectionId}/keys
```
Returns the key fields of a specific collection

```
GET /collections/{collectionId}/keys/{keyFieldId}
```

Returns the key values of a specific key field of a specific collection

```
GET /joins
```

Returns a list of the joins available on the server

```
POST /joins
```

Creates a new join by joining attribute data from a inputted attribute data file with a specific collection

```
GET /joins/{joinId}
```

Returns metadata on a specific join

```
DELETE /joins/{joinId}
```

Deletes a specific join

```
POST /filejoin
```

Joins data between two input files

## Using the draft standard

The draft standard can be read [here](https://docs.ogc.org/DRAFTS/22-026.html).

Those who want to just see the endpoints and responses can explore [examples of
OpenAPI definitions](https://github.com/opengeospatial/ogcapi-joins/tree/master/sources/core/openapi).

## Server and client implementations

[Overview of software products that implement OGC API Joins](implementations)

## Communication

Communicate your ideas or comments to the Standards Working Group by posting [GitHub issues](https://github.com/opengeospatial/ogcapi-joins/issues).

Most all work on the specification takes place in [GitHub issues](https://github.com/opengeospatial/ogcapi-joins/issues), so browse there to get a good idea of what is happening, as well as past decisions.

## Building

After cloning the repository, navigate to the folder.

` cd /ogcapi-joins/sources/core`

Then compile with docker (on Linux or MacOS):

`docker run -v "$(pwd)":/metanorma -v ${HOME}/.fontist/fonts/:/config/fonts  metanorma/metanorma  metanorma compile --agree-to-terms -t ogc -x html,pdf standard/22-026.adoc`


## [Contributing](CONTRIBUTING.md)

The contributor understands that any contributions, if accepted by the OGC Membership and ISO/TC 211, shall be incorporated into OGC and ISO/TC 211 OGC API standards documents and that all copyright and intellectual property shall be vested to the OGC.

The OGC API - Joins Standards Working Group (SWG) is the group at OGC responsible for the stewardship of the standard, but is working to do as much work in public as possible.

* [Copy of License Language](https://raw.githubusercontent.com/opengeospatial/ogcapi-joins/master/LICENSE)

Pull Requests from contributors are welcomed. However, please note that by sending a Pull Request or Commit to this GitHub repository, you are agreeing to the terms in the Observer Agreement https://portal.ogc.org/files/?artifact_id=97953
