---
title: Data Types
layout: default
permalink: /datatypes/
repolink: /blob/gh-pages/datatypes.md
---

###Endianness
Most Dragon Nest files are [Little Endian](http://en.wikipedia.org/wiki/Endianness#Little-endian). Situations where this is not the case are noted. 

###Integral Types
Integral types are noted as `[u]int[bits]`, where `u` indicates unsigned and `[bits]` indicates the width, in bits. 

For example, a 4 byte signed integer would be written as `int32` and an unsigned 1 byte integer would be written as `uint8`.

###Arrays
Arrays of other types are indicated by appending `[]` to the type, optionally enclosing a count. For arrays that are simply empty padding, the type is omitted and implied to be an unnamed 1 byte wide type.

For instance, an array of 12 `uint64` would be written `uint64[12]` and a 256 byte padding would be written `[256]`.

###Strings
The Strings used in DragonNest are all encoded using UTF-8. Strings are either fixed buffer null terminated or length prefixed null terminated. Null Terminated String is abbreviated NTSTR for convienence.

####Fixed Buffer Null Terminated Strings
Fixed Buffer NTSTRs are allocated a fixed size `n` and may take up from 0 to `n` bytes. The end of the string is marked by the `NUL` byte 0x00, or by the end of the buffer.

Fixed Buffer NTSTRS are notated using the array syntax with `FBSTR`, so a FBSTR with size 128 would be written `FBSTR[128]`, and an array of 12 size 128 FBSTRs would be written `FBSTR[128][12]`.

To read a `FBSTR`, allocate `n` bytes (or `n + 1` for languages that require the `NUL` byte) and read in `n` bytes from the file. For languages that are length-prefix based, truncate the string at the first `NUL` byte. For languages that are null-terminated based, nothing else need be done, unless there is a need to compact the buffer.

####Length Prefixed Null Terminated Strings
Length Prefixed NTSTRs have a `uint32` length field `len` prefixed to the string itself. The length includes the `NUL` byte at the end, so the actual string length is `len - 1`.

Length Prefixed NTSTRs are notated simply by `LPSTR`, with no array syntax (since the length is variable).

###Structures
Structures will be defined explicitly in each format and referred to using the listed tag.