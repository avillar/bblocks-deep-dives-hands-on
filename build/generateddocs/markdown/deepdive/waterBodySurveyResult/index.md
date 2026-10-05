
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
  depth:
    type: number
    description: Depth, in meters
    minimum: 0
  area:
    type: number
    description: Surface area, in square meters
    exclusiveMinimum: 0
anyOf:
- required:
  - elevation
- required:
  - depth
- required:
  - area
additionalProperties: false

```

Links to the schema:

* YAML version: [schema.yaml](https://avillar.github.io/bblocks-deep-dives-hands-on/build/annotated/deepdive/waterBodySurveyResult/schema.json)
* JSON version: [schema.json](https://avillar.github.io/bblocks-deep-dives-hands-on/build/annotated/deepdive/waterBodySurveyResult/schema.yaml)


# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/avillar/bblocks-deep-dives-hands-on](https://github.com/avillar/bblocks-deep-dives-hands-on)
* Path: `_sources/waterBodySurveyResult`

