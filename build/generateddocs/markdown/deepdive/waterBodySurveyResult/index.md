
# Water Body Survey Result (Schema)

`ogc.deepdive.waterBodySurveyResult` *v0.1*

The result of a water body survey: surface elevation, depth and area.

[*Status*](http://www.opengis.net/def/status): Under development

## Schema

```yaml
title: Water Body Survey Result
description: Result of a water body survey
type: object
properties:
  elevation:
    type: number
    description: Surface elevation above sea level, in meters
    x-jsonld-id: http://dbpedia.org/ontology/elevation
    x-jsonld-type: http://www.w3.org/2001/XMLSchema#double
  depth:
    type: number
    description: Depth, in meters
    minimum: 0
    x-jsonld-id: http://dbpedia.org/ontology/depth
    x-jsonld-type: http://www.w3.org/2001/XMLSchema#double
  area:
    type: number
    description: Surface area, in square meters
    exclusiveMinimum: 0
    x-jsonld-id: http://dbpedia.org/ontology/area
    x-jsonld-type: http://www.w3.org/2001/XMLSchema#double
anyOf:
- required:
  - elevation
- required:
  - depth
- required:
  - area
additionalProperties: false
x-jsonld-prefixes:
  dbo: http://dbpedia.org/ontology/
  xsd: http://www.w3.org/2001/XMLSchema#

```

Links to the schema:

* YAML version: [schema.yaml](https://avillar.github.io/bblocks-deep-dives-hands-on/build/annotated/deepdive/waterBodySurveyResult/schema.json)
* JSON version: [schema.json](https://avillar.github.io/bblocks-deep-dives-hands-on/build/annotated/deepdive/waterBodySurveyResult/schema.yaml)


# JSON-LD Context

```jsonld
{
  "@context": {
    "elevation": {
      "@id": "dbo:elevation",
      "@type": "xsd:double"
    },
    "depth": {
      "@id": "dbo:depth",
      "@type": "xsd:double"
    },
    "area": {
      "@id": "dbo:area",
      "@type": "xsd:double"
    },
    "dbo": "http://dbpedia.org/ontology/",
    "xsd": "http://www.w3.org/2001/XMLSchema#",
    "@version": 1.1
  }
}
```

You can find the full JSON-LD context here:
[context.jsonld](https://avillar.github.io/bblocks-deep-dives-hands-on/build/annotated/deepdive/waterBodySurveyResult/context.jsonld)


# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/avillar/bblocks-deep-dives-hands-on](https://github.com/avillar/bblocks-deep-dives-hands-on)
* Path: `_sources/waterBodySurveyResult`

