# QlikSense Load * Inline statement

In QlikSense you can upload a table with the Load * Inline statement.

The following code..
```
[EmployeeMatch]:
Load * Inline 
[EmployeeCode, Rate
WETQA0, 100
WETQA1, 80
WETQA2, 20
];
```
.. will upload this table:
|EmployeeCode|Rate|
|---|---|
|WETQA0|100|
|WETQA1|80|
|WETQA2|20|


