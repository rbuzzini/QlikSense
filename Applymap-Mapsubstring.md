# 1 - Applymap statement

`Applymap` function allows to create a field based on existing map configurations.

Syntax:
`Applymap('map_name', expression[, default_mapping])`

Parameters:
- `'map_name'`: the name of the searching map between single quotes
- `expression` it is the field in common between the searching map table and the table we are working with.
- `default_mapping` represents the default mapped value in case there is no match in the searching map. This is an optional parameter.


# 2 - Mapsubstring statement

`Mapsubstring` function allows to map parts of an expression from a mapping table

Syntax:
`MapSubstring('map_name', expression)`


# 2 - Rename Field statement

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