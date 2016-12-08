---
title: Terrain Texture Blending
subtitle: Terrain texture alpha blending information (alphatable.ini)
layout: default
parent:
  title: Map Files
permalink: /files/map/terrainalpha/
repolink: /blob/gh-pages/files/map/terrainalpha/index.md
---

### Purpose

Alphatable files appear to control the strength (alpha) of each of the four terrain textures for every heightmap vertex.

### General Format Overview

Alphatable files consist of a size followed by a 32-bit bitmap, where each color channel corresponds to the strength of 
the terrain texture. The dimensions of the bitmap are `gridinfo.gridwidth * 2 + 1` wide by 
`gridinfo.gridlength * 2 + 1` tall.

### Alphatable Format

{% include table.html data=site.data.map.terrainalpha.data %}
