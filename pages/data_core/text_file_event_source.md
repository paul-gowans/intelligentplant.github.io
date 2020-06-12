# Text File Event Source

## Overview

Text File Event Source is a datacore import object for flat text files
of delimited or fixed width formats.

It can be configured to monitor for files in an Import Directory.

The process is as follows:

1.  File dropped in Import Directory
2.  If Event Source has subscribers, the file is collected
3.  Datarows convert to Data Core Event Messages
4.  Event Messages sent to subscribers
5.  Once file has been processed, it is archived to the Archive
    Directory

## Event Message Structure

Text file fields are assigned to the Event message Event Property
collection.

All data is treated as text.

Event Property names are derived from the text file column names (if
available), or default to "Field00, Field01, Field02..." if no explicit
name is available.

## Configuration

Configuration options exists for:

  - Import Folder
  - Filename Filter
  - Archive Folder
  - File Format: Fixed width or delimited
  - Skip Rows: Skip the first n number of rows in the text file
  - Column Names: Are column Names included in the first data row?
  - Delimiter: Defines the delimitor for a text file
  - Field Widths: or fixed width format only. Example, "5, 10, 11, -1",
    the first is 5 characters wide, the second 10, the third 11, and the
    fourth is of variable width.

## Tips

The process which drops the file in the Import Directory should protect
against Data Core collecting the file prematurely. Consider employing
the Filename filter.

For example,

``` 
 - Set the Filename Filter to "*.csv" - only CSV files are considered for import
 - While writing a file to the Import Folder, use extension ".tmp"
 - Once file-write is complete, rename extension to ".csv"
```
