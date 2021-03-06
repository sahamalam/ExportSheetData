---
layout: docs
title: Export Cell Arrays
description: Documentation for Export Sheet Data's 'Export cell arrays' option.
group: json
---

Export cell arrays
------------------
Export cell arrys will export a cell's value as a JSON array if the cell contains commas ( , ).

To prevent your data from being exported as an array, wrap your cell value with quotation marks ( "" ).

Example:

Sheet: `Spies`<br>
Fields: `Name | Age | Aliases`<br>
Values: `Sterling | 30 | Duchess, Randy, "Sterling Archer, world's greatest spy"`

Default Output:
```
{
  "Spies" : {
    "Sterling" : {
      "Name":"Sterling",
      "Age":30,
      "Aliases":"Duchess, Randy, \"Sterling Archer, world's greatest spy\""
    }
  }
}
```

Cell Array Output:
```
{
  "Spies" : {
    "Sterling" : {
      "Name":"Sterling",
      "Age":30,
      "Aliases": [
        "Duchess",
        "Randy",
        "Sterling Archer, world's greatest spy"
      ]
    }
  }
}
```
