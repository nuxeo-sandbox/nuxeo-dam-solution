# About

[![Build Status](https://qa.nuxeo.org/jenkins/buildStatus/icon?job=Sandbox/sandbox_nuxeo-labs-thumbnails-enricher-master)](https://qa.nuxeo.org/jenkins/job/Sandbox/job/sandbox_nuxeo-labs-thumbnails-enricher-master/)

This Nuxeo Package contains a new [Enricher](https://doc.nuxeo.com/n/M8o) named `thumbnails`, for Folderish document types, to get the thumbnails of the children. This can be useful for displaying thumbnail images when looking at the parent, for example.

![example](images/example.png)


# Usage

* You can limit the number of results by setting the header `thumbnail-limit` to a number
* You can filter the children by type by setting the header `thumbnail-types` to a comma-separated list of types
* You can filter the children by facet by setting the header `thumbnail-facets` to a comma-separated list of facets

The result format is:

```
"contextParameters": {
 "thumbnails": [
   {
     "id": <doc-id>
     "thumbnailUrl": <thumbnail-url>
   },
   ...
 ]
}
```

# Build

Building requires the following software:

* git
* maven

```
git clone https://github.com/nuxeo-sandbox/nuxeo-labs-thumbnails-enricher
cd nuxeo-labs-thumbnails-enricher
mvn clean install
```

## Install

The build will produce a Nuxeo Pacakage in the folder `nuxeo-labs-thumbnails-enricher-package/target`. If you need help installing Nuxeo Packages, refer to [the documentation](https://doc.nuxeo.com/n/lHZ).

# Support

**These features are not part of the Nuxeo Production platform.**

These solutions are provided for inspiration and we encourage customers to use them as code samples and learning resources.

This is a moving project (no API maintenance, no deprecation process, etc.) If any of these solutions are found to be useful for the Nuxeo Platform in general, they will be integrated directly into platform, not maintained here.


# Licensing

[Apache License, Version 2.0](http://www.apache.org/licenses/LICENSE-2.0)


# About Nuxeo

Nuxeo dramatically improves how content-based applications are built, managed and deployed, making customers more agile, innovative and successful. Nuxeo provides a next generation, enterprise ready platform for building traditional and cutting-edge content oriented applications. Combining a powerful application development environment with SaaS-based tools and a modular architecture, the Nuxeo Platform and Products provide clear business value to some of the most recognizable brands including Verizon, Electronic Arts, Sharp, FICO, the U.S. Navy, and Boeing. Nuxeo is headquartered in New York and Paris.

More information is available at [www.nuxeo.com](http://www.nuxeo.com).