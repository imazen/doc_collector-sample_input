Tags: plugin
Edition: elite
Bundle: contract
Tagline: Automatic cropping based on a set of areas to preserve specified areas.
Aliases: /hello

# CropAround plugin

Provided a set of focus rectangles, will crop the image while preserving the specified areas.

Coordinates must be in the source image coordinates. 

Requires `mode=crop` and `width` and `height` to be specified to activate.

## Installation

1. Reference ImageResizer.Plugins.Faces.dll
2. Add `<add name="CropAround" />` to the `<plugins />` section.

## Syntax

* c.focus=x1,y1,x2,y2
* c.focus=x1,y1,x2,y2,x1,y2,x2,y2.....
* c.zoom=true (Crop as closely as possible to rectangles)
* c.zoom=false (Crop minimally to meet required aspect ratio)
* c.finalmode=crop|pad|max|stretch|carve (If we can't meet the desired aspect ratio given our constraints, what do we do next?)

## Special ability when installed alongside the Faces plugin

* c.focus=faces - Perfoms on-the-fly face detection and uses those coordinates. Can be resource intensive, so disk caching is reccommended.
