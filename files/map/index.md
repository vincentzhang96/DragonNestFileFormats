---
title: Map Files
subtitle: Map definition files
layout: jumbo
permalink: /files/map/
repolink: /blob/gh-pages/files/map/index.md
---

#Overview

Maps (or dungeons, or nests) in Dragon Nest reside in `/mapdata/grid/` as individual directories. The names of the 
directories are internal names, as referenced in `resource/ext/maptable.dnt`, column `_ToolName1`. Do note that 
letter casing **will not** match.

##Layout

Map directories have the following structure:

- `%DIR_NAME%/`
    - `%DIR_NAME%.dds` - Minimap texture
    - `gridinfo.ini` - [Map Information](gridinfo/)
    - `0_0/` - Zone (0, 0) data
        - `alphatable.ini` - [Terrain texture blending](terrainalpha/)
        - `colbuild.ini` - [Colbuild (unknown)](colbuild/)
        - `decalinfo.ini` - [Terrain decals](terraindecal/)
        - `default.ini` - [Zone definition](zonedefine/)
        - `eventareainfo.ini` - [Event area info (unknown)](eventareainfo/)
        - `grasstable.ini` - [Grass placement](terraingrass/)
        - `height.ini` - [Terrain heightmaps](terrainheight/)
        - `heightattribute.ini` - [Height attributes](terrainheightattrib/)
        - `navigation.ini` - [Navigation mesh](navmesh/)
        - `propinfo.ini` - [Prop placement](propinfo/)
        - `sectorsize.ini` - [Map size](sectorsize/)
        - `soundinfo.ini` - [Sound](sound/)
        - `textable.ini` - [Texture groups](texuregroups/)
        - `trigger.ini` - [Event triggers](trigger/)
        - `triggerdefine.ini` - [Event trigger declarations](triggerdefine/)
        - `water.ini` - [Water tuning](water/)

While it appears that there's some mechanism for multiple zones per map, it is currently not being used (only ever 
see `0_0`).
