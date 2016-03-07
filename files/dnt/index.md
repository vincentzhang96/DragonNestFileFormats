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

#### Length Prefixed Non Null Terminated String (LPNNTS)
DNT files use strings prefixed with `UINT16` length and no NUL termination byte.

#### Header
{% include table.html data=site.data.dnt.header %}

#### Column
{% include table.html data=site.data.dnt.column %}

#### Rows
{% include table.html data=site.data.dnt.rows %}

#### Row
{% include table.html data=site.data.dnt.row %}

#### Cell
Row cells are stored linearly, where the encoding is specified by the corresponding column. See Appendix A for how to read each data type.

### Appendices

#### Appendix A: Column Data Types
<table class="table">
    <thead>
    <tr>
        <th>ID</th>
        <th>Type</th>
        <th>Data Type</th>
    </tr>
    </thead>
    <tbody>
    <tr>
        <td>1</td>
        <td>Text</td>
        <td><code>LPNNTS</code></td>
    </tr>
    <tr>
        <td>2</td>
        <td>Boolean</td>
        <td><code>UINT32</code></td>
    </tr>
    <tr>
        <td>3</td>
        <td>Integer</td>
        <td><code>INT32</code></td>
    </tr>
    <tr>
        <td>4</td>
        <td>Float</td>
        <td><code>FLOAT32</code></td>
    </tr>
    <tr>
        <td>5</td>
        <td>Double&dagger;</td>
        <td><code>FLOAT32</code></td>
    </tr>
    </tbody>
</table>

&dagger; While DNT tables specify a type of double, it is still 32 bits long and equivalent to Float.
