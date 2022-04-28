# Mapping Load statement

The prefix `Mapping` allows to create a mapping table that can be used, for example,
to substitute a field values during the script execution.

Syntax:
`Mapping( loadstatement | selectstatement )`

The following code..
```
[mapEmployeeNames]:
Mapping Load
  Text(EmployeeCode) As EmployeeCode, 
  EmployeeName
From EmployeeTable
;
```
.. allows you to use this Map table during the script.


You can call back the Mapping table using
`Rename Field`, `Applymap()` or `Mapsubstring()` functions.

