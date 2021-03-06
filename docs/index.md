---
layout: docs
title: Index
description: Index page for Export Sheet Data's documentation.
group: overview
---

Welcome to the Export Sheet Data documentation compendium!
----------------------------------------------------------

Here you can find detailed descriptions for each of ESD's various options and settings, as well as a few guidelines for how to properly use ESD.

**This documentation is still being written, so please bear with us and forgive any missing content while it is being completed.**

[1. Format Settings](#format-settings)<br>
[2. General Settings](#general-settings)<br>
[3. JSON Settings](#json-settings)<br>
[4. XML Settings](#xml-settings)

Format Settings
---------------
These settings determine which format (JSON or XML) to export your data to, as well as the target sheets to export.

- [Select Format](format/selectformat.md) - Select the data format to export to (JSON or XML)
- [Select Sheet(s)](format/selectsheets.md) - Select the data range to include in the exported data

General Settings
----------------
These settings affect both JSON and XML data.

### Basic

- [Replace existing file(s)](general/replaceexistingfiles.md) - Trash files with the same name in the output folder as the exported data
- [Unwrap single row sheets](general/unwrapsinglerowsheets.md) - Place elements from a sheet containing one row in the root element
- [Collapse single row sheets](general/collapsesinglerowsheets.md) - Place a sheet's only row element fields in the sheet element
- [Ignore empty cells](general/ignoreemptycells.md) - Don't export cells with no value

### Advanced

- [Nested Elements](general/nestedelements.md) - Create complex data sets by using specific key syntax
- [Minify data](general/minifydata.md) - Output smaller files at the cost of human readability
- [Ignore prefix](general/ignoreprefix.md) - Don't export columns whose keys start with a specific prefix
- [Unwrap prefix](general/unwrapprefix.md) - Unwrap sheets with names using the specified prefix
- [Collapse prefix](general/collapseprefix.md) - Collapse sheets with names using the specified prefix

JSON Settings
-------------
These settings only affect exported JSON data.

### Basic

- [Force string values](json/forcestringvalues.md) - Export all values as their string version
- [Export cell arrays](json/exportcellarrays.md) - Export JSON arrays when a cell contains a specific character
- [Export sheet arrays](json/exportsheetarrays.md) - Export sheets as JSON arrays with each row creating a single element
- [Export value arrays](json/exportvaluearrays.md) - Export a sheet as a JSON array if it has only one column

### Advanced

- [Export contents as array](json/exportcontentsasarray.md) - Convert exported standalone JSON to a raw JSON array
- [Export cell objects](json/exportcellobjects.md) - Export a cell's value as a JSON object if it is properly formatted
- [Empty value format](json/emptyvalueformat.md) - Determines if empty cells are exported with null or empty string values
- [Array separator character](json/arrayseparatorcharacter.md) - Adjust the character used to separate values in a cell array
- [Array prefix](json/arrayprefix.md) - Force sheets or elements in a column to export as JSON arrays
- [Nested array prefix](json/nestedarrayprefix.md) - With Nested Elements checked, force sheets to export as nested arrays

XML Settings
------------
These settings only affect exported XML data.

### Basic

- [Export columns as child elements](xml/exportcolumnsaschildelements.md) - Export columns as child elements of their row's XML element
- [Include first column in export](xml/includefirstcolumninexport.md) - Export the first column of a row as a distinct XML element
- [Root element](xml/rootelement.md) - Name for the exported XML document's root element

### Advanced

- [Name replacement character](xml/namereplacementcharacter.md) - Character used when replacing illegal chars in element names
- [Include XML declaration](xml/includexmldeclaration.md)- Include a customized XML declaration in the exported document
  - [XML version](xml/xmlversion.md) - Version of the XML standard used by the exported document
  - [XML encoding](xml/xmlencoding.md) - Encoding used by the exported document
  - [Standalone](xml/standalone.md) - Specifies if the exported document depends on external resources
- [Attributes prefix](xml/attributesprefix.md) - Force elements in a column to export as attributes for their row element
- [Child elements prefix](xml/childelementsprefix.md) - Force elements in a column to export as child elements of their row element
- [Inner text prefix](xml/innertextprefix.md) - Force elements in a column to export as inner text for their row element
