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
