# 1 - Rename Field statement

This script function renames one or more existing fields after they are already loaded.

It is possible to use both `Rename Field` and `Rename Fields` syntax.
Syntax:
- `Rename Field (using mapname | oldname to newname{ , oldname to newname })`
- `Rename Fields (using mapname | oldname to newname{ , oldname to newname })`

Parameters:
- `mapname`: mapping table previously loaded, containing one or multiple couples
of field names obsolete or new.
- `oldname`: obsolete field names
- `newname`: new field name

*Keep in mind: it is not possible to rename to field in so they have the same name*


You saw that there are two methods to rename a field:

**1st Method**

You can use the following code...
`Rename Field oldname to newname`
... will rename *oldname* column to *newname*.

If you have to rename many fields in one run a mapping table could help.
Let's see it in the second method.

**2nd Method**

```
# Mapping table which maps oldnames and newnames:
[Map_Rename]:
Mapping Load * Inline [
OldName, NewName
Quantity, Qty
Value, ContractValue
Date, OrderDate
];


# Orders table:
[Orders]:
Load * Inline [
Quantity, Value, Date
10, 150, 01/02/2022
25, 400, 03/04/2022
3, 50, 20/04/2022
];

Rename Fields using [Map_Rename];
```

*Orders* table will have Qty, ContractValue and OrderDate as column names.


# 2 - Rename Table statement

Rename table statement is similar to *Rename Field* one.

Using the following code...
`Rename Table oldTableName to newTableName`
... will rename *oldTableName* table to *newTableName*.