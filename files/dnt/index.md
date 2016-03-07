---
title: DNT Files
subtitle: Dragon Nest Table Files (.dnt)
layout: default
permalink: /files/dnt/
repolink: /blob/gh-pages/files/dnt/index.md
---

### Purpose
DNT files contain various tabular relational data required by the game, containing information such as item stats, skill values, etc. 

### Examples
Files in /resource/ext/

### General Format Overview
The DNT file structure consists of a header, column headings, and rows of data.

### DNT Format

#### Header
{% include table.html data=site.data.dnt.header %}

#### Column
{% include table.html data=site.data.dnt.column %}

#### Rows
{% include table.html data=site.data.dnt.rows %}

#### Row
{% include table.html data=site.data.dnt.row %}

### Appendices

#### Appendix A: Column Data Types
