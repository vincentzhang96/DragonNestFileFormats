---
title: PAK Files
subtitle: Eyedentity Package Files (.pak)
layout: default
permalink: /files/pak/
repolink: /blob/gh-pages/files/pak/index.md
---

### Purpose
PAK files are the primary container format for Dragon Nest, containing almost all of the asset files for the game. 

### Examples
Resource00.pak through Resource13.pak in the Dragon Nest installation directory.

### General Format Overview
The PAK file structure consists of a header, containing the number of subfiles and the location of the index table; subfile data blocks, containing the compressed subfile data; and the index. The index may be located anywhere in the file after the header, but is usually the last section in the file.

### Pak Format

#### Pak Header
{% include table.html data=site.data.pak.header %}


